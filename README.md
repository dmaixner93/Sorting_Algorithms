# Sorting_Algorithms

**Sorting is the process of rearranging the items in a collection of data so that the items are in order (smallest to largest, highest to lowest, etc.)**.

When it comes to data, their are many ways to actually sort it. Before sorting the data, the user will need to take into account the present state of the data, the type of data, and the amount of data. Knowing these key factors will depend on the method that is used to actually sort the data.

The types of sorting algorithms that will be discussed in this repository are:

** Basic Sorting Algorithms**
- Bubble Sort
- Selection Sort
- Insertion Sort

** Intermediate Sorting Algorithms**
- Merge Sort
- Quick Sort
- Radix Sort

## Bubble Sort

**Time complexity: O(n) - Best case
                   O(n<sup>2</sup>) - Average/worst case**

Bubble sort is a sorting algorithm where the largest values "bubble" to the "top" of the data.

## Selection Sort

**Time complexity: O(n) - Best Case
                   O(n<sup>2</sup>)**

Selection sort is very similar to bubble sort, the main difference instead of the larger values being places at the top the smallest numbers will be placed at the top of the data.

## Insertion Sort

**Time complexity: O(n) - Best case
                   O(n<sup>2</sup>) Average/worst case**

Insertion sort works by sorting out the "left" half of the data until completely sorted. For example, if the data is completely unsorted we will start by taking say the lowest number in data set and placing it at the left-most position.

Next, the algorithm will find the second lowest number. Once the second lowest number is found, it will be moved to the left most position available (exactly to the right of the lowest number).

This process will repeat until the data is completely sorted from smallest to largest (left to right respectively).

## Merge Sort

**Time complexity: O(n log(n))

Merge sort is more complex than the previous three algorithms. Merge sort works by taking an array of data and splitting that array of data down into smaller arrays until each array has a length of one or zero.

Once we have broken down the data into arrays of length zero or one the algorithm will begin to compare all the arrays. Comparing the arrays smaller arrays will help us determine where each value will do in a larger array since all the data will be combined back into one large sorted array.

## Quick Sort

Quick sort is similar to merge sort in that it will break down the data into smaller arrays until the lengths have reach zero or one. To begin breaking down the data into smaller arrays, the algorithm begins by finding the **pivot** or the center of the data. So if the array were [] we would start with the number 3.

Then the algorithm will place all values larger than 3 to the right of 3 and anything lower than 3 to the left of three in as-is order. So the data willno look like []. After 3 has been placed in the middle of the array, the algorithm will pick a new pivot point in the array on the left side of the previous pivot point. So, in the [], the new pivot point will be