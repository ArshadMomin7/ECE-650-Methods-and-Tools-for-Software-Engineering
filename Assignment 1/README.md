# ECE650 : Assignment 1

Adding a street name with its Co-ordinates
For example,
"Weber Street" (2,-1) (2,2) (5,5) (5,6) (3,8)

With the help of below commands the following actions can be performed with the input data.
1. "add" - addition of street name and its co-ordinates
2. "mod" - modification into the street name and its co-ordinates
3. "gg"  - gets the vertices and edges data using provided street names and its co-ordinates and causes the program to output the corresponding graph.
4. "rm"  - removes the street data along with its co-ordinates


## The Output Graph

The interpretation of the coordinates as a poly-line segment.

There is a vertex corresponding to: 
(a) each intersection, and, 
(b) the end-point of a line segment of a street that intersects with another street. 
An example of (a) from above is Vertex 3. 
An example of (b) is Vertex 1. The identity of a vertex can be any string of letters or integers (but no specialcharacters). For example, v1xyz is acceptable as the identity of a vertex, but not v1 !!#xyz. (The space is unacceptable, as are '!' and '#'.

There is an edge between two vertices if: 
(a) at least one of them is an intersection, 
(b) both lie on the same street, and, 
(c) one is reachable from the other without traversing another vertex.
An example from above is the edge <1,3> which connects the end-point of a line segment to an intersection. Another example is the edge <3,6> which connects two intersections.