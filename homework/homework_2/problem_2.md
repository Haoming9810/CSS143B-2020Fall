## (35pt) Remove Duplicates From Sorted Array

Given a ascendingly (small to large) sorted array, remove the duplicates such that each element appears only *once*, and return the new length. This is to be done in-place which means any extra space for another array is not allowed. Similar to how you did it for the bubble sort problem.

Function signature is:

```java
public static int remove(int[] nums)
```

Things to pay attention to:

- Return value is the new length after all duplicates are removed
- The input array "nums" is to be modified directly without any additional space (such as another array)
- The input array should still be sorted after removing all the duplicates

A few examples: 

Given nums = [0, 0, 0, 1, 1, 2, 2, 3, 4, 5, 5]

- Return value is 6
- Array nums becomes [0, 1, 2, 3, 4, 5], array content after index 5 is ignored in tests

Given nums = [0, 0, 0]:

- Return value is 1
- Array nums becomes [0], array content after index 0 is ignored in tests

### Communication Points

For 5pt out of this 35pt, at the beginning of the code, describe your algorithm in up to 5 sentences in comments. Zero point if it's missing or exceeds 5 senteces. 

### Testing (5pt)
Only 1 test case is provided as an example. Please add at least another 5 cases.
