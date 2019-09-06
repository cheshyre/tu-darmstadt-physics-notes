---
title: Theoretical Nuclear Physics
subtitle: Collected notes for the course Theoretische Kernphysik as taught by A. Schwenk in the winter semester 2018/2019
numbersections: true
titlepage: true
toc-own-page: true
---

# Scope and guiding principles

## Scope

- focus on low-energy nuclear physics
- interested in properties and interactions of nuclei and nuclear matter
  - for nuclei:
    - ground state and low-lying ($< 50$ MeV) excited states
  - for nuclear matter:
    - equation of state at low densities (low temperature)
- spans the subfields nuclear structure, nuclear reactions, and nuclear astrophysics
- involves all four forces
  - for this reason, nuclei are an effective lab for the search for new physics

## Guiding principles

### Focus on modern developments and new perspectives

- from effective theories to many-body physics
- modern approaches unite (following) guiding principles for a more systematic
and predictive description of nuclear systems

### Resolution
- key idea: fine details at short distances are not important for reproduction of
long-distance features
- low energies correspond to low momenta
$$
E = \frac{p^2}{2m}
$$
- by Compton wavelength, low momenta correspond to long wavelengths (long distances)
$$
p = \frac{h}{\lambda}
$$
- at low energies, we have limited resolution
  - details at short distances (much smaller than $\lambda$) are not resolved
- we will leverage this to build systematic effective theories valid at low energies

### Effective theories

**Example: multipole expansion in electrostatics**

What is the electric potential $\Phi$ of a localized charge distribution at long distances?

### Uncertainty quantification

### Macroscopic description of nuclei *ab initio*

### Connect to underlying theory, quantum chromodynamics

# Introduction to nuclei and the strong interaction

## Nuclei

$m_N = 940\:\text{MeV/c}^\text{2}$

Deuteron properties:

* BE ~ $2.2\:\text{MeV}$
* radius ~ $2\:\text{fm}$

**fine-tuning!**

Natural scales:

* BE ~ $\frac{p^2}{m_N}=\frac{m_{\pi}^2 c^2}{m_N}=19\:\text{MeV}$
* radius ~ range of nuclear interaction ~ $\frac{1}{m_{\pi}}=1.4\:\text{fm}$

Typical nuclei:

* BE ~ $8\:\text{MeV}$ per nucleon
* radius ~ $r_0 A^{1/3}$ with $r_0 \sim 1.3\:\text{fm}$

Model (semi-empirical mass formula):

$$
\frac{BE}{A} = a_V + \frac{a_0}{A^{1/3}} + \frac{3 e^2 Z^2}{5 r_0 A^{4/3}} + \left(a_s + a_{0s} A^{1/3}\right)\left(\frac{N-Z}{A}\right)^2 + \text{...}
$$

## Nuclear matter

$A \rightarrow \infty$

$V \sim R^3 \sim A \rightarrow \infty$

$n=\frac{A}{V}=\text{constant}$

No Coulomb or surface

Symmetric nuclear matter (SNM):

## Nuclear landscape

# Nuclear forces: scattering and bound states

$$
\hat{H} = \hat{T} + \hat{V}_{NN} = \hat{T}_{COM} + \hat{T}_{rel} + \hat{V}_{NN}
$$

Disregard center-of-mass component from now on
(consider everything in the center-of-mass rest frame).

## Basic scattering

Scatter in with momentum $\vec{k}$, scatter out at angle $\theta$ with momentum $\vec{k}'$.

Convention:

\begin{align*}
\bra{\vec{r}}\ket{\vec{k}} &= e^{i \vec{k}\cdot \vec{r}} \\
\bra{\vec{r}}\ket{\vec{r}'} &= \delta^{(3)}(\vec{r} - \vec{r}') \\
\bra{\vec{k}}\ket{\vec{k}'} &= (2\pi)^3 \delta^{(3)}(\vec{k} - \vec{k}')
\end{align*}

### Lippmann-Schwinger equation

Ansatz for Schroedinger equation solution:

\begin{align*}
\ket{\psi} & = \ket{\phi} + \hat{X} \hat{V} \ket{\phi} \\
\left(\hat{H}_0 + \hat{V}\right)\ket{\psi} & = \hat{H}_0 \ket{\phi} + \hat{V} \ket{\phi} + \left(\hat{H}_0 + \hat{V}\right)\hat{X} \hat{V} \ket{\phi} \\
E \ket{\psi} & = E \ket{\phi} + \hat{V}\ket{\phi} + ??
\end{align*}

$$
\ket{\psi^{(\pm)}} = \ket{\phi} + \frac{1}{E - H_0 \pm i \epsilon} V \ket{\psi^{(\pm)}}
$$

### Green's function

Associate $-$ solution with unphysical incoming spherical wave via
projection onto coordinate space and solving for the Green's function:

$$
\frac{1}{2\mu} \mel{\vec{r}}{\frac{1}{E - H_0 \pm i \epsilon}}{\vec{r}'} = G_{\pm}(\vec{r}, \vec{r}')
$$

### Scattering amplitude and T-matrix

$$
f(\vec{k}', \vec{k}) = - \frac{\mu}{2\pi} \mel{\vec{k}'}{V}{\psi^{(+)}}
$$

$$
\mel{\vec{k}'}{T\left(E=\frac{\vec{k}^2}{2\mu}\right)}{\vec{k}} = - \frac{2\pi}{\mu} f(\vec{k},\vec{k}')
$$

where the equation above is on-shell.

LS-equations:

$$
\ket{\psi^{(+)}} = \ket{\phi} + G_{+}(E) V \ket{\psi^{(+)}}
$$

\begin{align*}
\mel{\vec{k}'}{V}{\psi^{(+)}} &= \mel{\vec{k}'}{V}{\phi} + \int \frac{d^3q}{(2\pi)^3}
\mel{\vec{k}'}{V}{\vec{q}}\mel{\vec{q}}{G_{+}(E)V}{\psi^{(+)}} \\
\mel{\vec{k}'}{T(E)}{\vec{k}} &= \mel{\vec{k}'}{V}{\vec{k}} + \int \frac{d^3q}{(2\pi)^3}
\frac{\mel{\vec{k}'}{V}{\vec{q}}\mel{\vec{q}}{T(E)}{\vec{k}}}{E - \frac{q^2}{2\mu} + i \epsilon}
\end{align*}

$$
T(E) = V + V G_{+}(E) T(E)
$$

### Differential cross section

Differential cross section:

$$
\vec{j} = \frac{1}{2i\mu}(\psi*\vec{\nabla}\psi - \psi\vec{\nabla}\psi*)
$$

$$
d\sigma = \frac{\abs{\vec{j}_{scattered}} dA}{\abs{\vec{j}_{in}}} = \abs{f}^2 d\Omega
$$

### Born approximation

Recall Born approximation.



### Partial wave expansion

Partial wave expansion:

$$
\bra{\vec{r}}\ket{\psi^{(+)}} \rightarrow \sum_{l=0}^{\infty}(2l+1)P_l\left(cos(\theta)\right)
\frac{1}{2ikr}
\left((-1)^{l+1}e^{-ikr} + \left(1 + 2ik f_l(k)\right)e^{ikr}\right)\:(r\rightarrow\infty)
$$

Note the S-matrix $S_l(k) = 1 + 2ikf_l(k)$ above.

### S-matrix properties



Due to conservation of probability (elastic scattering), $\abs{S}^2 = 1$.

S-matrix for complex $k$ shows poles on imaginary axis which are bound states.

### Phase shifts

Phase shifts:

$$
S_l(k) = e^{2i\delta_l(k)}
$$

Recall Levinson's theorem.

$$
f_l(k) = \frac{S_l(k) - 1}{2ik} = \frac{e^{i\delta_l(k)}sin(\delta_l(k))}{k} = \frac{1}{k cot(\delta_l(k)) - ik}
$$

$$
\bra{\vec{r}}\ket{\psi^{(+)}} \rightarrow \sum_{l=0}^{\infty}(2l+1)P_l\left(cos(\theta)\right)
i^l e^{i \delta_l(k)}
\frac{sin(kr - l\pi/2 + \delta_l(k))}{kr}
\:(r\rightarrow\infty)
$$

### Example: scattering off a hard sphere

### Effective range expansion


Effective range expansion:

$$
k^{2l + 1}cot(\delta_l(k)) = \sum_{n=0}^{\infty} c_{n,l} k^{2n}
$$

s-wave:

$$
k cot(\delta_l(k) = -\frac{1}{a} + \frac{1}{2} r_e k^2 - P r_{e}^{3}k^4 + ...
$$

### Scattering length properties

At low $k$:

$delta_l(k) = - a_l k^{2l + 1}$.

1. Weak potential: $\sigma_0(k) = 4\pi a^2$
2. Strong scattering at low $k$: $\sigma_0(k) = \frac{4\pi}{k^2}$

## Nucleon-nucleon scattering

### Partial-wave channels

Partial waves:

Have $L$, $S$, and $T$. Overall asymmetric is required.

Scattering length diagnostics:

For no bound state:

* positive $a$ is repulsive
* negative $a$ is attractive
* infinite negative $a$ is bound state at threshold

Deuteron:

* $3S1, a=5.4$
* $1S0, a=-23$




### Symmetries of nuclear forces

Symmetries of nuclear forces:

Before any constraints, we could have $V_{NN}(\vec{r}_1, \vec{r}_2, \vec{p}_1, \vec{p}_2, \vec{\sigma}_1, \vec{\sigma}_2, \vec{\tau}_1, \vec{\tau}_2)$.

Constraints:

1. Hermitian
2. Invariant under particle exchange
3. Translational invariance in space (relative in $\vec{r}$)
4. Translational invariance in time (time indep)
5. Rotational invariance in space and spin ($[\vec{J}, V]=0$)
6. Galilean invariance (relative in $\vec{p}$)
7. Invariant under parity
8. Invariant under time reversal
9. Baryon number and lepton number
10. Isospin charge symmetry and isospin charge independence

The first two are general constraints. 3-6 are continuous symmetries.
7 and 8 are discrete symmetries, but good symmetries of the strong interaction.
9 is a global symmetry (so far unbroken). 10 is a good approximate symmetry.

#### Breaking of approximate symmetries

With respect to 10, isospin charge symmetry exchanges $p$ and $n$ (rotation by $\pi$ in isospin space).
This is a good symmetry and we can estimate spectra of mirror nuclei with it.
For this a Coulomb shift is necessary.
Broken by strong isospin breaking (quark masses) and because protons are charged (EM effects).
Also, Thomas-Ehrman effect disrupts mirror symmetry when there are nearby open channels.
Charge independence is general rotational invariance in isospin space.
This is broken more strongly because $T=1$ $np$ scattering length ($-23.7$)
is larger than $nn$ or $pp$ ($-18$).

#### Accidental symmetries

We have an additional accidental $SU(4)$ symmetry with isospin and spin.
This is broken by spin-orbit effects.

### General operator structure of $V_{NN}$

So now we have $V_{NN}(\vec{r}, \vec{p}, \vec{\sigma}_1, \vec{\sigma}_2, \vec{\tau}_1, \vec{\tau}_2)$
and the following additional requirements:

* rotational invariance in space and spin demands that spatial and spin vectors be combined into scalars
* isospin charge indep requires isospin vectors to be combined into scalars.

\begin{align*}
V_{NN} & = V_1(\vec{r}, \vec{p}) + V_{\sigma}(\vec{r}, \vec{p})\vec{\sigma}_1 \cdot \vec{\sigma}_2 + V_{\tau}(\vec{r}, \vec{p}) \vec{\tau}_1 \cdot \vec{\tau}_2 + V_{\sigma\tau}(\vec{r}, \vec{p}) \vec{\sigma}_1 \cdot \vec{\sigma}_2 \vec{\tau}_1 \cdot \vec{\tau}_2 \\
& + V_{ls}(\vec{r}, \vec{p}) \vec{l} \cdot \vec{S} + V_{lst}(\vec{r}, \vec{p}) \vec{l} \cdot \vec{S} \vec{\tau}_1 \cdot \vec{\tau}_2 \\
& + V_T(\vec{r}, \vec{p}) S_{12}(\hat{\vec{r}}) + V_{T,\tau}(\vec{r}, \vec{p}) S_{12}(\hat{\vec{r}}) \vec{\tau}_1 \cdot \vec{\tau}_2
\end{align*}

If $V_i$ just depends on $\abs{\vec{r}}$, then they are linear in $\vec{p}$.
This is the Argonne V8 potential.
Considering terms with $p^2$ in $L^2$, $(l\cdot S)^2$, and $p^2$ gives AV18.

### Momentum-space properties

Rules for allowed transformations in momentum space:



# Effective theories at low energies

We want to restrict ourselves now to scattering in the low-energy regime.
This means we have a small momentum scale, $Q=\left\{\abs{\vec{k}},\abs{\vec{k}'}\right\}$,
which corresponds to long wavelengths in terms of what is probed during scattering.
This means we cannot resolve short-distance details: $\lambda >> R \sim \frac{1}{\Lambda_b}$.
This $\Lambda_b$ is the breakdown scale for our to-be-constructed effective theory,
and it signals where details for short-distance physics become relevant.
The theory we will discuss includes no meson exchange,
so we will see that the breakdown scale should be given by the mass of the lightest exchanged meson, the pion.

With this, we have declared our separation of scales,
$Q$ as the low-momentum scale and $\Lambda_b$ as the high-momentum scale.
We have made explicit our desire to work at low energies
and can now use the limited resolution to construct an expansion in $\frac{Q}{\Lambda_b}$.

## Spin- and isospin-independent contact interaction expansion

Focusing on spin- and isospin-less potential terms we find:

$$
V_{\text{ET}}(\vec{k}', \vec{k}) = c_0 + c_2 (\vec{k}^2 + \vec{k}'^2) + c_2' \vec{k} \cdot \vec{k}' + ...
$$

Here, $c_0$, $c_2$, and $c_2'$ are free parameters of our theory that we need to fit to data,
the so-called low-energy constants (LECs).
Furthermore, the number in the subscript indicates the power of $Q/\Lambda_b$ in the term,
which is also the order in the expansion.

Questions:

* Why are 1st order terms not allowed?
* What about $(k + k')^2$?
* What partial waves do these interactions contribute in?

We need to define observables to determine the values of each of these LECs:
s-wave scattering length and effective range, p-wave scattering volume.


Note also we have currently absorbed the breakdown scale into the coefficients,
but we should keep in mind that it is there and our momenta should not get too large.

## Solving the Lippmann-Schwinger equation

Recall diagramatic representation of T-matrix and LS-equation (bubble diagrams).

## Lippmann-Schwinger equation for leading-order contact interaction

Consider for now only the first term in our effective theory:
the $c_0$ contact term.
It is called a contact because if we transform it back to coordinate space we just get a delta function.

We now want to solve the LS-equation for this leading-order potential:

$$
T^{+}(E) = c_0 \frac{1}{1 - c_0 I(E)}
$$

where:

$$
I(E) = \int \frac{d^3q}{(2\pi)^3} \frac{1}{E - \frac{q^2}{2\mu} + i\epsilon}.
$$

We can also verify that the previous result is a proper solution to the LS-equation.

### Observed divergences

Now we want to evaluate this integral, but it is divergent (by dimensional analysis).
In fact only in 1-dimensional integrals are delta function potentials well-behaved.
In 2D, the integral is logarithmically divergent.
In 3D, it is linearly divergent.

### Regularization and renormalization

The solution here is to regularize the integral (introduce cutoff $\Lambda$)
and renormalize coefficients in theory to correct for cutoff dependence.

To compute the integral $I(E)$ with a cutoff, the following identity will prove useful:

$$
\frac{1}{z - z_0 \pm i\epsilon} = P\frac{1}{z-z_0} \mp i \pi \delta(z - z_0)
$$

using the principal value integral.
Further, in the principal value integral, setting $k=0$ as a low-energy approximation proves useful.

We arrive at:

$$
I(E) = \frac{m}{4\pi}\left(-\frac{2}{\pi}\Lambda - ik\right)
$$

### T-matrix matching and artifacts

We can now plug this back into the expression for the T-matrix we arrived at
and compare this to the T-matrix with the effective range expansion.

$$
c_0(\Lambda) = \frac{4\pi}{m}\frac{1}{\frac{1}{a_s} - \frac{2}{\pi}\Lambda}
$$

We see that the contact is uniquely determined by the scattering length and the renormalization scale and scheme.
We also see that there is a residual effective range artifact due to our cutoff.

### General regularization principles

Consider the following points:

1. Cutoff dependence in coefficients implies many potentials give same results
2. For small $a_s$, $\Lambda a_s << 1$ so $c_0=\frac{4\pi a_s}{m}\left(1 + \frac{2}{\pi}\Lambda a_s\right)$
3. For large $a_s$, $c_0=-\frac{2\pi^2}{m\Lambda}$, a fine-tuned contact.
4. Transforming potential to coordinate space, we remove high momentum nodes so delta function is smeared out.
5. We can estimate uncertainty based on left-out terms $\text{max}\left(\frac{Q^2}{\Lambda_b^2},\frac{Q^2}{\Lambda \Lambda_b},\frac{Q^2}{\Lambda^2}\right)$

Exercise: show that for small $a_s$ at the 2nd term in the Born series the T-matrix is independent of $\Lambda$.

### Non-perturbative renormalization

We can also show that this is true for the strong coupling (large $a_s$) limit,
where we need to approach it differently because the Born series does not fall off.
We use the requirement:

$$
\frac{d}{d\Lambda}T^{+} = 0,
$$

which will given us a renormalization group equation for coupling.

## Nuclear force properties from phase shifts

We now want to look at certain phase shifts and few-body properties to deduce properties of certain potential terms.
We will use the 3P2 phase shift to extract the sign of the spin-orbit potential term
and see that this is consistent with the other 3PJ phase shifts, but incomplete.
We will then look at the deuteron magnetic moment and electric quadrupole moment to learn about coupled channels and the sign of the tensor force.

### Spin-orbit from P-wave phase shifts

We see from the 3PJ phase shifts that:

* 3P0 is attractive at low E and repulsive at high E
* 3P1 is repulsive
* 3P2 is attractive

But the central must be the same for all 3, so we look to spin-orbit for splitting.

$$
\ev{l\cdot s} = \frac{J^2 - L^2 - S^2}{2}
$$

This gives $-2$ for 3P0, $-1$ for 3P1, $1$ for 3P2.
So from 3P2 we see that the spin-orbit force must be attractive to overcome the weakly repulsive central force.
Our prediction that 3P1 and 3P0 should see a net repulsive contribution (due to the minus sign) is also validated,
but we see that for 3P0 this is incomplete because we need a long-range attractive part.

### Tensor force from deuteron properties

The quantum numbers of the deuteron are $1^{+}$ (consider this determined by experiment).
Now let us consider the dipole magnetic moment of the deuteron.
This is (in general):

$$
\mu_d = \mu_N ( g_p S_p + g_n S_n) + \mu_N l_p
$$

Experiment measured a value of $0.8574 \mu_N$.
If we assume deuteron lives only in the lowest valid partial wave (3S1), we get:

$$
\mu_d = \mu_N / 2 (g_p + g_n) = 0.8796 \mu_N.
$$

Here $g_p = 5.5855$ and $g_n=-3.8263$.
This difference to experiment is small, but it can be explained by
non-S-wave components in the deuteron wavefunction
and meson-exchange currents.
The only suspect for the mixed-in channel is 3D1
since all other channels are prohibited by either
parity conservation of the nuclear force or
spin angular momentum coupling.
We find that:

$$
\mu_d(3D1) = \frac{\mu_N}{4}\left(3 - (g_p + g_n)\right)=0.3102\mu_N
$$

So we can postulate that we must treat 3S1 and 3D1 as a coupled channel.

We will now seek to describe the deuteron as having s- and d-wave components.

$$
\ket{\psi_{d,M}} = \sum_{l=0,2} c_l \ket{\phi_l}\ket{(l,S=1)J,M}\ket{T=0,M_T=0}
$$

where $\phi_l$ are the radial wavefunctions.
We will consider a Hamiltonian with relative kinetic energy
and isospin-independent central, spin-orbit, and tensor terms
(central is also spin-independent).
Given the Schroedinger equation for this system,
we want to isolate single partial waves.
We define:

$$
\bra{r}\ket{\phi_0}=\frac{u(r)}{r}
$$

$$
\bra{r}\ket{\phi_2}=\frac{w(r)}{r}
$$

and project the Schroedinger equation on each partial wave.
We need the matrix elements of $l\cdot s$ and $S_{12}$ for this:

$$
\begin{array}{c|cc}
l\cdot s & 3S1 & 3D1 \\
\hline
3S1 & 0 & 0 \\
3D1 & 0 & -3
\end{array}
$$

$$
\begin{array}{c|cc}
S_{12} & 3S1 & 3D1 \\
\hline
3S1 & 0 & \sqrt{8}/3 \\
3D1 & \sqrt{8}/3 & -2/3
\end{array}
$$

We arrive at the Rarita-Schwinger equations for the 3S1 and then 3D1 waves of the deuteron:

$$
\left(-\frac{1}{2\mu}\frac{\partial^2}{\partial r^2} + V_c(r) - E_d\right)u(r) = -\frac{\sqrt{8}}{3}V_T(r)w(r)
$$

$$
\left(-\frac{1}{2\mu}\left(\frac{\partial^2}{\partial r^2} - \frac{l(l+1)}{r^2}\right) + V_c(r) -3V_{ls}(r) - E_d - \frac{2}{3}V_T(r)\right)w(r) = -\frac{\sqrt{8}}{3}V_T(r)u(r)
$$

Important to note: tensor force is only reason for coupling.

Now we move on to consider the electric quadrupole moment of the deuteron
in order to learn something about the tensor force.
The reason for this is that the quadrupole operator $Q$ is

$$
Q=3z^2 - r^2 = r^2(3 cos^2(\theta) - 1)
$$

where we note that for spherical systems $\ev{r^2}=3\ev{z^2}$.
So the quadrupole moment of the deuteron is sensitive to d-wave contributions to the wavefunction,
which are the result of the tensor force.
The measured value of the electric quadrupole moment of the deuteron is
$Q_d = 0.2859\:\text{e fm}^2$.
This is larger than 0, meaning $\ev{z^2}>\ev{(x,y)^2}$,
so the nucleus is prolate deformed (football).
We want to predict what the sign for the tensor force is, so we need to know how it behaves.
Basically, the tensor force is attractive for same spin if they are stacked on top of each other,
and it is attractive for opposite spin if they are placed next to each other.

The electric quadrupole moment is defined from theory as:

$$
Q_d = \ev{e Q}{\psi_d, M=J},
$$

or, stated intuitively, the expectation value of the quadrupole operator in the state with maximal angular momentum projection.
Maximum $M$ means spins must be aligned,
so the tensor force overall must be attractive in this channel.

We will now look at $V_T(r)S_{12}$.
We want to determine the sign of $V_T$,
and to do this we will calculate the spin-space matrix elements of $S_{12}$.

$$
\ev{S_{12}}{S=1,M_S=\pm1} = cos^2(\theta) - \frac{1}{3}
$$

$$
\ev{S_{12}}{S=1,M_S=0} = \frac{2}{3} - 2 cos^2(\theta)
$$

Important properties of $S_{12}$ are it is traceless and has $\ev{S_{12}}{0,0}=0$.
We read off now that $cos^2(\theta)$ is maximal at $\theta=0,\pi$,
and since $M=J$ implies $M_S=1$, we know $\ev{S_{12}}$ is maximal ($2/3$).
This means $V_T<0$ to have net attractive tensor force for deuteron.
Specifically, the tensor force at long ranges is attractive in $T=0$.

## More advanced topics in nuclear forces

### Coupled-channel scattering

We observed previously that channels can get coupled by certain parts of the nuclear force,
which forces us solve the Schroedinger equation for them together.
This naturally also extends to the LS equation and the S-matrix.
In two-body scattering, we can have at worst two channels coupled,
since the nuclear force preserves parity
and with maximal total spin $1$, we can only couple up or down 1 unit.
We can write the S-matrix in the coupled channel as:

$$
S = I_2 + 2ik f_{l,l'}
$$

Once again, the S-matrix is unitary,
so we can parametrize this in terms of single channel phase shifts and mixing angles.

$$
S = \begin{pmatrix}
e^{2i\delta_l}cos(2\epsilon_J) & i e^{i(\delta_l + \delta_{l'})}sin(2\epsilon_J) \\
i e^{i(\delta_l + \delta_{l'})}sin(2\epsilon_J) & e^{2i\delta_{l'}}cos(2\epsilon_J)
\end{pmatrix}
$$

Here $J=(l + l')/2$ and $\epsilon_J$ is the mixing angle for the coupled channels.
For example, the 3S1 3D1 channel has a mixing angle of less than 5 degrees.

### One-pion-exchange interaction

It was previously mentioned that the nuclear interaction is mediated primarily by pions,
which set the range of the interaction.
In fact, our qualitative understanding is that at long and intermediate ranges
one-pion and two-pion exchange form the primary attractive and repulsive components of the nuclear force.
Our previous effective theory was developed with only nucleons and no pions,
and as a result was only valid at best up to momenta equal to the pion mass.
For normal nuclei, we know that typical momenta are closer to the Fermi momentum,
that is $\sim270\:MeV/c$.
Thus, for the construction of an effective theory valid for most nuclei,
we need to include pions explicitly and shift our breakdown scale up in energy.

So what does this one-pion exchange look like? Well:

\begin{align*}
V(k', k) &= 2 \sum_j - \frac{1}{\omega_q}\left(-i\frac{g_A}{2 f\pi} \sigma_1 \cdot q \tau_1^j \frac{1}{\sqrt{2\omega_q}}\right) \left(-i\frac{g_A}{2 f\pi} \sigma_2 \cdot q \tau_2^j \frac{1}{\sqrt{2\omega_q}}\right) \\
& = - \left(\frac{g_A}{2 f\pi}\right)^2 \frac{\sigma_1 \cdot q \sigma_2 \cdot q \tau_1\cdot\tau_2}{q^2 + m_{\pi}^2}
\end{align*}

The overall factor of 2 is for 2 processes that contribute identically,
pion exchanged in one direction and pion exchanged in the opposite direction.
The sum is over isospin projections of the exchanged pion.

# Many-body basics

When working with many-body systems, we span the $A$-body Hilbert space with product states of single-particle states (plane waves, HO states).
Following the spin-statistics theorem, these should have appropriate symmetry.

## Many-body states and symmetrization

For fermions:

$$
\ket{x_1,x_2,...,x_A}_a = \frac{1}{\sqrt{A!}}\sum_{permutations P} sign(P) \ket{x_{P(1)}}...\ket{x_{P(A)}}
$$

This is a Slater determinant, because it can be seen as the determinant of a square matrix where particle label and quantum number label are varied across the two axes.
This notation is inconvenient.

## Second quantization

We go from the Hilbert space to the Fock space which is the sum over all Hilbert spaces.
In the 0th Hilbert space, we have the vacuum with 0 nucleons.

### Creation and annihilation operators

Creation operator:

$$
a_{x}^{\dagger}\ket{0} = \ket{x}
$$

Recall other standard properties.

These creation operators automatically create states with appropriate symmetry.

Also have annihilation operator: $a_x$.
This anticommutes with creation operator if $x=x'$.

### Basis transformations

New single particle basis $\ket{x'}$.

$$
\ket{x'} = \sum_x \ket{x}\bra{x}\ket{x'} = \sum_x a_{x}^{\dagger} \bra{x}\ket{x'}
$$

\begin{align*}
a_{x'}^{\dagger} &= \sum_x a_{x}^{\dagger} \bra{x}\ket{x'} \\
a_{x'} &= \sum_x a_{x} \bra{x}\ket{x'}^*
\end{align*}

### Representation of operators

One-body operator:

$$
O = \sum_{x,x'}\mel{x}{O}{x'}a_{x}^{\dagger} a_{x'}
$$

Two-body operator (take note of ordering):

$$
O_2 = \frac{1}{(2!)^2}\sum_{x_1,x_2,x_1',x_2'} anti\mel{x_1,x_2}{O_2}{x_1',x_2'}a_{x_1}^{\dagger} a_{x_2}^{\dagger} a_{x_2'} a_{x_1'}
$$

Three-body operator:

$$
O_3 = \frac{1}{(3!)^2}\sum_{x_1,x_2,x_3,x_1',x_2',x_3'} anti\mel{x_1,x_2,x_3}{O_3}{x_1',x_2',x_3'}a_{x_1}^{\dagger} a_{x_2}^{\dagger} a_{x_3}^{\dagger} a_{x_3'} a_{x_2'} a_{x_1'}
$$

For two- and three-body operators, the matrix elements are antisymmetrized.


### Examples of different operators

One-body:

* Occupation number
* Density operator
* Total number operator
* Kinetic energy

Two-body:

* 2-body potential
* 2-body density

Three-body:

* 3-body potential

## Basic many-body methods

### Variational principle

The solution of the Schroedinger equation is equivalent to finding stationary points of the energy functional

$$
E[\ket{\psi}] = \frac{\ev{H}{\psi}}{\bra{\psi}\ket{\psi}}
$$

under variation of $\ket{\psi}$ over all possible states.

$$
\delta E[\ket{\psi}] = E[\ket{\psi} + \ket{\delta \psi}] - E[\ket{\psi}] = 0
$$

for infinitesimally small variations.
This gives:

$$
\mel{\delta \psi}{H - E}{\psi} = 0
$$

See handwritten proof.

The Ritz variational principle says this functional has a global minimum at the ground state.
The proof involves expanding a trial state in eigenstates of the Hamiltonian and looking at the energy functional.

### Hartree-Fock equations

The Hartree-Fock approximation makes use of the variational principle in a restricted state space, namely the space of $A$-body Slater determinants.
We do this by considering:

1. A local 2-body potential
2. Forcing new single particle states to be normalized via Lagrange multipliers.
3. Employing the stationary condition:

$$
\delta E[\ket{\psi}] - \delta \left(\sum_{i=1}^A \epsilon_i \int d^3r \abs{\phi_i(\vec{r}}^2\right) = 0
$$

This gives:

$$
(-1/2m \nabla^2)\phi_i(r) + \sum_{j=1}\int d^3r' \phi_j^*(r') V(r - r') \left(\phi_i(r)\phi_j(r') - \phi_i(r')\phi_j(r)\right) = E_i \phi_i(r)
$$

which can be rewritten as:

$$
-1/2m \nabla^2 \phi_i(r) + V_H[\rho](r)\phi_i(r) - \int d^3r' V_F[\rho](r, r') \phi_i(r') = E_i \phi_i(r)
$$

This is solved self-consistently.

### Fermi gas approximation

The Fermi gas approximation is the Hartree-Fock approximation for uniform matter (large $N$, $V$, constant density).
From this starting point, we can find corrections beyond Hartree-Fock via many-body perturbation theory, the so-called dilute gas expansion.

For uniform matter, plane wave states solve the HF equations.
So we define:

$$
\ket{\psi_{FG}} = \ket{\psi_{HF}} = \left( \prod_{\abs{k}\leq k_F}\prod_{m_s=+,-}a_{k,m_s}^{\dagger}\right)\ket{0}
$$

Note: here typically the total energy would just be the sum over the individual HF energies,
but $E_{HF}$ actually includes corrections from underlying interactions.

$$
E_{HF} = \ev{T + V}{\psi_{HF}}
$$

$$
E_{kin} = \ev{T}{\psi_{HF}} = N \frac{3}{5} \epsilon_{F}
$$

Now, we will compute the first-order (in $V$) correction to the energy due to the interaction.
Here we will use the leading-order contact from our effective theory discussion, $V=c_0(\Lambda)$.
I will typically just use $c_0$ for $c_0(\Lambda)$, but we work with the renormalized coefficient using the theta function regularization scheme.

$$
c_0(\Lambda) = \frac{4 \pi}{m} \frac{1}{\frac{1}{a} - \frac{2}{\pi}\Lambda}
$$

The first-order correction to the energy is:

$$
E_{int}^{(1)} = \ev{V}{\psi_{HF}} = \frac{1}{4V}\sum_{\abs{k_1}\leq k_F, m_{s1}}\sum_{\abs{k_2}\leq k_F,m_{s2}} c_0
$$

This follows from considering $V$ in second quantized form and doing all the contractions with the states.
At the end we find:

$$
\frac{E_{int}^{(1)}}{N} = \frac{1}{4} c_0 n
$$

Working in the weakly-interacting limit (small $a$), we arrive at:

$$
\frac{E_{HF}^{(1)}}{N} = \frac{k_F^2}{2m} \left(\frac{3}{5} + \frac{2}{3 \pi} k_F a (1 + \frac{2}{\pi}\Lambda a)\right)
$$

We will see that this residual cutoff dependence is cancelled by second-order corrections to the energy in the dilute gas expansion.

### Dilute gas expansion

We can write the full state as:

$$
\ket{\psi_{full}} = \ket{\psi_{FG}} + \sum_{1p1h}c_{1p1h}\ket{\psi_{1p1h}} + \sum_{2p2h}c_{2p2h}\ket{\psi_{2p2h}}
$$

Note here that 1 particle 1 hole excitations do not contribute to the ground state because the ground is at rest (no net total momentum), which is disturbed by a $1p1h$ excitation.
This means the first correction beyond Hartree-Fock comes from considering 2 particle 2 hole intermediate states in 2nd order perturbation theory.

**Fish diagram here**

We define incoming and outgoing states with momenta:

$$
p/2 \pm k
$$

where $p$ is total momentum and $k$ is relative momentum, and intermediate states with momenta:

$$
p/2 \pm q
$$

since our potential conserves center of mass momentum.

Second-order perturbation theory gives us:

$$
E_{int}^{(2)} = \frac{1}{4V} \sum_{k, p, m_{s1}, m_{s2}} \int_{0}^{\Lambda} \frac{d^3q}{(2\pi)^3} \frac{(1 - n_{p/2 + q})(1 - n_{p/2 - q})}{\epsilon_{p/2 + k} + \epsilon_{p/2 - k} - \epsilon_{p/2 + q} - \epsilon_{p/2 - q}} c_0^2 n_{p/2 - k} n_{p/2 + k}
$$

Here, the densities are Fermi-Dirac occupation numbers which at 0 temperature are just Heaviside step functions.
These also regulate our integration space so we do not need to worry about any poles from the denominator.
Using:

$$
(1 - n)(1 - n) - 1 + 1
$$

we can split the integral into a divergent part (the last $1$) and a part that is regulated by the densities (no cutoff dependence).
We find the contribution for the divergent part is:

\begin{align*}
E_{int,+1}^{(2)} & = \frac{1}{4V} c_0^2 n^2 \left(\frac{-m\Lambda}{2 \pi^2}\right)
& = \frac{n^2}{4V}\frac{4\pi a}{m}\frac{-2 \Lambda a}{\pi}
\end{align*}

which exactly cancels the cutoff dependence in the previous first-order interaction energy.
The remaining term gives us:

$$
\frac{E_{int}^{(2)}}{N} = \frac{k_F^2}{2m}\frac{4}{35 \pi^2}\left(11 - 2 ln(2)\right)(k_F a)^2
$$

# Many-body methods for strongly interacting systems

Right now, this only offers a brief overview of the concepts that go into modern many-body methods that go into strongly interacting systems.

## Many-body perturbation theory

What we did for the uniform weakly interacting gas can also be done for closed shell nuclei and be extended from there.

## Quantum Monte Carlo

Typical range: $A \leq 12$

1. Start from trial state (perhaps Hartree-Fock)
2. Evolve this state in imaginary time $\tau = i t$ using $e^{-H t}$
3. Project onto $A$-body coordinate state final state and insert complete set of coordinate states
4. Resulting $3A$-dimensional integral done via Monte Carlo integration
5. Large $\tau$ projects out ground state

## No-core shell model

Typical range: $A \leq 24$

This large-scale diagonalization of $H$ proceeds like:

1. Consider HO basis with Slater determinants up to $N_{max} \hbar \omega$ excitations
2. Construct $A$-body Hamiltonian from 2- and 3-body forces
3. Get lowest eigenstates and eigenvalues via Lanczos methods (take advantage of sparsity of Hamiltonian)

Primary difficulty: even if naive lowest-energy configuration is a filled shell, due to the combinatorics of constructing excited Slater determinants the basis grows factorially in $N_{max}$.
This situation grows even worse if you consider nuclei where there are degenerate lowest-energy configurations (partially filled shells).

Other useful properties: variational in $\hbar \omega$. Convergence pattern in $N_{max}$ allows extrapolation (usually exponential).

## Coupled-cluster method

Initial development in Bochum in 1960s, but failed due to extremely hard-core potentials available at the time.
Since then it was developed and used extremely successfully in quantum chemistry.

Typical range: closed shell $A$ and nearest neighbors via particle removal/attachment

Primary advantage: polynomial computational scaling with system size

Concept:

Ansatz for many-body state:

$$
e^{S}\ket{\psi_{ref}}
$$

where the reference state is is a closed shell Hartree-Fock ground state or naive $0\hbar\omega$ HO state.

$$
S = \sum_{i=occ,a=unocc}t_i^a a_a^{\dagger} a_i + \sum_{ij, ab}t_{ij}^{ab} a_{a}^{\dagger} a_{b}^{\dagger} a_i a_j
$$

Since these 1p1h 2p2h operators are in the exponential, they each generate up to ApAh excitations.
The amplitude $t_i^a$ etc are obtained by solving the coupled cluster equations.
The state of the art today is complete singles and doubles and partial inclusion of triples.

Features: Method is not variational.
There is a truncation that has to be made in the single-particle basis: $e_{max} = (2n + l)_{max}$.

## In-medium similarity renormalization group

Similar to coupled cluster in range and basic concept.

Evolve $H(s)$ via the SRG, decoupling reference state from 1p1h, 2p2h states.

$$
H(s) = U(s) H(0) U^{\dagger}(s)
$$

Also polynomial scaling but not variational.

## Shell model method

Basic concept: static core + valence space model space.

Need to find an $H_{eff}$ that acts only in model space, but gives approximately correct lowest eigenvalues when diagonalized.
