# Quick-sort Algorithm
The algorithm was developed by a British computer scientist Tony Hoare in 1959. The name "Quick Sort" comes from the fact that, quick sort is capable of sorting a list of data elements significantly faster (twice or thrice faster) than any of the common sorting algorithms. It is one of the most efficient sorting algorithms and is based on the splitting of an array (partition) into smaller ones and swapping (exchange) based on the comparison with 'pivot' element selected. Due to this, quick sort is also called as "Partition Exchange" sort. 

Like Merge sort, Quick sort also falls into the category of divide and conquer approach of problem-solving methodology.

## Application

Quicksort works in the following way
Before diving into any algorithm, its very much necessary for us to understand what are the real world applications of it. Quick sort provides a fast and methodical approach to sort any lists of things. Following are some of the applications where quick sort is used.

* Commercial computing: Used in various government and private organizations for the purpose of sorting various data like sorting of accounts/profiles by name or any given ID, sorting transactions by time or locations, sorting files by name or date of creation etc.

* Numerical computations: Most of the efficiently developed algorithms use priority queues and inturn sorting to achieve accuracy in all the calculations.
Information search: Sorting algorithms aid in better search of information and what faster way exists than to achieve sorting using quick sort.
Basically, quick sort is used everywhere for faster results and in the cases where there are space constraints.

## Explanation
Taking the analogical view in perspective, consider a situation where one had to sort the papers bearing the names of the students, by name from A-Z. One might use the approach as follows:

* Select any splitting value, say L. The splitting value is also known as Pivot.
* Divide the stack of papers into two. A-L and M-Z. It is not necessary that the piles should be equal.
* Repeat the above two steps with the A-L pile, splitting it into its significant two halves. And M-Z pile, split into its halves. The process is repeated until the piles are small enough to be sorted easily.
* Ultimately, the smaller piles can be placed one on top of the other to produce a fully sorted and ordered set of papers.
* The approach used here is reduction at each split to get to the single-element array.
* At every split, the pile was divided and then the same approach was used for the smaller piles by using the method of recursion.

## Technically, quick sort follows the below steps:
* Step 1 − Make any element as pivot
* Step 2 − Partition the array on the basis of pivot
* Step 3 − Apply quick sort on left partition recursively
* Step 4 − Apply quick sort on right partition recursively

# Quick Sort Example:

## Problem Statement
Consider the following array: 50, 23, 9, 18, 61, 32. We need to sort this array in the most efficient manner without using extra place (inplace sorting).

## Solution

### Step 1:

1. Make any element as pivot: Decide any value to be the pivot from the list. For convenience of code, we often select the rightmost index as pivot or select any at random and swap with rightmost. Suppose for two values “Low” and “High” corresponding to the first index and last index respectively.
1. In our case low is 0 and high is 5.
1. Values at low and high are 50 and 32 and value at pivot is 32.
1. Partition the array on the basis of pivot: Call for partitioning which rearranges the array in such a way that pivot (32) comes to its actual position (of the sorted array). And to the left of the pivot, the array has all the elements less than it, and to the right greater than it.
1. In the partition function, we start from the first element and compare it with the pivot. Since 50 is greater than 32, we don’t make any change and move on to the next element 23.
1. Compare again with the pivot. Since 23 is less than 32, we swap 50 and 23. The array becomes 23, 50, 9, 18, 61, 32
1. We move on to the next element 9 which is again less than pivot (32) thus swapping it with 50 makes our array as 23, 9, 50, 18, 61, 32.
1. Similarly, for next element 18 which is less than 32, the array becomes 23, 9, 18, 50, 61, 32. Now 61 is greater than pivot (32), hence no changes.
1. Lastly, we swap our pivot with 50 so that it comes to the correct position.
1. Thus the pivot (32) comes at its actual position and all elements to its left are lesser, and all elements to the right are greater than itself.

### Step 2: The main array after the first step becomes
* 23, 9, 18, 32, 61, 50

### Step 3: Now the list is divided into two parts:
* Sublist before pivot element
* Sublist after pivot element

### Step 4: Repeat the steps for the left and right sublists recursively. The final array thus becomes
* 9, 18, 23, 32, 50, 61.

