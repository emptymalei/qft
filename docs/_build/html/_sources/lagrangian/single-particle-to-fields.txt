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



Noether's Theorem
-----------------------------------

Noether's theorem deals with continuous symmetry.


Noether's Theorem of Particles
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



Noether's Theorem of Fields
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Suppose we have a continuous transformation, which is internal, that transforms the fields according to

.. math::
   \phi_i (x^\mu) \to \phi_i (x^\mu) + \delta \phi_i(x^\mu).

For convenience, we explicity write the variation :math:`\delta \phi_i(x^\mu)` as a continuous quantity :math:`\alpha`, i.e.,

.. math::
   \delta \phi_i(x^\mu) = \alpha \Delta\phi(x^\mu).


.. admonition:: Planning the Proof
   :class: toggle

   1. Write down the variation of Lagrangian.
   2. Combine the terms and apply the Euler-Lagrangian equation.
   3. If the Lagrangian is invariant under such a continuous tranformation, blablabla.


The variation of Lagrangian is

.. math::
   \delta \mathcal L(\phi_i, \dot \phi_i) = \frac{\partial \mathcal L}{\partial \phi_i} \delta \phi_i + \frac{\partial \mathcal L}{\partial \phi_{i,\mu}} \delta(\phi_{i,\mu}).
   :label: variation-of-lagrangian-fields

We know that the variation and partial derivative can be exchanged, such that

.. math::
   \delta(\phi_{i,\mu}) = \partial_\mu (\delta \phi_i).

We rewrite the second term in Eq. |nbsp| :eq:`variation-of-lagrangian-fields`,

.. math::
   &\frac{\partial \mathcal L}{\partial \phi_{i,\mu}} \delta(\phi_{i,\mu}) \\
   = & \frac{\partial \mathcal L}{\partial \phi_{i,\mu}} \partial_\mu( \delta \phi_{i} ) \\
   = & \partial_\mu\left( \frac{\partial \mathcal L}{\partial \phi_{i,\mu}} \delta \phi_{i} \right) - \delta \phi_{i} \partial_\mu \left( \frac{\partial \mathcal L}{\partial \phi_{i,\mu}}  \right).

Plug it back into Eq. |nbsp| :eq:`variation-of-lagrangian-fields`, we have

.. math::
   \delta \mathcal L(\phi_i, \dot \phi_i) =&  \frac{\partial \mathcal L}{\partial \phi_i} \delta \phi_i + \partial_\mu\left( \frac{\partial \mathcal L}{\partial \phi_{i,\mu}} \delta \phi_{i} \right) - \delta \phi_{i} \partial_\mu \left( \frac{\partial \mathcal L}{\partial \phi_{i,\mu}}  \right) \\
   = &  \delta \phi_i \left(  \frac{\partial \mathcal L}{\partial \phi_i} - \partial_\mu \left( \frac{\partial \mathcal L}{\partial \phi_{i,\mu}}  \right) \right) + \partial_\mu\left( \frac{\partial \mathcal L}{\partial \phi_{i,\mu}} \delta \phi_{i} \right).

The first term is zero by Euler-Lagrangian equation. Thus

.. math::
   \delta \mathcal L(\phi_i, \dot \phi_i) =\partial_\mu\left( \frac{\partial \mathcal L}{\partial \phi_{i,\mu}} \delta \phi_{i} \right).

Now we impose the condition that the Lagrangian is invariant under such a continuous transformation, so that :math:`\delta \mathcal L = 0`.

.. math::
   \partial_\mu\left( \frac{\partial \mathcal L}{\partial \phi_{i,\mu}} \delta \phi_{i} \right) = 0.
   :label: constant-of-motion-fields-1

Eq. |nbsp| :eq:`constant-of-motion-fields-1` defines the :highlight-text:`constant of motion`. Put the definition of :math:`\delta \phi_i` back in,

.. math::
   \alpha \partial_\mu\left( \frac{\partial \mathcal L}{\partial \phi_{i,\mu}} \Delta \phi_{i} \right) = 0.
   :label: constant-of-motion-fields




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
