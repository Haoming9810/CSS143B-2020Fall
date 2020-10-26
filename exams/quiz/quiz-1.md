## Quiz-1

### Dates

- Assigned: 10/26 (Monday)
- Due: 10/29 11:59pm (Thursday midnight)

### Tasks

In the media store problem of homework 2, we were asked to implement the *equals* function for both Book and Movie class.

```java
    @Override
    public boolean equals(Object obj) {
        // homework
    }
```

And the definition of "being equal" for books and movies are:

```
A movie equals another movie only when their id are the same. Same rule for books being equal.
```

Unfortunately, Lots of us missed this and instead implemented it this way:

```java
 return id.equals(theOtherBook.id) &&
                author.equals(theOtherBook.author) &&
                title.equals(theOtherBook.title);
```

Now comes the interesting part. The tests provided for this problem would still pass even with this wrong implementation. So it's a bug that is not caught by our tests. #awkward.

In this quiz, let's fix this issue by doing the following tasks:

1. Find out why tests can still pass with this bug in effect. Explain it with a paragraph in your PR description (30pt)
2. Add some new tests to catch this bug.

Starter code is [here](https://github.com/pdgetrf/media-store-bug-fix.git)

"*But how do I know whether my tests catch this bug?*" You ask.

The location of the bug is already marked in both Movie and Book class, and the fix is also provided. So debugging is already done for you. All you need to do is to add the tests. Here's the rule to make sure your tests are correct:

- (35pt) Your new tests should fail with this bug without the fix, and pass when the bug is replaced with the fix provided. 
- (35pt) All the other previous tests should still all pass with or without the fix. 

DO NOT CHANGE OR REMOVE OLD TESTS OR ALL IS LOST.

Submit your PR the same way as other homeworks. In the submission, make sure your code has switched to the fix given for PR check to pass.

