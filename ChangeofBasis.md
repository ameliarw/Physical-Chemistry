{% include mathjax.html %}

## Change of basis:

There are some subtle yet very fundamental concepts in quantum mechanics that, we as students, tend to overlook when we first learn quantum mechanics. The concept of changing the basis for the Hamiltonian and eigenvectors is probably the epitome of these overlooked concepts. When solving a quantum system It is to be overwhelmed by the math we are solving and forget what basis we are working on. 
This page is designed to show the importance of paying attention to the basis we are working on and how to change between bases to simplify the math of solving quantum problems as well as extracting the needed information from the quantum system. Our work will be using examples from the paticle in a box system, but our derivations can be applied to any quantum system.

We know that an energy eigenvector in the position space $(\psi_n)_x$ can be represented as a linear combination of the orthonormal basis vectors ${\vec{x_1},\vec{x_2},\vec{x_3}...}$ as: $(\psi_n)_x=c_1\vec{x_1}+c_2\vec{x_2}+c_3\vec{x_3}+...$.
The main idea of the position basis in 1-D is that a vector $\vec{X_i}$  represents a delta function with a values of $1$ at $i$ and has a values of $0$ everywhere else. In vector form, this is represented as $\vec{X_1}={\begin{pmatrix} 1\\\ 0\\\ 0\\\ \vdots \end{pmatrix}}_x$ and $\vec{X_2}={\begin{pmatrix} 0\\\ 1\\\ 0\\\ \vdots \end{pmatrix}}_x$ etc... as shown in the following figure.

<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/35716147-d57ce0c8-07a4-11e8-95c0-6e951cf81814.jpg" width="500">
</p>
<p align="center"> Graphical representation of some basis vectors </p>

We can now write the energy eigenvector in the position space $(\psi_n)_x$ in vector form as:

<p align="center">
$(\psi_n)_x=c_1{\begin{pmatrix} 1\\\ 0\\\ 0\\\ \vdots \end{pmatrix}}_x+c_2{\begin{pmatrix} 0\\\ 1\\\ 0\\\ \vdots \end{pmatrix}}_x+c_3{\begin{pmatrix} 0\\\ 0\\\ 1\\\ \vdots \end{pmatrix}}_x...={\begin{pmatrix} c_1\\\ 0\\\ 0\\\ \vdots \end{pmatrix}}_x+{\begin{pmatrix} 0\\\ c_2\\\ 0\\\ \vdots \end{pmatrix}}_x+{\begin{pmatrix} 0\\\ 0\\\ c_3\\\ \vdots \end{pmatrix}}_x...$
</p>

we can visualize this by plotting any of the eigenvectors, for example the ground state $(\psi_1)_x$, and the basis vectors on the same graph. This is shown in the figure bellow, where we discretized space to 10 distinct points. The intersect of the eigenvector and each of the basis vectors $\vec{x_i}$ represents the coefficient $c_n$.

<p align="center">
  <img src="https://user-images.githubusercontent.com/35305574/35718208-73a73ae4-07b1-11e8-9bf4-a139ccc8a928.jpg" width="500">
</p>
<p align="center"> Genergy eigenvectors in position basis</p>




