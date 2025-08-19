# 🧮 Generate Parentheses

> [LeetCode Problem Link](https://leetcode.com/problems/generate-parentheses/submissions/1740230978/)  
> Difficulty: Medium  
> Tags: Backtracking, Recursion, String Generation

---

## 🧠 Problem Statement

Given `n` pairs of parentheses, write a function to generate all combinations of well-formed parentheses.

### Example:
```text
Input: n = 3
Output: ["((()))", "(()())", "(())()", "()(())", "()()()"]
```

## 🚀 Approach
We use backtracking to explore all valid combinations of parentheses. At each step:

Add '(' if the count of open brackets is less than n.

Add ')' if the count of close brackets is less than open brackets.

This ensures only valid sequences are built.


## 📊 Complexity Analysis
| Metric            | Value       | Explanation                                                                 |
|-------------------|-------------|------------------------------------------------------------------------------|
| Time Complexity   | O(2ⁿ)       | Each recursive call explores two choices: add '(' or ')', pruned by rules. |
| Space Complexity  | O(2ⁿ)       | Result list stores all valid combinations.                                  |
| Auxiliary Space   | O(n)        | Recursion depth goes up to 2n, but only n open/close pairs are tracked.     |


## 🧵 Additional Notes
- ✅ This problem is a textbook example of **backtracking with constraints**.
- 🧠 The key pruning condition is: only add `')'` if `close_count < open_count`.
- 🔍 Helps build intuition for **DFS-style recursion** and **state tracking**.
- 🧰 Useful for interview prep, especially in problems involving **combinatorics**.
- 📚 Can be extended to generate other balanced structures (e.g., brackets, tags).
