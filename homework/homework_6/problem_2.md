## (40pt) Performance Test

In [our lecture](https://youtu.be/5Gpc3kicQgc?t=1467) we saw a performance comparision of performance when searching an identity using four different data structures. The code for that test can be found in the [*IdentitySearchTest*](https://github.com/pdgetrf/CSS143B-2020Fall-homework6/blob/master/src/test/java/IdentitySearchTest.java) class. 

In this homework, let's add another test result similarly using the [*IdentityRemovalTest*](https://github.com/pdgetrf/CSS143B-2020Fall-homework6/blob/master/src/test/java/IdentityRemovalTest.java) class. The driver for the test is here:

```java
public void runTestOfSize(int size) {
        fillEmUp(size);
        Identity targetIdentity = idsArray.get(0);
        String targetByName = targetIdentity.username;

        StringBuilder sb = new StringBuilder();
        sb.append(String.format("%d\t", size));

        removeInArray(targetIdentity, sb);  // column 2
        removeInLinkedList(targetIdentity, sb); // column 3
        removeInBST(targetByName, sb); // column 4
        removeInHashtable(targetByName, sb); // column 5

        System.out.println(sb);
    }
```

In this test, the first element is removed from all 4 data structures and we'll compare the time it takes at different input sizes. When this code runs, it prints to the console the following:

```
5000	0.008142	0.024334	0.024799	0.004410	
10000	0.007464	0.003234	0.013507	0.003407	
15000	0.008610	0.002849	0.013852	0.003780	
```

The first column is problem size, and the rest 4 columns are the running time corresponding to the 4 function calls as commented above. 

The codes are already provided. No real coding work required for this task (except changing problem size in the loop). What's to be done is:

- Change the problem size to go from 5000 to something large (up to 1550000 depending on how large your computer can run). Gather the result from the console and plot the result following the same format of the graph on page 16 of the slides [class10_Monday.pptx](https://github.com/pdgetrf/CSS143B-2020Fall/blob/master/class10/class10_Monday.pptx)
- Add an analysis of this result. Focus on comparing the running time between the four data structures. Also a good idea to compare this to the result from searching and explain the difference. 

For submission, send in a doc (word or pdf) containing both the graph and the analysis text.  

## The End

As you reach this point, you've finished all the materials of this quarter. It's been a challenging special time with all covid threats and the online-only lecture, and we made it through! Great job! I hope the material was helpful and you had some fun. Best luck to your further adventure! Code on!


<img src="https://github.com/pdgetrf/CSS143B-2020Fall/blob/master/images/overview.png"
     alt="course"
     width="35%" />
