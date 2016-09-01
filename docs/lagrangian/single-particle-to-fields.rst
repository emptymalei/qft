From Particles to Fields
==========================================


In this chapter we discuss the Lagrangian formalism of particles and fields.

1. Lagrangian and Euler-Lagrangian equation of single particle;
2. Generalize single particle formalism to fields;
3. Using the least action principle to derive some famous equation of motions: Klein-Gordon equation, Dirac equation, Maxwell equation, and equation for massive vector particles.
4. Relation to statistical mechanics.


Classical Mechanics
----------------------------

For single particle, we define a Lagrangian :math:`L(q_i,\dot q_i, t)` which is a function of generalized coordinate :math:`q_i`, its derivative, and time :math:`t`. To be precise, the generalized coordinates could be time dependent.

Action is defined as the integral of Lagrangian over time,

.. math::
   S = \int dt L(q_i,\dot q_i, t).

The principle that leads to the equation of motion that the particle obays is the one that extremize the action. Mathematically,

.. math::
   \delta S = 0,

which gives us the Euler-Lagrangian equation,

.. math::
   \partial_t \left( \frac{\partial L}{\partial \dot q_i} \right) - \frac{\partial L}{\partial q_i} = 0.

.. admonition:: Derivation of Euler-Lagrangian Equation
   :class: toggle

   - [ ] Here goes the derivation


On the other hand, a Legendre transform of the Lagrangian is the Hamiltonian. For single particle

.. math::
   H = \dot q p - L,

where the generalized momentum is :math:`p = \partial L/\partial \dot q`. The equation of motion starting from Hamiltonian is

.. math::
   \dot q &= \frac{\partial H}{\partial p},\\
   \dot p &= -\frac{\partial H}{\partial q}.



Generalization to Fields
------------------------------------------

For single particle, the dynamics is described by where the particle is at a certain time. However, field spans over space and evolve over time. Thus we define a Lagrangian :math:`\mathcal L` at each space point, which should be called Lagrangian density. Integrate over space we find the Lagrangian

.. math::
   L = \int d^3x \mathcal L.

To be more specific, Lagrangian density is a function of :math:`\phi_i(x^\mu)`, :math:`\phi_i(x^\mu)_{,\mu}`, where :math:`x^\mu` are the space time coordinates. Then

.. math::
   L(t) = \int d^3x \mathcal L(\phi_i(x^\mu),\phi_i(x^\mu)_{,\mu}).


.. admonition:: Lagrangian and Lagrangian Density
   :class: hint

   In quantum field theory, Lagrangian density is usually called Lagrangian.


Similar to single particle theory, action is defined as integral of Lagrangian over time,

.. math::
   S = \int dt L(t).

Apply the same principle as the single particle case, we can derive the Euler-Lagrangian for the fields

.. math::
   \partial_\mu \left( \frac{\partial \mathcal L}{\partial ( \phi_{i,\mu} )} \right) - \frac{\partial \mathcal L}{\partial \phi_i} = 0.



.. admonition:: Derivation of Euler-Lagrangian Equation
   :class: toggle

   - [ ] Here goes the derivation


We can also define a momentum of field :math:`\phi_i`,

.. math::
   \Pi(x^\mu) = \frac{ \partial \mathcal L }{ \partial ( \partial_0 \phi_i )  }.

The Hamiltonian density follows

.. math::
   \mathcal H = \dot \phi_i \Pi - \mathcal L.





Examples of Lagrangian
---------------------------------------

Klein-Gordon Equation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



Dirac Equation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



Maxwell Equation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



Equation for Massive Vector Particles
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Shrodinger Equation
~~~~~~~~~~~~~~~~~~~~~~~~~~~



Refs and Notes
------------------


1. *Field Theory : A Modern Primer* by Pierre Ramond. The first chapter of this book is "How to Build an Action Functional", which is self-explanary.
