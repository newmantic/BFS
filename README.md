# BFS

Breadth-First Search (BFS) is a graph traversal algorithm that explores the nodes of a graph in layers. Starting from a given node, BFS visits all of its immediate neighbors first before moving on to nodes at the next level of the graph.


Graph Representation:
A graph G consists of a set of nodes (or vertices) V and a set of edges E that connect pairs of nodes. A graph can be directed or undirected.
G = (V, E)
The graph is often represented using an adjacency list, where each node u in V has a list of neighbors (nodes directly connected by an edge).
Adj[u] = {v | (u, v) is in E}

Algorithm Description:
BFS starts from a specified starting node s and explores all its neighbors, then the neighbors' neighbors, and so on, until all nodes reachable from s have been visited.


Initialization:
Mark all nodes as unvisited.
Create a queue Q to keep track of nodes to be explored.
Enqueue the starting node s and mark it as visited.

Exploration:
While Q is not empty:
Dequeue the front node u from Q.

For each neighbor v of u (i.e., for each v in Adj[u]):
If v is not visited:
Mark v as visited.
Enqueue v into Q.

Termination:
The algorithm terminates when all reachable nodes from s have been visited.

Time Complexity:
The time complexity of BFS is O(V + E), where V is the number of nodes and E is the number of edges. This is because each node is enqueued and dequeued at most once, and each edge is explored once.
