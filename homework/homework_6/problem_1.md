## (40pt) Remove From ArrayDictionary

The [*ArrayDictionary*](https://github.com/pdgetrf/CSS143B-2020Fall-homework6/blob/master/src/main/java/Problem1/ArrayDictionary.java) class implements the [*Dictionary*](https://github.com/pdgetrf/CSS143B-2020Fall-homework6/blob/master/src/main/java/Problem1/Dictionary.java) interface as a dictionary with chaining capability for key collision. 

The hash function of this class is:

```java
    private int hashFunction(String key) {
        // not ideal
        return key.length();
    }
```

As stated in the comment, this is not the most capabable solution for a hash function but it helps us test the knowledge of the hash key vs entry key. "Hash key" is the integer value (return value of the hash function) produced by passing the entry key through the hash function. If multiple entry keys have the same hash key, these entries will be "chained" under the same hash key. Here's an example:

```
dictionary[0] = null
dictionary[1] = {(b, 18283)}
dictionary[2] = {(al, 00112233)}
dictionary[3] = {(ron, 451)(tom, 9999)(sam, 456)}
dictionary[4] = {(tony, 789)(alex, 123)}
dictionary[5] = {(katie, 1122)}
```

"tony" and "alex" both has the same hash key 4 because both are 4 character long, and therefore they are chained (much like in a single linked list) in *dictionary[4]*.

Write the code to implement the remove function.

```java
    @Override
    public void remove(String key) {
        // homework
    }
```

This function removes a key value pair in the dictionary by it's key if it exists. Noop if otherwise. Tests are provided. Notice the key in the parameter is the entry key, not the hash key. All tests are provided and should pass upon correct completion. 

