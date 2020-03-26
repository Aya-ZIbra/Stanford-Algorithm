*   You are given as input an unsorted array of n distinct numbers, where n is a power of 2. Give an algorithm that identifies the second\-largest number in the array, and that uses at most n+log2⁡n−2 comparisons.
*   You are a given a unimodal array of n distinct elements, meaning that its entries are in increasing order up until its maximum element, after which its elements are in decreasing order. Give an algorithm to compute the maximum element that runs in O(log n) time.
*   You are given a sorted (from smallest to largest) array A of n distinct integers which can be positive, negative, or zero. You want to decide whether or not there is an index i such that A\[i\] = i. Design the fastest algorithm that you can for solving this problem.
-------------------
1\. Give the best upper bound that you can on the solution to the following recurrence: T(1)\=1 and T(n)≤T(\[n\])+1 for n\>1. (Here \[x\] denotes the "floor" function, which rounds down to the nearest integer.)

2\. You are given an n by n grid of distinct numbers. A number is a local minimum if it is smaller than all of its neighbors. (A neighbor of a number is one immediately above, below, to the left, or the right. Most numbers have four neighbors; numbers on the side have three; the four corners have two.) Use the divide\-and\-conquer algorithm design paradigm to compute a local minimum with only O(n) comparisons between pairs of numbers. (Note: since there are n2 numbers in the input, you cannot afford to look at all of them. Hint: Think about what types of recurrences would give you the desired upper bound.)

-----------------------------------
*   Prove that the worst\-case expected running time of every randomized comparison\-based sorting algorithm is Ω(nlog⁡n). (Here the worst\-case is over inputs, and the expectation is over the random coin flips made by the algorithm.)
*   Suppose we modify the deterministic linear\-time selection algorithm by grouping the elements into groups of 7, rather than groups of 5. (Use the "median\-of\-medians" as the pivot, as before.) Does the algorithm still run in O(n) time? What if we use groups of 3?
*   Given an array of n distinct (but unsorted) elements x1,x2,…,xn with positive weights w1,w2,…,wn such that ∑i\=1nwi\=W, a weighted median is an element xk for which the total weight of all elements with value less than xk (i.e., ∑xi<xkwi) is at most W/2, and also the total weight of elements with value larger than xk (i.e., ∑xi\>xkwi) is at most W/2. Observe that there are at most two weighted medians. Show how to compute all weighted medians in O(n) worst\-case time.
*   We showed in an optional video lecture that every undirected graph has only polynomially (in the number n of vertices) different minimum cuts. Is this also true for directed graphs? Prove it or give a counterexample.
*   For a parameter α≥1, an α\-minimum cut is one for which the number of crossing edges is at most α times that of a minimum cut. How many α\-minimum cuts can an undirected graph have, as a function of α and the number n of vertices? Prove the best upper bound that you can.
--------------------------

In the 2SAT problem, you are given a set of clauses, where each clause is the disjunction of two literals (a literal is a Boolean variable or the negation of a Boolean variable). You are looking for a way to assign a value "true" or "false" to each of the variables so that all clauses are satisfied \-\-\- that is, there is at least one true literal in each clause. For this problem, design an algorithm that determines whether or not a given 2SAT instance has a satisfying assignment. (Your algorithm does not need to exhibit a satisfying assignment, just decide whether or not one exists.) Your algorithm should run in O(m+n) time, where m and n are the number of clauses and variables, respectively. \[Hint: strongly connected components.\]

-----------------

*   In lecture we define the length of a path to be the sum of the lengths of its edges. Define the *bottleneck* of a path to be the maximum length of one of its edges. A *mininum\-bottleneck path* between two vertices s and t is a path with bottleneck no larger than that of any other s\- t path. Show how to modify Dijkstra's algorithm to compute a minimum\-bottleneck path between two given vertices. The running time should be O(mlog⁡n), as in lecture.
*   We can do better. Suppose now that the graph is undirected. Give a linear\-time (O(m)) algorithm to compute a minimum\-bottleneck path between two given vertices.
*   What if the graph is directed? Can you compute a minimum\-bottleneck path between two given vertices faster than O(mlog⁡n)?
--------------

1.  Recall that a set H of hash functions (mapping the elements of a universe U to the buckets {0,1,2,…,n−1}) is universal if for every distinct x,y∈U, the probability Prob\[h(x)\=h(y)\] that x and y collide, assuming that the hash function h is chosen uniformly at random from H, is at most 1/n. In this problem you will prove that a collision probability of 1/n is essentially the best possible. Precisely, suppose that H is a family of hash functions mapping U to {0,1,2,…,n−1}, as above. Show that there must be a pair x,y∈U of distinct elements such that, if h is chosen uniformly at random from H, then Prob\[h(x)\=h(y)\]≥1/n−1/|U|.

-----------------------------

The following problems are for those of you looking to challenge yourself beyond the required problem sets and programming questions. They are completely optional and will not be graded. While they vary in level, many are pretty challenging, and we strongly encourage you to discuss ideas and approaches with your fellow students on the "Theory Problems" discussion forum.

1.  Consider a connected undirected graph G with not necessarily distinct edge costs. Consider two different minimum\-cost spanning trees of G, T and T′. Is there necessarily a sequence of minimum\-cost spanning trees T\=T0,T1,T2,…,Tr\=T′ with the property that each consecutive pair Ti,Ti+1 of MSTs differ by only a single edge swap? Prove the statement or exhibit a counterexample.
2.  Consider the following algorithm. The input is a connected undirected graph with edge costs (distinct, if you prefer). The algorithm proceeds in iterations. If the current graph is a spanning tree, then the algorithm halts. Otherwise, it picks an arbitrary cycle of the current graph and deletes the most expensive edge on the cycle. Is this algorithm guaranteed to compute a minimum\-cost spanning tree? Prove it or exhibit a counterexample.
3.  Consider the following algorithm. The input is a connected undirected graph with edge costs (distinct, if you prefer). The algorithm proceeds in phases. Each phase adds some edges to a tree\-so\-far and reduces the number of vertices in the graph (when there is only 1 vertex left, the MST is just the empty set). In a phase, we identify the cheapest edge ev incident on each vertex v of the current graph. Let F\={ev} be the collection of all such edges in the current phase. Obtain a new (smaller) graph by contracting all of the edges in F \-\-\- so that each connected component of F becomes a single vertex in the new graph \-\-\- discarding any self\-loops that result.Let T denote the union of all edges that ever get contracted in a phase of this algorithm. Is T guaranteed to be a minimum\-cost spanning tree? Prove it or exhibit a counterexample.
4.  Recall the definition of a minimum bottleneck spanning tree from Problem Set #1. Give a linear\-time (i.e., O(m)) algorithm for computing a minimum bottleneck spanning tree of a connected undirected graph. \[Hint: make use of a non\-trivial linear\-time algorithm discussed in Part 1.\]

------------------------------------

The following problems are for those of you looking to challenge yourself beyond the required problem sets and programming questions. They are completely optional and will not be graded. While they vary in level, many are pretty challenging, and we strongly encourage you to discuss ideas and approaches with your fellow students on the "Theory Problems" discussion forum.

1.  Consider a connected undirected graph G with edge costs, which need not be distinct. Prove the following statement or provide a counterexample: for every MST T of G, there exists a way to sort G's edges in nondecreasing order of cost so that Kruskal's algorithm outputs the tree T.
2.  Consider a connected undirected graph G with distinct edge costs that are positive integers between 1 and n3, where n is the number of vertices of G. How fast can you compute the MST of G?
3.  Read about matroids. Prove that the greedy algorithm correctly computes a maximum\-weight basis. For the matroid of spanning trees of a graph, this algorithm becomes Kruskal's algorithm. Can you formulate an analog of Prim's MST algorithm for matroids?
4.  Prove that our analysis of union\-find with lazy unions and union by rank (but without path compression) is asymptotically optimal (i.e., there are sequences of operations where you do Θ(log⁡n) work on most of the operations).
5.  Prove that in our union\-find data structure with lazy unions, union by rank, and path compression, some operations might require Θ(log⁡n) time.

------------------------------

Give a dynamic programming algorithm that computes an optimal binary search tree and runs in O(n2) time.

--------------------
Recall the asynchronous version of the Bellman\-Ford algorithm discussed in the "Internet Routing" lectures. Prove that, in the worst case, this algorithm requires an exponential number of iterations to converge.Recall the asynchronous version of the Bellman\-Ford algorithm discussed in the "Internet Routing" lectures. Prove that, in the worst case, this algorithm requires an exponential number of iterations to converge.

------------------------------

Consider an undirected graph G\=(V,E) with nonnegative edge costs. You are given a set T⊆V of k vertices called terminals. A Steiner tree is a subset F⊆E of edges that contains a path between each pair of terminals. For example, if T\=V, then the Steiner trees are the same as the connected subgraphs. It is a fact that the decision version of the Steiner tree problem is NP\-complete. Give a dynamic programming algorithm for this problem (i.e., for computing a Steiner tree with the fewest number of edges) that has running time of the form O(ck⋅poly(n)), where c is a constant (like 4) and poly is some polynomial function.

Prove that in graphs with positive integer edge weights, the local search algorithm for the maximum cut problem is not guaranteed to converge in a polynomial number of iterations.
