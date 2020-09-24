## (45pt) Binary Search

Write a function to perform binary search in an ascendingly **sorted** integer array. Also write as many tests as you think necessary to demonstrate your binary search code works correctly. 

The binary search function takes an integer to find, and returns the first **index** of the input value if found. -1 if target is not found.

For example:

- Searching 6 in array [1, 3, 6, 8, 9] should return 2 because number 6 appears at index 2.
- Searching 9 in array [1, 3, 6, 8, 9] should return 4.
- Searching 7 in array [1, 3, 6, 8, 9] should return -1 because 7 is not found in this array.
- Searching 6 in array [1, 3, 6, 6, 9] should return 2 because the first 6 appears at index 2.

Your test can assume input array is correctly sorted. 

Binary search will be discussed in class as part of the search problem. If you need help, [here](https://www.geeksforgeeks.org/binary-search/) is a good start. Note that binary search can be implemented with or without recursion. If you are comfortable with recursion already, feel free to use it. Otherwise for-loop would be just fine. In fact, which method do you think is faster? (you can answer this in your code as a comment if you want to)

When the homework is done, your code should pass all the tests that come from the assignment and those your added.

