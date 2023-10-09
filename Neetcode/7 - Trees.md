
## Tips 
- DFS (tracking height level)
	- ![[Pasted image 20230831220324.png]]
	- ![[Pasted image 20230831225655.png]]
- BFS (tracking total node count) + (height)
	- ![[Pasted image 20230831222707.png]]
	- ![[Pasted image 20230831223227.png]]

## [Invert Binary Tree](https://leetcode.com/problems/invert-binary-tree/)
- when doing recursion, first think about base case, then go from there 
- memorize and understand the structure of the graph recursions 

## [Maximum Depth of Binary Tree](https://leetcode.com/problems/maximum-depth-of-binary-tree/)
- all the basic height method for a tree (DFS + BFS)

## [Balanced Binary Tree](https://leetcode.com/problems/balanced-binary-tree/)
- use bottom top approach 
	- evaluating the sub tree and returning two information. Whether it is balanced and its height
	- so we don't have to double count each node 

## [Diameter of Binary Tree](https://leetcode.com/problems/diameter-of-binary-tree/)
- same as the previous question, returns multiple variables to keep track of max length 

## [Same Tree](https://leetcode.com/problems/same-tree/)
- algorithm to make sure two subtree matches 
	- ![[Pasted image 20230901202758.png]]

## [Subtree of Another Tree](https://leetcode.com/problems/subtree-of-another-tree/)
- need two recursions to properly check each node 

## [Lowest Common Ancestor of a Binary Search Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-search-tree/description/)
- understand the definition of [binary search tree]([Binary Search Tree - GeeksforGeeks](https://www.geeksforgeeks.org/binary-search-tree-data-structure/)) 

## [Binary Tree Level Order Traversal](https://leetcode.com/problems/binary-tree-level-order-traversal/description/)
- use **BFS** and the `len` of each queue to determine the size of each level 



[[8 - Tries]]
[[9 - Backtracking]]
[[10 - Heap&Priority Queue]]