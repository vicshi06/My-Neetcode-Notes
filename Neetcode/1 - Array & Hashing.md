
## Tips 
- use `dictionary` to deal with duplicates and for faster lookups 
- use `set` when you just need to know whether or not you've already got a particular value 

## [Contains Duplicate](https://leetcode.com/problems/contains-duplicate/)
- use `set` to determine duplicates 

## [Valid Anagram](https://leetcode.com/problems/valid-anagram/)
- construct two `dict` that keeps track of the frequency of each character in the strings 
- compare the final two `dict`. If they are the same, they are anagram

## [Two Sum](https://leetcode.com/problems/two-sum/)
- contract a `dict`. The value should be the `key`. The index should be the `value` 
- use the difference to find the value in the `dict`

## [Group Anagrams](https://leetcode.com/problems/group-anagrams/)
- For finding anagrams in a large string list, we can use the `ACII` values of each character in a string to figure out the occurrences
- **Cannot use sum of the characters score because their sum might be the same, but they are different strings**
- We can then use this score as the key and append each string into a hashmap 
- This makes sure that all the strings with the same key will belong to a same list 
- Then return the values of the hash map 

## [Top K Frequent Elements](https://leetcode.com/problems/top-k-frequent-elements/)
- Remove the top `k` of the most frequent numbers
- use `dict` to keep track of the count of each number 
- use another `array` to covert the `dict` into the `array` that the index means the number of occurrence for that number 
	- This automatically sort the occurrence because the most frequent would capture the last index in the array, and so on  
- iterate the `array` backwards, stop until the length of the final result is `k`

## [Valid Sudoku](https://leetcode.com/problems/valid-sudoku/)
- create three list of `set()` to keep track of the conditions 
- use the index of the individual elements to track it
- use `(r // 3) * 3 + c // 3` condition to place each element into respective box ![[Pasted image 20230824230720.png]]


## [Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)(n)
- **Prefix Sum**
	- declare 3 arrays `L`, `R`, `answer`
	- the `L` keeps track of all the multiplication result on the left of the element, while `R` keeps track of all the multiplication results on the right of the element 
	- we fill the `L` from left, keeping the first element 1. we fill the `R` from the right, keeping the last element 1 
	- for `answer`, we just multiply the left element with the right element for the same index 


--- 
[[2 - Two Pointers]]
[[3 - Stack]]