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

Usually return value of the result of recursion or iteration may forgettable but using memorization effectively enhance the programme performance.

The example is given and have a look at memorization, dynamic programming method and  before finish it, briefly look at vaious approaches to solve the problem.

	Assume, there is a 2D graph start from (0,0) and it wants to reach to (5,4). 
	How many ways to reach to the desination?

From the above question, what could be the best approach to solve the question? <br>
Mathmatical approach? Graph algorithm such as DFS, BFS?

In this post, solution would be given step by step using Memorized recursion and dynamic approach. After then, I will briefly talk about methods with graph and mathmatics.

### Memorized Recursion

<br>To express the problem on tree, we can illustrate it as below.<br><br>
![tree](/images/algorithm/dynprog/tree.png)

<br>However, there are redundancies as shown in below figure.<br><br>
![tree](/images/algorithm/dynprog/tree_redundant.png)

<br>We can optimize the redundancies and can express it as below.<br><br>
![tree](/images/algorithm/dynprog/tree_improved.png)

<br>Now, in this tree, we can store the value of visited nodes.<br>
	For example, after a visit to (1,1), **35** is stored in node (1,1).<br><br>
![tree](/images/algorithm/dynprog/tree_improved_path.png)

<br>After the first visit, retrieve 35 by accessing (1,1).<br><br>
![tree](/images/dynprog/algorithm/tree_improved_path2.png)



### Dynamic Recursion




1. Searching Approach

    there would be simply ***Depth First Search(DFS)*** and ***Breadth First Search (BFS)***.
    However, this would be an ineffective solution because each node needs to be visited without pruning. If the size becomes greater, it would take very long time.

2. Mathmatical Approach

	In other way to saying the question is "How many paths are there to move 5 steps to the right, 4 steps to the up?" or "9 steps can be moved to the right and how many patterns are there to move 4 steps to the up"

	In this case, we can use ***combination*** in mathmatical approach.
	9C4 = 126.

3. 