# Graph

## what is a graph ?

A Graph is a non-linear data structure consists of a finite set of vertices(or nodes) and set of Edges which connect a pair of nodes.

![](https://www.geeksforgeeks.org/wp-content/uploads/undirectedgraph.png)

In the above Graph, the set of vertices ```V = {0,1,2,3,4}``` and the set of edges ```E = {01, 12, 23, 34, 04, 14, 13}```.

### Graph Applications

Graphs are used to represent **networks and relations**.

- Friendships.

- Roads between cities.

- Network points.

### Undirected Graph

Edges are not associated with the directions with them.

![](Images/Selection_234.png)

An undirected graph is shown in the above figure since its edges are not attached with any of the directions. If an edge exists between vertex ```1``` and ```4``` then the vertices can be traversed from ```4``` to ```1``` as well as ```1``` to ```4```.

### Directed Graph

In a directed graph, edges form an ordered pair.

A directed graph is shown in the following figure.

![](Images/Selection_235.png)

Edges represent a specific path from some vertex ```1``` to another vertex ```4```. Node ```1``` is called initial node while node ```4``` is called terminal node.

### Weighted Graph

In a weighted graph, each edge is assigned with some data such as length or weight. The weight of an edge e can be given as ```w(e)``` which must be a positive ```(+)``` value indicating the cost of traversing the edge.

![](Images/Selection_237.png)

### Unweighted Graph

![](Images/Selection_236.png)
