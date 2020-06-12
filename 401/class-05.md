## Code 401 Reading Assignment Notes - Class 5

_June 12, 2020_

### Linked Lists

[Linked Lists](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html)

#### Terminology

**Linked List** - A data structure that contains nodes that links/points to the next node in the list.

**Singly** - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.

**Doubly** - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.

**Node** - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.

**Next** - Each node contains a property called Next. This property contains the reference to the next node.

**Head** - The Head is a reference type of type Node to the first node in a linked list.

**Current** - The Current reference is a reference type of type Node that is currently being looked at. This node is traditionally used when traversing through a full linked list. When traversing, you typically reset the current to the head to guarantee you are starting from the beginning of the linked list.

#### Traversal

When traversing a linked list, you are not able to use a `foreach` or `for` loop. The best way to approach a traversal is through the use of a `while()` loop.

[What's a linked list anyway pt 1](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d)

Linked lists are linear data structures. This means that there is a sequence and an order to how they are constructed and traversed. 

In order to get to the end of the list, we have to go through all of the items in the list in order, or sequentially.

Arrays are also linear data structures. The biggest differentiator between arrays and linked lists is the way that they use memory in our machines. For arrays, the memory is in one contiguous block. For linked lists, the nodes can be scattered in memory.

Arrays are static data structures, while linked lists are dynamic.

Linked lists are made up of nodes. The end of the empty list is a node that points to null.

A single node has two parts: the data and a reference to the next node.

In a doubly linked list, each node has data and a reference to the previous node and the next node.

A circular linked list is a little odd in that it doesn’t end with a node pointing to a null value. Instead, it has a node that acts as the tail of the list (rather than the conventional head node), and the node after the tail node is the beginning of the list.

[What's a linked list anyway pt 2](https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996)

Big O Notation is a way of evaluating the performance of an algorithm.

There are two major points to consider when thinking about how an algorithm performs: how much time it requires at runtime given how much time and memory it needs.

Big O Notation takes into account the speed and efficiency with which something functions when its input grows to be any (crazy big!) size.


An **O(1)** function takes constant time, which is to say that it doesn’t matter how many elements we have, or how huge our input is: it’ll always take the same amount of time and memory to run our algorithm. 

An **O(n)** function is linear, which means that as our input grows (from ten numbers, to ten thousand, to ten million), the space and time that we need to run that algorithm grows linearly.

An **O(n²)** function takes exponentially more time and memory the more elements that you have.

To grow a linked list, we rearrange our pointers. 

Steps to add a node in a singly linked list. It's important to do these in the correct order:

1. First, we find the head node of the linked list.

2. Next, we’ll make our new node, and set its pointer to the current first node of the list.

3. Lastly, we rearrange our head node’s pointer to point at our new node.

A linked list is usually efficient when it comes to adding and removing most elements, but can be very slow to search and find a single element.



---
[Home page](https://marlene-rinker.github.io/reading-notes/)