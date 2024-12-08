# Minimum-in-Rotated-Sorted-Array
Suppose an array of integers sorted in ascending order is rotated at some pivot unknown to you beforehand. (i.e., [0,1,2,4,5,6,7] might become [4,5,6,7,0,1,2]).  You are given a rotated sorted array nums of unique integers. Write a function to find the minimum element in the array.
Example 1:
Input: nums = [3,4,5,1,2]
Output: 1

Example 2:
Input: nums = [4,5,6,7,0,1,2]
Output: 0

Example 3:
Input: nums = [11,13,15,17]
Output: 11

Constraints:

n == nums.length
1 <= n <= 5000
-5000 <= nums[i] <= 5000
All integers in nums are unique.
nums is a rotated array.

Explanation:
Binary Search Logic:

If the middle element (nums[mid]) is greater than the rightmost element (nums[right]), the minimum lies in the right half.
Otherwise, the minimum lies in the left half (or mid itself).
Why Use right = mid?
When nums[mid] <= nums[right], it ensures that mid could be the minimum, so we include it in the search.

Termination:
The loop stops when left == right, and at that point, nums[left] is the minimum element.
