# 401 Linked Lists

## Vocabulary Terms
| Term | Definition |
| ---- | ---- |
| Big O | A resource agnostic way of evaluating the performance of an algorithm. It describes the worst case of efficiency an algorithm can have in performing its job. |
| Running Time | The amount of time a function needs to complete. |
| Memory Space | The amount of memory resources a function uses to store data and instructions. |
| Constant Complexity Growth | No matter the inputs are thrown at our algorithm it always uses the same amount of time or space. This is represented in Big O notation as O(1). |
| Logarithmic Complexity Growth | A function that sees a decrease in the rate of complexity growth relative to input. A classic example of this is binary search on a sorted dataset |
| Linear Complexity Growth | The size of our inputs will directly determine the amount of memory space and running time length.Commonly see with loops and recursion. |
| Linked List | A linear data structure that contains nodes that links/points to the next node in the list. |
| Singly | Refers to the number of references the node has; a singly linked list has a value and a next pointer. |
| Doubly | Refers to the number of references the node has; a doubly linked list has a value, a previous pointer and a next pointer. | 
| Node | Nodes are the individual items/links that live in a linked list. Each node contains the data for each link. |
| Next | Each node contains a property called `Next`. This property contains the reference to the next node. |
| Head | `Head` is a reference of type `Node` to the first node in a linked list. |
| Current | `Current` is a reference of type `Node` to the node that is currently being looked at. |
| Linear Data Structure | Data structure where data elements are arranged sequentially or linearly where the elements are attached to its previous and next adjacent. |
| Static data structures | A static data structure is an organization or collection of data in memory that is fixed in size. |
| Dynamic data structures | Dynamic data structures are data structures that grow and shrink as you need them to by allocating and deallocating memory. |

### Traversal of a Linked List
The best way to approach a traversal is through the use of a while() loop. This allows us to continually check that the Next node in the list is not null. The Big O of time for traversal of a linked list would be O(n) & O(1) time and space respectively.

### Prepending a node Linked List
Replace the current `Head` of the linked list with the new node, without losing the reference to the next node in the list. This can be done with O(1) time complexity.

### Inserting a node into a Linked List
Adding a node to the middle of a linked list requires that we must re-allocate to make room for the new node. This can be down with O(n) time complexity.

### Memory management
Arrays and linked lists use memory differently. Arrays need memory in a contiguous block whereas linked lists can use memory in unconnected blocks.

### A warning on Linked Lists
A linked list is usually efficient when it comes to adding and removing most elements, but can be very slow to search and find a single element.


## Sources

[Big O: Analysis of Algorithm Efficiency](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/big_oh.html)

[Linked Lists](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html)

[Difference between Linear and Non-linear Data Structures](https://www.geeksforgeeks.org/difference-between-linear-and-non-linear-data-structures/)

[Dynamic Data Structures](https://computer.howstuffworks.com/c27.htm)

[Static and dynamic data structure](https://computersciencewiki.org/index.php/Static_and_dynamic_data_structure)

[What’s a Linked List, Anyway? [Part 1]](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d)

[What’s a Linked List, Anyway? [Part 2]](https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996)

[A beginner's guide to Big O Notation](https://rob-bell.net/2009/06/a-beginners-guide-to-big-o-notation)

