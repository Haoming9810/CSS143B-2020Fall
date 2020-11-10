## (20pt) Insert a value in a Binary Search Tree

### 3.1 (10pt) Write the following function that inserts a value into a binary search tree:

```java
    public static void insert(TreeNode<Integer> root, int valToInsert) {
        // homework
    }
```

This can be done either recursively or iteratively. The insertion is to follow the rule of BST and the tree after the insertion would still be a BST. 

### 3.2 (5pt) Write the following function that verifies an in-order traverse:

In the given tests for 3.1, the following function is provided:

```java
    private static List<Integer> inOrderTraverse(TreeNode<Integer> node) {
        List<Integer> result = new ArrayList<>();
        inOrderTraverse(node, result);
        return result;
    }
```

This is used to verify the tree is still a BST after insertion. However, this test code itself also needs to be verified. Finish the test for this test:

```java
    @Test
    public void testInOrderTraverse() {
        // homework
        // to verify inOrderTraverse(TreeNode<Integer> node)
    }
```

You read that right. This is a test for test. #recursion eh.

### 3.3 (5pt) With your BST insertion, analyze this test:

```java
        //      1
        //     / \
        //    N   N
        // homework
        // what problem can you see for insertInBst from this test case?
        // answer:
        // discuss how you would solve it in a comment below
        // answer:
        root = new TreeNode<>(1);
        testCases.add(new BSTTestCase<>(root, 2, Arrays.asList(1, 2)));
        testCases.add(new BSTTestCase<>(root, 3, Arrays.asList(1, 2, 3)));
        testCases.add(new BSTTestCase<>(root, 4, Arrays.asList(1, 2, 3, 4)));
        testCases.add(new BSTTestCase<>(root, 5, Arrays.asList(1, 2, 3, 4, 5)));
```

What problem can you see from your insertion? The idea comes from how binary search tree is supposed to provide fast search. As fast as a binary search. After inserting all these values, can the resulted BST still guarentee that fast search any more? Explain your findings in a comment near this test case.





