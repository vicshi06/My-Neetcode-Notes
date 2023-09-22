
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

## [Clone Graph](https://leetcode.com/problems/clone-graph/description/) (n + m)
- use a hashmap to map the old node to the new copy node 
- **traversing neighbors for DFS**
- since all the nodes are connected, use `dfs` to traverse all of the node's neighbors and return until the node is in the hashmap
	- connect the neighbors with the new node her 
- when we visit a node, we add that node into our map, so in the end, when we add all the nodes, we connect them together 

## [Pacific Atlantic Water Flow](https://leetcode.com/problems/pacific-atlantic-water-flow/description/)(n * m)
- instead of doing **DFS** on every single node, start from the ocean sides and do **DFS** starting from the ocean nodes to see which nodes can be hit 
- then, traverse all the nodes again and append the ones that are included in two ocean sets 

## [Surrounded Regions](https://leetcode.com/problems/surrounded-regions/)(n)
- same idea as the previous question. We start from the border to significantly increase runtime 

## [Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)(n * m)
- **BFS** to traverse the rotten oranges and use level algorithm to increase the time 
- understand the requirements and the problem, the actual implementation isn't hard 

## [Course Schedule](https://leetcode.com/problems/course-schedule/)
- **Topological Sort**
- **DFS**

## [Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **DFS** is a little different 

## [Walls and Gates](https://leetcode.com/problems/walls-and-gates/)
- start from the gates and do **BFS** to get to all the rooms. Their levels are their distance 
- However, need to start **BFS** at once with all the gate since that guarantees the shortest distance for all the rooms 