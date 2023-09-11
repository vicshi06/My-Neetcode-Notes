
## Tips
- fast and slow pointer (for median in a linked list)
	- ![[Pasted image 20230905224129.png]]
- fast and slow pointer (for Floyd's Cycle Finding Algorithm)
	- ![[Pasted image 20230904115047.png]]
- reverse list 
	- ![[Pasted image 20230906212657.png]]

## [Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/)
- two pointers: `cur` and `prev` 
- use `while head` not `while head != None` for cleaner code 

## [Reverse Linked List II](https://leetcode.com/problems/reverse-linked-list-ii/?envType=daily-question&envId=2023-09-07)
-  [(code)]([Reverse Linked List II - LeetCode](https://leetcode.com/problems/reverse-linked-list-ii/submissions/1042716068/?envType=daily-question&envId=2023-09-07)) cannot take out the chunk, reverse it, and stich together. 
- use the differences in the `left` and `right` pointers to reverse the chunk in place. 
	- using this way can take care of many edge cases 
- then reconnect it 

## [Linked List Cycle](https://leetcode.com/problems/linked-list-cycle/)
- use `set()` to keep track of the hash of the node, and if the node is already in the `set()`, there is a cycle 
- use fast and slow pointer to check if there is a cycle. If there is, the fast and slow pointers will meet 

## [Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/)
- initialize a dummy node first to take care of edge cases 
- if one list is empty, directly append the other one 

## [Reorder List](https://leetcode.com/problems/reorder-list/)
1. use fast and slow pointer to split the list into two 
2. reverse the second list so we can traverse it 
3. merge the two lists based on the condition 
- **need to learn how to utilize pointers better to do the linked list**

## [Remove Nth Node From End of List](https://leetcode.com/problems/remove-nth-node-from-end-of-list/)
- use two pointers. left and right. their distance should be `n` 
- when right pointer reaches the end, the left pointer is at the position we want 
- we also need to make a dummy node so that the left pointer stops at the node right before the node we want, so we can manipulate it
	- because we cannot traverse the list back 

## [Copy List with Random Pointer](https://leetcode.com/problems/copy-list-with-random-pointer/)
- first, create a hashmap that maps the old node to the new node 
- second, link the new node according to the information in the old nodes 

## [Split Linked List in Parts](https://leetcode.com/problems/split-linked-list-in-parts/description/?envType=daily-question&envId=2023-09-06)
- no pointer tricks, just need to figure out the total length of the list first 
- iterate through the whole list and figure out the length 
- use `length // k` to figure out the size for small chunk 
- use `legnth % k` to figure out the number of big chunk. `big_chunk = small_chunk_size + 1`
- read through the answer to understand how to split the list based on the number of nodes 



[[7 - Trees]]