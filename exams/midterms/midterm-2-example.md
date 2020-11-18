# ------ Example ------

## 2020 Autumn CSS143B Midterm 2 

**All choice questions are single choice**

**By "array" or "Java array", it means the primitive Java array like int[], not collection like ArrayList**

**2. (2pt) Without stopping condition, a recursion function will**

- (A) Crash immediately with a NullPointerException
- (B) Continue executing till the stack memory is exhausted
- (C) Continue executing till the heap memory is exhausted
- (D) Function as usual and produce correct result without crash

**3.（2pt) When implementing a Stack using a linked list vs array, which statement is WRONG?**

- (A) Array is faster for push and pop because linked list requires traversal to access nodes
- (B) Linkedlist is better in terms of flexible stack capacity without need for memory copy
- (C) Array and linked list can have comparably fast pop and push implementation
- (D) Stack implemented using linked list has slightly higher storage overhead comparing to using array due to the additional node references storage

**9.1 (10pt) Write code to return all the non-leaf nodes in a binary tree.**

The definition of the tree node is:

```java
public class TreeNode<T> {
     public T val;
     public TreeNode left;
     public TreeNode right;
     TreeNode(T x) { val = x; }
 }
```

The leaf nodes are the ones without any child node (both left and right references are null). For example:

``` 
    3
   / \
  9  20
 /    \
1      8
      / \
     7   2
```

The result will be [3, 9, 20, 8], and the order of print does not matter

```java
List<Integer> getNonLeafNodes(TreeNode root) {
  
  
  
  
}
```

**12. (15pt) What is the pre-order traversal of the following tree?**

```bash
          1
        /   \
       4     5
     /      / 
    7      3
```

pre-order:



**13. (5pt) What's the relationship between HashMap and TreeMap in terms of the interface and internal data storage? And which one is faster for searching?**


