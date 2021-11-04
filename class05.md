# Linked Lists

## What Is a Linked List?

A linked list is a a sequence of Nodes that are connected/linked to each other. The most defining feature of a Linked List is that each Node references the next Node in the link, linear data structure that contains a sequence of nodes, and made up of data elements or nodes that are linked together by pointers, in which each node contains data and a pointer to the next node. The most common example is a singly linked list, where each node contains a piece of data and a pointer to the next list, as shown in the diagram below.

![p1](./pic/c05-01.gif)
![p2](./pic/c05-02.png)

## A linked list has the following properties

* Successive nodes are connected by pointers.
* The last node points to null.
* A head pointer is maintained which points to the first node of the list.
* A linked list can grow and shrink in size during execution of the program.
* It can be made just as long as required.
* It allocates memory as the list grows.. 


## Types of Linked List

* singly Linked List => Item navigation is forward only (which means that there is only one reference, and the reference points to the next node in a linked list).

* Doubly Linked List => Item can be navigated forward and backward (which means that there is a reference to both next and previous nodes).

* Circular Linked List => Last item contains link of the first element as next and the first element has a link to the last element as previous (which means that there is a reference from the last node to the first node.)
  
## Basic Operations

* Insertion => Adds an element at the beginning of the list.

* Deletion =>  Deletes an element at the beginning of the list.

* Display =>  Displays the complete list.

* Search => Searches an element using the given key.

* Delete => Deletes an element using the given key.

### Advantages for linked lists

* Insertion and deletion operations are easier.

* Efficient memory utilization.

* Linked list can expand in constant time.

* Linked is a dynamic data structure.

 ****

### DisAdvantages of linked lists

* Reverse Traversing is difficult in the linked list(though we can achieve this with the help of Doubly Linked List)
* The memory is wasted as pointers require extra memory for storage.
* No element can be accessed randomly, it has to access each node sequentially i.e. proper traversal must be done.
  
****
