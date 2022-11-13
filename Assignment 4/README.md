# ECE650 : Assignment 4
We will be using MiniSat SAT solver available at https://github.com/agurfinkel/minisat
MiniSat provides a CMake build system. You can compile it using the usual sequence:
`cd PROJECT && mkdir build && cd build && cmake ../ && make`

Created a polynomial reduction of the decision version of VERTEX COVER to CNF-SAT.Implemented
the reduction and use minisat as a library to solve the minimum VERTEX COVER problem for
the graphs that are input to your program (as in Assignment 2).  
As soon as you get an input graph via the ’V’ and ’E’ specification you should compute a
minimum-sized Vertex Cover, and immediately output it. The output should just be a sequence of
vertices in increasing order separated by one space each

Sample Output:
V 5  
E {<1,5>,<5,2>,<1,4>,<4,5>,<4,3>,<2,4>}  
4 5  
The lines starting with V and E are the inputs to your program, and the last line is the output.
Note that the minimum-sized vertex cover is not necessarily unique.  

# A Polynomial-Time Reduction from VERTEX-COVER to CNF-SAT:
A vertex cover of a graph G = (V,E) is a subset of vertices C union of V such that each edge in E is
incident to at least one vertex in C.  
  
VERTEX-COVER is the following problem:
Input: An undirected graph G = (V,E), and an integer k [0, |V|].
Output: True, if G has a vertex cover of size k, false otherwise  
  
  CNF-SAT is the following problem:  
  Input: a propositional logic formula, F, in Conjunctive Normal Form (CNF).  
  That is, F = c1 ^ c2 ^ . . . ^ cm, for some positive integer m. Each such ci is called a “clause  
  A clause ci = li V  . . . V l(i,p) for some positive integer p. Each such l(i,j) is called a“literal.” A literal l(i,j) is either an atom, or the negation of an atom.  
  We present a polynomial-time reduction from VERTEX-COVER to CNF-SAT. A polynomial-time
reduction is an algorithm that runs in time polynomial in its input. In our case, it takes as input
G, k and produces a formula F with the property that G has a vertex cover of size k if and only if
F is satisfiable.  
The use of such a reduction is that given an instance of VERTEX-COVER that we want to
solve, (G, k), we use the reduction to transform it to F, and provide F as input to a SAT solver.
The true/false answer from the SAT solver is the answer to the instance of VERTEX-COVER.
Assuming the SAT solver works efficiently (for some characterization of “efficient”), we now have
an efficient way of solving VERTEX-COVER.


You might need to modify `CMakeLists.txt` if you are adding additional
source files for your code and/or tests.


