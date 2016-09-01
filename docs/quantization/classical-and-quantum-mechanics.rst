Classical Mechanics and Quantum Mechanics
==============================================================

:highlight-text:`Throughout this section, we use Einsten's summation rule.`

Poisson Brackets in Classical Mechanics
------------------------------------------------------------

.. admonition:: Definition of Poisson Bracket
   :class: toggle

   Poisson bracket is defined as

   .. math::
      \{A,B\}= \frac{\partial A}{\partial q_i} \frac{\partial B}{\partial p_i} - \frac{\partial A}{\partial p_i} \frac{\partial B}{\partial q_i}.

In classical mechanics, we can find conserved quantities without the help of symmetries, by using Hamilton's form.

For an conserved quantity :math:`A(q_i,p_i)`, we have

.. math::
   \partial_t A(q_i,p_i) = 0.

By using Hamilton's equations, we can find that

.. math::
   \partial_t A(q_i,p_i) = \{ A(q_i,p_i), H \}.

Thus the conservation condition is

.. math::
   \{ A(q_i,p_i), H \} = 0.

.. admonition:: Derivation of the Relation between Conserved Quantities and Poisson Bracket
   :class: toggle

   On the other hand,

   .. math::
      \partial_t A(q_i,p_i) = \frac{\partial A(q_i,p_i)}{\partial q_i} \partial_t q_i + \frac{\partial A(q_i,p_i)}{\partial p_i} \partial_t p_i.
      :label: derivation-conserved-a-1

   Recall that the Hamilton's equations are

   .. math::
      \partial_t q_i = & \frac{\partial H}{\partial p_i}, \\
      \partial_t p_i = & -\frac{\partial H}{\partial q_i}.

   Plug them back into Eq. |nbsp| :eq:`derivation-conserved-a-1`, we have

   .. math::
      \partial_t A(q_i,p_i) =& \frac{\partial A(q_i,p_i)}{\partial q_i} \frac{\partial H}{\partial p_i} + \frac{\partial A(q_i,p_i)}{\partial p_i} \left( -\frac{\partial H}{\partial q_i} \right) \\
      =& \{A(q_i,p_i), H\}.


.. admonition:: Self-consistancy Check of Poisson Bracket and Conserved Quantities
   :class: toggle

   We can easily find the Poisson brackets :math:`\{q_i,H\}` and :math:`\{p_i,H\}`, which are in fact :math:`\partial q_i` and :math:`\partial_t p_i`.

   We would actually get the Hamilton's equations.
