[Reading-notes](https://odehyazan.github.io/reading-notes/)

# Stacks and Queues

## What is a Stack

**A stack is a data structure that consists of `Nodes`. Each `Node` references the next Node in the stack, but does not reference its previous.**

***Common terminology for a stack is:***

**1. Push - Nodes or items that are put into the stack are pushed.**

**2. Pop - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.**

**3. Top - This is the top of the stack.**

**4.Peek - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.**

**5. IsEmpty - returns true when stack is empty otherwise returns false.**

***Stacks follow these concepts:***

**1. FILO(First In Last Out):**
**This means that the first item added in the stack will be the last item popped out of the stack.**

**2. LIFO(Last In First Out):**
**This means that the last item added to the stack will be the first item popped out of the stack.**

***Stack Visualization***

**Here’s an example of what a stack looks like. As you can see, the topmost item is denoted as the `top`. When you `push` something to the stack, it becomes the new top. When you `pop` something from the stack, you pop the current `top` and set the next `top` as `top.next.`**

![stack](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/stack1.PNG)

You can see codes and graphs on [Stack Visualization](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)

## What is a Queue

**A queue is a linear data structure in which elements can be inserted only from one side of the list called rear, and the elements can be deleted only from the other side called the front. The queue data structure follows the FIFO (First In First Out) principle, i.e. the element inserted at first in the list, is the first element to be removed from the list. The insertion of an element in a queue is called an enqueue operation and the deletion of an element is called a dequeue operation. In queue we always maintain two pointers, one pointing to the element which was inserted at the first and still present in the list with the front pointer and the second pointer pointing to the element inserted at the last with the rear pointer.**

***Common terminology for a queue is***

**1. Enqueue - Nodes or items that are added to the queue.**

**2. Dequeue - Nodes or items that are removed from the queue. If called when the queue is empty an exception will be raised.**

**3. Front - This is the front/first Node of the queue.**

**4. Rear - This is the rear/last Node of the queue.**

**5 . Peek - When you `peek` you will view the value of the `front` Node in the queue. If called when the queue is empty an exception will be raised.**

**6. IsEmpty - returns true when queue is empty otherwise returns false.**

***Queues follow these concepts:***

**1. FIFO(First In First Out):**
**This means that the first item in the queue will be the first item out of the queue.**

**2. LILO(Last In Last Out):**
**This means that the last item in the queue will be the last item out of the queue.**

**Queue Visualization:**

**Here is what a Queue looks like:**

![Queue](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Queue.PNG)

[Queue Visualization](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)