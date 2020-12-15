## 2020 Fall CSS143B Final Exam - Example

**All choice questions are single choice**

**2. (2pt) Which of the following statements about Stack and Queue ADT is FALSE?**

- (A) Stack is First-In-Last-Out
- (B) Queue is First-In-First-Out
- (C) Stack can be used to implement a recursive algorithm iteratively
- (D) Stack can only be implemented with array, and therefore its size is limited by the initial capacity

**6. (10pt) You can't handle the truth!**

In the lecture we saw the following code that calculate and sort the word frequency based on part of the movie "a few good men".

```java
        // use map to count the occurrences of each word
        HashMap<String, Integer> wordMap = new HashMap<>();
        for (String word : words) {
            if (wordMap.containsKey(word)) {
                wordMap.put(word, wordMap.get(word)+1);
                continue;
            }
            wordMap.put(word, 1);
        }

        // sort the map based on number of occurrences
				// 2nd block starts here
        TreeMap<Integer, Set<String>> sortedMap = new TreeMap<>(Collections.reverseOrder());
        for (Map.Entry<String, Integer> entry : wordMap.entrySet()) {
            int key = entry.getValue();
            Set<String> values = sortedMap.containsKey(key) ? 
                       sortedMap.get(key) : new HashSet<>();
            values.add(entry.getKey());
            sortedMap.put(entry.getValue(), values);
        }
```

Answer the following question about this code:

6.1 (2pt) Explain why the entry value of the variable ***sortedMap*** is a Set<String>, instead of a String.

```bash




```

**9. (15pt) Based on the following tree**

```bash
          25
        /    \
       19    33
      / \    / 
     11  3  1  
```

What is the pre-order, in-order and post-order traversal of the above tree
```bash
pre-order:


In-order:


post-order:


```

**11. (5pt) Answer the following questions about the Cats and animal classes**

```java
public abstract class Animal {
    private String name;
    private String gender;
    private int age;
    
    public abstract void speak();
    
    public Animal(String name, String gender, int age) {
        this.name = name;
        this.gender = gender;
        this.age = age;
    }
    
    public String getName() {
        return name;
    }
}

public class Cat extends Animal {
  private String furColor;
  public Cat(String name, String gender, int age, String furColor) {
        super(name, gender, age);
        this.furColor = furColor;
    }
    
    @Override
    public void speak() {
        System.out.println("Cat " + getName() + " says 'meow'");
    }
}
```

11.1 (2pt) Why does the keyword ***abstract*** do in the definition of ***speak()***  in Animal class?

```bash


```
