Supersymmetric Quantum Mechanics
========================================


For a quantum mechanical system, it is always possible to find a partener potential.

Suppose we have a Hamiltonian :math:`H_1` in quantum mechanics, which is defined as

.. math::
   H_1 = - \frac{\hbar}{2m}\partial_x^2 + V_1(x).

By decomposing it into

.. math::
   H_1 = A^\dagger A,

we can define the two operators

.. math::
   A = & \frac{\hbar}{\sqrt{2m}} \partial_x + W(x),\\
   A&\dagger = & -\frac{\hbar}{\sqrt{2m}}\partial_x + W(x).

The quantity :math:`W(x)` is so called superpotential. The partener Hamiltonian of :math:`H_1` is

.. math::
   H_2 = A A^\dagger,

using which one find the corresponding potential is

.. math::
   V_2(x) = W(x)^2 - \frac{\hbar}{\sqrt{2m}} \partial_x W(x).

The interesting part is that the superpotential is closely related to ground state wave functions of the orginal system

.. math::
   W(x) = -\frac{\hbar}{\sqrt{2m}} \frac{ \psi_0'(x) }{\psi_0(x)}.


.. admonition:: Proof
   :class: toggle

   HERE

One can also find the relation between the new wave function :math:`\psi^{(2)}` and the original one :math:`\psi^{(1)}`,

.. math::
   \psi_n^{(2)} =& \frac{1}{\sqrt{ E^{(1)}_{n+1} }} A \psi_{n+1}^{(1)}, \\
   \psi_{n+1}^{(1)} = & \frac{1}{\sqrt{E^{(2)}_n}} A^\dagger \psi_n^{(2)}.

Meanwhile the energy levels are also related

.. math::
   E^{(1)}_{n+1} = E^{(2)}_n.

.. admonition:: Proof
   :class: toggle

   QED.



References and Notes
-----------------------


1. `An Introduction to Supersymmetry in Quantum
Mechanical Systems by T. Wellman <http://gaitskell.brown.edu/courses/SeniorThesis/2003_SeniorThesis/2003SeniorThesis_Wellman.pdf>`_
2. Cooper, F., Khare, A., & Sukhatme, U. (1995). Supersymmetry and quantum mechanics. Physics Reports, 251(5-6), 267–385. doi:10.1016/0370-1573(94)00080-M.
