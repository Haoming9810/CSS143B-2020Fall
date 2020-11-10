## (20pt) Lowest Common Ancester 

Given a binary tree, write code to find the lowest common ancestor (LCA) of two given nodes in the tree.

According to the [definition of LCA on Wikipedia](https://en.wikipedia.org/wiki/Lowest_common_ancestor): “The lowest common ancestor is defined between two nodes p and q as the lowest node in T that has both p and q as descendants (where we allow **a node to be a descendant of itself**).”

There will be a video around Wednesday to discuss this.

Tests are provided. Good test also serves as a manual. For example:

```java
	//      1
        //     / \
        //    2   3
        //   / \   \
        //  4   5   6
        root = new TreeNode<>(1);
        root.left = new TreeNode<>(2);
        root.left.left = new TreeNode<>(4);
        root.left.right = new TreeNode<>(5);
        root.right = new TreeNode<>(3);
        root.right.right = new TreeNode<>(6);
        testCases.add(new LCATestCase<>(root, 4, 5, 2));
        testCases.add(new LCATestCase<>(root, 4, 5, 2));
        testCases.add(new LCATestCase<>(root, 4, 6, 1));
        testCases.add(new LCATestCase<>(root, 4, 3, 1));
        testCases.add(new LCATestCase<>(root, 5, 3, 1));
        testCases.add(new LCATestCase<>(root, 6, 2, 1));
```

In this tree, the LCA of nodes 4 and 6 is 1. The LCA of nodes 4 and 5 is 2. 

This is to be done with recursion.

***Important Assumptions:***

1. The given two nodes always exist in the given tree
2. All nodes in a given tree have unique values. 
