Probability Theory
==================

**Probability Theory** is the branch of mathematics that formalizes and analyzes random events, chance, and uncertainty. It assigns numerical values between **0** (impossible) and **1** (certain) to the likelihood of an event occuring.

**Probability** can be conceptualized as finding the chance of occurence of an event. Mathematically, it is the study of random processes and their outcomes. The laws of probability have wide applicability in a variety of fields like genetics, weather forecasting, opinion polls, stock markets, etc.

Probability theory was invented in the 17th century by two French mathematicians, Blaise Pascal and Pierre de Fermat, who were dealing with mathematical problems regarding of chance.

.. admonition:: Concepts
    :class: tip

    Random Experiment
      An experiment in which all possible outcomes are known and the exact output cannot be predicted in advance is called a **random experiment**. Tossing a fair coin is an example of random experiment.

    Sample Space
      When we perform an experiment, then the set :math:`S` of all possible outcomes is called the **sample space**. If we toss a coin, the sample space is :math:`S = \{H, T\}`.

    Event
      Any subset of a sample space is called an **event**. After tossing a coin, getting head on the top is an event.

The word "probability" means the chance of occurrence of a particular event. The best we can say is how likely they are to happen, using the idea of probability.

.. math::

    Probability\:of\:occurence\:of\:an\:event = \frac{Total\:number\:of\:favourable \: outcome}{Total\:number\:of\:Outcomes}

As the occurence of any event varies between 0% and 100%, the probability varies between 0 and 1.


Probability Axioms
++++++++++++++++++

- The probability of an event always varies from :math:`0` to :math:`1`. :math:`[0 \leq P(x) \leq 1]`.

- For an impossible event, the probability is :math:`0`; and for a certain event, the probability is :math:`1`.

- If the occurence of one vvent is not influenced by another event, they are called **mutually exclusive** or **disjoint**. If :math:`A_1, A_2....A_n` are mutually exclusive/disjoint events, then :math:`P(A_i \cap A_j) = \emptyset` for :math:`i \ne j` and :math:`P(A_1 \cup A_2 \cup.... A_n) = P(A_1) + P(A_2)+..... P(A_n)`.


Properties of Probability
+++++++++++++++++++++++++

If there are two events :math:`x` and :math:`\overline{x}`, which are complementary, then the probability of the complementary event is:

.. math::

    p(\overline{x}) = 1-p(x)

For two non-disjoint events :math:`A` and :math:`B`, the probability of the union of two events:

.. math::

    P(A \cup B) = P(A) + P(B)

If an event :math:`A` is a subset of another event :math:`B` (i.e. :math:`A \subset B`), then the probability of :math:`A` is less than or equal to the probability of :math:`B`. Hence, :math:`A \subset B` implies :math:`P(A) \leq p(B)`.


Steps to Find the Probability
+++++++++++++++++++++++++++++

1. Calculate all possible outcomes of the experiment.
2. Calculate the number of favorable outcomes of the experiment.
3. Apply the corresponding probability formula.

.. admonition:: Example: Tossing a Coin
    :class: hint

    If a coin is tossed, there are two possible outcomes---Heads (:math:`H`) or Tails (:math:`T`).

    So total number of outcomes = :math:`2`.

    Hence, the probability of getting a Head (:math:`H`) on top is :math:`1/2` and the probability of getting a Tails (:math:`T`) on top is :math:`1/2`.

.. admonition:: Example: Throwing a Dice
    :class: hint

    When a dice is thrown, six possible outcomes can be on top---:math:`1, 2, 3, 4, 5, 6`.

    The probability of any one of the numbers is :math:`1/6`.

    The probability of getting even numbers is :math:`3/6`` = :math:`1/2`.
    
    The probability of getting odd numbers is :math:`3/6`` = :math:`1/2`.

.. admonition:: Example:: Taking Cards from a Deck
    :class: hint

    From a deck of 52 cards, if one card is picked, find the probability of an ace being drawn, and also find the probability of a diamond being drawn.

    Total number of possible outcomes = :math:`52`.

    Outcomes of being an ace = :math:`4`.

    Probability of being an ace = :math:`4/52` = :math:`1/13`.

    Probability of being a diamond = :math:`13/52` = :math:`1/4`.


Conditional Probability
+++++++++++++++++++++++

The **conditional probability** of an event :math:`B` is the probability that the event will occur given an event :math:`B` has already occured. This is written as :math:`P(B|A)`.

Mathematically: :math:`P(B|A) = P(A \cap B)/ P(A)`.

If event :math:`A` and :math:`B` are mutually exclusive, then the conditional probability of event :math:`B` after the event :math:`B` will be the probability of event :math:`B` that is :math:`P(B)`.

.. admonition:: Problem 1
    :class: hint

    In a country, 50% of all teenagers own a cycle and 30% of all teenagers own a bike and cycle. What is the probability that a teenager owns bike given that the teenager owns a cycle?

    Let us assume :math:`A` is the event of teenagers owning only a cycle and :math:`B` is the event of teenagers owning only a bike.

    So, :math:`P(A) = 50/100 = 0.5` and :math:`P(A \cap B) = 30/100 = 0.3` from the given problem.

    :math:`P(B|A) = P(A \cap B)/ P(A) = 0.3/ 0.5 = 0.6`

    Hence, the probability that a teenager owns bike given that the teenager owns a cycle is :math:`60%`.

.. admonition:: Problem 2
    :class: hint

    In a class, 50% of all students play cricket, and 25% of all students play cricket and volleyball. What is the probability that a student plays volleyball given that the student plays cricket?

    Let us assume :math:`A` is the event of students playing only cricket and :math:`B` is the event of students playing only volleyball.

    So, :math:`P(A) = 50/100 =0.5` and :math:`P(A \cap B) = 25/ 100 =0.25` from the given problem.

    :math:`P\lgroup B\rvert A \rgroup= P\lgroup A\cap B\rgroup/P\lgroup A \rgroup =0.25/0.5=0.5`

    Hence, the probability that a student plays volleyball given that the student plays cricket is :math:`50%`.

.. admonition:: Problem 3
    :class: hint

    Six good laptops and three defective laptops are mixed up. To find the defective laptops, all of them are tested one-by-one at random. What is the probability to find both of the defective laptops in the first two pick?

    Let :math:`A` be the event that we find a defective laptop in the first test and :math:`B` be the event that we find a defective laptop in the second test.

    Hence, :math:`P(A \cap B) = P(A)P(B|A) =3/9 \times 2/8 = 1/12`.