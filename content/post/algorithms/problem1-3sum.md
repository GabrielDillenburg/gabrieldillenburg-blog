---
title: "Problem 1 - 3Sum Closest"
description: "Exploring an Efficient Solution Using Two Pointers and Sorting"
slug: Algorithms
date: 2024-02-06
categories:
    - Algorithms
tags:
    - Two Pointers
    - Sorting
    - Array
image: 
math: true
license: 
comments: true
draft: false
---

Finding three numbers in an array whose sum is closest to a given target is a common problem that tests a software engineer's ability to implement efficient algorithms. This blog post dives into a solution that leverages sorting and the two-pointer technique to achieve this with optimal efficiency.

## Problem Statement

Given an integer array `nums` of length `n` and an integer `target`, find three integers in `nums` such that the sum is closest to `target`. Return the sum of the three integers. You may assume that each input would have exactly one solution.

### Examples

- Input: `nums = [-1,2,1,-4]`, `target = 1`
  Output: `2`
  Explanation: The sum that is closest to the target is `2`. (`-1 + 2 + 1 = 2`).

- Input: `nums = [0,0,0]`, `target = 1`
  Output: `0`
  Explanation: The sum that is closest to the target is `0`. (`0 + 0 + 0 = 0`).

## Solution Strategy

The solution to this problem involves two key techniques: **sorting** and the **two-pointer technique**. Here's a step-by-step guide to the approach:

1. **Sort the Array**: First, we sort the array to allow efficient iteration and adjustment of two pointers based on their sum comparison with the target.

2. **Initialize Variables**: A variable to keep track of the closest sum found so far is initialized. This can start as the sum of the first three elements or any large number.

3. **Iterate with Two Pointers**: For each element (up to the third-to-last), we explore possible sums using two additional pointers—left and right—starting immediately to the right of the current element and at the array's end, respectively.

4. **Adjust and Compare**: We adjust the left and right pointers based on whether their sum is greater or lesser than the target, aiming to find the closest possible sum.

5. **Return the Closest Sum**: Once all combinations are considered, the closest sum found is returned as the solution.

## Code Implementation in Go

```go
package main

import (
	"fmt"
	"sort"
)

func threeSumClosest(nums []int, target int) int {
	// Step 1: Sort the array
	sort.Ints(nums)

	// Initialize the closest sum with a value that's definitely replaced by the first calculated sum
	closestSum := nums[0] + nums[1] + nums[2]
	n := len(nums)

	for i := 0; i < n-2; i++ {
		left, right := i+1, n-1

		// Step 3: Iterate with two pointers
		for left < right {
			currentSum := nums[i] + nums[left] + nums[right]

			// Step 4: Adjust and Compare
			if abs(target-currentSum) < abs(target-closestSum) {
				closestSum = currentSum
			}

			if currentSum < target {
				left++
			} else if currentSum > target {
				right--
			} else {
				// If the sum is exactly the target, we've found the closest possible sum
				return currentSum
			}
		}
	}

	// Step 5: Return the closest sum
	return closestSum
}

// Helper function to find the absolute value
func abs(x int) int {
	if x < 0 {
		return -x
	}
	return x
}

func main() {
	nums := []int{-1, 2, 1, -4}
	target := 1
	fmt.Println("Closest sum:", threeSumClosest(nums, target))

	nums2 := []int{0, 0, 0}
	target2 := 1
	fmt.Println("Closest sum:", threeSumClosest(nums2, target2))
}


```

## Explanation of Key Concepts

- **Sorting:** Ensures that we can efficiently navigate the array and adjust sums towards the target.
- **Two-Pointer Technique:** Allows for dynamic adjustment of the search range based on the comparison of sums, significantly reducing the search space.
- **Absolute Value Comparison:** Crucial for determining how close a sum is to the target, allowing for a straightforward comparison of distances regardless of direction.

This approach, combining sorting with the two-pointer technique, provides an elegant and efficient solution to the 3Sum Closest problem, showcasing the power of algorithmic optimization and problem-solving strategies in software development.