

# Assignment #1: C Programming Practice

 

## Guidelines

*Deviation from these guidelines will result in deductions or a zero score*

- This assignment is to be implemented in C (not C++, no other languages)
- No use of global arrays or variables.  You must use malloc (and free) to allocate memory
 
## Overview

The purpose of this assignment is to help you get started with programming in C and give you practice with pointer manipulation. The following specification is quite long and wordy. We are providing code skeleton files below. In those files, the specific wordy requirements (from this spec) are inserted as comments to make it clear what we expect for each function. If you have any questions regarding the assignment, please use the Canvas discussion forum

 
In the following specification, function prototypes and names of variables that appear in questions are formatted as code.  They are to be taken as is. Do not modify function prototypes. For this purpose, skeleton code has been provided (see red linked files below) with the questions in comments. It allows you to fill in the appropriate statements.

 
Use the main method of each file to test your code, samples are provided for this assignment.  We will be using a test harness that calls your functions individually, but we will not call main. You are responsible for making sure each function operates as specified.

In general 

 - A solution that does not compile is worse than...
 - ... a solution that seg faults or otherwise crashes. This is worse than...
 - ... a solution with the incorrect solution

 

### Q0.c

Write a program (Q0.c) to do the following: 

 
1. In the main function, declare an integer, `x`. Print the address of `x` (using the address of operator). Pass `x` as an argument to a function void `fooA(int* iptr)` (Hint: can you pass x itself directly?).

2. In `fooA(int * iptr)`, print the value of the integer pointed to by iptr, the address pointed to by iptr, and the address of iptr itself.

3. In the main function, following the call to `fooA(...)` , print the value of x.

4. Implement function `int fooB(int* a, int *b, int c)` which should perform the following computations

- Set the value pointed to by a a to twice its original value.
- Set the value pointed to by b b to half of its original value.
- Assign a + b to c .
- Return the value of c

 
## Q1.c

Write a program (Q1.c) in which you consider the following structure:

 
~~~
struct student {
     int id;
     int score;
};
~~~
 

and the declaration in the main function:

 
~~~
struct student* stud = NULL;
~~~
 

Implement the following functions and demonstrate their functionality by calling them (in the order given) from the main function

1. Write a function `struct student* allocate()` that allocates a contiguous chunk of memory for ten students and returns the pointer.

2. Write a function `void generate(struct student* students)` that populates the id and score fields.  Each student should have an id that corresponds to their index in the array (i.e., the first student in the array should have id 0). If each student's id is `x`, the student's score should be `(10*x)%50`

3. Write a function `void output(struct student* students)` that prints the ids and scores of all the students.

4. Write a function `float avg(struct student* students)` that computes the average of all scores

5. Write a function `int min(struct student* students)` that computes the average of all scores

5. Write a function void `deallocate(struct student* stud)` that frees the memory allocated to students. Check that students is not NULL (NULL == 0) before you attempt to free it.

6. Write a function void `sort(struct student* stud)` that sorts students by their score descending (i.e., highest scores at the top). You must sort the array *in-place* - that is, you should not allocate any additional memory.  *You may not use C sorting routines like qsort, you must implement it yourself*.  

 



What to turn in:

You will turn in 2 files Q0.c, Q1.c via TEACH . Use the provided makefile to compile on flip.

 
