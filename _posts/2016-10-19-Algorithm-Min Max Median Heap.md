---
title: "Algorithm: Min-Max Median Heap: Array vs Priority Queue"
header:
  image: main_algorithm1.jpg
  teaser: main_algorithm1.jpg
  caption: "Photo credit: [**pixabay**](https://pixabay.com)"
tag: 
  - MinMax Median Heap
  - median heap
  - gnuplot

categories:
  - Algorithm
author_profile: true
---

One of the way of getting track of median in real-time: using two heaps (Min & Max heaps)

![Min-Max Median Heap](/images/algorithm/minmax/minmax.jpg)

Design of Operation:

	1. compare value with median
	2. if the value is smaller than median, insert it to Max heap,
	     else Min heap
	3. balance two trees: the difference of size of the node should be under 1, 
		 otherwise, pop root from the bigger size heap and push it into smaller size heap.
	4. get Median value: 
		 if same size of two heaps => median = (minRoot + maxRoot) >> 1,
            more nodes in max heap => median = minRoot,
            else median maxRoot

![gnuplot](/images/algorithm/minmax/heap.png)
		 