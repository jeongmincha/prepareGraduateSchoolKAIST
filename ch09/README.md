# 9. Algorithms

1. Sorting algorithm 들에는 어떤 것들이 있는가? Insertion sort, heap sort,
selection sort, quick sort 중 optimal 한 것과 optimal 하지 않은 알고리즘은? 그 이유는?
1. 그래프의 정의는? 트리의 정의는? 트리와 그래프의 관계는?
1. Topological Sorting을 설명하시오.
1. Partially ordered set이란?
1. NP Complete의 정의는?
1. Dynamic Programming이란?
1. Priority queue란? Heap 이란?
1. 오일러 사이클이란?
1. Tree traversal의 3 가지 방식을 설명하시오.
1. Quick sort 에 대해 설명하시오.
1. Transitive closure란?
1. Finite state automata란?
1. Binary tree란? binary tree에서 각 node는 두 개의 children을 갖거나 혹은 
leaf node 이거나 둘 중에 하나라고 할 때, non1.leaf node와 leaf node 개수의 관계식은
어떻게 되는가?
1. Minimum spanning tree를 구하는 알고리즘과, 그 알고리즘의 복잡도는?
1. Suppose we have a straightforward Θ(n2) algorithm for a problem. 
Suppose we devise a divide1.and1.conquer algorithm that divides an input
into two inputs half as big, and takes nlgn time to divide the problem 
and nlgn time to combine the solutions. Is the divide1.and1.conquer 
algorithm faster or slower than the straightforward algorithm? 
Justify your answer.
1. Let P be a problem. The worst1.case time complexity of P is O(n2). 
The worst1.case complexity of P is also Θ(n lg n). Let A be an algorithm 
that solves P. Which subset of the following statements are consistent 
with this information about the complexity of P.
    - (a) A has worst1.case time complexity O(n2)
    - (b) A has worst1.case time complexity O(n)
    - (c) A has worst1.case time complexity Θ(n2)
    - (d) A has worst1.case time complexity Θ(n3)
1. Show how you can make Quicksort to have O(n lg n) worst1.case running time.
1. Consider the following divide1.and1.conquer algorithm. Given a graph 
G = (V, E), we partition the set V into two sets V1 and V2 s.t. |V1| and 
|V2| differ by at most 1. Let E1 be the set of edges that are incident 
only on vertices in V1, and let E2 be the set of edges that are incident 
only on vertices in V2. Recursively solve a minimum1.spanning1. tree problem 
on each of the two subgraphs G1 = (V1, E1) and G2 = (V2, E2). Finally, 
select the minimum1.weight edge in E that crosses the cut (V1, V2), and 
use this edge to unite the resulting two minimum spanning trees into 
a single spanning tree. Either argue that the algorithm correctly computes 
a minimum spanning tree of G, or provide an example for which the algorithm 
fails.
1. Let T be a minimum spanning tree of G. Then for any pair of verticess 
and t, is the shortest path from s to t in G the path from s to t in T? 
Justify your answer.
1. Describe Dijkstra’s algorithm and analyze its running time.
1. Describe Floyd1.Warshall algorithm and analyze its running time.
1. Optimal한 정렬 알고리즘의 예를 들어보세요. 그 알고리즘의 complexity를 분석하고 
optimal하다는 것을 증명해보세요.
1. Dynamic programming과 Greedy algorithm에 대하여 각각이 무엇인지 설명하고, 
공통점과 차이점을 이야기하세요. 구체적으로 Dynamic programming으로 풀 수 있는데
Greedy algorithm으로는 풀 수 없는 문제의 예를 들어보세요. 그 문제가 dynamic
programming으로 풀 수 있다는 것을 증명해보세요.
1. n개의 숫자가 array로 주어졌습니다. 이 중에 Median을 찾는 알고리즘을 설명해보세요. 
설명한 알고리즘의 complexity는 무엇입니까? Median을 찾는 optimal한 알고리즘의 
complexity는 무엇입니까? optimal하다는 것을 어떻게 증명할 수 있나요? 
Median을 찾는 알고리즘을 이용하여 n개의 숫자를 정렬해보세요. 이 정렬 알고리즘의 
complexity는 무엇입니까? 두 가지 문제를 통해 Reduction이라는 개념을 설명해 보세요. 
