{% include mathjax.html %}


## Introduction to Quantum Mechanical Concepts Using Linear Algebra
Linear algebra is the natural language of quantum mechanics. So, it is crucial to begin our explorations by a quick refresher on the main ideas in linear algebra that are most relevant to our study.

Linear algebra allows us to express quantum states in vector forms. This, in my opinion, makes the ideas of orthogonality and normalization of wavefunctions more intuitive. We all know from introductory linear algebra what it means to normalize a vector and what orthogonal sets of vectors mean, here we will put our math background to some real scientific use.

### 1.1 Orthonormal basis
Consider a basis formed by the linearly independent and normalized vectors $|1>, |2>, |3>...|n>$ in a n-dimensional space. We can use this basis to write any vector in this space as a linear combination of the above vectors.
For example, we can write an arbitrary vector $|v>$ as 

<p align="center"> $|v>=v_1\begin{bmatrix} 1 \\\ 0 \\\ \vdots \\\ 0 \end{bmatrix}+v_2\begin{bmatrix} 0 \\\ 1 \\\ \vdots \\\ 0 \end{bmatrix}+...v_n\begin{bmatrix} 0 \\\ 0 \\\ \vdots \\\ 1 \end{bmatrix}=\begin{bmatrix} v_{1} \\\ v_{2} \\\ \vdots \\\ v_{n} \end{bmatrix}$. </p>
and another vector $|w>$ as

<p align="center"> $|w>=w_1\begin{bmatrix} 1 \\\ 0 \\\ \vdots \\\ 0 \end{bmatrix}+w_2\begin{bmatrix} 0 \\\ 1 \\\ \vdots \\\ 0 \end{bmatrix}+...w_n\begin{bmatrix} 0 \\\ 0 \\\ \vdots \\\ 1 \end{bmatrix}=\begin{bmatrix} w_{1} \\\ w_{2} \\\ \vdots \\\ w_{n} \end{bmatrix}$. </p>
We can also write $|v>$ and $|w>$ in a more formal and concise way as
 <p align="center">$|v>= \sum_{n=1}^{n}v_i |i> \ and \ |w>= \sum_{n=1}^{n}w_i |i> $. </p>

### 1.2 Inner Product
Inner products are ubiquitous in the realm of quantum mechanics. So it is important to have a quick refresher on inner products and get familiar with the notation we will be using in our study.

The inner product of $|v>$ and $|w>$ is defined as
<p align="center"> $<v,w>={\begin{bmatrix} v_{1} & v_{2} & ... & v_{n} \end{bmatrix}}^* \begin{bmatrix} w_{1} \\\ w_{2} \\\ \vdots \\\ w_{n} \end{bmatrix}=\sum_{n=1}^{n}v_i ^*w_i $.</p>
In quantum mechanics, the basis vectors $|1>, |2>... |n>$ represent the eigenvectors of a quantum operator such as the Hamiltonian $\hat{H}$ or the momentum operator $\hat{P}$. These vectors are orthonormal, meaning that they are unit vectors and are mutually orthogonal. This can be mathematically summarized as
<p align="center"> $<i,j>=\begin{cases} 1 \ for \ i=j \\ 0 \ for \ i\neq j \end{cases} = \delta_{ij}$. </p>
Inner products are particularly useful in quantum mechanics for normalizing  vectors and computing expectation values. The magnitude of a vector $\vec{v}$ can be expressed as an inner product $|\vec{v}|= \sqrt{< \vec{v},\vec{v} >} $. Therefore, we can normalize $\vec{v}$ as follow
 
<p align="center"> $\hat{v}=\frac{1}{\sqrt{< \vec{v},\vec{v} >}} \vec{v} $. </p>
 
 Similarly, the expectation value of a quantum operator $\hat{Q}$ can be expressed as an inner product 
 
 <p align="center"> $ < \hat{Q} >= < \psi, \hat{Q} \psi > $, </p>
 
 where $\psi$ is an energy eigenvector of the quantum system. This is analogous to the way we are used to compute expectation values using integrals. An integral is by definition the sum of infinitesimal elements, while the inner product is a sum of discrete elements.
 
### 1.3 Time Independent Schroedinger Equation (TISE)
The single most important piece of quantum mechanics is the TISE expressed as an eigenvalue equation

<p align="center"> $\hat{H}\psi_n=E_n\psi_n$, </p>
where $\psi$ is the eigenfunction of the system, $E$ is the value of the energy of the system and $\hat{H}=\hat{T}+\hat{V}$ is the Hamiltonian operator. $\hat{T}=-\frac{\hbar^2}{2m}\frac{d^2}{dx^2}$ for a one-dimensional system and $\hat{V}$, the potential energy operator, is described by the particular quantum system studied.

### 1.4 Quantum Operators
Quantum operators such as position, angular and linear momentum and the Hamiltonian, the total energy opertor, are all represented by square matrices. 

So, let’s see one example of an operator matrix.

### 1.5 Constructing the Potential Energy Matrix
From the TISE, we know that the potential energy operator, $\hat{V}$ should be a matrix operating on the wavefunction represented by a vector $\psi$ of size n. So, $\hat{V}$ should be an $n \times n$ square matrix. Then, we need to determine the entries of this square matrix. We know that applying the potential energy operator on a position eigenvector yields the value of the potential energy (eigenvalue) at the position represented by the vector:

<p align="center"> $\hat{V}|r>=V(r)|r> $. </p>

This means that when operating the potential energy matrix on the independent vectors $|1>, |2>, |3>...|n>$ we obtain $v_{11}|1>, v_{22}|2>, v_{33}|3>...v_{nn}|n>$, respectively.
Therefore, $\hat{V}$ must be a diagonal matrix of the form

<p align="center"> $\begin{bmatrix}
 v_{11} & 0 & & \cdots & &  0 \\\
 0 & v_{22} & & \cdots & & 0 \\\
 \vdots &  \vdots &  & \ddots & & \vdots\\\
0 & 0 & & \cdots & &  v_{nn}
\end{bmatrix}$ </p>

For example, we can consider the potential shown in the figure bellow. This potential can be expressed in matrix form as

<p align="center"> $\hat{V}= \begin{bmatrix}
4& 0& 0& 0& 0&0 & 0\\\
0& 0& 0& 0& 0&0 & 0\\\
0& 0& 0& 0& 0&0 & 0\\\
0& 0& 0& 3& 0&0 & 0\\\
0& 0& 0& 0& 2&0 & 0\\\
0& 0& 0& 0& 0&0 & 0\\\
0& 0& 0& 0& 0&0 & 0
\end{bmatrix}$ </p>

<p align="center"> <img src="https://user-images.githubusercontent.com/35305574/35784820-b0dd9018-09e9-11e8-8597-b341a167d9eb.jpg" width="600"> </p>

[Go back to home page](/README.md)
