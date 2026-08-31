
# Lab 1

## Overview

In this lab you will design an efficient algorithm to search for some `target` item in a custom data structure `SortedList`. Here are the properties of this custom data structure. 

1. It is a finite list in which all the items are sorted in ascending order. This list allows for duplicates of items. 
2. You do not know the number of items in the list, and there is no `O(1)` operation which gives you this number.  
3. The data structure does have a `O(1)` operation: `get(index)`. This returns the item at index if it exists. In other words, it returns: 
* The item at position `index`  if `index` is less than the number of items in the list
* `null` otherwise 


Your goal is to design a search algorithm that minimizes the number of `get` operations. 

### Input

* A `SortedList` `s` with possibly duplicate items
* A `target` item to located

### Output

* If the `target` is present in `s`, an index in `s` that contains `target`. If `target` occurs multiple times, it is okay to return *any* index with `target` in it. 
* If the `target` is absent in `s`, -1. 

## Step 0: Creating a shared collaborative document


* **One** person in your team should create a copy of [the google doc template for this lab](https://docs.google.com/document/d/1gEwIrruZe2dXQj3HV3OUcnlEQveeqe5x7zSwe3VZd20/edit?usp=sharing), and share it with your group. 

* Familiarize yourself with how to: 
	* Create code blocks
	* Create sub-headings



## Step 1: Comparing two naive algorithms

There are two naive approaches you can take to implement search in a `SortedList`. 

**Naive approach 1**

```

def naive_search1(s, target):
	index = 0
	item = s.get(index)
	
	while item != null:
		if item == target:
			return index
		index +=1
		item = s.get(index)

	return -1
```  
**Naive approach 2**

```

def helper(s):
	index = 0
	while s.get(index) != null:
		index +=1

	return index

def naive_search2(s, target):
	n = helper(s)

	start = 0
	end = n-1

	while start <= end:
		mid = (start + end)//2 ##integer division
		if s.get(mid) == target:
			return mid
		elif s.get(mid) > target:
			end = mid-1
		else:
			start = mid+1

	return -1

```

In your write up include **for each algorithm**: 

1. A brief description of what the algorithm is doing, along with a justification of correctness. 

2. Describe the best-case and worst-case scenarios for the algorithm, along with indicating time and space complexity for these scenarios.  In your analysis, assume that `s` has `n` items. 

3. A description of how you would modify and use the algorithm if you had to search for not just one `target` but `k` `target`s, along with the time and space complexity for this use case. 


Finally, also include an answer to the following question: what are the circumstances in which you would use `naive_search1` over `naive_search2` and vice versa. 

## Step 2: Designing a more efficient algorithm

Design, describe and analyze an algorithm that is more efficient than the two naive approaches described above. In your write-up include:

* A clear, unambiguous, human-readable prose description of the algorithm. To make the description unambiguous, you might want to include a few lines of pseudo-code. But the pseudo-code shouod be an addition to, and not a replacement of, prose description.

* An explanation or justification of correctness.

* An analysis of the time and space complexity of the algorithm when you are searching for one `target` and when you are searching for k `target`s. Make sure to include descriptions of what the best and worst case would look like.


## Step 3: Submit the write-up

* **One** person in your team should export the google doc as pdf and upload it to gradescope under Lab 1

* **Make sure to add all the group members to the submission**

