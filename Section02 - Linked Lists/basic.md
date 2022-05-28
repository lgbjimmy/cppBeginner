# Linked List
## Table of Content
* [Singly Linked List](https://github.com/lgbjimmy/cppBeginner/edit/section/Section02%20-%20Linked%20Lists/basic.md#singly-linked-list)
* [Doubly Linked List](https://github.com/lgbjimmy/cppBeginner/edit/section/Section02%20-%20Linked%20Lists/basic.md#doubly-linked-list)

__________

### **Singly Linked List**
   `c++` `std::forward_list`

   * not bidirectional
   * can't access element directly.
   * reverse iterator not available
   * definition
       * [linked list](https://en.cppreference.com/w/cpp/container/forward_list)
 
__________

### **Doubly Linked List**
   `c++` `std::list`

   * bidirtional
   * can't access element directly.
   * definition
       * [linked list](https://en.cppreference.com/w/cpp/container/list)
   * example
     ```
     std::list<int> v{5} // an int element 5
     std::list<int> v(5) // five int element
     ```
   * additional info
       *  [sort for list](https://stackoverflow.com/questions/10652674/sorting-stdlists-using-stdsort)
  
__________
