---
title: LeetCode 1 - Two Sum
authors: 
  - leogsouza
date: 2021-03-19
featured: false
reading_time: true
draft: true
image:
  placement: 3
  caption: 'Image credit: [**Javier Esteban**](https://unsplash.com/photos/4rmvT-RhRUw)'
---

I am initiating a series of posts where I solve some LeetCode problems starting from the easy problems until to hard problems. 
Today I will start with the first problem Two Sum*

## Problem Description

Given an array of integers ```nums``` and an integer ```target```, return indices of the two numbers such that they add up to ```target```.

You may assume that each input would have **exactly one solution**, and you may not use the same element twice.

You can return the answer in any order.


**Example 1:**
```
Input: nums = [2, 7, 11, 15], target = 9

Output: [0,1]

Explanation: Because nums[0] + nums[1] == 9, we return [0, 1]
```


**Constraints**

* ```2 <=nums.length <= 10^3```
* ```-10^9 <= nums[i] <= 10^9```
* ```-10^9 <= target <= 10^9```
* **Only one valid answer exists.**

### Approach