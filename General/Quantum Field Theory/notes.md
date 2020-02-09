---
title: Quantum Field Theory I
subtitle: "Collected notes for the course Introduction to Quantum Field Theory
    as taught by M. Buballa in the summer semester 2019"
numbersections: true
titlepage: true
toc: true
toc-own-page: true
---

# Preface

These notes are adapted from the "Introduction to Quantum Field Theory" course taught by M. Buballa at the TU Darmstadt during the summer semester in 2019.
The course was originally taught in German, but these notes are being written in English to be more useful to the broader physics community.
In the process of writing these notes, the structure and content of the course has been adapted a little.
In particular, these notes contain more thorough derivations of key results, which were often left as exercises to the student.
However, the content is still essentially the same as presented by M. Buballa.

Quantum field theory is a critical tool in many modern research areas in physics.
As such, it forms the basis for many methods used in calculations, such as effective field theories and path-integral calculations.
While this course will not be able to cover all of these topics, it will cover the foundations.
As a result, learning about these foundations in a quantum field theory course should be of great interest to many physics students.
These notes aim to offer a self-contained treatment on the level of a graduate student in physics familiar with classical mechanics (the Lagrangian formulation), electrodynamics, and quantum mechanics.
Later discussions of scattering processes will benefit from prior exposure to scattering theory.

# Introduction and foundations

## Motivation

Quantum field theory is the union between quantum mechanics, classical field theory, and special relativity.
It forms the basis for the standard model and has many applications currently in different sub-fields.
To illustrate how different theories have different features and different corresponding ranges of validity, let us do a quick conceptual review.

### Classical mechanics

Classical mechanics describes point-like particles that interact with each other and the environment via forces, $F(\va{r}, \va{r}')$.
It is often convenient to introduce a potential, $V(\va{r}, t)$, but this quantity is not ever associated with any physical quantity.
Classical mechanics is an example of a purely classical theory.

### Electrodynamics

For classical electrodynamics, we need to introduce the physical fields $\va{E}(\va{r}, t)$ and $\va{B}(\va{r}, t)$.
These fields have a physical interpretation, carry energy, and have interesting, non-trivial physics on their own (independent of matter).
Electrodynamics is a classical field theory as made evident by the existence of physically meaningful fields in addition to whatever matter is in the system.
It is again convenient to work in terms of the scalar and vector potentials, $\Phi(\va{r}, t)$ and $\va{A}(\va{r}, t)$, which once again do not have a real physical interpretation.
They are simply a reformulation of the degrees of freedom of the electric and magnetic fields.
It is also worth mentioning that electrodynamics naturally includes special relativity, via the recasting of $\Phi$ and $\va{A}$ into the field strength tensor $F^{\mu\nu}$.

### Quantum mechanics

In quantum mechanics, after canonical quantization with respect to single-particle position and momentum, we arrive at a semi-classical treatment of matter.
We have single particles described by wavefunctions which behave both like waves and like particles.
However, the interactions with those particles are taken to be classical.
This treatment is uneven, and attempting to directly generalize it to special relativity leads to contradictions.

### Quantum field theory

In quantum field theory, we shall see that systems are modeled via a symmetric description in terms of quantized matter fields and interaction fields.
This leads to the intuitive assignment of particles to interactions, where these particles mediate the interaction of interest.
Consider the example of electron-electron scattering in quantum electrodynamics (QED).

**TODO Missing figure of Feynman diagram**

In this diagram, each of the incoming and outgoing electrons is described by a field, $\psi(x)$.
Also, the potential between them is given by the field $A^{\mu}(x)$, to which we assign the photon.
It is clear that the gauge field $A^{\mu}(x)$ has a fundamental meaning in the process.

## Successes of quantum field theory

### QED

Among other things, QED predicted the existence of two processes that were later observed: particle-anti-particle annihilation and photon-photon scattering.
Additionally, QED is able to make a very precise prediction of the magnetic moments of the electron and muon.
The magnetic moment is given by $\mu_i = g_i s \mu_{B}$, where $i$ is an index indicating particle species, $\mu_{B}$ is the Bohr magneton, $s$ is the spin ($1/2$ for the electron and muon), and $g$ is a dimensionless scaling value.
The leading-order approximation by Dirac for QED predicted $g_i=2$, a remarkable improvement over the classical expectation, $g_i=1$.
Extensive QED calculations including many orders of corrections give the prediction $g_i=2.0023318361(10)$, which agrees with experiment up to a relative precision of $10^{-8}$.

### The standard model

The standard model provides a unified description of the electromagnetic, weak, and strong interactions via quantum field theory.
The interactions are described as gauge theories with different symmetry groups.
We will learn over the course of these notes what exactly this means.

## Conventions

### Units

These notes use the convention $\hbar=c=1$, the so-called natural units.
This gives the following identity: $\hbar c=1=197\:\textrm{MeV}$.
A result of this is that every dimension-full quantity has units of a power of one unit of choice, either $\textrm{MeV}$ or $\textrm{fm}$.
For example,
$$
[E]=[m]=[p]=1\:\textrm{MeV},
$$
$$
[t]=[x]=1\:\textrm{MeV}^{-1}.
$$
Conversions to $\textrm{fm}^{-1}$ from $\textrm{MeV}$ can be achieved via a convenient multiplicative insertion of $\hbar c$. Another thing worth noting is that in these units charges will in general be dimensionless.

### Relativistic notation

Since quantum field theories are relativistic theories, we will need to consider space and time similarly.
Here I will outline some conventions for the relativistic notation used in these notes.

To start, $\va{x}$ will denote a standard spatial 3-vector:
$$
\va{x}=x^i=(x^1, x^2, x^3).
$$
We will adopt the Einstein summation convention, where repeated indices in a term are summed over:
$$
x_i x^i = \sum_{i}x_i x^i \overset{?}{=} \va{x}^2.
$$
Here, we take $\va{x}^2=\sum_{i}{x^i}^2$ to be the typical vector inner product result, and we will see that in our notation the last equality above does not hold.
Roman indices, like $i$, will be used for indices that run over $i=1,2,3$.

$x$ will denote a contravariant 4-vector:
$$
x=x^{\mu}=(x^0, x^i)=(x^0, \va{x})=(t, \va{x}).
$$
Greek indices, like $\mu$, will be used for indices that run over $\mu=0,1,2,3$.
The covariant $x_{\mu}$ will be related to $x^{\mu}$ via:
$$
x_{\mu}=g_{\mu\nu}x^{\mu}.
$$
We will use the "mostly minus" or "west coast" convention for $g_{\mu\nu}$:
$$
g_{\mu\nu}=\begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & -1 & 0&0\\
0 & 0 & -1&0\\
0 & 0 & 0&-1
\end{pmatrix}.
$$
This means
$$
x_{\mu}=(x_0, x_i)=(x^0, -\va{x})=(t, -\va{x})
$$
and $x_i=-x^i$, which means
$$
x_ix^i=-\va{x}^2.
$$
This is the reason that we will refer to individual components of spatial and space-time vectors via superscripts (for example, $x^1$) instead of the typically used subscripts, to avoid ambiguity about the sign of these quantities.

## Foundations: existing theories

### Lorentz transformations

Lorentz transformations are the special-relativistic analog of Galilean transformations.
The homogeneous Lorentz transformations are reflections in space-time, rotations, and boosts.
The inhomogeneous Lorentz transformations are translations in space-time.
Under a homogeneous Lorentz transformation, we have
$$
x^{\mu} \rightarrow x'^{\mu} = \Lambda^{\mu}_{\nu} x^{\nu},
$$
$$
x_{\mu} \rightarrow x'_{\mu} = \Lambda_{\mu}^{\nu} x_{\nu}.
$$
This allows us to define that a contravariant (covariant) Lorentz vector is a 4-vector that transforms under Lorentz transformations like $x^{\mu}$ ($x_{\mu}$).
This means $\frac{\partial}{\partial x^{\mu}} = (\frac{\partial}{\partial t}, \va{\nabla})$ is the covariant derivative $\partial_{\mu}$, and $\frac{\partial}{\partial x_{\mu}} = (\frac{\partial}{\partial t}, -\va{\nabla})$ is the contravariant derivative $\partial^{\mu}$.

**TODO Could use a proof of these counterintuitive transformation properties here**

It is useful to note here that the scalar product of Lorentz vectors is invariant under Lorentz transformations.

### Classical mechanics

The general problem statement of classical mechanics is: given $n$ point-like masses each described by a generalized coordinate $q_k(t)$ and some boundary conditions (initial conditions are sufficient, for example), how does the system behave as a function of time?
The tools we use to solve this problem are:
the Lagrangian
$$
L(q_k(t), \dot{q}_k(t)) = T - V
$$
and the action
$$
S = \int_{t_1}^{t_2} dt L(q_k(t), \dot{q}_k(t)).
$$
Hamilton's principle of stationary action states that the classical path is the one at which the action is stationary.
This gives the Euler-Lagrange equation:
$$
\frac{d}{dt}\frac{\partial L}{\partial \dot{q}_k} - \frac{\partial L}{\partial q_k} = 0,
$$
where we define $p_k=\frac{\partial L}{\partial \dot{q}_k}$ as the canonical conjugate momentum.
With this definition, we can construct the Hamiltonian:
$$
H = \sum_{k} p_k \dot{q}_k - L.
$$
With all of this, getting the equations of motion of the system is a matter of constructing the correct Lagrangian and then solving the Euler-Lagrange equation.

### Electrodynamics (the covariant formulation)

The key steps to the covariant formulation of electrodynamics are:
constructing the 4-potential
$$
A^{\mu} = (\Phi, \va{A})
$$
from the scalar and vector potentials (note: this a proper Lorentz vector),
defining the field strength tensor
$$
F^{\mu\nu}=\partial^{\mu}A^{\nu}-\partial^{\nu}A^{\mu},
$$
and defining the 4-vector current
$$
j^{\mu}=(\rho, \va{j}).
$$
For the field strength tensor, it is easy to show that $F^{0i}=-E^{i}$ and $F^{ij}=-\epsilon^{ijk}B^{k}$.
The resulting form of Maxwell's equations is
$$
\partial_{\mu}F^{\mu\nu}=j^{\nu},
$$
$$
\partial_{\mu}\widetilde{F}^{\mu\nu}=0,
$$
with $\widetilde{F}^{\mu\nu}=\epsilon^{\mu\nu\rho\sigma}F_{\rho\sigma}$ being the dual field strength tensor.
At this point, we have a theory that is easy to transform via Lorentz transformations, and solutions can be arrived at through the straight-forward application of Maxwell's equations.

### Non-relativistic quantum mechanics

# The Klein-Gordon field

This chapter will introduce the key concepts for the development of quantum field theories through the example of the Klein-Gordon field.
We start with a quick review of classical continuum mechanics, classical field theory, and classical conservation laws.
These are important because at the very least, we expect expectation values of observable quantities to match classical values.
Conservation laws and symmetries also play a critical role in quantum field theories.
Then, we work through the consistent quantization of a relativistic field theory in the case of the "simple" Klein-Gordon field.

## Continuum mechanics in 1+1 dimensions

## Classical theory of relativistic scalar fields

### Lagrangian formalism

### Hamiltonian formalism

### Noether's theorem

Noether's theorem connects conserved quantities in a theory with the symmetries of the theory.
As symmetries play an essential role in quantum field theories, we will review this here.

Consider an infinitesimal transformation of a field,

$$
\phi(x) \rightarrow \phi'(x) = \phi(x) + \alpha \Delta \phi(x),
$$

where $\alpha$ is an infinitesimal Lagrange multiplier and $\Delta \phi(x)$ is some deformation of the field in some space-time volume $\Omega$.
This means that we have some surface $\partial \Omega$ such that $\Delta \phi(x)$ for every $x$ on or outside the surface.

The Lagrangian changes as a result of this transformation like

$$
\mathcal{L} \rightarrow \mathcal{L}' = \mathcal{L} + \alpha \Delta \mathcal{L}.
$$

For an infinitesimal $\alpha$, we get:

$$
\alpha \Delta \mathcal{L} = \frac{\partial \mathcal{L}}{\partial \phi} (\alpha \Delta \phi) + \frac{\partial \mathcal{L}}{\partial (\partial_{\mu}\phi)} \partial_{\mu}(\alpha \Delta \phi).
$$

Via integration by parts, we see that:

$$
\alpha \frac{\partial \mathcal{L}}{\partial (\partial_{\mu}\phi)} \partial_{\mu}(\Delta \phi) = \alpha \partial_{\mu} \left(\frac{\partial \mathcal{L}}{\partial (\partial_{\mu}\phi)} \Delta \phi \right) - \alpha \partial_{\mu} \left(\frac{\partial \mathcal{L}}{\partial (\partial_{\mu}\phi)}\right) \Delta \phi.
$$

Plugging this in and rearranging things, we get:

\begin{align*}
  \alpha \Delta \mathcal{L} &= \alpha \partial_{\mu} \left(\frac{\partial \mathcal{L}}{\partial (\partial_{\mu}\phi)} \Delta \phi \right) + \alpha {\underbrace{\textstyle \left[\frac{\partial \mathcal{L}}{\partial \phi} - \partial_{\mu}\left(\frac{\partial \mathcal{L}}{\partial (\partial_{\mu}\phi)}\right)\right]}_{\mathclap{= 0 \text{ by Euler-Lagrange equation}}}} \Delta \phi, \\
  &= \alpha \partial_{\mu} \left(\frac{\partial \mathcal{L}}{\partial (\partial_{\mu}\phi)} \Delta \phi \right).
\end{align*}

At this point, we define that a symmetry transformation is any transformation of the fields and the Lagrangian that leaves the resulting equations of motion unchanged.
One general class of transformations for which this is the case is

$$
\mathcal{L} \rightarrow \mathcal{L}' = \mathcal{L} + \alpha \partial_{\mu} J^{\mu}
$$

for any vector field $J^{\mu}$.
This is because this changes the action by a $\phi$-independent term,

$$
S \rightarrow S' = S + \text{surface integral over $\partial \Omega$},
$$

leaving the equations of motion unchanged.

Thus, for a symmetry transformation,

$$
\alpha \partial_{\mu} \left(\frac{\partial \mathcal{L}}{\partial (\partial_{\mu}\phi)} \Delta \phi \right) = \alpha \partial_{\mu} J^{\mu},
$$

giving us a conserved current ($\partial_{\mu} j^{\mu}(x) = 0$):

$$
j^{\mu} \coloneqq \frac{\partial \mathcal{L}}{\partial (\partial_{\mu}\phi)} \Delta \phi - J^{\mu}.
$$

With this, we've arrived at the central statement of Noether's theorem:
**every continuous symmetry is related to a conserved current**.

**TODO Examples**

## Quantization of the Klein-Gordon field

In developing the quantization approach for our classical scalar field theory,
we want to lean on our intuition from the quantization of classical point mechanics.
To go from classical mechanics to quantum mechanics,
we promote our generalized momenta and their conjugate momenta to operators which in general no longer commute.
Specifically, in the Schoedinger picture (or the Heisenberg picture at a fixed time),
we demand that the following relations hold:

\begin{align*}
  [q_m, p_n] &= i \delta_{mn}, \\
  [q_m, q_n] &= [p_m, p_n] = 0.
\end{align*}

We can take an analogous approach to quantizing our fields, by demanding:

\begin{align*}
  [\phi(\vec{x}), \pi(\vec{x}'] &= i \delta^{(3)}(\vec{x} - \vec{x}'), \\
  [\phi(\vec{x}), \phi(\vec{x}')] &= [\pi(\vec{x}), \pi(\vec{x}')] = 0.
\end{align*}

This means $\phi$ and $\pi$ are no longer fields, but operators,
which has the consequence that $\mathcal{H}$ and $H$ are also operators now.

As a first glimpse into what the greater consequences of this step are,
let us consider the energy spectrum of $H$.
To do this, we will look at the theory in momentum space.
For the classical theory, the momentum-space fields are related to the coordinate-space ones via Fourier transform:

$$
\phi(t, \vec{x}) = \int \frac{d^3p}{(2 \pi)^3} \phi(t, \vec{p}) e^{i \vec{p} \cdot \vec{x}}.
$$

**TODO Decide on convention or disclaimer for Fourier transformed functions**

The Klein-Gordon equation in coordinate space,

$$
\left(\frac{\partial^2}{\partial t^2} - \va{\nabla}^2 + m^2 \right)\phi(t, \vec{x}) = 0,
$$
in momentum space is given by:

$$
\left(\frac{\partial^2}{\partial t^2} + \vec{p}^2 + m^2 \right)\phi(t, \vec{p}) = 0.
$$

By comparing to the harmonic oscillator,

$$
\ddot{q}(t) + \omega^2 q(t) = 0,
$$

we can quickly connect the momentum-space Klein-Gordon equation to the harmonic oscillator via:

$$
\vec{p}^2 + m^2 \leftrightarrow \omega^2.
$$

This gives us the obvious interpretation that every Fourier mode of the Klein-Gordon field corresponds to a harmonic oscillator with frequency:

$$
\omega_{\vec{p}} \coloneqq \sqrt{\vec{p}^2 + m}.
$$

## Klein-Gordon field in the Heisenberg picture

Review

## Causality

## The Klein-Gordon propagator

Review

# The Dirac field

## Historical approach to the Dirac equation

## A modern approach to the Dirac equation: Lorentz transformations and spin

### Lorentz-invariant field equations

Review

### Representations of the rotational group

### Representations of the Lorentz group

Review

### Spinor transformations and the form-invariance of the Dirac equation

## Solutions of the free Dirac equation

## Lagrangian and Hamiltonian of the Dirac field

## Quantization of the Dirac field

## The Dirac propagator

## Discrete symmetries

# The electromagnetic field

## Classical electrodynamics (the covariant treatment)

## Quantization of the electromagnetic field

## The photon propagator

# Interacting fields and Feynman diagrams

## Interactions in quantum field theory

## Perturbative expansion of correlation functions

## Wick's theorem

## Feynman diagrams

## Crosssections and the S-matrix

## Computing S-matrix matrix elements

## Feynman rules for quantum electrodynamics

# Elementary QED processes

## Electron-muon scattering and $e^+e^-\rightarrow \mu^+ \mu^-$

## Compton scattering

Probably not relevant
