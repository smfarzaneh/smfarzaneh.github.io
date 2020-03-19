---
layout: page
title: Group Theory Notes
permalink: /academics/group_theory/
exclude: true
---

Here is a summary of main group theory mathematics and theorems from **Group Theory: Applications to the Physics of Condensed Matter** book by M. & G. Dresselhaus and A. Jorio. The goal of this summary is by no means mathematical rigor or condensing the whole book. Rather, I wrote this summary so I could quickly refresh my memory of the group theory math so I won't have to read the whole book again. 

## Chapter 1: Introduction

**Definition of Group $\mathcal{G}$**  
1. **Closure:** $A,B \in \mathcal{G}$ then $AB=C\in \mathcal{G}$.  
2. **Association:** $A(BC) = (AB)C$.  
3. **Identity:** $AE = EA = A$.
3. **Inverse:** $A^{-1}A = AA^{-1} = E$. 

**Abelian** group: All elements commute with each other.  
**Isomorphism:** One-to-one correspondence between elements of two groups.  
**Homomorphism:** Many-to-one correspondence.  
**Coset:** Collection of $\mathcal{B}X$ where $\mathcal{B}$ is a subgroup of $\mathcal{G}$ and $X\in\mathcal{G}$.  
**Order** of $\mathcal{G}:h$ and order of $\mathcal{B}:h_{B}$. $m=h/h_B$ is an integer.  
$B$ is **conjugate** to $A$ if $B = XAX^{-1}$.  
**Class:** Totality of $XAX^{-1}$ for all $X \in \mathcal{G}$.  
Subgroup $\mathcal{N}$ is **self-conjugate, invariant, or normal** if $X\mathcal{N}X^{-1}\equiv \mathcal{N}$ which contains entire classes.  
A group without any $\mathcal{N}$ is a **simple** group.  
Cosets of $\mathcal{N}$ are elements of the **quotient or factor** group.  
**Index** of $\mathcal{B}$ is its number of cosets $m = h/h_B$. 

## Chapter 2: Representation Theory

An $\ell_n$-dimensional representation denoted by $\Gamma_n$ corresponds to matrix $D^{(\Gamma_n)}(A)$ for each element $A$.  
**Reducible** representations can be brought into the same block diagonal form for all elements by a **similarity, equivalence, or canonical** transformation ($UD^{(\Gamma_n)}(A)U^{-1}$). **Irreducible** representations cannot.  
A representation $D(A)$ with non-vanishing determinant can be brought into unitary form for all $A$.  
Any Hermitian matrix can be diagonalized by a unitary transformation.  
The following theorems apply for Irreducible representations (IR).  
**Schur's Lemma 1:** If $MD^{(\Gamma_n)}(A)=D^{(\Gamma_n)}(A)M$ for all elements $A$ then M is a constant.  
**Schur's Lemma 1:** If $MD^{(\Gamma_1)}(A)=D^{(\Gamma_2)}(A)M$ for all elements $A$ then $M=0$ for $\ell_1=\ell_2$. Otherwise ($\ell_1\not=\ell_2$) either $M=0$ or $D^{(\Gamma_1)}(A) = UD^{(\Gamma_2)}(A)U^{-1}$.  
**Wonderful Orthogonality Theorem:**  
<center>$\displaystyle\sum_R D_{\mu\nu}^{(\Gamma_j)}(R)[D_{\mu'\nu'}^{(\Gamma_{j'})}(R)]^* = \frac{h}{\ell_j}\delta_{\Gamma_j\Gamma_{j'}}\delta_{\mu,\mu'}\delta_{\nu,\nu'}$. (Eq 2.7)</center>  
**Vector Space** of representations: vectors $V_{\mu,\nu}^{(\Gamma_j)}=[D_{\mu\nu}^{(\Gamma_j)}(A_1), \cdots, D_{\mu\nu}^{(\Gamma_j)}(A_h)]$ are orthogonal.  

## Chapter 3: Character of a Representation 
**Character:** $\chi^{(\Gamma_j)}(R) = \sum_{\mu=1}^{\ell_j} D_{\mu\mu}^{(\Gamma_{j})}(R)$.  
If $A$ is conjugate to $B$ then $\chi(A) = \chi(B)$.  
Elements of a class have the same character.  
**Orthogonality** of characters: $\sum_R \chi^{(\Gamma_j)}(R)[\chi^{(\Gamma_{j'})}(R)]^* = h\delta_{\Gamma_j\Gamma_{j'}}$. (Eq 3.5, 3.12)  
Orthogonality in terms of classes: $\sum_k N_k\chi^{(\Gamma_j)}(C_k)[\chi^{(\Gamma_{j'})}(C_k)]^* = h\delta_{\Gamma_j\Gamma_{j'}}$. (Eq 3.13)  
Two IRs are equivalent **if and only if** they share the same characters.  
**Decomposition Theorem:** A reducible representation can be decomposed as follows  
<center>$\displaystyle \chi(C_k) = \sum_{\Gamma_j}a_j\chi^{(\Gamma_j)}(C_k)$ (Eq 3.16) where $\displaystyle a_j=\frac{1}{h}\sum_kN_k[\chi^{(\Gamma_j)}]^*\chi(C_k)$ (Eq 3.20).</center>  
Number of IRs = Number of Classes.  
**Second** orthogonality of characters: $\sum_{\Gamma_j} N_k\chi^{(\Gamma_j)}(C_k)[\chi^{(\Gamma_{j'})}(C_{k'})]^* = h\delta_{kk'}$. (Eq 3.28)  
**Regular** representation: starting with the multiplication table, rearranging the rows and columns so $E$ elements are on the diagonal, then regular representation of element $A$ is given by putting ones where $A$ shows up and zeros otherwise.  
**Theorem:** $\sum_j \ell_j^2 = h$.  
**Setting up character tables**
1. \# of IRs = \# of classes.
2. $\sum_j \ell_j^2 = h$.
3. Row of ones for the first row ($\Gamma_1$).
4. First column's (E) elements are $\ell_j$ for each $\Gamma_j$.
5. Orthogonality of row characters.
6. Orthogonality of column characters (second orthogonality). 