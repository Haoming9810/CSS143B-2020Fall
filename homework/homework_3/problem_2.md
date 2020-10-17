## Linked List

All the following problems are assuming SingleLinkedList *using a dummy node*.

### 1. (10pt) Implement a copy constructor for SingleLinkedList
A [copy constructor](https://www.baeldung.com/java-copy-constructor) initializes a list by making an identical copy of the values in all the nodes in the given list.

#### Implement the following copy constructor in SingleLinkedList.java
```java
public SingleLinkedList(SingleLinkedList list) {
    // homework
}
```

For example:
Given a list that is  *h->1->2->3*, *h* is the head pointer. Run:
```java
SingleLinkedList newList = new SingleLinkedList(list);
```
and newList will be initialized as h->1->2->3.

Note that copy constructor will copy the values in each node, not the references. 

### 2. (15pt) Implement the remove function
```java
    public int removeAll(int valueToRemove) {
    // homework
    return 0; // place holder
}
```
This function removes *all* nodes whose val == valueToRemove and returns the number of node actually removed.

For example:

- If the list is empty, after calling the removeAll() with any input, the list will still be empty and return 0
- If the list is 1->2->3, after calling the remove(3) the list will be 1->2, and return 1
- If the list is 1->2->4->2, after calling remove(2) the list will be 1->4, and return 2
- If the list is 1->1->4->2, after calling remove(1) the list will be 4->2, and return 2
- if the list is 3->3->3->3, after calling remove(3) the list will be empty, and return 4
- If the list is 1->1->4->2, after calling remove(5) the list will still be 1->1->4->2, and return 0

### 3. (15pt) Implement the linked list reversal iteratively
```java
public void reverse() {
    // homework
}
```

reverse() reverses the order of nodes (**not just the value**) in a linked list. For example:

* If the list is empty, after calling the reverseIterative() the list will still be empty
* If the list has 1, after calling the reverseIterative() the list will be 1
* If the list has 1->2->3, after calling the reverseIterative() the list will be 3->2->1
* If the list has 1->2->3->4, after calling the reverseIterative() the list will be 4->3->2->1

reverse() works by changing the order of existing nodes without creating any new node or changing the value of any node. This is to be done iteratively which means recursion is not allowed.

No additional storage like array, stack, queue or another linkedlist is allowed for this problem.
