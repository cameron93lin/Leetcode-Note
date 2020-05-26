# Explore

## Max Consecutive Ones
>Given a binary array, find the maximum number of consecutive 1s in this array.

Change array to string with **map** and **join** in python3: 
```python3
def findMaxConsecutiveOnes(self, nums):
    max(map(len, ''.join(map(str, nums)).split('0')))
```

map(str, nums) #change array nums to str format array

''.join(array) #merge all element in array to a single string

split('0') #split the string with string '0' in this step we got all consecutive ones

map(len, array) #find length for each string in array

max() #find the max of the array

## Squares of a Sorted Array
>Given an array of integers A sorted in non-decreasing order, return an array of the squares of each number, also in sorted non-decreasing order.

Use two pointer to read positive and negative parts of the array and then merge them together

## Duplicate Zeros
>Given a fixed length array arr of integers, duplicate each occurrence of zero, shifting the remaining elements to the right.

O(1) Space solution

Use two pointer: Slow and fast. Fast pointer will move twice once slow pointer is point to zero while slow pointer only move one positon per time. Slow pointer will point to the last element of the new list while the fast pointer is at the end of the old list position. And then we start to move the slow pointer back once a time. If the slow pointer is pointing zero, the fast pointer will change current and current-1 element to zero, else the fast pointer will change current positon element to what the slow point is pointing.

## Merge Sorted Array
>Given two sorted integer arrays nums1 and nums2, merge nums2 into nums1 as one sorted array.
> - The number of elements initialized in nums1 and nums2 are m and n respectively.
> - You may assume that nums1 has enough space (size that is greater or equal to m + n) to hold additional elements from nums2.

Since the arrays nums1's length is the total length of the new array and the last n element in nums1 are all zero, we can pocessed from the largest element to the smallest element. We will use three pointer. First pointer will start at the mth of the nums1 array. Second pointer will start at the nth of the nums2 array. Third pointer will start at the end of nums1 array which is m + n - 1. For each pair element pointed by first and second pointer, we will put the larger number to the position where the third pointer is pointing. Move the third pointer to the next potion. Move the larget number pointer to the next position and loop it. 

## Remove Element
>Given an array nums and a value val, remove all instances of that value in-place and return the new length.

>Do not allocate extra space for another array, you must do this by modifying the input array in-place with O(1) extra memory.


By using two pointer, slow pointer will point the next positon, fast pointer will check if the element is the instance to be removed. If not, move the element to the slow pointer postion and move slow pointer to the next postion. If it is the instance need to be removed, move fast pointer to the next position. Loop it. Return slow pointer position which should be the new array length.

## Remove Duplicates from Sorted Array
>Given a sorted array nums, remove the duplicates in-place such that each element appear only once and return the new length.

>Do not allocate extra space for another array, you must do this by modifying the input array in-place with O(1) extra memory.

By using two pointer, slow pointer will point the next positon, fast pointer will check if the element is same as the previous element. If yes, move fast pointer to next postion. If not, move element to slow pointer position and move both pointer to the next position. 

## Check If N and Its Double Exist
>Given an array arr of integers, check if there exists two integers N and M such that N is the double of M ( i.e. N = 2 * M).

For each element in array, check if hashmap has such element key or has element\*2 value. If not store element as key and element\*2 as value into the hashmap. If yes return true.

## Valid Mountain Array
>Given an array A of integers, return true if and only if it is a valid mountain array.

Walk up until we can't and then check if the peak position is the first or last position of the array. If yes, return false. If not, walk down until we can't, and then check if the position is the last position of the array. If yes, return true. If not, return false.

## Replace Elements with Greatest Element on Right Side
>Given an array arr, replace every element in that array with the greatest element among the elements to its right, and replace the last element with -1.

>After doing so, return the array.

We can loop the element from right to left and keep store the max of the list.

## Remove Duplicates from Sorted Array
>Given a sorted array nums, remove the duplicates in-place such that each element appear only once and return the new length.

>Do not allocate extra space for another array, you must do this by modifying the input array in-place with O(1) extra memory.

Use two pointer.

## Move Zeroes
>Given an array nums, write a function to move all 0's to the end of it while maintaining the relative order of the non-zero elements.

Since we dont care the order of the zero, we can use two pointer to move the Non-zero element. 