# LeetCode 300 - Longest Increasing Subsequence

## Problem Statement

Given an integer array `nums`, return the length of the longest strictly increasing subsequence.

A subsequence can be created by removing some elements without changing the order of the remaining elements.

## Example

### Input

```text
nums = [10,9,2,5,3,7,101,18]
```

### Output

```text
4
```

### Explanation

One longest increasing subsequence is:

```text
2 → 3 → 7 → 101
```

Its length is `4`.

## Approach

Use Dynamic Programming.

For each index, store the length of the longest increasing subsequence ending at that index.

If `nums[j] < nums[i]`, then `nums[i]` can be added after the subsequence ending at `j`.

## Algorithm

1. Create a `dp` array filled with `1`.
2. For every element `i`, check all previous elements `j`.
3. If `nums[j] < nums[i]`, update `dp[i]`.
4. Return the maximum value in `dp`.

## Time Complexity

**O(n²)**

## Space Complexity

**O(n)**

## Author

T. Nandhini
