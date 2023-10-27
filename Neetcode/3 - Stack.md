
## [Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- use a stack to keep track of the result 
- if find a closing bracket, immediately check if the previous is a opening bracket for its kind. Pop if found
- after everything, if there is still some elements left, return false 

## [Min Stack](https://leetcode.com/problems/min-stack/)
- **have two stacks, one for the number, and one for tracking the minimum**
- need to think about what happens when the stack is empty, the min from last stack shouldn't persist 
- instead of creating a variable, do a min comparison on the spot 

## [Evaluate Reverse Polish Notation](https://leetcode.com/problems/evaluate-reverse-polish-notation/)
- try to find the pattern, and use stack to slowly pop the elements 

## [Basic Calculator II](https://leetcode.com/problems/basic-calculator-ii/description/)(n)
- we handle the previous operations when we are pointing at something that is not a number  
- we set the first operator to `+` because we want to append the first number to the stack 
- we also need to append an extra string to the end so we last operator can be evaluated 
- using this logic, we handle all the multiplication and division first, and then sum up all the numbers in the stack in the end since the order of addition and subtraction doesn't matter 

## [Basic Calculator III](https://leetcode.com/problems/basic-calculator-iii/description/)
- we still use previous question as the foundation 
- when we encountered a `(`, we use append the previous operator to the stack to remember it 
- when we encountered a `)`, we sum up all the integers up to the previous operator on the stack for outer operator to calculate 

## [Score of Parentheses](https://leetcode.com/problems/score-of-parentheses/description/)(n)
- the trick is to keep track of the depth. Understand the intricate part of the algo 
- when we see an opening bracket, we append 0 to increase our depth 
- when we see a closing bracket, we add twice the score of the previous deeper part - except when counting (), which has a score of 1

## [Decode String](https://leetcode.com/problems/decode-string/)
- recursion
	- need an index to keep track of where you are at when iterating 
	- we create a string each time we go down the recursion 
	- the base case is when the index is out of range and it is pointing at the `]`, we return the appended string upwards to the previous call 
	- also need to be careful of treating two digits numbers 
- stack 
	- we only want to handle multiplication logic when we have encountered `]`
	- we append all the strings before we encountered `[`, and handle the digits
	- then we append the completed string back to stack, for the topmost layer 