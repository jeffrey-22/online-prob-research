## The Power of Clairvoyance for Multi-Level Aggregation and Set Cover with Delay

Proofs TBD

- [The Power of Clairvoyance for Multi-Level Aggregation and Set Cover with Delay](https://epubs.siam.org/doi/10.1137/1.9781611977554.ch59)

### Intro

the delay cost of request $q$ is $d_q(t)$ if it is served at time $t$

Request $q$, delay $d_q(t')$ known for $t' \leq t$, $t$ being the current time

JRP K + |A|

MLAP tree, subtree sum of weight. Tree depth is $D$.

SCD 

### Results

- Any randomized non-clairvoyant algorithm for JRP with deadlines is $\Omega(\sqrt{n})$-comp.

- Deterministic $O(D + \sqrt{n})$-comp algorithm for MLAP non-clairvoyant.

- There is a randomized $O(\sqrt{n} log n)$-competitive non-clairvoyant algorithm for edge-weighted Steiner tree.

- Deterministic $O(log n log m)$-competitive non-clairvoyant algorithm (tight) for Set Cover with Delay.

### Techniques

- Start a service once a set of requests Q accumulate enough delay to pay for the subtree $T_Q$ connecting them to the root. We say these requests are critical.
- Invest on not including requests in critical.

### Related work

- Source of MLA and history of improvements
- MLAP mostly settled
- SCD history
- ONDwD network version's history
- CJRP, for concave g(|A|)'s history

### Proofs

TBD