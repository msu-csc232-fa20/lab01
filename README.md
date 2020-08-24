# lab01

An excursion into working with arrays in C++.

## Background

Arrays are one of the first "data structures" introduced in introductory programming classes. An array contains a number of data items, or **entries**, that have the same data type. In memory, each of these entries reside in _contiguous_ memory locations.

## Getting Started

1. Accept the GitHub Classroom Assignment Link provided to you in Microsoft Teams for Lab 1 - Arrays
1. Once your repository has been created, clone it to your local machine

   ```bash
   $ git clone <url-of-your-repository>
   ```

1. Before you get started on any work, let's create the `develop` branch and push it to `origin`.

   ```bash
   $ git push -u origin develop
   ```

## Tasks

This lab is composed of three parts:

1. Part 1: Exploring One-dimensional Arrays
1. Part 2: Exploring the Indexes and Addresses of Arrays
1. Part 3: A Brief Look at Multidimensional Arrays

As you follow along in this lab assignment, you'll be asked to

1. Erase `TODO` comments in this `README.md` file
1. Add and/or edit files.
1. Commit your changes.
1. Push your changes to GitHub

In the end, i.e., after your final commit and push, you'll be asked to create a pull request and then submit the URL of your repository in a Microsoft Teams assignment.

### Part 1: Exploring One-dimensional Arrays

1. Create a file name `array.cpp` that contains the following stub:

   ```c++
   #include <cstdlib>
   #include <iomanip>
   #include <iostream>
   #include "lab01.h"

   int main()
   {
       return EXIT_SUCCESS;
   }
   ```

   A stub is a complete program fragment that will compile but won't necessarily do anything. To verify your stub is syntactically correct, compile, link and execute this program using the following commands (in a Cygwin terminal window, or any shell available on your system) from your working directory (the root folder of your repository):

   ```bash
   $ g++ -Wall -std=c++11 -o lab01 array.cpp
   $ ./lab01.exe
   ```

   When you execute these commands, you will discover that nothing happens. It compiles and links, but when executed, it doesn't do anything. Not a big surprise, right?

   Now that we're confident our stub compiles and executes, let's commit our changes.

   ```bash
   $ git add array.cpp
   $ git commit -m"LAB01 - Complete Part 1, Step 1."
   ```

   // TODO: Remove this line when you have finished this step.

1. Next, add two `typedef` statements of the form

   ```c++
   typedef array-element-type type-name[array-size];
   ```
   
   ahead of `main()` to define the two data types:
   
   `IntegerArray` for arrays with 16 integer elements
   `CharArray` for arrays with 10 character elements
   
    Save your file and commit your changes.

   ```bash
   $ git add array.cpp
   $ git commit -m"LAB01 - Complete Part 1, Step 2."
   ```

   // TODO: Remove this line when you have finished this step.

1. Inside the `main()` function, declare and initialize an `IntegerArray` variable `prime` to be an array containing the 16 integers: 2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47, 53, using a declaration of the form:

   ```c++
   type-name array-name = {comma-separated-list-of-values};
   ```

    Save your file and commit your changes.

    ```bash
   $ git add array.cpp
   $ git commit -m"LAB01 - Complete Part 1, Step 3."
   ```
   
   // TODO: Remove this line when you have finished this step. 

1. Check that the array has been initialized properly by writing a `for` loop to display the elements of `prime`. Then recompile and execute your program (as you did in Step 1) to check if your statements are correct.

   Use `std::setw(n)` and `std::right` IO manipulators to produce right-aligned output that looks like this:
   
   ```text
   prime[ 0] =  2
   prime[ 1] =  3
   prime[ 2] =  5
   prime[ 3] =  7
   prime[ 4] = 11
   prime[ 5] = 13
   prime[ 6] = 17
   prime[ 7] = 19
   prime[ 8] = 23
   prime[ 9] = 29
   prime[10] = 31
   prime[11] = 37
   prime[12] = 41
   prime[13] = 43
   prime[14] = 47
   prime[15] = 53
   ```

   Once you have your program working properly, commit your changes.


    ```bash
   $ git add array.cpp
   $ git commit -m"LAB01 - Complete Part 1, Step 4."
   ```

   // TODO: Remove this line when you have finished this step.

1. An initializer list with too many values is an error. Some compilers detect this error while others do not. Those that do not may allow the program to actually compile and run, and this will result in errors. Now you are to test your particular compiler to determine its behavior.

   What happens when you try to compile a statement with too many values in the initializer list? You can find out by adding one or more values to your initializer list for `prime`. Do this and describe what happens below:
   
   ```text
   TODO: Erase this line and put your answer in this text block.
   ```

1. It is not an error to give too few values in the initializer list of an array.

   What happens in this case? You can find out by changing the initialization of `prime` to use fewer than 16 integers and outputting the array elements. Describe what happens below:
   
   ```text
   TODO: Erase this line and put your answer in this text block.
   ```
   
1. Now you will repeat the experiment performed on the `IntegerArray` using a `CharArray`. First surround the declaration of the integer array `prime` and the `for-loop` that displays the elements with macros to remove it from compilation:

   ```c++
   #if EXECUTE_BLOCK
   
   // statements to ignore when EXECUTE_BLOCK is set to FALSE
   // in the lab01.h file
   
   #endif
   ```
   
   When you have blocked out the integer array `prime` and the `for` loop, then declare the `CharArray` variable `animal` initializing it with the characters `'r', 'h', 'i', 'n', 'o', 'c', 'e', 'r', 'o', 's'`. Check that the array has been properly initialized by adding a `for` loop that displays the elements of `animal` followed by something like `****`, all on the same line. After you have completed this, execute the `Part1` target. Describe what happens (i.e., what is printed) below:
   
   ```text
   TODO: Erase this line and put your answer in this text block.
   ```
   
1. Now check if adding one or more characters, i.e., adding too many initialization values, affects what happens. If so, add one or more characters and repeat the test. Describe what happens below.

   ```text
   TODO: Erase this line and put your answer in this text block.
   ```
   
1. Now check what happens when there are fewer values in the initializer list. Remove all but the first five characters in the initializer list and run the `Part1` target again. Describe what happens below.
                                                                                                                                                                                  
   ```text
   TODO: Erase this line and put your answer in this text block.
   ```
   
1. It may not be completely clear what happened when the uninitialized character array locations were reached. What did the output operator do when the `for` loop sent it the character array elements that had not been initialized? To see this, modify the output in the `for` loop to display the actual ASCII codes being generated for each character array element. (_Hint_: Use a static cast `static_cast<int>(animal[i])` to convert `char`s to `int`s.) Tell below what is used to initialize the uninitialized array elements.

   ```text
   TODO: Erase this line and put your answer in this text block.
   ```
   
1. Now try initializing the character array in a different way. Character arrays can also be initialized by using string literals like `"elephant"` -- so we can initialize the character array `animal` using the string literal in place of the curly brace initializer list syntax. We can also output a character array using `<<` directly, as in 

    ```c++
    std::cout << animal << "****\n";
    ```
   
   Make the necessary changes to use the string `"elephant"` and record what happens below.
   
   ```text
   TODO: Erase this line and put your answer in this text block.
   ```
   
1. Now repeat the test using the string `"rhinoceros"` instead. Describe what happens below.

   ```text
   TODO: Erase this line and put your answer in this text block.
   ```
   
   You may have gotten a warning message, even though the array has been declared to have 10 elements. The reason is that the character arrays are terminated by **null characters**, `'\0'`, whose ASCII code is 0, provided there is room to store this character. Since functions that process character arrays and expect to find this null character at the end of the string that is stored, they may not work properly when there is none.

   Thus, character arrays such as `animal` that are used to store strings should be declared large enough to store at least one extra character at the end of each string value, namely, the null character. This character is used by functions that process strings stored in character arrays to mark the end of the string. To see how this is done:
   
   (i) Change the initialization string of `animal` to `"zebra"`.
   
   (ii) Now write C++ statements below that could be used to determine the length of the string stored in `animal`, that is, the number of non-null characters. Test that your code works by entering it into your program and executing it. (_Note_: For fun ;-), see if you can do this using a `for` loop with an empty body.)
   
   ```c++
   TODO: Put your snippet of code here.
   ```

_Remember_: The end-of-string mark (i.e., the null character `'\0'`) that gets placed at the end of each initialization string or a string that is input for a character array (e.g., `cin >> animal;`) provided that the character array has space for it. If it doesn't get stored, one cannot expect string operations and functions to work correctly. Thus, one must be sure the array is large enough so that it has space for this null character.

### Part 2: Exploring the Indexes and Addresses of Arrays

1. fsefsdf
1. sdfsdf

### Part 3: A Brief Look at Multidimensional Arrays

1. sdfsdf
1. sdfsd

## Submission Details

sldkfsdlf

## Due Date

This assignment is due by the end of the lab period.

## Grading Rubric

_This assignment is not graded. However, if it were, it would be assessed using the following rubric._

This assignment is worth 3 points.

Category | Acceptance Criteria | Points
---------|---------------------|-------
Pull Request | A pull request is created and the URL of the repository is submitted as a link in Microsoft Teams by the due date. | 0.5
Programming Style | All source code written by the student follows a consistent, reasonable style for C++. | 0.5
Program Correctness | Program correctness is assessed through the use of Google Test unit tests.* | 2.0

_When Google Test unit tests are utilized for assessing program correctness, the points assigned are normalized to 2.0 points based on the fraction of tests that pass._