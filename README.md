# Sorting_Algorithms

**Sorting is the process of rearranging the items in a collection of data so that the items are in order (smallest to largest, highest to lowest, etc.)**.

When it comes to data, their are many ways to actually sort it. Before sorting the data, the user will need to take into account the present state of the data, the type of data, and the amount of data. Knowing these key factors will depend on the method that is used to actually sort the data.

The types of sorting algorithms that will be discussed in this repository are:

**Basic Sorting Algorithms**
- Bubble Sort
- Selection Sort
- Insertion Sort

**Intermediate Sorting Algorithms**
- Merge Sort
- Quick Sort
- Radix Sort

## Bubble Sort

**Time complexity: O(n)** - Best case | **O(n<sup>2</sup>)** - Average/worst case

Bubble sort is a sorting algorithm where the largest values "bubble" to the "top" of the data.

## Selection Sort

**Time complexity: O(n)** - Best Case | **O(n<sup>2</sup>)** - Average/worst case

Selection sort is very similar to bubble sort, the main difference instead of the larger values being places at the top the smallest numbers will be placed at the top of the data.

## Insertion Sort

**Time complexity: O(n)** - Best case | **O(n<sup>2</sup>)** Average/worst case

Insertion sort works by sorting out the "left" half of the data until completely sorted. For example, if the data is completely unsorted we will start by taking say the lowest number in data set and placing it at the left-most position.

Next, the algorithm will find the second lowest number. Once the second lowest number is found, it will be moved to the left most position available (exactly to the right of the lowest number).

This process will repeat until the data is completely sorted from smallest to largest (left to right respectively).

## Merge Sort

**Time complexity: O(n log(n))**

Merge sort is more complex than the previous three algorithms. Merge sort works by taking an array of data and splitting that array of data down into smaller arrays until each array has a length of one or zero.

![](images/merge_sort_one.png)

Once we have broken down the data into arrays of length zero or one the algorithm will begin to compare all the arrays. Comparing the arrays smaller arrays will help us determine where each value will do in a larger array since all the data will be combined back into one large sorted array.

![](images/merge_sort_two.png)

## Quick Sort

**Time complexity: O(n log(n))** - Best/average case | **O(n<sup>2</sup>)** - Worst case

Quick sort is similar to merge sort in that it will break down the data into smaller arrays until the lengths have reach zero or one. To begin breaking down the data into smaller arrays, the algorithm chooses a **pivot** value. It will then move the values less than the pivot to the left of the pivot, and numbers greater than the pivot to the right of the pivot.

4 will become the first pivot

[<strong>4</strong>,6,2,5,1,3]

Say our array of is [3,5,4,2,1] the algorithm will start by chosing the number 3. The algorithm will then run through the rest of the data, placing values less than 3 to the left of 3 and values greater 3 to the right of 3. The array of numbers will now look like [2,1,**3**,5,4].

Next, the algorithm picks a new number to the left of the previous pivot point, to be the new pivot value. In this scenario, there are only two numbers left of 3 which are 2 and 1. The algorithm splits these two numbers up into their own arrays. Now that the algorithm has broken every value to the left of the 3 down into their own arrays it will compare 1 and 2 and place them back into the original array in order. Thus, the data now will look like [1,2,3,5,4].

After the left side has been sorted, the algorithm moves to the right side of 3, selectes a new pivot and repeats the entire process until the data is sorted.

## Radix Sort

**Time Complexity:**

Radix sort is different than any of the previous sorting algorithms because it sorts data but does not compare number to number. Radix sort exploits the fact tha information about the size of a number is encoded in the number of digits (Example: 200 > 78 = true).

Radix sort begins by looking at all the numbers in a data set. Say we have [1554,6,3554,591,410,4388,900,5,8155,84,9635], the algorithm will look at all of the values in the array. The first pass through the array, the algorithm will look at the **right most digit** of **every value** in the array. The algorithm then sorts the values based on the digit and groups the numbers together.

<img>

After each number in the array is sorted by its right-most digit, the algorithm moves on to the next most right digit in the array (exactly one place to the left of the previous digit). The numbers will then be sorted by this digit and placed in there corresponding groupings. If the number is a single digit, then the number is left where it was last moved to.

<img>

Radix sort continues to sort the numbers in the groupings until all the digits have been "read" in the number with the most digits.