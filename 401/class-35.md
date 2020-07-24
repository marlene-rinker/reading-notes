## Code 401 Reading Assignment Notes - Class 35

_July 24, 2020_

### Graphs

[Graphs](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/graphs.html)

A graph is a non-linear data structure that can be looked at as a collection of `vertices` (or `nodes`) potentially connected by line segments named `edges`.

#### Terminology

**Vertex** - A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.

**Edge** - An edge is a connection between two nodes.

**Neighbor** - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.

**Degree** - The degree of a vertex is the number of edges connected to that vertex.

#### Directed vs Undirected

An `Undirected Graph` is a graph where each edge is undirected or bi-directional. This means that the undirected graph does not move in any direction.

A `Directed Graph` also called a `Digraph` is a graph where every edge is directed.

Unlike an undirected graph, a `Digraph` has direction. Each node is directed at another node with a specific requirement of what node should be referenced next.

#### Complete vs Connected vs Disconnected

**Complete Graph**:  all nodes are connected to all other nodes

**Connected Graph**: all of the vertices/nodes have at least one edge. A `Tree` is a form of a connected graph.

**Disconnected Graph**: some vertices may not have edges. It is completely possible to have standalone nodes or edges (also known as islands) in a graph data structure.


#### Acyclic vs Cyclic

**Acyclic Graph**: An acyclic graph is a directed graph without cycles. A cycle is when a node can be traversed through and potentially end up back at itself. A directed acyclic graph is also called a DAG. This can also be represented as what we know as a tree.

**Cyclic Graph**: A Cyclic graph is a graph that has cycles. A cycle is defined as a path of a positive length that starts and ends at the same vertex.

#### Graph Representation

We represent graphs through:

- Adjacency Matrix

- Adjacency List

**Adjacency Matrix**: An Adjacency matrix is represented through a 2-dimensional array. If there are n vertices, then we are looking at an n x n Boolean matrix

Each row and column represents each vertex of the data structure. The elements of both the column and the row must add up to 1 if there is an edge that connects the two, or zero if there isn’t a connection.

**Adjacency List**: 

An Adjacency list is the most common way to represent graphs. An adjacency list is a collection of linked lists or array that lists all of the other vertices that are connected.

Adjacency lists make it easy to view if one vertices connects to another.

#### Weighted Graphs

A weighted graph is a graph with numbers assigned to its edges. These numbers are called weights.

#### Traversals

You will be required to traverse through a graph. The traversals itself are like those of trees.

**Breadth First:** 

In a breadth first traversal, you are starting at a specific vertex/node. This node must be specified when calling the `BreadthFirst()` method. The breadth-first traversal of a graph is like that of a tree, with the exception that graphs can have cycles. When a graph has cycles and we are trying to traverse, this leaves the possibility to be in an infinite loop….this is bad. To prevent such behavior, we need to have some sort of flag that specifies if we have already visited that vertices. Upon each visit, we just set the “visited” flag from `false` to `true`.

A few things to note about breadth-first traversals:

- If there are any disconnected nodes (such as islands) with the graph data structure, they will not be traversed.

- Breadth-first only outputs the nodes that are connected in some relation to the root that you pass in.

**Depth First**:

In a depth first traversal, we approach it a bit different than the way we do when working with a depth first traversal of a tree. Similar to how the breadth-first uses a queue, we are going to use a Stack for our depth-first traversal.

The algorithm for a depth first traversal is as follows:


1. Push the root node into the stack

2. Start a while loop while the stack is not empty

3. Peek at the top node in the stack

4. If the top node has unvisited children, mark the top node as visited, and then Push any unvisited children back into the stack.

5. If the top node does not have any unvisited children, Pop that node off the stack

6. Repeat until the stack is empty

[Today's article](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/graphs.html) has good explanations of what graphs look like and how to traverse them.

#### Real World Usage

- GPS and Mapping
- Driving directions
- Social networks
- Airline traffic
- Netflix uses graphs for suggestions of products

#### Additional Resources

None for today




---
[Home page](https://marlene-rinker.github.io/reading-notes/)