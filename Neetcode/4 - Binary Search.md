
## Tips:
- binary search
	- ![[Pasted image 20230828221039.png]]

## [Binary Search](https://leetcode.com/problems/binary-search/)
- the idea is simple, but need to be careful of the updated left and middle index 
- only update the index appropriately  

## [Search a 2D Matrix](https://leetcode.com/problems/search-a-2d-matrix/)
- use the special property of the rows to further shorten the runtime  

## [Koko Eating Bananas](https://leetcode.com/problems/koko-eating-bananas/)
- establish lower and upper bound 
- then use binary search property to solve this. However, the logic is a little different
	- if the sum is smaller than `h`, it might be a potential solution since this `k` is able to eat all the bananas, but it might not be the minimum, so we need to keep going 
	- if the sum is bigger than `h`, we need a bigger `k` 

## [Find Minimum in Rotated Sorted Array](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/)
- carefully observe the special property of the array, and then think about how binary search idea can be used 
- ## When do I use while l <= r????

## [Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- 



[[7 - Trees]]