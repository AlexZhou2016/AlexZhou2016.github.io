---
title: Hello World
---

高级算法 Problem Set 1
==

姓名：周文吉
学号：MG1633108

----

### Problem 1.
(1)
Let $e_1,e_2,e_3,...,e{n-2}$ denote the sequence of random edges chosen to contract in a running of RandomContract algorithm.
Let $G_1 = G$ denote the original input multi-graph. And for $i=1,2,\ldots,n-2$, let $G_i + 1 = Contract(G_i,e_i)$ be the multigraph after $i$th contraction. 

Let
$p_{correct} $ = $Pr$[a $\alpha$-minimum-cut is returned by algorithm]  
 
$p_{C} $ = $Pr$[a certain $\alpha$-minimum-cut is returned by algorithm]

Obviously, $p_{correct} \geq p_C$


> Proposition 1
> If $C$ is a $\alpha$ minimum cut in a multi-graph $G$ and $e\not\in C$, then $C$ is still a minimum cut in the contracted graph $G' = contract(G,e)$.

The proof of Proposition 1 is the same as the proof of Proposition 1 in Lecture Note 1. Therefore:
$p_{C} = Pr$[a certain $\alpha$-minimum-cut is returned by algorithm$]$  
&ensp;&ensp;&ensp;$=Pr[e_i \notin C $ for all $i=1,2,...,n-2]$  
&ensp;&ensp;&ensp;$=\prod^{n-2}_{i=1} Pr[e_i \notin C | \forall j<i, e_j \notin C]$

> Proposition 2
> If C is a min-cut in a multi-graph $G(V,E)$, then $|E|\ge \frac{|V||C|}{2}$.

The proof of proposition above can find in Lecture Note1, which apply the *handshaking lemma* to the fact that every vertex in $G$ has degree at least $|C|$
Therefore:
$p_i = Pr$[$e_i \notin C | \forall j<i, e_j \notin C$]
&ensp;&ensp;&ensp;$=1-\frac{\alpha|C|}{|E_i|}$
&ensp;&ensp;&ensp;$\geq 1 -\frac{2\alpha}{|V_i|}$
&ensp;&ensp;&ensp;$=1-\frac{2\alpha}{n-i+1}$

So:
$p_{correct} = Pr[$a $\alpha$-minimum-cut is returned by algorithm$]$
　　　&ensp;$\geq Pr[C $ is returned by algorithm$]$
　　　&ensp;$= Pr[e_i \notin C $ for all $ i=1,2,...,n-2 ]$
　　　&ensp;$= \prod^{n-2}_{i=1}Pr[e_i \notin C | \forall j<i, e_j\notin C]$
　　　&ensp;$\geq \prod^{n-2}_{i=1}(1-\frac{2\alpha}{n-i+1})$

(2)
Let $\mathcal{C}$ denote the set of all $\alpha$-minimum-cuts in $G$. For each $\alpha$-min-cut $C\in\mathcal{C}$, let $A_C$ denote the event "$C$ is returned by algorithm", whose probability is given by 
$$p_C=Pr[A_C]$$

For any distinct $C,D \in \mathcal{C}$, $A_C$ and $A_D$, are disjoint events and the union $\bigcup_{C\in\mathcal{C}}A_C$ is precisely the event "a minimum cut is returned by algorithm", whose probability is given by $p_{correct}$. Therefore,
$$p_{correct} = \sum_{C \in \mathcal{C}}Pr[A_C] = \sum_{C \in \mathcal{C}}p_C$$
Since $p_{correct}$ is a well defined probability, due to the *unitarity of probability*, it must hold that $p_{correct}\le 1$. Therefore,
$$1\geq p_{correct} = \sum_{C \in \mathcal{C}}p_C \geq |C|\prod^{n-2}_{i=1}(1-\frac{2\alpha}{n-i+1}),$$
which means $|\mathcal{C}| \leq \frac{1}{\prod^{n-2}_{i=1}(1-\frac{2\alpha}{n-i+1})}$


### Problem 2.
(1)

### Problem 3.


### Problem 4.

### Problem 5.
