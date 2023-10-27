
## Tips:
- Union Find 
	- Path Compression 
		- ![[Pasted image 20230904213747.png]]
	- Rank
		- ![[Pasted image 20230904213825.png]]

## [Number of Islands](https://leetcode.com/problems/number-of-islands/description/)
- the main idea is when arriving at an island, we use either **BFS** or **DFS** to traverse all of the neighbor islands by using four directions. Marking all of them as visited 
- iterate through all of the elements in the list, trigger **BFS/DFS** when that particular island has not been visited 

## [Max Area of Island](https://leetcode.com/problems/max-area-of-island/)(n * m)
- similar to counting the height of a tree using **DFS**, but instead the tree can only be connected in 4 directions 
- understand and internalize the recursive nature of **DFS**
- **base case** returns 0 because the number of iterations is the the max area 

## [Shortest Bridge](https://leetcode.com/problems/shortest-bridge/)
- 

## [Bus Routes](https://leetcode.com/problems/bus-routes/description/)(m * n)
- 

---
## [Clone Graph](https://leetcode.com/problems/clone-graph/description/) (n + m)
- use a hashmap to map the old node to the new copy node 
- **traversing neighbors for DFS**
- since all the nodes are connected, use `dfs` to traverse all of the node's neighbors and return until the node is in the hashmap
	- connect the neighbors with the new node her 
- when we visit a node, we add that node into our map, so in the end, when we add all the nodes, we connect them together 

---
## [Pacific Atlantic Water Flow](https://leetcode.com/problems/pacific-atlantic-water-flow/description/)(n * m)
- **DFS**: instead of doing **DFS** on every single node, start from the ocean sides and do **DFS** starting from the ocean nodes to see which nodes can be hit 
	- then, traverse all the nodes again and append the ones that are included in two ocean sets 
	- need to check whether the current height is greater than the previous height 

## [Surrounded Regions](https://leetcode.com/problems/surrounded-regions/)(n)
- same idea as the previous question. We start from the border to significantly increase runtime 

## [Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)(n * m)
- **BFS**: traverse the rotten oranges and use level algorithm to increase the time 
- two conditions for ending the algorithm:
	- queue is empty 
	- no more fresh oranges 
- because of the second condition, we also need to count the total of fresh oranges ahead of time 

---
## [Walls and Gates](https://leetcode.com/problems/walls-and-gates/) (m * n)
- start from the gates and do **BFS** to get to all the rooms. Their levels are their distance 
- However, need to start **BFS** at once with all the gate since that guarantees the shortest distance for all the rooms 

## [01 Matrix](https://leetcode.com/problems/01-matrix/description/)(m * n)
- **BFS**: need to start from all the 0 to guarantee shortest path for all 1s and minimize runtime since we don't need to double run on each 0 
	- need `seen` to keep track of which node has been visited since no other conditions satisfy 
	- need to copy the original matrix to be able to change the value based on the distance 

--- 
## [Word Search](https://leetcode.com/problems/word-search/) (n * m * 4^n (four recursion calls))
- **DFS**: using backtracking on **DFS** to make sure we don't lose any potential variables. 
	- We need to use backtracking because each iteration needs to have its own unique `visited`. We cannot have one global `visited` since we would lose potential solutions 

--- 
## [Shortest Path with Obstacles Elimination](https://leetcode.com/problems/shortest-path-in-a-grid-with-obstacles-elimination/editorial/)(m * n * k)
- **BFS**: when finding shortest path, we should use **BFS**. 
	- since we can eliminate obstacles, we need to track another variable, which is the number of obstacles you have broken already
	- we need to record all the possible states that have positive obstacles number left to make sure we don't lose any potential solutions 

---
## [Redundant Connection](https://leetcode.com/problems/redundant-connection/description/)
- **Union Find**
- when the parents of the new edge are the same, it is the redundant edge. 
- need the recursive find to make sure we have path compression 

---
## [Course Schedule](https://leetcode.com/problems/course-schedule/)
- **Topological Sort**
- **DFS**

## [Course Schedule II](https://leetcode.com/problems/course-schedule-ii/)
- **DFS** is a little different 