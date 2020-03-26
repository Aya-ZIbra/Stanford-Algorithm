### Programming Assignment 1 \- Question 1

1/1 point (graded)

In this programming problem and the next you'll code up the greedy algorithms from lecture for minimizing the weighted sum of completion times.

Download the text file below (right click on the file and select "Save As..."):
[jobs.txt](https://lagunita.stanford.edu/assets/courseware/v1/85f7268f796f7014abab35a19999783c/asset-v1:Engineering+Algorithms2+SelfPaced+type@asset+block/jobs.txt)

This file describes a set of jobs with positive and integral weights and lengths. It has the format

\[number\_of\_jobs\]

\[job\_1\_weight\] \[job\_1\_length\]

\[job\_2\_weight\] \[job\_2\_length\]

...

For example, the third line of the file is "74 59", indicating that the second job has weight 74 and length 59.

You should NOT assume that edge weights or lengths are distinct.

Your task in this problem is to run the greedy algorithm that schedules jobs in decreasing order of the difference (weight \- length).

Recall from lecture that this algorithm is not always optimal. IMPORTANT: if two jobs have equal difference (weight \- length), you should schedule the job with higher weight first. Beware: if you break ties in a different way, you are likely to get the wrong answer. You should report the sum of weighted completion times of the resulting schedule \-\-\- a positive integer \-\-\- in the box below.

ADVICE: If you get the wrong answer, try out some small test cases to debug your algorithm (and post your test cases to the discussion forum).

  correct

69119377652 ![Loading](https://lagunita.stanford.edu/static/images/spinner.bc34f953403f.gif)

Submit

You have used 1 of 10 attempts Some problems have options such as save, reset, hints, or show answer. These options follow the Submit button.

Save Save your answer Show Answer

Review

None

Review

Answers are displayed within the problem

Review

### Programming Assignment 1 \- Question 2

1/1 point (graded)

For this problem, use the same data set as in the previous problem.

Your task now is to run the greedy algorithm that schedules jobs (optimally) in decreasing order of the ratio (weight/length).

In this algorithm, it does not matter how you break ties. You should report the sum of weighted completion times of the resulting schedule \-\-\- a positive integer \-\-\- in the box below.

  correct

67311454237 ![Loading](https://lagunita.stanford.edu/static/images/spinner.bc34f953403f.gif)

Submit

You have used 1 of 10 attempts Some problems have options such as save, reset, hints, or show answer. These options follow the Submit button.

Save Save your answer Show Answer

Review

None

Review

Answers are displayed within the problem

Review

### Programming Assignment 1 \- Question 3

1/1 point (graded)

In this programming problem you'll code up Prim's minimum spanning tree algorithm.

Download the text file below (right click on the file and select "Save As..."):
[edges.txt](https://lagunita.stanford.edu/assets/courseware/v1/1f93e6cee93cbcf26ee59e2f801646cd/asset-v1:Engineering+Algorithms2+SelfPaced+type@asset+block/edges.txt)

This file describes an undirected graph with integer edge costs. It has the format

\[number\_of\_nodes\] \[number\_of\_edges\]

\[one\_node\_of\_edge\_1\] \[other\_node\_of\_edge\_1\] \[edge\_1\_cost\]

\[one\_node\_of\_edge\_2\] \[other\_node\_of\_edge\_2\] \[edge\_2\_cost\]

...

For example, the third line of the file is "2 3 \-8874", indicating that there is an edge connecting vertex #2 and vertex #3 that has cost \-8874.

You should NOT assume that edge costs are positive, nor should you assume that they are distinct.

Your task is to run Prim's minimum spanning tree algorithm on this graph.

You should report the overall cost of a minimum spanning tree \-\-\- an integer, which may or may not be negative \-\-\- in the box below.

IMPLEMENTATION NOTES: This graph is small enough that the straightforward O(mn) time implementation of Prim's algorithm should work fine. OPTIONAL: For those of you seeking an additional challenge, try implementing a heap\-based version. The simpler approach, which should already give you a healthy speed\-up, is to maintain relevant edges in a heap (with keys = edge costs). The superior approach stores the unprocessed vertices in the heap, as described in lecture. Note this requires a heap that supports deletions, and you'll probably need to maintain some kind of mapping between vertices and their positions in the heap.

  correct

−3612829

### Programming Assignment 2 \- Question 1

1/1 point (graded)

In this programming problem and the next you'll code up the clustering algorithm from lecture for computing a max\-spacing k\-clustering.

Download the text file below (right click on the file and select "Save As...":
[clustering1.txt](https://lagunita.stanford.edu/assets/courseware/v1/d24f26d8392f2215ee8d8e8945b1cbff/asset-v1:Engineering+Algorithms2+SelfPaced+type@asset+block/clustering1.txt)

This file describes a distance function (equivalently, a complete graph with edge costs). It has the following format:

\[number\_of\_nodes\]

\[edge 1 node 1\] \[edge 1 node 2\] \[edge 1 cost\]

\[edge 2 node 1\] \[edge 2 node 2\] \[edge 2 cost\]

...

There is one edge (i,j) for each choice of 1≤i<j≤n, where n is the number of nodes.

For example, the third line of the file is "1 3 5250", indicating that the distance between nodes 1 and 3 (equivalently, the cost of the edge (1,3)) is 5250. You can assume that distances are positive, but you should NOT assume that they are distinct.

Your task in this problem is to run the clustering algorithm from lecture on this data set, where the target number k of clusters is set to 4. What is the maximum spacing of a 4\-clustering?

ADVICE: If you're not getting the correct answer, try debugging your algorithm using some small test cases. And then post them to the discussion forum!

  correct

106 ![Loading](https://lagunita.stanford.edu/static/images/spinner.bc34f953403f.gif)

Submit

You have used 2 of 10 attempts Some problems have options such as save, reset, hints, or show answer. These options follow the Submit button.

Save Save your answer Show Answer

Review

None

Review

Answers are displayed within the problem

Review

### Programming Assignment 2 \- Question 2

1/1 point (graded)

In this question your task is again to run the clustering algorithm from lecture, but on a MUCH bigger graph. So big, in fact, that the distances (i.e., edge costs) are only defined implicitly, rather than being provided as an explicit list.

The data set is below (right click on the file and select "Save As...":
[clustering\_big.txt](https://lagunita.stanford.edu/assets/courseware/v1/d9dc8f4b1324fa1f18e51376d0f8d6f1/asset-v1:Engineering+Algorithms2+SelfPaced+type@asset+block/clustering_big.txt)

The format is:

\[# of nodes\] \[# of bits for each node's label\]

\[first bit of node 1\] ... \[last bit of node 1\]

\[first bit of node 2\] ... \[last bit of node 2\]

...

For example, the third line of the file "0 1 1 0 0 1 1 0 0 1 0 1 1 1 1 1 1 0 1 0 1 1 0 1" denotes the 24 bits associated with node #2.

The distance between two nodes u and v in this problem is defined as the Hamming distance\-\-\- the number of differing bits \-\-\- between the two nodes' labels. For example, the Hamming distance between the 24\-bit label of node #2 above and the label "0 1 0 0 0 1 0 0 0 1 0 1 1 1 1 1 1 0 1 0 0 1 0 1" is 3 (since they differ in the 3rd, 7th, and 21st bits).

The question is: what is the largest value of k such that there is a k\-clustering with spacing at least 3? That is, how many clusters are needed to ensure that no pair of nodes with all but 2 bits in common get split into different clusters?

NOTE: The graph implicitly defined by the data file is so big that you probably can't write it out explicitly, let alone sort the edges by cost. So you will have to be a little creative to complete this part of the question. For example, is there some way you can identify the smallest distances without explicitly looking at every pair of nodes?

  correct

6118

### Programming Assignment 3 \- Question 1

1/1 point (graded)

In this programming problem and the next you'll code up the knapsack algorithm from lecture.

Let's start with a warm\-up. Download the text file below (right click on the file and select "Save As..."):
[knapsack1.txt](https://lagunita.stanford.edu/assets/courseware/v1/d55a5fe1d0942cf624532f2a2fc133f9/asset-v1:Engineering+Algorithms2+SelfPaced+type@asset+block/knapsack1.txt)

This file describes a knapsack instance, and it has the following format:

\[knapsack\_size\]\[number\_of\_items\]

\[value\_1\] \[weight\_1\]

\[value\_2\] \[weight\_2\]

...

For example, the third line of the file is "50074 659", indicating that the second item has value 50074 and size 659, respectively.

You can assume that all numbers are positive. You should assume that item weights and the knapsack capacity are integers.

In the box below, type in the value of the optimal solution.

ADVICE: If you're not getting the correct answer, try debugging your algorithm using some small test cases. And then post them to the discussion forum!

  correct

2493893.0 ![Loading](https://lagunita.stanford.edu/static/images/spinner.bc34f953403f.gif)

Submit

You have used 1 of 10 attempts Some problems have options such as save, reset, hints, or show answer. These options follow the Submit button.

Save Save your answer Show Answer

Review

None

Review

Answers are displayed within the problem

Review

### Programming Assignment 3 \- Question 2

1/1 point (graded)

This problem also asks you to solve a knapsack instance, but a much bigger one.

Download the text file below (right click on the file and select "Save As..."):
[knapsack\_big.txt](https://lagunita.stanford.edu/assets/courseware/v1/64df53c958263a22ba04e37ce9204a74/asset-v1:Engineering+Algorithms2+SelfPaced+type@asset+block/knapsack_big.txt)

This file describes a knapsack instance, and it has the following format:

\[knapsack\_size\]\[number\_of\_items\]

\[value\_1\] \[weight\_1\]

\[value\_2\] \[weight\_2\]

...

For example, the third line of the file is "50074 834558", indicating that the second item has value 50074 and size 834558, respectively. As before, you should assume that item weights and the knapsack capacity are integers.

This instance is so big that the straightforward iterative implemetation uses an infeasible amount of time and space. So you will have to be creative to compute an optimal solution. One idea is to go back to a recursive implementation, solving subproblems \-\-\- and, of course, caching the results to avoid redundant work \-\-\- only on an "as needed" basis. Also, be sure to think about appropriate data structures for storing and looking up solutions to subproblems.

In the box below, type in the value of the optimal solution.

ADVICE: If you're not getting the correct answer, try debugging your algorithm using some small test cases. And then post them to the discussion forum!

  correct

4243395

### Programming Assignment 4 \- Question 1

1/1 point (graded)

In this assignment you will implement one or more algorithms for the all\-pairs shortest\-path problem. Here are data files describing three graphs:

[g1.txt](https://lagunita.stanford.edu/assets/courseware/v1/c614f1fbb78bca7c98067a9038976ffb/asset-v1:Engineering+Algorithms2+SelfPaced+type@asset+block/g1.txt)
[g2.txt](https://lagunita.stanford.edu/assets/courseware/v1/617a8dccb5474bdf76f973f553f83777/asset-v1:Engineering+Algorithms2+SelfPaced+type@asset+block/g2.txt)
[g3.txt](https://lagunita.stanford.edu/assets/courseware/v1/9f0236832060a0f2ccfcb43f07301b7d/asset-v1:Engineering+Algorithms2+SelfPaced+type@asset+block/g3.txt)

The first line indicates the number of vertices and edges, respectively. Each subsequent line describes an edge (the first two numbers are its tail and head, respectively) and its length (the third number). NOTE: some of the edge lengths are negative. NOTE: These graphs may or may not have negative\-cost cycles.

Your task is to compute the shortest shortest path. Precisely, you must first identify which, if any, of the three graphs have no negative cycles. For each such graph, you should compute all\-pairs shortest paths and remember the smallest one (i.e., compute minu,v∈Vd(u,v), where d(u,v) denotes the shortest\-path distance from u to v ).

If each of the three graphs has a negative\-cost cycle, then enter "NULL" in the box below. If exactly one graph has no negative\-cost cycles, then enter the length of its shortest shortest path in the box below. If two or more of the graphs have no negative\-cost cycles, then enter the smallest of the lengths of their shortest shortest paths in the box below.

OPTIONAL: You can use whatever algorithm you like to solve this question. If you have extra time, try comparing the performance of different all\-pairs shortest\-path algorithms!

OPTIONAL: Here is a bigger data set to play with.
[large.txt](https://s3-us-west-1.amazonaws.com/prod-edx/Algo2/Files/large.txt)

For fun, try computing the shortest shortest path of the graph in the file above.

  correct

−19

### Programming Assignment 5 \- Question 1

1/1 point (graded)

In this assignment you will implement one or more algorithms for the traveling salesman problem, such as the dynamic programming algorithm covered in the video lectures. Here is a data file describing a TSP instance.

[tsp.txt](https://lagunita.stanford.edu/assets/courseware/v1/0557f47943b80364030343bfd38d0c72/asset-v1:Engineering+Algorithms2+SelfPaced+type@asset+block/tsp.txt)

The first line indicates the number of cities. Each city is a point in the plane, and each subsequent line indicates the x\- and y\-coordinates of a single city.

The distance between two cities is defined as the Euclidean distance \-\-\- that is, two cities at locations (x,y) and (z,w) have distance (x−z)2+(y−w)2 between them.

In the box below, type in the minimum cost of a traveling salesman tour for this instance, rounded down to the nearest integer.

OPTIONAL: If you want bigger data sets to play with, check out the [TSP instances from around the world](http://www.tsp.gatech.edu/world/countries.html). The smallest data set (Western Sahara) has 29 cities, and most of the data sets are much bigger than that. What's the largest of these data sets that you're able to solve \-\-\- using dynamic programming or, if you like, a completely different method?

HINT: You might experiment with ways to reduce the data set size. For example, trying plotting the points. Can you infer any structure of the optimal solution? Can you use that structure to speed up your algorithm?

  correct

26442

### Programming Assignment 6 \- Question 1

1 point possible (graded)

In this assignment you will implement one or more algorithms for the 2SAT problem. Here are 6 different 2SAT instances:

[2sat1.txt](https://lagunita.stanford.edu/assets/courseware/v1/3b06ac260bfdf1f6b9b2c740f64aa767/asset-v1:Engineering+Algorithms2+SelfPaced+type@asset+block/2sat1.txt)
[2sat2.txt](https://lagunita.stanford.edu/assets/courseware/v1/00f3826732c3bf38ce375da9b8890b16/asset-v1:Engineering+Algorithms2+SelfPaced+type@asset+block/2sat2.txt)
[2sat3.txt](https://lagunita.stanford.edu/assets/courseware/v1/3a99efb07b6d4e79e80b1b7cc4409a47/asset-v1:Engineering+Algorithms2+SelfPaced+type@asset+block/2sat3.txt)
[2sat4.txt](https://lagunita.stanford.edu/assets/courseware/v1/c91f372b2e97093f55924c6915854451/asset-v1:Engineering+Algorithms2+SelfPaced+type@asset+block/2sat4.txt)
[2sat5.txt](https://s3-us-west-1.amazonaws.com/prod-edx/Algo2/Files/2sat5.txt)
[2sat6.txt](https://s3-us-west-1.amazonaws.com/prod-edx/Algo2/Files/2sat6.txt)

The file format is as follows. In each instance, the number of variables and the number of clauses is the same, and this number is specified on the first line of the file. Each subsequent line specifies a clause via its two literals, with a number denoting the variable and a "\-" sign denoting logical "not". For example, the second line of the first data file is "\-16808 75250", which indicates the clause ¬x16808∨x75250 .

Your task is to determine which of the 6 instances are satisfiable, and which are unsatisfiable. In the box below, enter a 6\-bit string, where the ith bit should be 1 if the ith instance is satisfiable, and 0 otherwise. For example, if you think that the first 3 instances are satisfiable and the last 3 are not, then you should enter the string 111000 in the box below.

DISCUSSION: This assignment is deliberately open\-ended, and you can implement whichever 2SAT algorithm you want. For example, 2SAT reduces to computing the strongly connected components of a suitable graph (with two vertices per variable and two directed edges per clause, you should think through the details). This might be an especially attractive option for those of you who coded up an SCC algorithm for my Algo 1 course. Alternatively, you can use Papadimitriou's randomized local search algorithm. (The algorithm from lecture is probably too slow as stated, so you might want to make one or more simple modifications to it \-\-\- even if this means breaking the analysis given in lecture \-\-\- to ensure that it runs in a reasonable amount of time.) A third approach is via backtracking. In lecture we mentioned this approach only in passing; see Chapter 9 of the Dasgupta\-Papadimitriou\-Vazirani book, for example, for more details.
