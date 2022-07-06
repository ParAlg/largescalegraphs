---
layout: default
title: Laxman Dhulipala
---

# Workshop on Large-Scale Graph Processing (SPAA 2022)

Quickly processing very large graphs containing billions to trillions of vertices and edges is increasingly important in practice today. The goal of this workshop is to bring together researchers studying theoretical and practical aspects of large-scale parallel graph processing to share their results on new problems, models, and algorithms, and to share progress in translating theoretical results to practical large-scale graph processing solutions.

Some topics that will be covered include industrial applications of parallel graph processing, frameworks for graph processing, representations of dynamic graphs, parallel graph-clustering, theoretically-efficient graph algorithms, and parallel graph partitioning.

The workshop will take place on Monday, July 11th from 2--6pm. Please
see the [SPAA site][spaa] for more details.

<b>Virtual Participation:</b> We will stream and record the workshop on zoom. Please find the meeting info [here](zoom).

### Agenda:

* Overview progress across the topics and areas mentioned above
* Present successes and limitations of existing approaches
* Discuss future research directions


### Schedule and Speaker List

* <b>2:00 --2:05</b> --- Introduction
* <b>2:05 --2:35</b> --- Parallel Algorithm Design for Classic Graph Problems, <em>[Yan Gu][yan]</em>
* <b>2:40 -- 3:10</b> --- Scaling up Hierarchical Agglomerative Clustering to Trillion-Edge Graphs, <em>[Jakub Łącki][kuba]</em>
* <b>3:15 -- 3:45</b> --- Recent Advances in Parallel Graph Partitioning, <em>[Lars Gottesbüren][lars]</em>
* <b>3:50 -- 4:00</b> --- Break
* <b>4:00 -- 4:35</b> --- Title TBA, <em>[Brian Wheatman][brian]</em>
* <b>4:40 -- 5:10</b> --- GraphIt - A High-Performance DSL for Graph Analytics, <em>[Julian Shun][julian]</em>
* <b>5:15 -- 6:00</b> --- Panel Discussion.
If you have any questions/topics you would like to see discussed during the panel, please submit them [here][form]!

<b>Organized by:</b> [Laxman Dhulipala][laxman]

### Abstracts

<b>Title: Parallel Algorithm Design for Classic Graph Problems</b> <em>([Yan Gu][yan])</em>

<b> Abstract:</b>
This talk will cover a few new parallel algorithms on classic graph problems such as single-source shortest-paths (the rho-stepping and the delta\*-stepping algorithms), biconnectivity (the vertex-labeling algorithm), and strongly connected components (the BGSS algorithm).  These algorithms are simple and have good theoretical guarantees on work, span, and space.  In addition, this talk will discuss a new data structure, the parallel hash bag, that can maintain the vertex subset in many graph algorithms efficiently, and the local-search technique that can accelerate many traversal-based graph algorithms.


<b>Title: Scaling up Hierarchical Agglomerative Clustering to Trillion-Edge Graphs</b>  <em>([Jakub Łącki][kuba])</em>

<b> Abstract:</b>
Hierarchical agglomerative clustering (HAC) is a simple and widely popular clustering method known for its high empirical quality. However, the applications of HAC on large datasets have been limited by the high computational cost of the existing implementations. Addressing this limitation has been an elusive task, as the algorithm has been believed to be inherently sequential and computationally expensive.

In this talk we study the HAC problem on edge-weighted graphs assuming the widely-used average linkage similarity function. We first give conditional hardness results showing that HAC requires time that is super-linear in the input size, and cannot be parallelized efficiently, formalizing the commonly held intuitions about the algorithm. We then show how both of these limitations can be bypassed by allowing approximation. Namely, we show that 1+ε approximate HAC can be implemented in near-linear work and polylogarithmic depth.

Finally, we show that our ideas lead to highly scalable HAC implementations. In a shared memory parallel setting (i.e., on a single machine) we obtain an over 50x speedup over the best existing baseline. Moreover, in the distributed setting, we demonstrate that our implementation scales to graphs containing trillions of edges.


<b>Title: Recent Advances in Parallel Graph Partitioning</b> <em>([Lars Gottesbüren][lars])</em>

<b>Abstract:</b>
Dividing data or workload among capacity-bounded processors in a way that minimizes inter-processor communication is a fundamental application of balanced graph partitioning. This talk gives an overview of our recent work on parallelizing techniques for a variety of time-quality trade-offs. I will also discuss adaptations to hypergraphs, buffered streaming, partitioning into a large number of blocks, as well as intricacies of efficient parallel implementations.


<b>Title: GraphIt - A High-Performance DSL for Graph Analytics</b> <em>([Julian Shun][julian])</em>

<b>Abstract:</b> 
This talk will present GraphIt, a domain-specific language for parallel graph computations that generates fast implementations for algorithms with different performance characteristics running on graphs with different sizes and structures. GraphIt separates what is computed (algorithm) from how it is computed (schedule). Programmers specify the algorithm using an algorithm language, and performance optimizations are specified using a separate scheduling language. The algorithm language simplifies expressing the algorithms, while exposing opportunities for optimizations. The scheduling language enables programmers to easily search through the complex optimization tradeoff space for graph processing. GraphIt supports efficient implementations of both unordered and ordered graph algorithms using combinations of existing as well as new optimizations that we design. Furthermore, we were able to make GraphIt portable across multicore CPUs, GPUs, Swarm, and the Hammerblade manycore architecture with reasonable effort by decoupling the architecture-independent algorithm from the architecture-specific schedules and backends.


### Code of Conduct

The workshop follows the [ACM Policy on Harassment and Discrimination][acmharass].


[acmharass]: https://www.acm.org/special-interest-groups/volunteer-resources/officers-manual/policy-against-discrimination-and-harassment
[spaa]: https://spaa.acm.org/
[laxman]: https://ldhulipala.github.io/
[yan]: https://www.cs.ucr.edu/~ygu/
[kuba]: https://research.google/people/105517/
[lars]: https://scholar.google.de/citations?user=G5XO7J4AAAAJ&hl=en
[brian]: https://brianwheatman.com/
[julian]: https://people.csail.mit.edu/jshun/
[form]: https://forms.gle/myvcibc9Bs7wrJPd7
[zoom]: https://docs.google.com/document/d/1om-PvjaC49-zOxKRjcUxOGXcDayXjpq6VtrXr8CEoEg/edit
