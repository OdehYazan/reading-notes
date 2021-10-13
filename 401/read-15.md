[Reading-notes](https://odehyazan.github.io/reading-notes/)

# Trees

**In this tutorial, we’ll be covering Binary Trees, Binary Search Trees, and K-ary Trees. We will review some common terminology that is shared amongst all of the trees and then dive into specifics of the different types.**

## Common Terminology

**1. Node - A Tree node is a component which may contain it’s own values, and references to other nodes.**
**2. Root - The root is the node at the beginning of the tree.**
**3. K - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, `k = 2`.**
**4. Left - A reference to one child node, in a binary tree.**
**5. Right - A reference to the other child node, in a binary tree.**
**6. Edge - The edge in a tree is the link between a parent and child node.**
**7. Leaf - A leaf is a node that does not have any children.**
**8. Height - The height of a tree is the number of edges from the root to the furthest leaf.**

**Sample Tree:**<br>

![sample](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/BinaryTree1.PNG)

<br>

## Traversals

**An important aspect of trees is how to traverse them. Traversing a tree allows us to search for a node, print out the contents of a tree, and much more! There are two categories of traversals when it comes to trees:**

**1. Depth First.**
**2. Breadth First.**

***Depth First***

**Depth first traversal is where we prioritize going through the depth (height) of the tree first. There are multiple ways to carry out depth first traversal, and each method changes the order in which we search/print the root. Here are three methods for depth first traversal:**

**1. Pre-order: `root >> left >> right`.**
**2. In-order: `left >> root >> right`.**
**3. Post-order: `left >> right >> root`.**

<br>

![sam](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/tree-example.png)
<br>

***Breadth First***

**Breadth first traversal iterates through the tree by going through each level of the tree node-by-node. So, given our starting tree one more time:**<br>

![d](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/tree-example.png)
<br>

## Binary Tree Vs K-ary Trees

**In all of our examples, we’ve been using a Binary Tree. Trees can have any number of children per node, but Binary Trees restrict the number of children to two (hence our `lef`t and `right` children).**

**There is no specific sorting order for a binary tree. Nodes can be added into a binary tree wherever space allows. Here is what a binary tree looks like:**
<br>

![s](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/BinaryTree2.PNG)
<br>

## K-ary Trees

**If Nodes are able have more than 2 child nodes, we call the tree that contains them a K-ary Tree. In this type of tree we use `K` to refer to the maximum number of children that each Node is able to have.**

***Breadth First Traversal***

**Traversing a K-ary tree requires a similar approach to the breadth first traversal. We are still pushing nodes into a queue, but we are now moving down a list of children of length k, instead of checking for the presence of a left and a right child.**

<br>

![a](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/KaryTree1.png)

<br>

![f](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/BreadthKary1.png)

<br>

## Binary Search Trees

**A Binary Search Tree (BST) is a type of tree that does have some structure attached to it. In a BST, nodes are organized in a manner where all values that are smaller than the `root` are placed to the left, and all values that are larger than the `root` are placed to the right.**

**Here is how we would change our Binary Tree example into a Binary Search Tree:**

<br>

![d](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/BST1.PNG)
<br>

## Searching a BST

 **Searching a BST can be done quickly, because all you do is compare the node you are searching for against the root of the tree or sub-tree. If the value is smaller, you only traverse the left side. If the value is larger, you only traverse the right side.**

 **Let’s say we are searching `15`. We start by comparing the value `15` to the value of the root, `23`.**

 **`15 < 23`, so we traverse the left side of the tree. We then treat `8` as our new “root” to compare against.**

 **`15 > 8`, so we traverse the right side. `16` is our new root.**

 **`15 < 16`, so we traverse the left side. And aha! `15` is our new root and also a match with what we were searching for.**
 <br>

 ![e](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/BST2.PNG)

 <br>

 **The best way to approach a BST search is with a while loop. We cycle through the while loop until we hit a leaf, or until we reach a match with what we’re searching for.**

## Big O

 **The Big O time complexity of a Binary Search Tree’s insertion and search operations is `O(h)`, or `O(height)`. In the worst case, we will have to search all the way down to a leaf, which will require searching through as many nodes as the tree is tall. In a balanced `(or “perfect”)` tree, the height of the tree is `log(n)`. In an unbalanced tree, the worst case height of the tree is `n`.**

 **The Big O space complexity of a BST search would be `O(1)`. During a search, we are not allocating any additional space.**
