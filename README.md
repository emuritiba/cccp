This repository contains the files referring to the benchmark instances used in the article referred to below.

# Path-Relinking with Tabu Search for the Capacitated Centered Clustering Problem

## Authors

* Albert Einstein Fernandes Muritiba
* Marcos José Negreiros Gomes
* Michael Ferreira de Souza
* Hedley Luna Gois Oria 
 
## Abstract 

The capacitated centered clustering problem (CCCP) involves partitioning a set of $n$ points on $R^d$ ($d\ge2$) into $p$ disjoint clusters within a given capacity. Each point has an associated demand, and the objective is to minimize the sum of the Euclidean distances between the points and their respective cluster centroids. This challenge has garnered the interest of researchers from diverse fields because of its applicability and theoretical aspects. In this study, we propose effective methodologies for the construction and diversification of solutions—multi-start clustering packing and an effective neighborhood search movement-wave. These strategies were carefully designed for classical tabu search and path-relinking metaheuristics to solve CCCP cases. We demonstrate that the proposed method is experimentally robust, and is more effective than the most recently published methods based on cluster search, biased random key genetic algorithm, and Gnägia and Baumann matheuristic.

## Repository Content

### Instance files:

All instances are in the *instance.zip* file.

#### Format 

```
<number of points> <number of clusters>
<X1> <Y1> <Capacity> <Demand 1>
<X2> <Y2> <Capacity> <Demand 2>
...
<Xn> <Yn> <Capacity> <Demand n>

```
Obs.: Coordinates may be non-integer

#### Example TA25.dat


    25  10
       362        -93    6   1
       590       -335    6   1
       346       -197    6   1
       439       -130    6   1
       441       -171    6   1
       341       -393    6   1
       347       -324    6   1
       483       -311    6   1
       282       -294    6   1
       433       -121    6   1
       420       -198    6   1
       373       -298    6   1
       554       -222    6   1
       411       -279    6   1
       588       -179    6   1
       515       -335    6   1
       363       -353    6   1
       491       -396    6   1
       522       -421    6   1
       254        -98    6   1
       368       -400    6   1
       320       -320    6   1
       502       -344    6   1
       544       -130    6   1
       336       -360    6   1

 
### Executable file

Our approach is compiled for a 64-bit linux system in the object file *exefile*

#### Command

```
# ./exefile <instance file> 0 0 <tenure> <tabu iterations> <PR iterations> <random seed>

```

#### Command Example

```
# ./exefile ../instances/X-n322-k28.dat  0  0  10  2  150  941

```

#### Output

The execution will result in writing the './out/result.txt' file with the computational results in the format:

```
X-n322-k28.dat, 0, 0, 10, 2, 150, 941, 21689.45931, 0.1645510048, 21586.33184, 0.175398007, 0.6070330143, 2
```

```
<7 run parameters>  <phase 1 best cost>, <phase 1 time (sec)>, <best cost>, <time to best (sec.)>, <overall time (sec.)>, <fallback>
```

At the end of execution, the console presents the solution in the format:

```
<number of clusters>
<sol. cost>
<count> <cluster size> <cluster demand> <cluster cost> <cluster centroid X> <cluster centroid Y>: [cluster points indexes (zero based)]
...

```

