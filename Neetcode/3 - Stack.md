
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

## [Generate Parentheses](https://leetcode.com/problems/generate-parentheses/)
- draw out the tree, find the pattern, then do recursion based on the finding 
- need to pop the elements after the recursion to clean up the variable and go up the tree 