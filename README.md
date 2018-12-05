# Algorithm

내가 배운 알고리즘 개념을 정리합니다.

__1. What is an Algorithm?

__1. Desirable Algorithm

__1. Types of Algorithms

> Text books
>
> * Introduction to Algorithms, 3rd edition by Cormen, Leiserson, Rivest, and Stein, The MIT Press, 2009

***



## What is an Algoritm?

An algorithm is a finite set of instructions that if followed accomplishes a particular task.

* well-defined computational procedure that tasks some value, or set of values, as input and produces some value, or set of values, as output.

* a sequence of computational steps that transform the input into the output.

* A tool for soving a well-specified computational problem. 


<br>



## Desirable Algorithm

An algorithm must satisfies the following criteria.

* **Input**: zero or more inputs are supplied.
* **Output**: at least one output should be produced as results of procedure.
* **Definiteness**: each instruction should be clear and unambiguous (i.e.) not more than one meaning.
* **Finiteness**: if all the instructions are traced in algorithm, then for all cases the algorithm must terminate after a finite number of steps.
* **Effectiveness**: every instruction must be very basic so that it can be carried out briefly said "Operation must be feasible".


<br>



## Types of Algorithms 

* 재귀호출, 백트래킹
* 그리디
* 다이나믹
* 기하
  + 내부-외부 판별
  + 단순 닫힌 경로
  + Convex Hull(Graham Scan & Jarvis March)
  + 선분의 교차
  + 백터 외적
  + Rotating Calipers
* 문자열 & 오토마타 & 구조
  * KMP(Knuth-Morris-Pratt)스트링 매칭
  * Boyer Moore 스트링 매칭
  * 유한 오토마타 (Finite Automata)
  * Trie 구조
* 수학 & 정수론
  * 유클리드 호제법
  * 에라토스테네스의 체
  * 페르마 소정리
  * Totient Function(오일러 함수)
  * Stern-Brocot Tree
  * Miler Rabin 소수 판정, Pollard Rho의 소인수분해
  * 포함배제의 원리
* 근사 알고리즘
  * 국소 탐색(LS; Local Search)
  * 시뮬레이티드 어닐링(Simulated Annealing)
  * 유전자 알고리즘(GA)
* NP 문제
  * Minimum Vertex Cover, Edge Cover, Maximum Independent Set
  * 헤밀턴 회로
  * TSP

***그래프 & 자료구조***

* 검색(이분검색, 이진검색트리)
* 스택, 큐
* Deque(Double Ended Queue)
* 링크드리스트(Linked List)
* 힙 구조
  * Binary Heap
  * Binomial Heap
  * Fibonacci Heap
  * (Binary) Indexed Tree
  * Interval Tree
* 정렬 (합병정렬, 퀵정렬, 힙정렬, 버블정렬, 선택정렬, 삽입정렬, 기수정렬)
  * K 번째 숫자를 최악의 경우 O(n)에 찾는 문제
* 최소비용신장트리
  * Prim
  * Kruskal
  * Matroid Theory
* 최단경로
  * Dijkstra
  * Floyd
  * Bellman Ford
* 그래프 탐색
  * BFS, DFS
* 위상 정렬(Topological Sort)
* 최대 유량 알고리즘(Maximum Flow Algorithm)
  * Ford-Fulkerson의 방법
  * Minimum Cut(최소 절단 문제)
  * 푸시-재명명 방법
  * 최대 이분매칭(Bipartite Maximum Matching)
    * Hungarian Method(가중치가 들어간 매칭)
    * Gale-Shapely Matching
    * Hopcroft-Karp
  * Mincost-Maxflow Algorithm
  * Stoer-Wagner Algorithm(간선열결도 문제에 쓰이는 최적 알고리즘)
* 트리 관련
  * 최소 비용 채색 문제
  * 절점 찾기
  * Bridge 찾기
  * 등등등등...
* 강한 연결 성분(Strongly Connected Components; SCC)
  * Kosaraju, Tarjan의 방법
* 2-CNF(2-SAT의 일종)
* 서로소 집합(Disjoint Set)
  * 순위 정하기(휴리스틱의 일종)
  * 경로 압축(휴리스틱의 일종, Path Compression)

***