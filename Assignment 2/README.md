# ECE650 : Assignment 2


With the data entered with respect to the coordinates of the Street, this assignment will be able to focus majorly on finding the shortest path from Source Vertex to destination Vertex.
For example:
`V 15
E {<2,6>,<2,8>,<2,5>,<6,5>,<5,8>,<6,10>,<10,8>}
s 2 10
2-8-10`

As the example above indicates, one kind of input is the specification of a set of vertices V, and
set of edges E of the undirected graph. The specification of a set of vertices starts with 'V', followed by a space, followed by an integer greater than one, all in one single line. If the integer that follows the V is i, then we assume that the vertices are identified by 1,.......,i.
The specification for a set of edges starts with `E'. It then has a space, followed by the set of
edges in a single line delimited by '{' and '}'. The two vertices of an edge are delimited by '<' and '>' and separated by a comma. The edges in the set are also separated by a comma. There are no
whitespace characters within the { }.

## Output

The only other kind of input starts with an ‘s'. It asks for a shortest path from the first vertex
to the second that is specified after the s. The s is followed by a space, a vertex ID, another space, and a second vertex ID. The lines 2-8-10 and 5-2-3-1 above are outputs of the s commands that
immediately precede them. The output comprises vertex IDs separated by ‘-‘, with no whitespace
within. If a path does not exist between the vertices, should output an error.

The graph is specified by the specification of the set of vertices V followed by the set of edges E,
in that order. V and E always occur together. There is no relationship between subsequent graphs
specification’s; when a new V specification starts, all previous information can be forgotten. After
the specification of the graph there can be zero or more shortest-path queries s. For each s query,
only one shortest path should be output, multiple shortest paths might exist and an arbitrary choice
can be made

## Compilation Instructions

### Using default compiler
```bash

$ mkdir build 
$ cd build
$ cmake -DCMAKE_BUILD_TYPE=Debug ../
$ make
```

### Using Clang compiler

```bash
$ mkdir build 
$ cd build
$ cmake -DCMAKE_BUILD_TYPE=Debug -DCMAKE_C_COMPILER=clang -DCMAKE_CXX_COMPILER=clang++ ../
$ make
```

### With AddressSanitizer

AddressSanitizer is a run-time checker that monitors your program for potential
memory errors. It is very useful for thoroughly testing your C/C++ code at the
early stages of development. It is recommended that you always compile with
AddressSantizer enabled and fix any of the errors that it uncovers.


```bash
$ mkdir build 
$ cd build
$ cmake -DCMAKE_BUILD_TYPE=Debug -DCMAKE_C_COMPILER=clang -DCMAKE_CXX_COMPILER=clang++ -DWITH_ASAN=ON ../
$ make
```

