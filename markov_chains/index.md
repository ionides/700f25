# Continuous time Markov chains and Kolmogorov's equations

Sources: [Wikipedia](https://en.wikipedia.org/wiki/Kolmogorov_equations)

Let $\{X(t),t\ge o\}$ be a Markov process in continuous time, taking values in a set __X__ called the state space.


## Countable state space

Write $P_{ij}(s,t)=\mathrm{Prob}[X(t)=j | X(s)=i]$.
The Kolmogorov forward equation (KFE) is
```math
\partial P_{ij}(s,t)/\partial t = \sum_k P_{ik}(s,t)Q_{kj}(t).
```
The Kolmogorov backward equation (KBE) is
```math
\partial P_{ij}(s,t)/\partial s = - \sum_k P_{kj}(s,t)Q_{ik}(s).
```
$Q_{ij}(t)$ is called the generator, or the rate matrix, or the $Q$-matrix, though formally it is a matrix only when $\mathcal{X}$ is finite.
To preserve formality, since rate operator or $Q$-operator are non-standard, we will use the name _generator_.

For $i\neq j$, inspection of the KFE shows that $Q_{ij}(t)$ is the rate of transitioning from $i$ to $j$ at time $t$.
Summing the KFE over $j$ we expect $\sum_j \partial P_{ij}(s,t)/\partial t = 0$ due to the law of total probability: $\sum_j P_{ij}(s,t)=1$.
This suggests that $\sum_j Q_{ij}(t)=0$ and so $Q_{ii}(t) = -\sum_{j\neq i}Q_{ij}(t)$, which is minus the total departure rate from $i$.
We write $Q_i(t)=-Q_{ii}(t)$.
Here, we do not focus on regularity conditions, but be aware that pushing infinite sums through derivatives and expectations may break down without sufficient regularity.

### Time-homogeneous finite state space

Here, $Q_{ij}(t)=Q_{ij}$ is a matrix, and we write $P_{ij}(t)=P_{ij}(0,t)=P_{ij}(s,s+t)$.
Then, the KFE can be written using matrix multiplication, as
```math
dP(t)/dt = P(t)Q
```
and the KBE is
```math
dP(t)/dt = QP(t).
```
The negative sign in the general KBE has disappeared: why?
In this case, we see that $P$ and $Q$ commute: $PQ=QP$.
The KBE and KFE have a solution given by a matrix exponential,
```math
P(t) = \exp\{ Qt\} = \sum_{k=0}^{\infty} Q^kt^k/k!.
```
Each term in the sum commutes with $Q$, and so $P(t)$ must also do so. 

## The jump chain and sojourn times

Also known as the embedded Markov chain, the jump chain is the sequence of states into which $X(t)$ arrives.
It can be shown that a transition from state $i$ at time $t$ has probability distribution $Q_{ij}(t)/Q_i(t)$.

When the generator does not depend on time, the sojourn time in a state $i$ is exponentially distributed, independent of the subsequent transition.
The sojourn in state $i$ has rate $Q_i$ and therefore mean $1/Q_i$.




