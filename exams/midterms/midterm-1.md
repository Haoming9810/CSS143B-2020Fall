## 2020 Autumn CSS143B Midterm 1 &nbsp; &nbsp; &nbsp; Student Name:

**1. (2pt) Single Choice**

```java
void foo() {}
```

The "void" keyword means this *foo()* method:

- (A) can return any primitive data type includng null
- (B) can only return reference, not primitive type
- (C) does not return anything
- (D) has optional return type

**2. (2pt) Single choice.** 

In the first lecture, a lego truck was used to illustrate:

- (A) How a car engine works
- (B) The idea and importance of testing
- (C) How to put together a lego piece
- (D) Software testing through mathmatical proof

**3. (2pt) Single choice.**
Suppose we have a class FooClass that has two public instance member variables, x and y, both of which are int. Both variables are set to 2 in the constructor.

What is output of the following code?

```java
MooClass a = new MooClass();
MooClass b = new MooClass();
b.x = a.y + 4;
a = b;
a.y = 7;
System.out.println(b.x + " " + b.y);
```
- (A) 2 7
- (B) 6 2
- (C) 2 2
- (D) 6 7
- (E) 4 7

**4. (2pt) Single choice. Consider the following code:**

```java
public static String addString(String str) {
  str = str + "rains too much";
  return str;
}
public void foo() {
  String str1 = "seattle ";
  String str2 = addString(str1);
}
```
After running the *foo()* function, which of the following is NOT correct:

- (A) Variable *str1* and *str2* are references both pointing at the same String object in memory
- (B) Variable *str1* never changed its String value
- (C) *str2* is "seattle rains too much" 
- (D) *str* inside *addString* changed its referenced object because String in Java is immutable

**5. (2pt) Single choice.**

The 'new' operator

- (A) creates a new object in memory
- (B) returns the memory location of a pre-existing object
- (C) is always required when declaring a class-type variable
- (D) must always be used when assigning values to variables

**6. (2pt) Consider the following code:**

```java
public static int foo(int x, int y) {
    return x*2+y+3;
}
public static double foo(double x, double y) {
    return x+y;
}
```
What is result of the following code?

```java
foo(10.0, 20.5)
foo(3, 4)
```

<br/>
<br/><br/>
<br/>

**7. (2pt) Is the code in problem 6 overloading or overriding?**

<br/>
<br/>
<br/>
<br/>

**8. (2pt) In the Cat & Dog classes, Cat inherites the Animal class.**

The Animal class code can be found [here](https://github.com/pdgetrf/OOBPet/blob/master/src/main/java/Animal.java). Here's one of the constructors of the Cat class:

```java
    public Cat(String name, String gender, int age) {
        super(name, gender, age);
        furColor = "known color";
    }
```

Explain what this *super* call does?

<br/>
<br/>
<br/>
<br/>

**9. (2pt) Dog and Cat classes both inherite the [Animal class](https://github.com/pdgetrf/OOBPet/blob/master/src/main/java/Animal.java). Assume the Animal class has a new function called sleep():**

```java
public String sleep();
```

And Cat and Dog classes both override this function. 

Now, suppose we want to keep 1000 Dog objects and 2000 Cat objects in the same array called ***animals***, What should be the data type for this ***animals*** array so they could be visited by the sleep() function?

 (hint: Not the Object class)

<br/>
<br/>

Next write the code to call the sleep() function in all of these 3000 objects in the ***animals*** array. Assume array is provided. The code can only have ONE loop without any condition statements (e.g. "if")

<br/>
<br/><br/>
<br/>

**10. (2pt) Recall our media store homework:**

The StoreMediaOperations interface has function ***getLateFeeInDollar()*** declared:

```java
public interface StoreMediaOperations {
    int calcLateFees(int numOfDaysPastDue);
    int getLateFeeInDollar();
}
```

However the Movie class that implements this interface does not actually implement this function:

```java
public abstract class Movie implements StoreMediaOperations {
    String rating;
    String title;
    UUID id;
    public Movie(String rating, String title) {
        this.id = UUID.randomUUID();
        // ...
    }
    public Movie(Movie anotherMovie) {
        // ...
    }
    @Override
    public boolean equals(Object obj) {
        // ...
    }
}
```

Even without implementing that two functions in the *StoreMediaOperations* interface, the Movie class still compiles correctly. Explain why this Movie class can compile without explicitly implementing these two functions.

<br/>
<br/>
<br/>
<br/>

**11. (5pt) In binary search**

```java
int mid = (start + end)/2;
```
what's the potential issue with the above code and how to fix it?
<br/>
<br/>
<br/>
<br/>

**12. (15pt) Write a function to check whether an integer array is Palindrome. **

When the content of an array reads the same from left to right as from right to left, it's called a palindrom or symmetrical. 

For example, 

- If the input is empty or null, the output should be True
- If the input is [3], the output should be True
- If the input is [2, 2], the output should be True
- If the input is [1, 2, 3, 2, 1], the output should be True
- If the input is [8, 2, 3, 3, 2, 8], the output should be True
- If the input is [2, 3], the output should be False
- If the input is [1, 2, 3, 4], the output should be False
- If the input is [1, 2, 3, 3, 1], the output should be False

```java
public static boolean isSPalindrome(int[] data) {

}
```

**13 (5pt) How would you test your isPalindrome function? Write down the test cases as you think necessary.**
<br/>
<br/>
<br/>
<br/>

**14. (5pt) What's the problem with the following testing strategy for the [reverseArray code](https://github.com/pdgetrf/code-along-reverse-array/blob/work/src/main/java/Problem.java)?**

"To verify reverseArray works correctly, for any given array, for example [3,2,1], call the reverse function twice. By reversing the input array twice, the input array should now be the same as before calling the reverse function. If it's not the same, that means the reverse function is wrong."
<br/>
<br/>
<br/>
<br/>

**15. (5pt) Given the following class**

```java
public class Student {
  int age;
  String name;
}
```
Implement the setter and getter functions for this class
<br/>
<br/>
<br/>
<br/>

**16. (5pt) When inplementing the Queue interface with an array, there's a capacity limitation because array cannot be resized. Describe how we can achieve the "illusion" of a resizable Queue for the add(int val) function with a primitive array (not ArrayList). What's the performance impact with this change?**
<br/>
<br/>
<br/>
<br/>

**17. (15pt) Design a storage system for Snapchat**

17.1 (6pt) When someone tries to log in to Snapchat, it needs to validate a user's identity. This is done by searching in a set of usernames. Login is permitted if username exists in the stored set of usernames, denied otherwise. As there's a huge number of users, and users log into Snapchat pretty often, this search needs to be very efficient. People don't have much patience nowadays. 

To achieve fast search, which data structure would you pick to store the usernames: array or a linked list? Explain how you can perform fast search with your choice and why you think it is faster than using the other data structure.  

<br/>
<br/>
<br/>
<br/>

17.2 (6pt) New users sign up for Snapchat pretty often, too. Suppose you decided to use an array to store the list of users for faster search, what are the downsides of using an array for inserting new users if you use binary search to search for logins. Analyze the performance cost when new users are constantly to an array? Would linked list have better performance for inserting user?

<br/>
<br/>
<br/>
<br/>

17.3 (3pt) It seems that both array and linked list have their pros and cons in the design for the user storage system for Snapchat. Now consider a hybrid design using both data structures. Usernames can be stored in linked lists while array can be used to quickly locate which linked list a username belongs to. Follow this thought and finish the design of the username storage system. The goal is still to be able to find old and insert new username as fast as possible. 

<br/>
<br/>
<br/>
<br/>

**18. (15pt) The following code comes from the array implementation for Queue**

```java
 1   @Override
 2   public Integer poll() {
 3       if (size == 0) {
 4           return null;
 5       }
 6       Integer val = data[front];
 7       front = (front + 1) % data.length;
 8       size--;
 9       return val;
 10  }
```

18.1 (5pt) Explain what this *poll()* function does. 

<br/>
<br/>
<br/>

(5pt) what does line #7 do? Supposed before calling the function, *front* is 8 and array *data[]* has capacity **10**. What's the value of *front* after calling poll?

<br/>
<br/>
<br/>
<br/>

(5pt) Again, supposed *front* is 9 upahead, and array *data[]* has capacity **10**. What's the value of *front* after calling poll?

<br/>
<br/>
<br/>
<br/>

**19. (4pt) What's the difference between Stack and Queue in terms of access pattrn?**

<br/>
<br/>
<br/>
<br/>

**20. (4pt) Write code to remove duplicates from a sorted single linked list in-place**

```
Input: 1->2->2
Output: 1->2
```

```
Input: 1->2->2->3->3
Output: 1->2->3
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

- Given the reference to the first node, the return linked list shall have all the unique elements in the original list. 
- Cannot use array or other collection type data structure.
- Cannot create new node.
- No dummy node.

``` java
public void removeDuplicates(ListNode head) {
  
  
  
  
  
}
```

**(3pt) Extra Credit**

You are writing tests for one of your project homework. Your friend Jerry came by and saw this. He said "The testing you are writing is meaningless! You wrote both the function and its tests. Of course the tests you write will always pass. What's the point?" Knowing the rule of testing, you decide to correct his mistake and strike the smirk off his face. how would you reply?

<br/>
<br/>
<br/>
<br/>
