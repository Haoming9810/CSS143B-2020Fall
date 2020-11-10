## (20pt) Iterative in-order binary tree traversal

Complete the following function that returns the values of an in-order traversal from a binary tree.

```java
public static List<Integer> inorderTraversalIterative(TreeNode<Integer> root) {
        // homework
        List<Integer> result = new ArrayList<>();
        return result;  // place holder
}
```

As discussed in class, "in order" means the order of tree node visit goes by

- Left
- Root
- Right

The recursive solution is trivial. Let's here write the iterative solution. From the hint of recursive method, we can infer that a stack would be helpful. The return value is a list that containts the values of the tree nodes in the order of an "in-order" traversal.

Just to be clear, no recursion is allowed or zero point will be given.

## (20pt) Implement the level-order traversal for binary tree

Unlike the 3 regular ways to traverse a binary tree to visit all the nodes, level-order traversal visits the binary tree one level at a time from the top. Here's the function to work on:

```java
    public static List<List<Integer>> levelOrder(TreeNode<Integer> root) {
        // homework
        List<List<Integer>> result = new ArrayList<>();
        return result;  // place holder
    }
```

For example, given the tree

```
      1
     / \
    2   N
```

The returned list should be

```
[
  [1],
  [2],
]
```

Given the tree

```
      1
     /  \
    2    3
   / \    \
  4   5    6
```

The returned list should be

```
[
  [1],
  [2,3],
  [4,5,6],
]
```

The return value is a list of lists, each of which contains the values on that level of the tree from left to right.

Different from the other 3 traversals, level traversal is considered "[breadth first search](https://medium.com/basecs/breaking-down-breadth-first-search-cebe696709d9)" or "BFS". As you can see from the example, it explores nodes closer to the root before going further away. For depth first search, a stack can be used, while for BFS, a queue would be the choice as the helper data structure. In this work, no recursion is allowed and a queue of some kind has to be used. Please use something that implements the [Queue](https://docs.oracle.com/javase/7/docs/api/java/util/Queue.html) interface. Explain your choice in a comment.