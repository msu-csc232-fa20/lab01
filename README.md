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

### Part 1: Exploring One-dimensional Arrays

1. Create a file name `array.cpp` that contains the following stub:

   ```c++
   #include <cstdlib>
   #include <iomanip>
   #include <iostream>

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

1. sdlfksf

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