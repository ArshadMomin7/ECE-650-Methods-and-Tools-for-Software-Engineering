# ECE650 : Assignment 3

This assignment focuses majorly on the combination of Assignment 1 and Assignment 2. The street data is entered and modified in Assignment 1 and the Edges are obtained as an output. This output stream can be fed as input string to Assignment 3 and with the BFS algorithm implemented in the Assignment 2 the shortest path can be found from source vertex to the destination vertex.

# Assignment 1 Output:
add "Weber Street" (2,-1) (2,2) (5,5) (5,6) (3,8)  
add "King Street S" (4,2) (4,8)  
add "Davenport Road" (1,4) (5,8)  
gg  
V = {  
    1: (2,2)  
    2: (4,2)  
    3: (4,4)  
    4: (5,5)  
    5: (1,4)  
    6: (4,7)  
    7: (5,6)  
    8: (5,8)  
    9: (3,8)  
    10: (4,8)  
    }  
    E = {  
        <1,3>,  
        <2,3>,  
        <3,4>,  
        <3,6>,  
        <7,6>,  
        <6,5>,  
        <9,6>,  
        <6,8>,  
        <6,10>  
        }

# Assignment 2 Output:
V 15  
E {<2,6>,<2,8>,<2,5>,<6,5>,<5,8>,<6,10>,<10,8>}  
s 2 10  
2-8-10

# Assignment 3 Output:
V 8  
E {<1,3>,<1,4>,<1,5>,<2,4>,<5,8>,<6,3>,<6,7>}  
s 3 5  
3-1-5

# Description :
In the above, the first three lines makes executable, and run the driver program with some
command-line arguments. Then, the lines “V = ...", “E = ...", and “3-1-5" are output. The
input the user provided to your program via stdin is “s 3 5".

As the example above indicates, there are two kinds of input the user provides. One is via the
command-line arguments, with switches such as -s and -n . This is done only once, when your
program is first started. The other type of input is the 's' command on stdin, which may be issued
repeatedly, just as in Assignment 2. For the 's' command, program should output a shortest
path.

You might need to modify `CMakeLists.txt` if you are adding additional
source files for your code and/or tests.