Substring with Concatenation of All Words (LeetCode #30)
This solution finds all starting indices in a given string s where the substring is formed by the concatenation of all words in the list words exactly once, in any order, without any extra characters in between.

Problem Statement
Given:

A string s.

An array of words words (all words have the same length).

Return:

All starting indices of substrings in s that are a concatenation of each word in words exactly once.

Approach
Use sliding window with two pointers (left, right) and a word frequency counter.

Iterate through s with offsets 0 to word_len - 1 to handle word alignment.

Maintain a current_count of words within the window.

Adjust the window when a word's frequency exceeds its expected count.

If the window length matches len(words) * word_len, record the starting index.

Complexity
Time: O(n * word_len) where n = len(s).

Space: O(m) where m = number of unique words.

Example
python
Copy
Edit
Input:
s = "barfoothefoobarman"
words = ["foo", "bar"]

Output:
[0, 9]
Key Features
✔ Optimized O(n) approach using sliding window
✔ Handles overlapping words
✔ Works for any number of words with equal length
