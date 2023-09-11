
## [Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)
- use built-in functions like `max()` and `min()` to be more concise 
- when dealing with comparison, don't compare forward. Compare backward 

## [Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- need to do better at writing concise code and logic 
- the idea is to use right pointer to iterate through all the elements in the list. 
- once there is a duplicate, remove the left index pointer element, then increment left pointer to account for duplicate in the middle of the string 
- once there is no duplicate, use `right - left + 1` to calculate the current length and max length so we don't have to create a new variable  

## [Longest Repeating Character Replacement](https://leetcode.com/problems/longest-repeating-character-replacement/)
- same logic as the previous one, except need to change the order of the logic a little 
- insert first then validating the string 
