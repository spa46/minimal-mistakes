---
layout: single
title: "Algorithm: Memorized recursion and dynamic programming"
header:
  image: main_algorithm1.jpg
  teaser: main_algorithm1.jpg
  caption: "Photo credit: [**pixabay**](https://pixabay.com)"
tag: 
  - Hash
  - Hashtable
  - Hashset
  - Hashmap
  - HashMultiset
  - HashMultimap
  - Map
  - Set	
categories:
  - Algorithm
author_profile: true
---

#Hash, map, set

Dealing with key value is widely used in data world but there are many terms such as hashmap and hashset based on its structure including those which do not have hash in front of the words. Then what are the difference?

## Hash(unordered) versus Non-hash
   
This is intended in when inserting or deleting the data. when data are inserted or deleted, non-has functions (such as map and set) sort data; therefore, it takes longer processing time than hash or unordered method.
Using Hash function, even though elements are not ordered, it uses its has feature to search data quickly.
	
## MAP versus SET

The biggest difference is that SET contains only the key in contrast to the MAP which contains key and value. 
For the key duplication, both of these do not allow duplicate keys. When it is attempted, data is dropped. To have multiple duplicated keys, multiset and multimap could be used. 


## Confusion
As a side who can programme both Java and C++/C#, due to the complexity of the language, terminology could bring confusion: hashtable, hashmap and hashset in Java is different to those in C++ (Concept is similar though).

By my investigation, **in Java**, it seems more focused on having synchronization, and thread-safe as well as of course data structure. The detail is shown below:
	
|                   |  Hashtable | Hashmap | Hashset |
|-------------------| ---------- | ------- |-------- |
|**Synchronized**   | O          | X       | X       |
|**Key duplication**| X          | X       | X       |
|**Allow Null**     | X          | O       | O       |

To allow duplicated keys, use class such as HashMultiMap / Hash MultiSet


In **C++ STL**, Mutex is needed to have a synchronization.