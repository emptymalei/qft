Noether's Theorem
================================


Noether's theorem deals with continuous symmetry.


Noether's Theorem of Particles
----------------------------------------------------



Noether's Theorem of Fields
----------------------------------------------------

Suppose we have a continuous transformation, which is internal, that transforms the fields according to

.. math::
   \phi_i (x^\mu) \to \phi_i (x^\mu) + \delta \phi_i(x^\mu).

For convenience, we explicity write the variation :math:`\delta \phi_i(x^\mu)` as a continuous quantity :math:`\alpha`, i.e.,

.. math::
   \delta \phi_i(x^\mu) = \alpha \Delta\phi(x^\mu).

Noether's theorem states that if this continuous preserves the Lagrangian, we can define conserved Noether current thus conserved charge.


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



Examples of Noether Current
----------------------------------------------


Global Phase Transformation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

For the Lagrangian

.. math::
   \mathcal L = \partial^\mu \phi^* \partial_\mu \phi -  m^2 \phi^* \phi,

that leads to Klein-Gordon equation, a transformation

.. math::
   \phi \to e^{i\alpha}\phi,\\
   \phi^* \to e^{-i\alpha}\phi^*,

will not change the scalar particle Lagrangian.

The corresponding Noether current is defined by

.. math::
   \partial_\mu j^\mu = 0,

where

.. math::
   j^\mu = -i(\phi^* \partial^\mu \phi - \phi\partial^\mu \phi^*).

Along with the current we find the conserved charge

.. math::
   Q = \int d^3 x j^0,

which satisfies

.. math::
   \frac{\partial Q}{\partial t}= 0.


.. admonition:: Proof
   :class: toggle

   Here is the proof.


Space-time Translation
~~~~~~~~~~~~~~~~~~~~~~~~

For arbitary Lagrangian :math:`\mathcal L(x^\mu)` which is space-time dependent, we can calculate the action

.. math::
   S = \int d^4x \mathcal L.

If the action is invariant under space-time translation

.. math::
   x^\mu\to x^\mu + \alpha a^\mu,

we find the conserved current to be the energy-momentum tensor :math:`T^{\mu\nu}`

.. math::
   T^{\mu\nu} = \frac{\partial \mathcal L}{\partial (\partial_\mu\phi)}\partial^\nu \phi - g^{\mu\nu} \mathcal L.

The corresponding conservation equation is

.. math::
   \partial_\mu T^{\mu\nu} = 0,

which defines the four charges

.. math::
   Q^\mu = \int d^3 T^{\mu\nu} .

.. admonition:: Proof Energy-momentum Tensor as Noether Current
   :class: toggle

   QED.

For the Lagrangian

.. math::
   \mathcal L = \frac{1}{2} \partial^\mu \phi \partial_\mu \phi - \frac{1}{2} m^2 \phi^2,

one can easily prove that the corresponding energy-momentum tensor is

.. math::
   T^{\mu\nu} = \partial^\mu \phi\partial^\nu \phi - g^{\mu\nu} \mathcal L.

.. admonition:: Derivation of Energy-momentum for Real Scalar Lagrangian
   :class: toggle

   QED.

The 00 component is in fact the Hamiltonian density :math:`\mathcal H`.

.. admonition:: Prove that :math:`T^{00}=\mathcal H`
   :class: toggle

   Calculate :math:`T^{00}`,

   .. math::
      T^{00} =& \partial^0 \phi \partial^0\phi - \mathcal L \\
      =& \frac{1}{2} ( \partial^0\phi\partial^0\phi + \partial^i \phi \partial^i\phi + m^2\phi^2 ).

   Notice that the Hamiltonian density is

   .. math::
      \mathcal H = \Pi \partial^0 \phi - \mathcal L,

   where

   .. math::
      \Pi = \frac{\partial \mathcal L}{\partial (\partial^0 \phi)} = \partial^0\phi.

   Plug in the momentum we find

   .. math::
      \mathcal H = \partial^0\phi\partial^0\phi - \mathcal L = T^{00}.







References and Notes
----------------------------------------------------
