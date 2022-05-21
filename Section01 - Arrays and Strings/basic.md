# Arrays and Strings

## Table of Contents
* [Hash Tables](https://github.com/lgbjimmy/cppBeginner/edit/section/Section01%20-%20Arrays%20and%20Strings/basic.md#hash-tables)
* [ArrayLists](https://github.com/lgbjimmy/cppBeginner/edit/section/Section01%20-%20Arrays%20and%20Strings/basic.md#arraylists)
* [StringBuilder](https://github.com/lgbjimmy/cppBeginner/edit/section/Section01%20-%20Arrays%20and%20Strings/basic.md#stringbuilder)

> __Note:__ 
> These class are not included as a subset of C++ STL. I try to find the most similar class and make notes of these. 
__________


### **Hash Tables**

  `c++` `std::map`
   
   * elements are stored as Key, Valure pairs(std::pair).
   * ordered by Key.
   * no duplicate elements (keys are unique).
   * access element directly
   * definition
       * [map](https://en.cppreference.com/w/cpp/container/map)
       * [pair](https://en.cppreference.com/w/cpp/utility/pair)
   * example
       ```
            std::map <std::string, int> m {
               {"James", 6},
               {"Anthony", 7},
               {"Davids", 3}
            };
        
            std::pair<std::string, int> p {"Westbrook", 0};
            // insert Westbrook   
            m.insert(p);
            // insert Monk
            m.insert(std::make_pair("Monk", 11));
            // find Westbrook and erase
            auto it = m.find("Westbrook");
            if (it != m.end())
                m.erase(it)
            // count
            int cnt = m.count("Jamse");
            // removce all element
            m.clear();
            // empty
            m.empty();
        ```
__________

### **ArrayLists**

  `c++` `std::vector`
   * elements are stored in contiguous memory. 
   * resize automatically.
   * access element directly.
   * definition
       * [vector](https://en.cppreference.com/w/cpp/container/vector)
   * example
       ```
           class Player { 
               std::string name;
               int num;
            public:
               Player(std::string pName="none", int pNum = 0)
               :name{pName}, num{pNum} { }
           };
           
           std::vector<Player> v;
           v.push_back(Player{"James", 6});
           v.push_back(Player{"Anthony", 7});
           v.emplace_back("Davids", 3); // efficient
           
           v.size(); //total: 3
           v.capacity(); //total: 3
           v.max_size; //large size
           
           v.at(0); // James 6
           v[1]; // Anthony 7

           v.front(); // James 6
           v.back(); // Anthony 7
           
           v.pop_back(); // James 6, Anthony 7
           v.push_back("Westbrook", 0); // James 6, Anthony 7, Westbrook 0
           
           auto it = std::find(v.begin(), v.end(), Player{"Westbrook", 0});
           v.insert(it, PLayer{"Davids", 3}); // James 6, Anthony 7, Davids 3, Westbrook 0
       ```
__________
### **StringBuilder**

  `c++` `std::string`
  * definition
      * [string](https://en.cppreference.com/w/cpp/string/basic_string)
