
## Tips 
- minheap time complexity 
	- heapify (n)
	- push (log n)
	- pop (log n)
- [Sorting Algorithms](https://www.geeksforgeeks.org/sorting-algorithms/)

## [Kth Largest Element in a Stream](https://leetcode.com/problems/kth-largest-element-in-a-stream/)
- use minheap size of `k` to make sure the minimum is already kth largest element 
- understand the time complexity of minheap 

## [Kth Largest Element in an Array](https://leetcode.com/problems/kth-largest-element-in-an-array/description/)
- understand [QuickSort](https://www.geeksforgeeks.org/quick-sort/)
	- two pointers: `pivot` and `left` 
		- `pivot` is always the rightmost element 
		- `left` is used to keep track of 
	- randomly pick a pivot and compare all the numbers in the array against the pivot 
	- the smaller one goes to the right, and increment the `left` pointer by 1 
	- finally, swap the pivot with the element `left` is pointing at 
	- **this algo guarantees that all the numbers on the left of pivot is smaller and right of pivot is bigger**
- since we want the kth largest element, we stop until the `left` pointer is at the desire position 
- understand how to handle the index of the next recursion for different situations 

