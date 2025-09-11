# Inference via Kingman's coalescent

* Kingman (1982) derived a coalescent with a unit rate of coalescence between all pairs of individuals at the leaves, and therefore a total coalescence rate of order $n^2$ for population size $n$.

* If each individual has a fixed rate of coalescing (branching, in forward time; transmitting in an epidemiological context) independent of population size, then the total coalescence rate should be order $n$, and we have to rescale time by a factor of $n$ to obtain Kingman's coalescent.

* We suppose the data are modeled as a coalescent for a subset $\ell(T)$ lineages from the population of size $n$ sampled at time $T$.
This subset coalescent is itself a coalescent, with rescaled leaf coalescent rate given by $\ell(T)(\ell(T)-1)/2n$.

* Additionally, time can be rescaled in Kingman's coalescent to account for the generation length, $\tau$, or equivalently the individual reproduction rate, $\beta=1/\tau$.

* The death rate from $\ell$ lineages to $\ell-1$ has rate $\ell(\ell-1)/2$ in Kingman's model, and therefore rate $\beta \ell(\ell-1)/2n$ in the rescaled coalescent.

* Kingman (1982) tells us that the shape of the tree is independent of the coalescence process, so inference for $\beta$ and $n$ can depend only on the coalescence times modeled by a death process.

* We can only hope to estimate $\lambda=\beta/n$.
If we know $n$, we can estimate $\beta$.
More commonly, if we have a satisfactory estimate of $\beta$, we can estimate $n$.

* Continuous time Markov chains in general (and the death process in particular) have exponentially distributed jump times.
The likelihood of coalescent times $t_2,\dots,t_{\ell(T)}$, with $t_\ell$ being the time at which $\ell-1$ lineages branch into $\ell$ lineages, is therefore
```math
\prod_{j=2}^{\ell(T)} \lambda {j\choose 2} \, \exp\left\{ \lambda {j \choose 2} (t_j-t_{j-1}) \right\}.
```

* We can proceed to construct a maximum likelihood estimate of $\lambda$, or conduct Bayesian inference.

* The coalescent estimate of $n$ is known as the _effective population size_, and is sometimes defined as the Wright-Fisher model population size that would match the observed coalescence rate.
Recall that Wright-Fisher corresponds to multinomial selection of descendants at each population of generation length $\tau$ in a population of fixed size $n$.

* Griffiths and Tavare (1994) extended this argument to a time-varying function $\lambda(t)$.
The identifiability issue between time-varying $n$ and $\beta$ remains.

* Pybus et al. (2000) introduced a non-parametric piecewise constant estimate of $\lambda(t)$ known as the _skyline plot_.

## References

Griffiths, R. C., and S. Tavare, 1994 Sampling theory for neutral
alleles in a varying environment. Philos. Trans. R. Soc. B Biol. Sci.
344: 403–410. [https://www.jstor.org/stable/56112](https://www.jstor.org/stable/56112)

Kingman, J. F. C. (1982). The coalescent. _Stochastic Processes and their Applications_, 13(3), 235-248. [https://doi.org/10.1016/0304-4149(82)90011-4](https://doi.org/10.1016/0304-4149(82)90011-4)

Pybus, O. G., Rambaut, A., & Harvey, P. H. (2000). An integrated framework for the inference of viral population history from reconstructed genealogies. Genetics, 155(3), 1429-1437. [https://doi.org/10.1093/genetics/155.3.1429](https://doi.org/10.1093/genetics/155.3.1429)
