<img src="images/chain.jpg"
     alt="bicycle"
     width="50%" />

## Linked List

### 1. (20pt) Reverse a linked list RECURSIVELY

Note that his linked list implementation uses dummy node.

reverse() reverses the order of nodes (**not just the value**) in a singly linked list. 

```java
public void reverse() {
    // homework
}
```

For example:

* If the list is empty, after calling the reverseIterative() the list will still be empty
* If the list has 1, after calling the reverseIterative() the list will be 1
* If the list has 1->2->3, after calling the reverseIterative() the list will be 3->2->1
* If the list has 1->2->3->4, after calling the reverseIterative() the list will be 4->3->2->1

reverse() works by changing the order of existing nodes ***without creating any new node*** or changing the value of any node. This is to be done ***recursively*** which means no loop of any kind is allowed.

No additional storage like array, stack, queue or another linkedlist is allowed for this problem.

### 2. (30pt) Sort a single linked list RECURSIVELY

Note that his linked list implementation does NOT use a dummy node.

In this task, we need to write the code to implement this sort. The requirements are:

- Must use recursion.
- Cannot allocate any collection storage such as array, stack or queue.
- Cannot change the value of any node. Only the *next* variable can be changed.

To be honest, the algorithm is pretty difficult to come up with (doesn't mean your shouldn't try), and it's not really the point for a homework. To make life a bit easier, the algorithm will be presented to you here. All you need to do is put the idea into code and see it come alive running, backed by tests. The followoing paragraph will describe the algorithm. You might want to pause here for some thinking if you want to challenge yourself to come up with your own algorithm following the above requirements.

Given a list e.g.

```
4->2->1->8->5->3->10->9->n
```

The idea is to split it into two halves:

List 1:

```
4->2->1->8->n
```

List 2: 

```
5->3->10->9->n
```

Using the idea of recursion, if we get both list 1 and list 2 sorted, then we'll have

List 1:

```
1->2->4->8->n
```

List 2: 

```
3->5->9->10->n
```

All we need to do now is to **combine** the two lists into one list:

```
1->2->3->4->5->9->9->10->n
```

But how do we sort list 1 and list 2 to begin with? Well, think about this question for a second, out loud even......

This is the same task of sorting a linked list right? Then we can use the same idea recursively. If we break each of these 2 lists into their two halves, sort all the halves and merge them, we can sort list 1 and list 2. 

So to get this task done, we essentially have 3 functions:

1. Break a linked list into two equally sized lists (or size by 1)
2. Sort both halves
3. Merge the sorted halves back into one lists. 

During this process, we cannot allocate any collection data structure like array or queue or array list or stack. And we cannot change any node's value. 

The sort function is provided to you

```java
    public static ListNode sortList(ListNode head) {
        if (head == null) {
            return null;
        }
        if (head.next == null) {
            return head;
        }
        ListNode mid = findMidAndBreak(head);
        return mergeLists(sortList(head), sortList(mid));
    }
```

This is the "glue" to put all 3 tasks together. And you need to write the other two functions:

```java
public static ListNode findMidAndBreak(ListNode head) {
        // homework
        return null;
}
```

This function takes the given list, break it from middle into two lists. The first half should still start with *head*, and it returns the beginning node of the 2nd half.

```java
public static ListNode mergeLists(ListNode list1, ListNode list2) {
    // homework
    return null;
}
```

This function takes two sorted linked list, merges them into one sorted list, and then returns the head node. No new node can be created for this, and both lists can be visited from head to end only once. 

Tests are provided for the above 2 functions. Once both tests passed, the sort list function should also pass its test. 

Happy sorting :)
