### Programming Question 1

1/1 point (graded)

Download the text file [here](https://lagunita.stanford.edu/assets/courseware/v1/20264e13e73a87dda60e8701d9f2c521/asset-v1:Engineering+Algorithms1+SelfPaced+type@asset+block/IntegerArray.txt). (Right click and select "Save As...")

This file contains all of the 100,000 integers between 1 and 100,000 (inclusive) in some order, with no integer repeated.

Your task is to compute the number of inversions in the file given, where the ith row of the file indicates the ith entry of an array.

Because of the large size of this array, you should implement the fast divide\-and\-conquer algorithm covered in the video lectures.

The numeric answer for the given input file should be typed in the space below.

So if your answer is 1198233847, then just type 1198233847 in the space provided without any spaces or commas or any other punctuation marks. You can make up to 5 attempts.

(We do not require you to submit your code, so feel free to use any programming language you want \-\-\- just type the final numeric answer in the following space.)

\[TIP: before submitting, first test the correctness of your program on some small test files or your own devising. Then post your best test cases to the discussion forums to help your fellow students!\]

  correct

2407905288

-------------------------------
GENERAL DIRECTIONS:

Download the following text file (right click and select "Save As..."): [QuickSort.txt](https://lagunita.stanford.edu/assets/courseware/v1/e4180be5ec3e5b00f55703423698327f/asset-v1:Engineering+Algorithms1+SelfPaced+type@asset+block/QuickSort.txt)

The file contains all of the integers between 1 and 10,000 (inclusive, with no repeats) in unsorted order. The integer in the ith row of the file gives you the ith entry of an input array.

Your task is to compute the total number of comparisons used to sort the given input file by QuickSort. As you know, the number of comparisons depends on which elements are chosen as pivots, so we'll ask you to explore three different pivoting rules.

You should not count comparisons one\-by\-one. Rather, when there is a recursive call on a subarray of length m, you should simply add m−1 to your running total of comparisons. (This is because the pivot element is compared to each of the other m−1 elements in the subarray in this recursive call.)

WARNING: The Partition subroutine can be implemented in several different ways, and different implementations can give you differing numbers of comparisons. For this problem, you should implement the Partition subroutine exactly as it is described in the video lectures (otherwise you might get the wrong answer).

### Programming Assignment 2 \- Question 1

1/1 point (graded)

DIRECTIONS FOR THIS PROBLEM:

For the first part of the programming assignment, you should always use the first element of the array as the pivot element.

HOW TO GIVE US YOUR ANSWER:

Type the numeric answer in the space provided.

So if your answer is 1198233847, then just type 1198233847 in the space provided without any space, commas, or other punctuation marks. You have 5 attempts to get the correct answer.

(We do not require you to submit your code, so feel free to use the programming language of your choice, just type the numeric answer in the following space.)

  correct

162085

----------------
### Programming Assignment 3

1/1 point (graded)

Download the following text file (right click and select "Save As..."): [kargerMinCut.txt](https://lagunita.stanford.edu/assets/courseware/v1/d81819849ab16ea07f97e4814a7f76d0/asset-v1:Engineering+Algorithms1+SelfPaced+type@asset+block/kargerMinCut.txt)

The file contains the adjacency list representation of a simple undirected graph. There are 200 vertices labeled 1 to 200. The first column in the file represents the vertex label, and the particular row (other entries except the first column) tells all the vertices that the vertex is adjacent to. So for example, the 6th row looks like : "6 155 56 52 120 ......". This just means that the vertex with label 6 is adjacent to (i.e., shares an edge with) the vertices with labels 155,56,52,120,......,etc

Your task is to code up and run the randomized contraction algorithm for the min cut problem and use it on the above graph to compute the min cut. (HINT: Note that you'll have to figure out an implementation of edge contractions. Initially, you might want to do this naively, creating a new graph from the old every time there's an edge contraction. But you should also think about more efficient implementations.) (WARNING: As per the video lectures, please make sure to run the algorithm many times with different random seeds, and remember the smallest cut that you ever find.) Write your numeric answer in the space provided. So e.g., if your answer is 5, just type 5 in the space provided.

  correct

17

-------------------
### Programming Assignment 4

5/5 points (graded)

Download the following text file (right click and select "Save As..."): [SCC.txt](https://s3-us-west-1.amazonaws.com/prod-edx/Algo1/Files/SCC.txt)

The file contains the edges of a directed graph. Vertices are labeled as positive integers from 1 to 875714. Every row indicates an edge, the vertex label in first column is the tail and the vertex label in second column is the head (recall the graph is directed, and the edges are directed from the first column vertex to the second column vertex). So for example, the 11th row looks liks : "2 47646". This just means that the vertex with label 2 has an outgoing edge to the vertex with label 47646

Your task is to code up the algorithm from the video lectures for computing strongly connected components (SCCs), and to run this algorithm on the given graph.

Enter the sizes of the 5 largest SCCs in the given graph using the fields below, in decreasing order of sizes. So if your algorithm computes the sizes of the five largest SCCs to be 500, 400, 300, 200 and 100, enter 500 in the first field, 400 in the second, 300 in the third, and so on. If your algorithm finds less than 5 SCCs, then enter 0 for the remaining fields. Thus, if your algorithm computes only 3 SCCs whose sizes are 400, 300, and 100, then you enter 400, 300, and 100 in the first, second, and third fields, respectively, and 0 in the remaining 2 fields.

WARNING: This is the most challenging programming assignment of the course. Because of the size of the graph you may have to manage memory carefully. The best way to do this depends on your programming language and environment, and we strongly suggest that you exchange tips for doing this on the discussion forums.

Largest SCC:

  correct

434821 968 459 313 211

----------------------------

### Programming Assignment 5

10/10 points (graded)

In this programming problem you'll code up Dijkstra's shortest\-path algorithm.

Download the following text file (Right click and select "Save As..."): [dijkstraData.txt](https://lagunita.stanford.edu/assets/courseware/v1/c8748131579ef6bd10b2d46f616988e9/asset-v1:Engineering+Algorithms1+SelfPaced+type@asset+block/dijkstraData.txt)

The file contains an adjacency list representation of an undirected weighted graph with 200 vertices labeled 1 to 200. Each row consists of the node tuples that are adjacent to that particular vertex along with the length of that edge. For example, the 6th row has 6 as the first entry indicating that this row corresponds to the vertex labeled 6. The next entry of this row "141,8200" indicates that there is an edge between vertex 6 and vertex 141 that has length 8200. The rest of the pairs of this row indicate the other vertices adjacent to vertex 6 and the lengths of the corresponding edges.

Your task is to run Dijkstra's shortest\-path algorithm on this graph, using 1 (the first vertex) as the source vertex, and to compute the shortest\-path distances between 1 and every other vertex of the graph. If there is no path between a vertex v and vertex 1, we'll define the shortest\-path distance between 1 and v to be 1000000.

You should report the shortest\-path distances to the following ten vertices, in order: 7,37,59,82,99,115,133,165,188,197. Enter the shortest\-path distances using the fields below for each of the vertices.

IMPLEMENTATION NOTES: This graph is small enough that the straightforward O(mn) time implementation of Dijkstra's algorithm should work fine. OPTIONAL: For those of you seeking an additional challenge, try implementing the heap\-based version. Note this requires a heap that supports deletions, and you'll probably need to maintain some kind of mapping between vertices and their positions in the heap.

Vertex 7:

  correct

2599 ![Loading](https://lagunita.stanford.edu/static/images/spinner.bc34f953403f.gif)

Vertex 37:

  correct

2610 ![Loading](https://lagunita.stanford.edu/static/images/spinner.bc34f953403f.gif)

Vertex 59:

  correct

2947 ![Loading](https://lagunita.stanford.edu/static/images/spinner.bc34f953403f.gif)

Vertex 82:

  correct

2052 ![Loading](https://lagunita.stanford.edu/static/images/spinner.bc34f953403f.gif)

Vertex 99:

  correct

2367 ![Loading](https://lagunita.stanford.edu/static/images/spinner.bc34f953403f.gif)

Vertex 115:

  correct

2399 ![Loading](https://lagunita.stanford.edu/static/images/spinner.bc34f953403f.gif)

Vertex 133:

  correct

2029 ![Loading](https://lagunita.stanford.edu/static/images/spinner.bc34f953403f.gif)

Vertex 165:

  correct

2442 ![Loading](https://lagunita.stanford.edu/static/images/spinner.bc34f953403f.gif)

Vertex 188:

  correct

2505 ![Loading](https://lagunita.stanford.edu/static/images/spinner.bc34f953403f.gif)

Vertex 197:

  correct

3068

-----------------------------

### Programming Assignment 6 \- Question 1

1/1 point (graded)

Download the following text file: [algo1\-programming\_prob\-2sum.txt](https://s3-us-west-1.amazonaws.com/prod-edx/Algo1/Files/algo1-programming_prob-2sum.txt)

The goal of this problem is to implement a variant of the 2\-SUM algorithm (covered in the Week 6 lecture on hash table applications).

The file contains 1 million integers, both positive and negative (there might be some repetitions!).This is your array of integers, with the ith row of the file specifying the ith entry of the array.

Your task is to compute the number of target values t in the interval \[\-10000,10000\] (inclusive) such that there are distinct numbers x,y in the input file that satisfy x+y\=t. (NOTE: ensuring distinctness requires a one\-line addition to the algorithm from lecture.)

Write your numeric answer (an integer between 0 and 20001) in the space provided.

OPTIONAL CHALLENGE: If this problem is too easy for you, try implementing your own hash table for it. For example, you could compare performance under the chaining and open addressing approaches to resolving collisions.

  correct

427

