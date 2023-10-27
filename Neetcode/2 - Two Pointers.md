
## [Valid Palindrome](https://leetcode.com/problems/valid-palindrome/)
- use `ord` to figure out whether a character is a alphanumeric or not 
- then use two pointers to iterate the string instead of constructing a new string 

## [Two Sum II](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/)
- use two pointers to iterate through the list 
- if the sum is bigger or smaller, move the pointers accordingly 

##  [3Sum](https://leetcode.com/problems/3sum/)
- we need to sort the list first to use Two Sum II logic 
- be careful of duplicate. need to move the left pointers accordingly if duplicate detected 

---
## [Next Permutation](https://leetcode.com/problems/next-permutation/description/)(n)
- understand the problem. Try to write out a few more examples to see the desire behavior of the algo
- understand how to order the permutations 
- we start from the end and find the immediate descending pair
- Then in the remaining part, we find the last ascending position and switch it to guarantee that this permutation is the next in order 

---

[[4 - Binary Search]]
[[5 - Sliding Window]]
[[6 - Linked List]]