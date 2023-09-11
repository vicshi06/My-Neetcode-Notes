
## [Maximum Subarray](https://leetcode.com/problems/maximum-subarray/description/)
- cannot do purely greedy, since we might need to include the elements that are bad right now but the subarray might contain the largest sum 
- find the right condition to discard, find the right condition to be greedy
	- when can we be absolutely certain that we can discard all the prior elements? 
	- in other words, in what situation should we start from a new element? 
