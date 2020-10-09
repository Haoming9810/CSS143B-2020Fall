## (30pt) Design OOP for A Media Store

A media retnal store needs to implement some operations for their books and movies. 

There are two kinds of media: Book and Movie. Both media types have an **id** field as its store unique identifier. 

There are two kinds of book in the store, fiction and romance.

There are two kinds of movie in the store, action and comedy.

Partial class implementation for Book, BookFiciton, BookRomance, Movie, MovieAction, MovieComedy are provided. Your task involves finishing all the parts marked with

```java
// homework
```

so that all tests can compile and run. All changes are to be made with provided files and provide functions. Do not add new files and there shouldn't be any need for new functions. Explain in comments if you strongly believe otherwise. Do not remve any code except comments from the given files. In fact, the tests will not pass if you do. 

### Tests Are Not Just For Testing

All tests are provided. You do not need to add any more tests, and more importantly, DO NOT CHANGE OR REMOVE any existing tests. Simply leave the test file alone. 

Use the tests as a "user manual" for how the media store functions should work. In specific, two functions to be implemented are

- equals

```java
    @Override
    public boolean equals(Object obj) {
        // homework
    }
```

This function is used to compare movie with movie, and book with book, but not book with movie. A movie equals another movie only when their **id** are the same. Same rule for books being eqaul. 

- calculate late fee

```java
    @Override
    public int calcLateFees(int numOfDaysPastDue) {
        // homework
    }
```

For all books and comedy movies, late fee is calculated by

```
numOfDaysPastDue x lateFeePerDayInDollar
```

For action movies, late fee is calculated slightly differently. Use the same fomula above if the number of days past due are less than 5 days. Otherwise use the following：

```
2 x numOfDaysPastDue x lateFeePerDayInDollar
```

As you can see, action movies are popular and therefore more penalty if returned late.

Both of the above two functions are declared in an interface:

```java
public interface StoreMediaOperations {
    int calcLateFees(int numOfDaysPastDue);

    int getLateFeeInDollar();
}
```

With this interface, the store can calculate late fees for a mixed set of store medias in a simple for-loop like this

```java
StoreMediaOperations[] s = new StoreMediaOperations[4];
s[0] = new BookFiction("t1", "au1", "g1");
s[1] = new BookRomance("t2", "au2");
s[2] = new MovieAction("r1", "t1");
s[3] = new MovieComedy("r2", "t2");
for (StoreMediaOperations storeMediaOperations : s) {
	fees += storeMediaOperations.calcLateFees(dayMissed);
}
```

Test 'testStoreMediaCalcLateFees' verifies this logic specificially. 
