# Day28 :You are given:  A string s (the text).  A string p (the pattern).  Your task is to return all starting indices of substrings in s that are anagrams of p.

**Test Cases**
1: Input: s = "cbaebabacd", p = "abc"
Output: [0, 6]

2. 2:
Input: s = "abab", p = "ab"
Output: [0, 1, 2]

**Intuition**
1.An anagram has the same frequency of characters.
2.So, instead of comparing substrings directly, we compare character counts.
3.Use a sliding window of size p.length() over s.
4.At each step, check if the character count of the window matches the character count of p


**Algorithm Flow**
1. For s = "cbaebabacd", p = "abc"
2. Build a frequency count for pattern p → {a:1, b:1, c:1}.
3. Start a sliding window of size 3 (len(p)) on s.
4. Move the window one step at a time, updating frequency counts.
5.If the frequency map matches p’s map → record the starting index.
6.Continue until the end of s..

**Complexity Analysis**
Time Complexity:O(n)
Space Complexity:O(1)
