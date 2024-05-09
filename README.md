# Shift-Scheduling
Optimization problem for workforce scheduling, proposed in _Planning and Scheduling in
Manufacturing and Services_ by Michael L. Pinedo, develop in python MIP  

We consider a cycle that is fixed in advance. In certain settings the cycle may be a single day, while in others it may be a week or a number of weeks.  

The problem can be formulated as follows. The predetermined cycle consists of $m$ time intervals or periods. The lengths of the periods do not necessarily have to be identical. During period $i, i = 1, . . . , m$, the presence of $b_i$ personnel is required. The number $b_i$. There are $n$ different shift patterns and each employee is assigned to one and only one pattern. Shift pattern j is defined by a vector $(a_{1j}, a_{2j}, . . . , a_{mj})$. The value $a_{ij}$ is either $0$ or $1$; it is a $1$ if period $i$ is a work period and 0 otherwise. Let $c_j$ denote the cost of assigning a person to shift $j$ and $x_j$ the (integer) decision variable representing the number of people assigned to shift $j$. The problem of minimizing the total cost of assigning personnel to meet demand can be formulated as the following integer programming problem:  

$$ minimize \, c_1x_1 + c_2x_2 + \cdots + c_nx_n $$
$ subject to: $  
$$ a_{11}x_1 +a_{12}x_2 + \cdots + a_{1n}x_n \geq b_1  \\
a_{21}x_1 +a_{22}x_2 + \cdots + a_{2n}x_n \geq b_2 \\
\vdots \\
a_{m1}x_1 +a_{m2}x_2 + \cdots + a_{mn}x_n \geq b_m \\
x_{j} \geq 0 \quad for \, j=1,...,n
 $$