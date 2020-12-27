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

![](Images/Selection_238.png)

### Unweighted Graph

![](Images/Selection_236.png)

### Graph Terminology

#### Path

A path can be defined as the sequence of nodes that are followed in order to reach some terminal node ```V``` from the initial node ```U```.

![](Images/Selection_239.png)

#### Closed Path

A path will be called as closed path if the initial node is same as terminal node. A path will be closed path if **V<sub>0</sub> = V<sub>N</sub>**.

#### Simple Path

A graph with no repeated vertices.

![](Images/Selection_240.png)

The path from ```A``` to ```B``` is a simple path.

#### Cycle

Simple path, except that the last vertex is the same as the first vertex. Its also known as a circuit or circular path.

![](Images/Selection_241.png)

#### connected graph

Any two vertices are connected by some path.

![](Images/Selection_242.png)

#### Complete Graph

A complete graph is the one in which every node is connected with all other nodes. A complete graph contain ```n(n-1)/2``` edges where ```n``` is the number of nodes in the graph.

![](Images/Selection_243.png)

#### Adjacent Nodes

Two nodes are adjacent if they are connected by an edge.

![](Images/Selection_235.png)

```4``` is adjacent to ```5```

#### Degree of the Node

A degree of a node is the number of edges that are connected with that node. A node with degree ```0``` is called as isolated node.

![](Images/Selection_238.png)

    the degree of 
       Node Number 0 is 3(3, 7, 8)
       Node Number 1 is 3(1, 3, 4) 
       Node Number 2 is 2(1, 2) 
       Node Number 3 is 4(2, 3, 4, 7) 
       Node Number 4 is 2(3, 8) 

## Graph Representation

### 1. Adjacency List

- An array of lists is used. The size of the array is equal to the number of vertices. Let the array be an ```array[]```. An entry ```array[i]``` represents the list of vertices adjacent to the **i<sup>th</sup>** vertex.

- An adjacency list is maintained for each node present in the graph which stores the node value and a pointer to the next adjacent node to the respective node.

- If all the adjacent nodes are traversed then store the ```NULL``` in the pointer field of last node of the list. 

- The sum of the lengths of adjacency lists is equal to the twice of the number of edges present in an undirected graph.

![](Images/Selection_246.png)

- In a **directed graph**, the sum of lengths of all the adjacency lists is equal to the number of edges present in the graph.

![](Images/Selection_247.png)

- In the case of weighted directed graph, each node contains an extra field that is called the weight of the node.

![](Images/Selection_248.png)

### 2. Adjacency Matrix

- In adjacency matrix, the rows and columns are represented by the graph vertices. A graph having ```n``` vertices, will have a dimension ```n * n```.

- An entry **M<sub>ij</sub>** in the adjacency matrix representation of an undirected graph ```G``` will be ```1``` if there exists an edge between **V<sub>i</sub>** and **V<sub>j</sub>**.

![](Images/Selection_249.png)

- In directed graph, an entry **A<sub>ij</sub>** will be ```1``` only when there is an edge directed from **V<sub>i</sub>** to **V<sub>j</sub>**.

![](Images/Selection_250.png)

- Representation of **weighted directed graph** is different. Instead of filling the entry by ```1```, the Non- zero entries of the adjacency matrix are represented by the **weight** of respective edges.

![](Images/Selection_251.png)

