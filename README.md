# OOES_Algorithm.cpp
An Exact Algorithm to optimize a Linear Function Over the Set of Efficient Solutions for BOMILP

This is a criterion space search for optimizing a linear function over the set of efficient solutions of bi-objective mixed integer linear programs. This project is a Netbeans IDE 8.2 C++ project which is written in Linux (Ubuntu).

The following problem classes are supported:

    i. Objectives:    2 linear objectives.
    ii. Constraints:  0 or more linear (both inequality and equality) constraints.
    iii. Variables:
        a. Binary
        b. Integer variables
        c. Continous variables
        d. Any combination between previous types of variables.

## Input File
A bi-objective mixed integer linear instance can be provided as an input file using the following format:
Problem example:

![Images](/Images/Example.jpg)
![Images](/Images/Obj_fun_example.jpg)

Description of the input file:

![Images](/Images/Input%20File.jpg)

All numbers must be separated by a single space or a tab space.

## CPLEX-Concert Technology
To compile the code, CPLEX (default version 12.7) must be installed on your computer. The default directory for CPLEX used is */opt/CPLEX/12.7/*. Changing the directory of CPLEX to your preferred directory can be done either in the *Makefile* or through Netbeans. If you would like to do it in the *Makefile* you should go to *nbproject/Makefile-Debug.mk* and *nbproject/Makefile-Release.mk* and change all instances of */opt/CPLEX/12.7/* to your preferred directory. If you would like to do it through Netbeans, you can open the project in Netbeans and right click on the name of the project and choose *Properties*. You should then change the directory in the *Include Directories* box which is located in the *C++ Compiler* sub-menu. Moreover, you should also change the directory in the *Libraries* box which is located in the *Linker* sub-menu.

## Compiling and Running
Compiling the project can be done using the *Terminal* by going to the directory in which the project is saved and typing ”make clean” followed by ”make” (you can also compile through Netbeans).

An instance can be solved by typing
*./OOES enhancements.txt <*address*>/<*instance*>

By default, the file *enhancements.txt* applies all enhancements available in the algorithm. To disable a specific set of enhancements, open to *enhancements.txt* and change the desirable parameter from 1 to 0.

You can run the example instance included in the repository by typing
*./OOES enhancements.txt input.txt*
