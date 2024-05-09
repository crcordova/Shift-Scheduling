# Shift-Scheduling
Optimization problem for workforce scheduling, develop in python MIP  

We consider a cycle that is fixed in advance. In certain settings the cycle may be a single day, while in others it may be a week or a number of weeks.  

The problem can be formulated as follows. The predetermined cycle consists of $m$ time intervals or periods. The lengths of the periods do not necessarilyhave to be identical. During period $i, i = 1, . . . , m$, the presence of
$b_i$ personnel is required. The number $b_i$. There are $n$ different shift patterns and each employee is assigned to one and only one
pattern. Shift pattern j is defined by a vector $(a_{1j}, a_{2j}, . . . , a_{mj})$. The value
a_{ij} is either $0$ or $1$; it is a $1$ if period $i$ is a work period and 0 otherwise. Let c_j denote the cost of assigning a person to shift $j$ and $x_j$ the (integer) decision variable representing the number of people assigned to shift j. The problem of minimizing the total cost of assigning personnel to meet demand can be formulated as the following integer programming problem:
