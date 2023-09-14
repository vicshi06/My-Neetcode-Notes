
## [Subsets](https://leetcode.com/problems/subsets/) (n * 2^n)
- **base case**: need to be careful not to finish too early. Think about when the recursion should stop base on each question 
- **recursion**: pop after append to make sure we can properly go up the recursion and to the next subtree 
- **behavior**: try to figure out if there is a way to reduce the number of loops
- use `i` to iterate through the whole array 
- each number has two choices, whether to include it or not, then branch out from there 

## [Subsets II](https://leetcode.com/problems/subsets-ii/description/) (n * 2^n)
- since we don't want to include duplicates, we need to make sure when we don't include a particular index, the next element shouldn't be the same as well 
- **sort** first, then use two pointer method to eliminate the duplicates  

##  [Combination Sum](https://leetcode.com/problems/combination-sum/) (2^n)
- we cannot blindly add all of the elements in the array to each leaf node. As this would lead to duplicate 
- instead, use index `i` to iterate through the whole array
- each number has again two choices, whether to include it or not, then branch out from there 
- this ensures no subtree shares the same answer
- **use tail recursion to pass in the total sum as a variable instead of computing it on the fly**

## [Combination Sum II](https://leetcode.com/problems/combination-sum-ii/description/)  (2^n)
- since we don't want to include duplicates, we need to make sure when we don't include a particular index, the next element shouldn't be the same as well 
- **sort** first, then use two pointer method to eliminate the duplicates  

## [Permutations](https://leetcode.com/problems/permutations/) (n * n!)
- same logic. Appending to the set and pop so we can go up the recursion 
- we want to iterate through all the numbers in the list but we should only continue if the number is not already in the list 
- since permutations means we want to include all the elements but in different orders, we have to iterate through all the elements in `nums` for every node to ensure complete inclusion 

## [Word Search](https://leetcode.com/problems/word-search/) (n * m * 4^n (four recursion calls))
- learn the cleaner version of **DFS** 

## [Palindrome Partitioning](https://leetcode.com/problems/palindrome-partitioning/description/)(n * 2^n)
- understand the fact that each level would have many nodes. The number based on the number of substring that is a palindrome  



[[11 - Graphs]]
[[12 - 1-D DP]]