# Class 5

Reading: King AA, Lin Q, Ionides EL. (2022)
Markov genealogy processes.
*Theoretical Population Biology* **143**:77--91.
[(doi:10.1016/j.tpb.2021.11.003)](https://doi.org/10.1016/j.tpb.2021.11.003).

This paper addresses many of the limitations of the linear birth-death process models we looked at last time.
Specifically, it shows how one can compute the phylodynamic likelihood under any one of a large class of Markov population processes, including ones with nonlinear and/or time-dependent rates.

The paper shows how a given Markov population process induces a process on the space of genealogical trees (Figs.&nbsp;2--4).
One projects these trees onto the space of observable trees through a process of *pruning* (Fig.&nbsp;5).
Using the Markovian structure of the pruned-tree process, we derive an expression for the likelihood of a given tree *conditional* on the history of the population process (Theorem&nbsp;2).
Finally, we show that one can then integrate over the set of all histories to obtain a filtering equation (Eqs.&nbsp;19--21).
Several examples showing how this can be solved numerically are provided (&sect;6).

The proof of the main result is based on a novel and somewhat technical construction that is of limited interest.
To get the most out of a first reading of the paper, it's best to focus on understanding what this approach makes possible rather than on exactly how it does so.
The following study questions are intended to help guide your reading:

1. For any one of the examples in Section 3, what is the corresponding Kolmogorov forward equation (Eq.&nbsp;3)?
1. Heuristically, how does tracking the history of the population process allow one to construct a genealogy (Figs.&nbsp;2--4)?
1. Roughly speaking, what is involved in the pruning process (Fig.&nbsp;5)?
1. Why is the pruned-tree process Markovian?
1. Compare the form of the filter equation for the linear birth-death-sampling model (&sect;6) to that obtained by Stadler (2010).
1. Compare the form of the filter equation for the SIR model (&sect;6) to that obtained by Volz (2009).

As before, you can get your class participation credit by submitting ahead of class, in writing, a few sentences describing (i) something you got out of reading this paper; (ii) something you got stuck on trying to understand.
You can [email this to ionides@umich.edu and kingaa@umich.edu with subject "700 participation"](mailto:ionides@umich.edu;kingaa@umich.edu?subject=700%20participation).

Note that each class is graded with one point for attendance and one for participation.

## Class 5: [slides](slides.pdf)

