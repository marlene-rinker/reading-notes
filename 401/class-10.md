## Code 401 Reading Assignment Notes - Class 10

_June 19, 2020_

[Stacks and Queues](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)


### Stacks and Queues

### Stacks

A stack is a data structure that consists of `Nodes`. Each `Node` references the next `Node` in the stack, but does not reference its previous.

Common terminology:

**Push** - Nodes or items that are put into the stack are pushed

**Pop** - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.

**Top** - This is the top of the stack.

**Peek** - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.

**IsEmpty** - returns true when stack is empty otherwise returns false.


Stacks follow First In Last Out (FILO) and Last In First Out (LIFO) conceptually.

#### Push

Pushing a Node onto a stack will always be an `O(1)` operation. This is because it takes the same amount of time no matter how many Nodes (n) you have in the stack.

When adding a Node, you `push` it into the stack by assigning it as the new top, with its `next` property equal to the original `top`.

#### Pop

Popping a Node off a stack is the action of removing a Node from the top. When conducting a `pop`, the `top` Node will be re-assigned to the Node that lives below and the `top` Node is returned to the user.

Typically, you would check `isEmpty` before conducting a `pop`. This will ensure that an exception is not raised. Alternately, you can wrap the call in a try/catch block.

#### Peek

When conducting a `peek`, you will only be inspecting the `top` Node of the stack.

Typically, you would check `isEmpty` before conducting a `peek`. This will ensure that an exception is not raised. Alternately, you can wrap the call in a try/catch block.

### Queues

Queues follow First In First Out (FIFO) and Last In Last Out (LILO) conceptually.

#### Enqueue

When you add an item to a queue, you use the `enqueue `action. This is done with an `O(1)` operation in time because it does not matter how many other items live in the queue (n); it takes the same amount of time to perform the operation.

#### Dequeue

When you remove an item from a queue, you use the `dequeue` action. This is done with an `O(1)` operation in time because it doesn’t matter how many other items are in the queue, you are always just removing the front Node of the queue.

Typically, you would check `isEmpty` before conducting a `dequeue`. This will ensure that an exception is not raised. Alternately, you can wrap the call in a try/catch block.

#### Peek

When conducting a `peek`, you will only be inspecting the `front` Node of the queue.

Typically, you want to check `isEmpty` before conducting a `peek`. This will ensure that an exception is not raised. Alternately, you can wrap the call in a try/catch block.


---
[Home page](https://marlene-rinker.github.io/reading-notes/)