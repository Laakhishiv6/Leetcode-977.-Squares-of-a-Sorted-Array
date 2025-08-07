# Leetcode-977.-Squares-of-a-Sorted-Array
# Description
Given an integer array nums sorted in non-decreasing order, return an array of the squares of each number sorted in non-decreasing order.
# Solution
In the given problem we have been given an array of decreasing numbers.

We need to return an array which contains the squares of those numbers in increasing order.

For example:

 nums = [-7,-3,2,3,11]

 After squaring the array nums = [49,9,4,9,121]

 In increasing order  : [4,9,9,49,121]

 Hnce the output is [4,9,9,49,121]

 # Algorithm
 1. Create a res array to store the resulting array.
 2. Loop through the array nums and find the square of each number.
 3. Append the squares in res .
 4. Sort the array and return the result.
# Code
class Solution:

    def sortedSquares(self, nums: List[int]) -> List[int]:
        res=[]
        for i in range(len(nums)):
            square=nums[i]*nums[i]   
            res.append(square)
        res.sort()
        return res     
# Complexity
Time Complexity

Loop to square elements:

Runs once for each element → O(n)

Each squaring operation is constant time.

Sorting the array:

Python’s .sort() uses Timsort → O(n log n) in worst case.

Total Time Complexity: O(n log n)

Space Complexity

You create a new list res to store the squares → takes O(n) space.

No other significant extra space is used.

Total Space Complexity: O(n)

