MSE706

Coding part of homework 1 for Phase Transformations and Kinetics of Materials class.

Main goal of this code was to utilize Java and graph theory for diffusion problems where crystal structure of solids can change dynamically. Advantage of this approach is completely determined domain which allows to implement straight forward visualization of lattice and diffusing atoms on the fly. Linked list provide efficient memory management and fast access to any part of the graph which guarantees order of O(n) steps for finding neighbors of any atom.

The disadvantage of this supercell appoach is in relatively slow Java library procedures and object oriented data manipulation which create huge overhead compared to optimized matlab. Thus it turned out impractical to simulate Problem 4 with this approach due to O(n^3) number of operations for one complete exchange even for relatively small supercell of 3000 atoms. However in future some parts of this code can be optimized and used with Apache Spark for massively parallelel execution on CPU clusters or utilization of GPU.

What you need in order to build: IntelliJ Maven JDK 8

There are two parts:

First part has GUI interface and 2D/3D visualization of vacancy diffusion in in cubic/hexagonal lattices. Main file is NetworkVis.java.

Second part is related to Problem 4 which is direct exchange of A-B atoms in binary alloy at high temperatures. This part doesnt use visualization due to slow performance.
