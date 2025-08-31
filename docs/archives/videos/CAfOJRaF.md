## Competitive Algorithms for Online Joint Replenishment and Friends

- [Competitive Algorithms for Online Joint Replenishment and Friends](https://www.youtube.com/watch?v=mrmZD4hM8Fk)

Research Areas:

Approximation & Online Algorithms

### Joint Replenish Problem (JRP)

- n item types, fixed global cost k, each item costs 1.
- Request for an item, a time interval (release - deadline), satisfied by having its item transmitted.
- cost of transmitting a set of items A is cost(A) = K + |A|
- final cost looks like K + 3 + K + 1, minimize it.
- Online version: only sees requests when past the release time.

Considerations:

- k = infinite - min interval hitting set = max disjoint intervals
- k = 0 - treat each item separately - serve on deadlines

With Delay:

- Instead of deadlines, incurs delay cost $d_q(t)$ - continuous and non-decreasing.
- Can simulate deadlines for $d_q(t)$ to jump from 0 to infinity at the deadline.

Compa-Ratio / CR - worst case analysis

Related work:

- Offline is NP-hard and APX-hard. 1.574-approx for deadlines
- Online is 3-comp with lower bound of 2.64

Additions:

- Different service cost functions
  - Multi-Level Aggregation / Inventory Routing or Network Design - Open Problems, maybe O(1) comp possible?
    - Item is a (leaf) node in a tree. cost(A) = weight of subtree connecting A to root. Or graph with minimum subgraph for covering.
    - comp: O(log n) or related to depth
  - Cost of transmitting A is f(A), f is non-decreasing and subadditive, f(A) + f(B) >= f(A | B), economies of scale
    - comp: O(log n) or O(log #requests)
    - Bounded be Set Cover Problem
- Deadline also not known on arrival

Cardinality JRP:

f(A) = g(|A|) for concave g. Offline 5-approx, online O(log n)

Current Work:

O(1)-comp for Cardinality JRP (can extend to weighted case)!

Algo idea:

- Concave = piece wise linear functions with O(log n) pieces = min of O(log n) affine functions = O(log n) JRP instances

### Non-Clairvoyant Algorithms

Non-Clair Model: Deadline revealed when it's reached.

Set Cover With Delay:

Randomized poly-log time O(log n log m)

JRP:

Deterministic lower bound $\Omega(\sqrt{n})$

Current Work:

JRP - $O(\sqrt{n})$. Randomized also $\Omega(\sqrt{n})$.

MLA - $O(\sqrt{n} + depth)$, close the gap

Set Cover With Delay - Derandomization of $O(log n log m)$

Related to submodular optimization

Learning-Augmented Algorithms