
## Tips:
- Union Find 
	- Path Compression 
		- ![[Pasted image 20230904213747.png]]
	- Rank
		- ![[Pasted image 20230904213825.png]]

## [Number of Islands](https://leetcode.com/problems/number-of-islands/description/)
- the main idea is when arriving at an island, we use either BFS or DFS to traverse all of the neighbor islands by using four directions. Marking all of them as visited 
- iterate through all of the elements in the list, trigger BFS/DFS when that particular island has not been visited 

## [Max Area of Island](https://leetcode.com/problems/max-area-of-island/)
- similar to counting the height of a tree using **DFS**, but instead the tree can only be connected in 4 directions 
- understand and internalize the recursive nature of **DFS**

## [Redundant Connection](https://leetcode.com/problems/redundant-connection/description/)
- **Union Find**
- when the parents of the new edge are the same, it is the redundant edge. 
- need the recursive find to make sure we have path compression 

## [Clone Graph](https://leetcode.com/problems/clone-graph/description/)
- use a hashmap to map the old node to the new copy node 
- **traversing neighbors for DFS**
- since all the nodes are connected, use `dfs` to traverse all of the node's neighbors and return until the node is in the hashmap
	- connect the neighbors with the new node 

## [Pacific Atlantic Water Flow](https://leetcode.com/problems/pacific-atlantic-water-flow/description/)(n * m)
- instead of doing **DFS** on every single node, start from the ocean sides and do **DFS** starting from the ocean nodes to see which nodes can be hit 
- then, traverse all the nodes again and append the ones that are included in two ocean sets 