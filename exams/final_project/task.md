## A (Mini) Search Engine (40pt)

In this project, we are going to build a mini search engine that facilitates fast phrase search. 

Ready to take on google yet? Let's give it a try. 

We'll call this "project Elgoog".

The idea and algorithm design of this project comes from [this post](http://www.ardendertat.com/2011/05/30/how-to-implement-a-search-engine-part-1-create-index/). The original post was using python. Here we'll use Java.

### The Requirements

- The search engine Elgoog hosts a "database" of documents. Each "document" contains a series of english words
- Elgoog serves search request in the form of a website
- A search request is a phrase of a series of english words spearated by white spaces
- For a search request, Elgoog returns the *ids* of all the documents that contain the search phrase in exact match (word & order)

### The Assumptions

- Search is conducted based on English word. Words in documents are separated by white spaces
- For simplicty, a document is represented by a String object, and all words are lowercase
- No non-alphabetical character in any document

### The Website

The code to run a website is way beyond this class, so the code is provided to you. It's written using [Spring Boot](https://spring.io/projects/spring-boot). It uses an in-memory database to store the documents and index. We'll review this in lecture. After the class, this project would also be a good starting point if you need to create a website of your own.

[Here](http://ec2-3-128-153-78.us-east-2.compute.amazonaws.com:8081/) is what the project website looks like when it's finished. Use this to see how searching should work.

The website works on port 8081. On your local machine, open it by typing *http://localhost:8081 in a browser.

There are 3 services:

1. http://localhost:8081: The main search home page. */search* and */home* are redirected to the same home page
2. http://localhost:8081/docs: Shows all the documents currently used
3. http://localhost:8081/reindex: Replace the documents with a new set

### The Tasks

The website is already set up for you. What's to be done is the indexer and searcher:

- Indexer: Process documents into a data structure named *index* that allows faster searches on the same data set.
- Searcher: Search given phrases using the index.

Indexer is to be done only once when a set of documents are loaded into website (at startup or through the */reindex* service), while search is carried out repeated using the same index. 

### The Tests

#### Unit tests

Unit tests for indexer and searcher are provided. Upon finish, these tests will pass.

#### End to end tests

Start the webiste on your dev machine. Then go to browser and type "http://localhost:8081" in the address bar. This brings up the website's search page. Use this to verify your code works end-to-end altogether including indexing and searching. 

### The Design

Ready for taking on this work? The design of indexer and searcher is [here](design.md).

### The Grading

Upon successfully finishing this project, your work will be graded based on the following criterias:

-  (5pt) Pull request (PR) correctly created
  - No new files added (such as .idea folder, .iml files)
  - Having the right changes
  - From your work branch to your master branch in your repo
-  (5pt) Pull request has clear-written description including:
  - What's the changes
  - How it's verified on your side
  - Any notes to reviewer

- (5pt) PR has auto-validation running
- (15pt) All provided unit tests passed
- (10pt) Website starts correctly and pass simple end-to-end search test
