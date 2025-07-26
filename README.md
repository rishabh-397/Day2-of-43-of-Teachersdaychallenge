# Day2-of-43-of-Teachersdaychallenge

 Group Anagrams
Problem Description: Given an array of strings strs, group the anagrams together. You can return the answer in any order. Anagrams are words or phrases formed by rearranging the letters of a different word or phrase, typically using all the original letters exactly once.

Approaches Discussed:

Sorting as Key (O(N⋅KlogK) Time Complexity): The most common and intuitive approach. For each string, sort its characters to create a unique "canonical" key (e.g., "eat" -> "aet", "tea" -> "aet"). Use a hash map where the sorted string is the key and the value is a list of strings that share that sorted form.

Character Counting as Key (O(N⋅K) Time Complexity): An alternative where a character frequency array (e.g., [1,0,0,1,1,0...] for 'a', 'b', 'c', 'd', 'e' respectively for "ade") is converted into a string or tuple to serve as the hash map key. This can be slightly more performant as sorting is K log K while counting is K.

Key Learning Points:

Identifying properties that remain constant for related items (e.g., sorted form of anagrams).

Effective use of hash maps for grouping based on a derived key.

Understanding the trade-offs between different key generation methods (sorting vs. counting).

Same Tree
Problem Description: Given the roots of two binary trees p and q, write a function to check if they are the same or not. Two binary trees are considered the same if they are structurally identical, and the nodes have the same value.

Approaches Discussed:

Recursive Depth-First Search (DFS): The most natural way to solve this. Recursively compare p and q:

Base Cases:

If both p and q are null, they are identical (return true).

If one is null and the other is not, they are not identical (return false).

If their values are different, they are not identical (return false).

Recursive Step: If the base cases pass, then recursively check if their left subtrees are the same AND their right subtrees are the same.

Key Learning Points:

Fundamentals of binary tree traversal (DFS).

Designing recursive functions with proper base cases and recursive steps.

Simultaneous traversal of two data structures.

File Location: solutions/same_tree.py (or solutions/sameTree.cpp, etc.)

Example (from LeetCode):
Input: p = [1,2,3], q = [1,2,3]
Output: true

Input: p = [1,2], q = [1,null,2]
Output: false
