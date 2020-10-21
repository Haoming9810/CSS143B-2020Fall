## 2020 Autumn CSS143B Midterm 1 &nbsp; &nbsp; &nbsp; Student Name:

**1. (2pt) Single choice.**

```java
void foo() {}
```
The "void" keyword means:
- (A) return Strings.
- (B) return primitive type values.
- (C) return class-type values.
- (D) have no return value.

**9. (2pt) Dog and Cat classes both inherite the Animal class, and Animal class has a sleep() function like this:**

```java
    public String sleep();
```

We need to create 3 Dog objects and 5 Dat objects, and then call the sleep() function in all of them. 

Write code for this by using only 1 loop.

<br/>
<br/>
<br/>
<br/>

**9. (15pt) Write a function to check whether an integer array is in ascending order.**

For example, 

- If the input is empty or null, the output should be True
- If the input is [1, 2, 3, 4], the output should be True
- If the input is [1, 5, 3, 4], the output should be False

```java
public static boolean isAscending(int[] data) {


}
```

**10. (5pt) How would you test your  isAscending function? Write down the test cases as you think necessary.**
<br/>
<br/>
<br/>
<br/>

**13. (5pt) What does "late binding" mean?**
<br/>
<br/>
<br/>
<br/>

**14. (15pt) The following code comes from the array implementation for Queue**

```java
    @Override
    public boolean add(int val) {
        if (data == null || data.length == 0 || size == data.length) {
            return false;
        }
        data[end] = val;
        end = (end + 1) % data.length;
        size++;
        return true;
    }
```

14.1 (3pt) Explain what this code does. 

<br/>
<br/>
<br/>

**15. (10pt) Write code to remove the given number from the given single linked list in-place**

```
Input: 1->2->3, target 2
Output: 1->3
```

```
Input: 3->5->2->3->3->6, target 3
Output: 5->2->6
```

The node is defined as

```java
public class ListNode {
    public int val;
    public ListNode next;
    public ListNode() {}
    public ListNode(int val) {
        this.val = val;
    }
}
```

- Given the reference to the first node, and a target value, after *remove()*, the linked list should have all the original nodes in the same order, except all the nodes with the target value have been removed.
- Cannot use array or other collection type data structure.
- Cannot create new node.
- No dummy node.

``` java
public ListNode remove(ListNode head, int target) {
  
}
```
