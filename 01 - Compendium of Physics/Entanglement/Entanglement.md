---
authors:
  - Martin Schnee
creation date: 2024-09-04
modification date: 2024-09-04
---
## Overview

Entanglement is special form of correlation between several systems that only exist in quantum physics. In this case the global state of these systems is only defined through the correlations they share but it is not possible to assign an individual state to them.

_How to simply define entanglement ?
How to quantify it ?
Why is it relevant to study entanglement ? 
What are the physical consequences of entanglement ?
How to measure it in experiments ?_

## What is entanglement ?

Let’s repeat the hand-wavy definition given at the beginning: _Entanglement is special form of correlation between several systems that only exist in quantum physics. In this case the global state of these systems is only defined through the correlations they share but it is not possible to assign an individual state to them._ Now let’s see what it means in details.

💡 Two parts $A$ and $B$ of a system are entangled if the state $|\psi\rangle_{AB}$ of the whole can be written as a particular superposition of the following general form

$$ |\psi\rangle_{AB} = \sum_{i=1}^{\chi} \lambda_i \ |i_A\rangle |i_B\rangle $$

where each component $|i_A\rangle |i_B\rangle$ of this superposition is a unique correspondance between some state for the part $A$ and some other state for the part $B$. Meaning there is no redundancy in the $\{|i\rangle\}$.

The coefficients $\{\lambda_i\}$ are called Schmidt values form the **entanglement spectrum** for the bipartite state $|\psi\rangle_{AB}$. The states $\{|i\rangle_{A(B)}\}$ represent the entanglement degrees of freedom of the subsystem $A$ (resp. $B$), and form an orthonormal basis of its Hilbert space, meaning they completely describe it in an unambiguous way (they do not overlap each other). 

The state $|\psi\rangle_{AB}$ is entangled when at least two of the Schmidt values are non-zero. We then have a superposition of $|i_A\rangle |i_{B}\rangle$ patterns weighted by the $\lambda_i$, thus describing a unique correspondence between a certain state of the $A$ part and a state of the complementary $B$ part. Thus, the global state of the system is defined solely by the correlations shared by its parts. 

> **Remark:** This decomposition of $|\psi\rangle_{AB}$ is unique if there is no degeneracy in the coefficients. However there are two ways of defining Schmidt decomposition. Either $\lambda_i$s are real, non-negative (and unique) and Schmidt vectors are unique up to a complex phase, **or,** $\lambda_i$s are complex, unique up to a phase and the Schmidt vectors are unique (of course if $\lambda_i$s are degenerate there is no unicity at all).

Two qubits forming a Bell pair is the simplest example of entangled state one can imagine ($\lambda_1 = \lambda_2 = 1/2$) : $|\phi\rangle = \frac{1}{2}(|00\rangle + |11\rangle)$ , it is written explicitely in its Schmidt decomposition.

> **Remark:** Bell states with a “$-$” relative phase _**are not**_ in their Schmidt form. For that you have to switch them from computational basis (0,1) to basis (+,-) (i.e. Z to X basis).


💡 An alternative, illuminating, way of defining entanglement is the following: _a composite system is entangled when performing a measurement on a subsystem A alters the state of the complement B, and reduces the set of possible measurement outcomes._

## How to quantify entanglement ?

What distinguishes entanglement is that, even if the state of the entire system is perfectly known (it is pure), the uncertainty about the state of each of its parts is high. In other words, unlike classical correlation, the state of the total system cannot be deduced from the measurement of its parts. It is therefore impossible to assign a pure individual state to them, but only a classical distribution of pure quantum states (mixed state), in the form of a reduced density matrix: $\rho_A = \text{Tr}_{B} |\psi \rangle \langle \psi| = \sum_{i=1}^{\chi} \lambda_i^2 \ |i_A\rangle \langle i_A |$ . The $\lambda_i^2 = p_i$ are therefore probabilities, and are normalized such that $\sum_{i=1}^{\chi} \lambda_i^2 = 1$. 

One can estimate the amount of entanglement in a bipartite state by quantifying the amount of randomness created at the level of subsystems. To do so we use entropy.

Von Neumann entropy measures the amount of entanglement between two complementary parts whose joint state is pure. It is calculated from the density matrix of either subsystem.
$$S_A = - \text{Tr} \,\rho_A \log \rho_A = - \sum_{i=1}^{\chi} \lambda_i^2 \log \lambda_i^2 = S_{B}$$
It can be interpreted as an average measure of the degree of randomness in the knowledge
of the subsystems. The two subsystems $A$ and $B$ are maximally entangled if the Schmidt values are all identical $\lambda_i = 1/\chi$. In this case, entanglement is also maximal and proportional to the size of the smaller of the two subsystems $S_A \propto L_A$ (if $|A|\leq|B|$). On the contrary, if there is only one non-zero Schmidt value, it is $\lambda = 1$, there is no entanglement between the two parts and $S_A = 0$. In the case of the Bell pair, the entanglement entropy is $S_A = \log 2$.

In the case of non-complementary regions of the system, for example between a small sub-region $C$ of $A$ and another $D$ of $B$, their joint state $\rho_{CD}$ is not pure. We must then rely on another quantity, the mutual information $I(C:D)$, to measure the entanglement they share. This is derived from Von Neumann's entropy:
$$I(C:D) = S_C + S_D - S_{CD} $$
If $C$ and $D$ are entangled, their mutual information is non-zero (and positive). Indeed, in this case, even if the joint system $CD$ has a certain entropy $S_{CD}$, the sum of the entropy of each of the parts taken separately $S_C + S_D$ is greater because of the entanglement they share. If, on the other hand, these two parts are not entangled, $I(C:D)$ is zero. Once again, this is a typically quantum property: the sum of the parts is greater than the whole.

## Why is it relevant to study entanglement ? 

Knowledge about entanglement is relevant for many different things:

- finding optimal representation of many-body quantum states, esp. memory-cheap numerical representations, 
- classifying many-body phases of matter according to their entanglement structure, 
- used as a ressource for quantum information protocols, 
- used to protect quantum information (error correcting codes),
- _supposedly_ quantum computing ressource estimation (complexity).
- ...


## What are the physical consequences of entanglement ?

...

## How to measure it in experiments ?

...


