---
title: "Memorized recursion and dynamic programming"
header:
  image: images/main_algorithm1.jpg
  teaser: images/main_algorithm1.jpg
  caption: "Photo credit: [**pixabay**](https://pixabay.com)"
tag:
  - dynamic programming
  - memorized recursion
  - Algorithm
categories:
  - Algorithm
---

Recursive method oftenly used to enhance readability and performance but sometimes it disgrades the effectiveness due to inappropriate approach. To use it rightfully, sometimes, memorized recursion may take the place.

In this post, the question is provided below to carefully analyze which algorithm would be a reasonable approach to solve the problem.

	Assume, there is a 2D graph start from (0,0) and it wants to reach to (5,4).
	How many ways to reach to the desination?

what could be the best approach above? <br>
Mathmatical or graph such as DFS, BFS or recursion?

To see it in brief, first, memorized recursion and dynamic prgoramming method would be illustrated and then, mathmatical and graph would come at second.

## Memorized Recursion

<br>Below is the conversion of the problem into tree.<br><br>
![tree](/images/algorithm/dynprog/tree.png)

<br>However, there are redundancies as shown in below figure.<br><br>
![tree](/images/algorithm/dynprog/tree_redundant.png)

<br>We could optimize the redundancies and can express it as below.<br><br>
![tree](/images/algorithm/dynprog/tree_improved.png)

<br>Nodes which is already explored could store its value in memory. <br>
	For example, after a visit to (1,1), **35** is stored in node (1,1).<br><br>
![tree](/images/algorithm/dynprog/tree_improved_path.png)

<br>After the first visit, the value 35 could be retrieved by accessing (1,1).<br><br>
![tree](/images/algorithm/dynprog/tree_improved_path2.png)

	/* Example of recursive memorization */

	const int x=5, y=4;
	int dp[x+1][y+1];

	int dfs(int posx, int posy) {
		if (posx > x || posy > y)
			return 0;
		if (posx == x && posy == y)
			return 1;
		if (dp[posx][posy] !=0 )
			return dp[posx][posy];

		return dp[posx][posy] = dfs(posx+1, posy) + dfs(posx, posy+1)
	}

## Dynamic Program

![dy](/images/algorithm/dynprog/dyn_prog.png)

	/* Example of dynamic programming */
	const int h = 5, w = 4;
	int dp[h+1][w+1];

	void dynamic() {
		int i,j;
		dp[0][0] = 1;

		for(i=0; i<=h; i++) {
			for(j=0; j <= w; j++) {
				if (i!=0) dp[i][j] += dp[i-1][j];
				if (j!=0) dp[i][j] += dp[i][j-1];
			}
		}
	}

## Graph

To solve the problem, we can think of using ***Depth First Search(DFS)*** and ***Breadth First Search (BFS)***.
However, it seems this would be an ineffective solution because each node needs to be visited without pruning. The greater the size becomes, the longer it takes.

## Mathmatical Approach

The question is in other words, we can say it differently in following way: "How many paths are there if you move 5 to the right and 4 to the up?" or "9 steps could be moved to the right and how many patterns are there if you move up 4 steps"

In this case, we can use ***combination*** method: 9C4 = 126.



Reference:
