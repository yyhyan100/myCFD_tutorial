# Tensor Analysis

## General Information

### Vector (1D Space)
$\vec{v} = v_ie_i$
$= v_1\vec{e}_1+v_2\vec{e}_2+v_3\vec{e}_3$ </br>
with $\vec{e}_1,\vec{e}_2,\vec{e}_3$ referring to the $\vec{i},\vec{j},\vec{k}$ directions in 3D
### Matrix (2D Space)
$\vec{A} = a_{ij}e_ie_j$
$=a_{1j}e_1e_j+a_{2j}e_2e_j+a_{3j}e_3e_j$ </br>
each term can be expanded out further for $j=1,2,3$ for a total of 9 terms
### Array (3D space)
$\vec{A} = a_{ijk}e_ie_je_k$ </br>
resulting in 27 terms with the expansions of $i,j,k$
### Array (higher dimensions)
general form of a tensor

$\vec{A} = a_{i_1i_2\dots in}e_{i1}e_{i2}\dots e_{in}$
resulting in an nD array (nth order tensor) in mD space </br>
$$ m*m*m*m* ... *m=m^n $$
## Kronecker Delta
$\delta = \delta_{ij}e_ie_j$

with 
$$
\delta_{ij}=
\begin{cases}
1 & \quad \text{if i=j}\\ 
0 & \quad \text{if i} \neq \text{j}
\end{cases}
$$

## Alternating Unit Tensor (Ricci Notation)
$$ \epsilon=\epsilon_{ijk}e_ie_je_k $$
with 
$$
\epsilon_{ijk}=
\begin{cases}
0 & \quad \text{if any two indices are equal}\\ 
1 & \quad \text{if the indices are different and are in cyclic order (1,2,3)}\\
-1 & \quad \text{if the indices are not in cyclic order}
\end{cases}
$$

### Free Indices
indices that only occur once in a tensor term
e.g. i is a free index in $v_{ij}w_{j}$

every term should have an equal number of free indices

### Dummy Indices
indices that occur twice in a tensor term
e.g. j is the dummy index in $A_{ij}B_{j}$


### Einstein's Notation
summation of all components are implied with each coordinate axis
$$ \sum_{i=1}^3 {a_ib_i}=a_ib_i $$

#### Back to Kronecker Tensor
applying Einstein's notation along with free and dummy indices:
$$ a_i\delta_{ij}=a_j $$
$$ a_{ik}\delta_{ij}=a_{jk} $$
$$ b_{ijk}\delta_{km}=b_{ijm} $$
$$ a_{ij}\delta_{ij}=a_{ii}=a_{11}+a_{22}+a_{33} $$

only when i = j and k = m in all of the above

Kronecker tensor is the tensor form of the identity matrix I.

#### Back to Ricci Tensor
$\vec{a} = \langle a_1, a_2, a_3\rangle=a_ie_i$
$\vec{b} = \langle b_1, b_2, b_3\rangle=b_ie_i$ </br>
$\vec{a} \times \vec{b}= a_ib_j \epsilon_{ijk}e_k$
$a_ie_i \times b_je_j =a_ib_j \epsilon_{ijk}e_k$ </br>

implying that:
$e_i \times e_j = \epsilon_{ijk}e_k$ </br>

and:
$\vec{i} \times \vec{j}= \epsilon_{123}e_k = \vec{k}$
$\vec{j} \times \vec{i}= \epsilon_{213}e_k = -\vec{k}$

## Tensor Operations

### Addition
must be the same order
$\vec{A} + \vec{B} = a_{ij}e_ie_j + b_{ij}e_ie_j$
$= (a_{ij} + b_{ij})e_ie_j$

### Subtraction
must be the same order
$\vec{A} - \vec{B} = a_{ij}e_ie_j - b_{ij}e_ie_j$
$= (a_{ij} - b_{ij})e_ie_j$

### Scalar Multiplication
$\alpha \vec{A} = \alpha a_{ij}e_ie_j$
$= (\alpha a_{ij})e_ie_j$

### Dyadic Operations
increases order
1. $\vec{a} \vec{b} = a_ie_ib_je_j = (a_ib_i)e_ie_j$
(1st order)(1st order) --> 2nd order

2. $\vec{a} \vec{B} = a_ie_ib_{jk}e_je_k = (a_ib_{jk})
e_ie_je_k$
(1st order)(2nd order) --> 3rd order

3. $\vec{A} \vec{B} = (a_{ij}b_{km})
e_ie_je_ke_m$
(2nd order)(2nd order) --> 4th order

### Dot Product
reduces order
1. $\vec{a} \cdot \vec{b} = a_ib_i = a_jb_j$

2. $\vec{A} \cdot \vec{B} = (a_{ij}b_{jmn})e_ie_me_n$

3. $ \vec{A} : \vec{B} = a_{ij}b_{jin}e_n $
i and j are both dummy indices so $ \sum_{i} \sum_{j}$

### Cross Product
also reduces order </br>
$e_i \times e_j = \epsilon_{ijk}e_k$ </br>
$\vec{A} \times \vec{B} = (a_{ij}b_{lmn} \epsilon_{ilk})e_ie_ke_me_n$

## Advanced Tensor Operations

### Tensor Derivative
#### Gradient
The gradient is the general derivative for all functions. These are dyadic operations that increases the order by 1. </br>

zeroth order scalar </br>
$\nabla f(x,y) = <f_x, f_y> = \partial_i f e_i$

1D vector </br>
$\nabla \vec{a} = (\partial_i a_j)e_ie_j$

2D tensor </br>
$\nabla \vec{A} = \partial_i a_{jk}e_ie_je_k$ </br>
resulting in 27 terms


#### Divergence
The divergence is the gradient dot product. </br>

1D vector </br>
$\nabla \cdot \vec{a} = \partial_i a_j \epsilon_{ijk} e_k$

2D tensor </br>
$\nabla \cdot \vec{A} = \partial_i a_{jl} \epsilon_{ijk} e_k e_l$


#### Curl
1D vector </br>
$\nabla \times \vec{a} = \partial_i a_i$

2D tensor </br>
$\nabla \times \vec{A} = \partial_i a_{ij} e_j$


#### Laplacian
$\nabla^2 = \nabla \cdot \nabla = \partial^2_i$

1D vector </br>
$\nabla^2 \vec{a} = \partial^2_i a_j e_j$

2D tensor </br>
$\nabla^2 \vec{A} = \partial^2_i a_{jk} e_j e_k$

### Tensor Integration
#### Kelvin-Stokes Theorem
$\oint A \cdot d\vec{r} = \iint \nabla \times A d\vec{s}$

#### Divergence Theorem
$\oint A \cdot d\vec{s} = \iiint (\nabla \cdot A) dV$
