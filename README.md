Download Link: https://assignmentchef.com/product/solved-csc3102-homework4-topological-ordering-and-minimum-spanning-trees
<br>
<h1></h1>

<ul>

 <li>Checking whether a Digraph is Bipartite</li>

 <li>Implementing Prim’s MST Algorithm Using a Binary Heap</li>

 <li>Implementing a Reverse Postorder DFS Topological Ordering Algorithm</li>

</ul>

This project involves the completion of a text-based menu-driven application that you began in project # 3. It involves writing three non-member functions (methods) to check whether an undirected graph is bipartite, to generate a topological ordering of the vertices of a directed acyclic graph (dag) using a reverse depth-first-search recursive algorithm or indicate that a topological ordering of the vertices is not possible because the digraph contains a cycle, and to find a minimum spanning tree of a simple connected undirected weighted graph using Prim’s algorithm or a minimum spanning forest if the graph is not connected by applying Prim’s algorithm to each component of the graph. One standard application of the minimum spanning tree algorithm is determining the lower bound on cost in a network. For example, a cable company may be interested in laying out cables between hubs in a city and minimizing cost. The hubs would be the vertices, the edges, the wires, and the lengths of the wires between them, the weights on the edges. A popular application of the topological sorting algorithm is in scheduling a sequence of jobs that require the observance of some precedence rules. The jobs are represented by vertices, and there is a directed edge from <em>j<sub>m </sub></em>to <em>j<sub>n </sub></em>if <em>j<sub>m </sub></em>must be performed before <em>j<sub>n</sub></em>. A notable computer science application is in instruction scheduling by CPUs. After this project, menu options 6-8 should work. The program will have the following user interface:

BASIC WEIGHTED GRAPH APPLICATION

=============================================

<ul>

 <li>Incidence Matrix of G</li>

 <li>Floyd’s Shortest Round Trip in G</li>

 <li>Postorder DFS Traversal of G Complement</li>

 <li>BFS Traversal of G of G Complement</li>

 <li>Check whether G is Bipartite [6] Topological Ordering of V)G)</li>

</ul>

[7] Prim’s Minimum Spanning Tree in G

[0] Quit

=============================================

<strong>Definition 1. </strong>A <strong>bipartite </strong>graph, also called a bigraph, is a graph that can be decomposed into two disjoint sets such that no two vertices within the same set are adjacent.

When option 5 is selected, your application will determine whether or not the input graph is bipartite. You will examine the adjacency relationships among pairs of vertices to determine whether the input graph is bipartite. This will require calls to the <em>isEdge </em>function (method) that you implemented in the previous project. A queue or stack may be used to keep track of vertices whose adjacency relationships have already been examined and additional secondary storage may be required to do bookkeeping of those relationships. Your implementation should work for connected and disconnected undirected graphs. When option 6 is selected, your application should generate a topological ordering of the vertices of the digraph if it contains no directed cycles. Your program calls a function (method) that implements the reversed postorder depth-first-search algorithm, whose pseudocode is given in the supplementary lecture notes, to generate a topological ordering of the vertices of the graph if one exists. Your implementation should explore the vertices of the graph in lexicographical order whenever the vertex being explored during the DFS traversal has several neighbors. When option 7 is selected, your program generate a minimum spanning tree or forest of an undirected weighted graph. To do this, your program calls a function (method) that uses a binary-heap as the underlying data structure for the priorty queue based implementation of Prim’s MST algorithm. See files for the tasks that you need to complete as well as specifications of required functions/methods that you will implement to complete the application.

The executable file is <strong>GraphDemo</strong>. The input graph file will be a variation on the DIMACS network flow format file described on the project # 3 handout. For example, to run your application to find a topological ordering of a directed acyclic graph in a file called <em>cities3.wdg</em>, the file name is entered as a command line argument. The assumption is that the input file is in DIMACS format. The <em>readGraph </em>function (method) has already been implemented for you and it reads the file whose name you entered as a command line argument and creates a <em>Graph </em>instance.