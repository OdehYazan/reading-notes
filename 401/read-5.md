[Reading-notes](https://odehyazan.github.io/reading-notes/)



# Linked Lists

## Big O

**Big O: The worst case analysis of algorithm efficiency.**

**Running Time: The amount of time required for an algorithm to complete.**

**Memory Space: The amount of memory resources required for an algorithm to complete.**

**Input Size: Represented by the variable n, the total size of values used as parameters in an algorithm.**

**Big Omega: The best case analysis of algorithm efficiency.**

**Big Theta: The typical or random case used for analysis of algorithm efficiency.**

### What is a Linked List ?

**Linked List is a part of the Collection framework present in java.util package. This class is an implementation of the LinkedList data structure which is a linear data structure where the elements are not stored in contiguous locations and every element is a separate object with a data part and address part. The elements are linked using pointers and addresses. Each element is known as a node. Due to the dynamicist and ease of insertions and deletions, they are preferred over the arrays. It also has few disadvantages like the nodes cannot be accessed directly instead we need to start from the head and follow through the link to reach to a node we wish to access.**

***Terminology:***

**1. Linked List - A data structure that contains nodes that links/points to the next node in the list.**
**2. Singly - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.**

![single](https://media.geeksforgeeks.org/wp-content/uploads/singly-linkedlist.png)

**3. Doubly - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.**

![doubly](https://image.slidesharecdn.com/linkedlist-160504172815/95/linked-list-33-638.jpg?cb=1462382964)

**4. Node - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.**

**5. Next - Each node contains a property called Next. This property contains the reference to the next node.**

**6. Head - The Head is a reference of type Node to the first node in a linked list.**

**7. Current - The Current is a reference of type Node to the node that is currently being looked at. When traversing, you create a new Current variable at the Head to guarantee you are starting from the beginning of the linked list.**

***Traversal***

**When traversing a linked list, you are not able to use a foreach or for loop. We depend on the Next value in each node to guide us where the next reference is pointing. The Next property is exceptionally important because it will lead us where the next node is and allow us to extract the data appropriately.**

**The best way to approach a traversal is through the use of a while() loop. This allows us to continually check that the Next node in the list is not null. If we accidentally end up trying to traverse on a node that is null, a NullReferenceException gets thrown and our program will crash/end.**

**When traversing through a linked list, the Current variable will tell us where exactly in the linked list we are and will allow us to move/traverse forward until we hit the end.**

***Traversal Big O***

**The Big O of time for Includes would be O(n). This is because, at its worse case, the node we are looking for will be the very last node in the linked list. n represents the number of nodes in the linked list.**

**The Big O of space for Includes would be O(1). This is because there is no additional space being used than what is already given to us with the linked list input.**

