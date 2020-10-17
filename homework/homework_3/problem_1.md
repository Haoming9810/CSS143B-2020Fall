## (40pt) Stacks

Stack is another ADT that's very commonly used. 

Unlike Queue which is First In First Out (FIFO), Stack is First In Last Out (FILO).

Similar to Queue, Stack can be implemented using array or list.

Interace of a stack is provided:

```java
public interface Stack<T> {
    boolean push(T val);
    T pop();
    T peek();
    int size();
}
```



### 1.1 Implement Stack Using Array (5pt)

Implement the ArrayStack where an array is used to store data.

### 1.2 Implement Stack Using LinkedList (5pt)

Implement the ArrayStack where a LinkedList is used to store data. Let's use [LinkedList](https://docs.oracle.com/javase/7/docs/api/java/util/LinkedList.html) from Java for this.

### 1.3 MinStack (15pt)

Design a special kind of stack can ***retrieve the minimum element in constant time without using loop to visit all the data in the stack***.

The MinStack class is based on your ArrayStack class from problem 1.1 as you can see from the "extends" operator. This means problem 1.1 needs to be done first.

```Java
public class MinStack extends ArrayStack<Integer> {
...
}
```

Complete the MinStack class such that:

- the constructor, pop(), push() work just like in a regular FILO stack.
- getMin() returns the minimum element currently existing in the stack in constant time. *"constant time"* means to find this minimum value, your code should have use constant number of steps no matter how many data elements exist in the stack. It shouldn't need to loop through all the elements in the stack. Take a look at *testMinStackPushPop* and *testMinStackPush* for examples on how getMin() works.

### 1.4 Validate Parentheses (15pt)

Now that you finished the Stack ADT, let's put it to some use.

Given a string containing just the characters '(', ')', '{', '}', '[' and ']', implement the ValidParentheses.isValid() ***using your ArrayStack or LinkedListStack*** in ValidParentheses to determind if the input string is valid. Using other stack implementation will loose you all the points for this problem 1.4.

An input string is valid if:

- Open brackets must be closed by the same type of brackets, and
- Open brackets must be closed in the correct order.

A null or empty string is also considered valid.

Here are some examples of valid parentheses:
- empty
- {}
- ()[]{}
- ([]) and []()
- ({[]}), [()()], ()[](), {}[[]]

On the countrary, the following are not "valid" parentheses string:
- ((]
- [)(}
- )(
- []{{]}
- [x]
