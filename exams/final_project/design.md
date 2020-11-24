### The Design

Given the following documents:

 - document 0: "hello world"
 - document 1: "hello"
 - document 2: "world"
 - document 3: "world world hello"
 - document 4: "seattle rains hello abc world"
 - document 5: "sunday hello world fun"

Each document is a series of words. In our code, each document is represented by a String.

search() returns the *document ids* that contain the given search phrase based on the indexes. 

```java
public interface Searcher {
    List<Integer> search(String keyPhrase, Map<String, List<List<Integer>>> indexes);
}
````

A search of "world" would return [0, 2, 3, 4, 5].

A search of "hello world" would return [0, 5].

Notice that a phrase kehyword like "hello world" only matches documents that have this phase as a whole, not by single word, e.g. here documents 0, and 5. Document 3 contains both "hello" and "world" but in the opposite order, so it is not a match. Also, search only matches **full words**. For example, with the above documents, search("llo wor") will return [] even though this string exists in documents 0, and 5.

### The Index

The search function works by utilizing an index of the given documents. Indexing collects, parses, and stores data to facilitate repeated fast search. An index is generated whenever a new set of documents are loaded to the system. It's only done once whereas search is carried out repeatedly using an index.

Before you say "just use string comparision with the keyword on each document", keep in mind that search engines usually deal with very large documents and see lots of repeated searches. Direct string comparison is usually *O(n)* complexity with *n* being the size of the string, so it's not an efficient and fast algorithm to use here. With an indexing (or hashing) based algorithm, on the other hand, the complexity can be largely reduced. The idea is to have a hash table data structure where key is each word in all the docs, and value is a vector of all the documents that contain that word. For example:

- "hello" : \[0, 1, 3, 5\]
- "seattle" : \[4\].

This way, if "hello" is searched, we can quickly return in *O(1)* time that it appears in document 0, 1, 3, and 5.

With this single layer of structure, it is still hard to search phrase composed of multiple words because words in a phrase matters in a search, and therefore the information of where each word appears in documents also need to be stored in the indexes. [This post](http://www.ardendertat.com/2011/05/30/how-to-implement-a-search-engine-part-1-create-index/) has good explanation on how the index is designed. We will review the design in the lecture.

The indexer signature is:

```java
public interface Indexer {
    Map<String, List<List<Integer>>> index(List<String> docs);
}
```

The index is a Map. They key is each word in all the documents, the value is a list representing all the documents. For each document, another list is used to store the location where the word appears in that document. Here's an exmaple:

For the set of 7 documents

```
                               "world world hello world",
                                "world world hallo",
                                "world seattle hello abc world day",
                                "abc hello world fun",
                                "sunny    better",
                                "     fun day fun",
                                "     day sunny fun   "
```

The index generated would be:

```
{
better=[[], [], [], [], [1], [], []], 
hallo=[[], [2], [], [], [], [], []], 
world=[[0, 1, 3], [0, 1], [0, 4], [2], [], [], []], 
abc=[[], [], [3], [0], [], [], []], 
hello=[[2], [], [2], [1], [], [], []], 
seattle=[[], [], [1], [], [], [], []], 
sunny=[[], [], [], [], [0], [], [1]], 
day=[[], [], [5], [], [], [1], [0]], 
fun=[[], [], [], [3], [], [0, 2], [2]]
}
```

