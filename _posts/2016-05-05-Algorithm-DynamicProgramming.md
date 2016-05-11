---
layout: single
title: "Algorithm: Memorized recursion and dynamic programming"
header:
  image: main_algorithm1.jpg
  teaser: main_algorithm1.jpg
  caption: "Photo credit: [**pixabay**](https://pixabay.com)"
tag: 
  - dynamic programming
categories:
  - Algorithm
author_profile: true
---

Recursive method oftenly used to enhance readability and performance but sometimes it disgrades the effectiveness due to inappropriate approach. To use it rightfully, sometimes, memorized recursion may take the place.

In this post, the question is provided below to carefully analyze which algorithm would be a reasonable approach to solve the problem.

	Assume, there is a 2D graph start from (0,0) and it wants to reach to (5,4). 
	How many ways to reach to the desination?

what could be the best approach above? <br>
Mathmatical or graph such as DFS, BFS or recursion?

To see it in brief, first, memorized recursion and dynamic prgoramming method would be illustrated and then, mathmatical and graph would come at second.

### Memorized Recursion

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
![tree](/images/dynprog/algorithm/tree_improved_path2.png)

<To be Updated more soon..>

### Dynamic Recursion
<To be updated soon ... >



1. Searching Approach

    To solve the problem, ***Depth First Search(DFS)*** and ***Breadth First Search (BFS)*** could be used.
    However, it seems this would be an ineffective solution because each node needs to be visited without pruning. If the size becomes greater, it would take very long time.

2. Mathmatical Approach

	For the question, it could be asked in different following way: "How many paths are there to move 5 steps to the right and 4 steps to the up?" or "9 steps can be moved to the right and how many patterns are there to move 4 steps to the up"

	In this case, we can use mathmatical ***combination*** approach. In this case, the answer becomes 9C4 = 126.

3. 