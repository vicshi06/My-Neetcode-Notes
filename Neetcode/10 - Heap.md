
## Tips 
- minheap time complexity 
	- heapify (n)
	- push (log n)
	- pop (log n)
- [Sorting Algorithms](https://www.geeksforgeeks.org/sorting-algorithms/)

## [Kth Largest Element in a Stream](https://leetcode.com/problems/kth-largest-element-in-a-stream/)(n * logn + m * logn)
- use minheap size of `k` to make sure the minimum is already kth largest element 
- understand the time complexity of minheap 

## [Last Stone Weight](https://leetcode.com/problems/last-stone-weight/)(n * logn)
- since python only has minheap, we first convert all the numbers to negative 
- then we check whether the secondly popped value is greater than the first
	- if the second value is bigger than the first, we can safely do the calculation 
	- if it is not bigger, that means they have the same weight, they are destroyed and not added back to the heap 

## [Task Scheduler](https://leetcode.com/problems/task-scheduler/description/)(n)
- `maxHeap` and `queue`
	- the `maxHeap` is used to finish the most frequent tasks first. so when we pop from it, it always gives us the most frequent task 
	- the `queue` is used to keep track of the next available task. We use `[-count, idelTime]` in `queue` and increment our `time`, so when `time` is equal to `idelTime`, that particular task is available to schedule
	- we use `queue` since we want FIFO so when we pop it is always the next available task
- if the count is 0, which means there is no more that task. if it not 0, we append that task to `queue` with their next available time 

## [Meeting Rooms II](https://leetcode.com/problems/meeting-rooms-ii/description/)(n * logn)
- first, we sort the rooms based on their start time 
- we then use minheap to keep track of all the end time and append the first room's end time to the minheap 
- for all the other tasks, we check if the end time for earliest room in minheap is smaller or equal to the end time for that task
	- if true, we pop the earliest room to "assign" that room 
- but we push the task's end time to the heap no matter what. 

## [Kth Largest Element in an Array](https://leetcode.com/problems/kth-largest-element-in-an-array/description/)(n * logk)
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

