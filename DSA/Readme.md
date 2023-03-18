# Data Structures And Algorithms
## Array 
  1. WHAT
    * Store elements in contiguous memory locations, resulting in easily calculable addresses for the elements stored and this allows faster access to an element at a specific index
  2. WHY
    * Arrays store multiple data of similar types with the same name.
    * It allows random access to elements.
    * As the array is of fixed size and stored in contiguous memory locations there is no memory shortage or overflow
    * The array is static in nature. Once the size of the array is declared then we can’t modify it.
    * Insertion and deletion operations are difficult in an array as elements are stored in contiguous memory locations and the shifting operations are costly.
    * The number of elements that have to be stored in an array should be known in advance
## Linked List 
  1. WHAT 
  ![imagename](https://www.notion.so/DSA-7de90660b1c8465ca7d7979648ba4084?pvs=4#e21fc3f2350d48a1b75ec5fb20b5e8a8) 
    * Line near data structure
    * A linked list consists of nodes where each node contains a data field and a reference(link) to the next node in the list ( data, pointer ).
  2. WHY
    * Having a lots of advantages: Dynamic, Quick insertion, Quick deletion…Linked lists are used for dynamic memory allocation which means effective memory utilization hence, no memory wastage
  3. WHEN
    * Linked Lists are used to implement **stacks** and **queues**.
    * It is used for the various representations of trees and graphs.
    * It is used in dynamic memory allocation
## Array VS Linked List
  ![imagename](https://www.notion.so/DSA-7de90660b1c8465ca7d7979648ba4084?pvs=4#ec65e4d4525e4f96b85df1e2885c0404)
## Double Linked List
   1. WHAT
    * A Doubly Linked List (DLL) contains an extra pointer, typically called the previous pointer, together with the next pointer and data which are there in the singly linked list
   2. WHY
    * A DLL can be traversed in both forward and backward directions.
    * The delete operation in DLL is more efficient if a pointer to the node to be deleted is given.
    * We can quickly insert a new node before a given node
   3. WHEN
    * It is used in the navigation systems where front and back navigation is required.
    * It is used by the browser to implement backward and forward navigation of visited web pages that is a back and forward button
    * It is also used by various applications to implement undo and redo functionality
   4. Stack VS Queue
   | Stack  | Queues |
   | ------------- | ------------- |
   | Stacks are based on the LIFO principle, i.e., the element inserted at the last, is the first element to come out of the list. | Queues are based on the FIFO principle, i.e., the element inserted at the first, is the first element to come out of the list  |
  