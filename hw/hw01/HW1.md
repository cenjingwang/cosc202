# COSC 202 Fall 2026: HW1


## Overview

In this HW you are given an implementation of the efficient search algorithm you designed in Lab 1. Your task is as follows:
* Remind yourself about how Java works, and understand how the different files work together.
* Find errors in the implementation, and fix them.
* Explain how the final implementation works and justify its correcntness.


### Files provided
1. `SortedList.java` with an implementation of the SortedList data structure
2. `CustomSearch.java` with the incorrect implementation
3. [A google doc template](https://docs.google.com/document/d/1SYUz5DxK2NKSU6aOH_Ncux8f_E-8ftxz47H28N_DebA/edit?usp=sharing) to put together the writeup with the justification of correctness. 

### Submission 

Submit the following two files to Gradescope: 
1. `CustomSearch.java`
2. `writeup.pdf`

## Grading

You will receive 2 points from autograder, and 1 point for the justification of correctness document. The syllabus has further details about how these scores fit into the overall course grade. 

Note: The names of test cases in the autograder are deliberately vague, since the goal is for you to be able to reason about what to test your implementation on. Some test cases give you expected output, whereas others just tell you whether you failed. 

| **Possible outcome** | **How it impacts autograder score**|
| --- | --- 
| Test case passed. | Full credit for test case | 
| Test case passed. Run time is correct asymptotically, but can do better. | Full credit for test case | 
| Correct output, incorrect runtime | Partial credit for test case| 
| Test failed. | No credit for test case | 


*Hint: When testing for efficiency, look at the `get_count` method in SortedList and think about how you might use it*