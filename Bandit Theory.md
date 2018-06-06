# Multi-armed Bandits

## Summary

* [Stochastic Bandits](#stochastic-bandits)
* [Contextual Bandits](#contextual-bandits)
* [Continuum-armed Bandits](#continuum-armed-bandits)
* [Adversarial Bandits](#adversarial-bandits)
* [Best Arm Identification](#best-arm-identification)
* [Applications](#applications)
* [Others](#others)

## Papers

### Stochastic Bandits

* **`UCB1`** [Finite-time Analysis of the Multi-armed Bandit Problem](https://homes.di.unimi.it/~cesabian/Pubblicazioni/ml-02.pdf), P. Auer et al., 2002.

### Contextual Bandits

* [An Information-Theoretic Analysis of Thompson Sampling](https://arxiv.org/abs/1403.5341), D. Russo and B. van Roy, 2014.
* **`WB`** [New Insights into Bootstrapping for Bandits](https://arxiv.org/abs/1805.09793), S. Vaswani et al., 2018.

### Continuum-armed Bandits

* **`UCB-V`** **`UCB-F`** [Algorithms for Infinitely Many-Armed Bandits](https://papers.nips.cc/paper/3452-algorithms-for-infinitely-many-armed-bandits.pdf), Y. Wang et al., 2008.
* **`HOO`** [X-armed Bandits](https://arxiv.org/abs/1001.4475), S. Bubeck et al., 2010. ([video](https://www.youtube.com/watch?v=G1abqjqffRE))
* [Lipschitz Bandits without the Lipschitz Constant](https://arxiv.org/abs/1105.5041), S. Bubeck et al., 2011.
* **`HCT`** [Online Stochastic Optimization under Correlated Bandit Feedback](https://arxiv.org/abs/1402.0562), M. Gheshlaghi-Azar et al., 2014.
* **`SiRI`** [Simple Regret for Infinitely Many Armed Bandits](https://arxiv.org/abs/1505.04627), M. Valko and A. Carpentier, 2015. ([talk](http://researchers.lille.inria.fr/~valko/hp/publications/carpentier2015simple.talk.pdf))
	- SiRI is an algorithm that provides minimax optimal rate up to at most some log(n) factor (depending on a parameter beta) on the simple regret for a infinitely many-armed bandit problem.
	- It assumes a reservoir distribution on means of the arms.
* **`POO`** [Black-box Optimization of Noisy Functions with Unknown Smoothness](https://papers.nips.cc/paper/5721-black-box-optimization-of-noisy-functions-with-unknown-smoothness), J-B. Grill et al., 2015.
* Adaptivity to Smoothness in X-armed Bandits, A. Locatelli and A. Carpentier, 2018. ([video](http://videocrm.ca/Machine18/Machine18-20180424-4-AlexandraCarpentier.mp4))

### Adversarial Bandits

* **`EXP3`** [The Non-stochastic Multi-armed Bandit Problem](http://homes.dsi.unimi.it/~cesabian/Pubblicazioni/J18.pdf), P. Auer et al., 2003.
	- EXP3 provides an upper bound of order O(sqrt(TKlog(K))) and a lower bound of O(sqrt(TK)) on the minimax rate.
	- The basic idea behind is to consider the policy as choosing a drawing probability distribution over the arms at each time step. Starting with a uniform distribution, this drawing distribution is updated according to the cumulative estimated gains at each time step.
* **`MOSS`** [Minimax Policies for Adversarial and Stochastic Bandits](https://hal-enpc.archives-ouvertes.fr/hal-00834882), J-Y. Audibert and S. Bubeck, 2009.

### Best Arm Identification

#### Fixed Budget

* **`UCB-E`** **`SR`** [Best Arm Identification in Multi-Armed Bandits](http://imagine.enpc.fr/publications/papers/COLT10.pdf), J-Y. Audibert and S. Bubeck, 2010.
	- Two fixed budget BAI algorithms are proposed in this paper. UCB-E is an UCB-liked algorithm, and SR is an elimination-typed algorithm in which one arm is eliminated in each phase.
* **`SH`** [Almost Optimal Exploration in Multi-Armed Bandits](http://proceedings.mlr.press/v28/karnin13.pdf), Z. Karnin et al., 2013.
	- Sequential Halving is an elimination-typed fixed-budget BAI algorithm that eliminated at each phase half of the arms.
	- We need at most T = O(H2*log(n)*log(log(n)/delta)) pulls.

#### Fixed Confidence

* **`RacingUnbiasedPF`** [Best Arm Identification in Multi-armed Bandits with Delayed Feedback](https://arxiv.org/abs/1803.10937), A. Grover et al., 2018.

#### Anytime

* **`TTPS`** **`TTVS`** **`TTTS`** [Simple Bayesian Algorithms for Best Arm Identification](https://arxiv.org/abs/1602.08448), D. Russo, 2016. ([video](https://www.youtube.com/watch?v=5Mb_IguFDmQ))
	- This paper describes three simple TS-liked algorithms for BAI problem. The original TS algorithm has a well-known drawback: in many cases, TS tends to exclusively focusing on one arm (probably the best arm under the current posterior distribution over the parameters). To avoid this, with a certain probability, we choose to sample another action, either according to the optimal action probabilities, either according to an utility function of the parameters, either according to the currently sampled parameters themselves.
* **`P1`** Best of Both Worlds: Stochastic & Adversarial Best Arm Identification, Y. Abbasi-Yadkori et al., 2018.

### Applications

* **`Hyperband`** [Hyperband: A Novel Bandit-Based Approach to Hyperparameter Optimization](https://arxiv.org/abs/1603.06560), L. Li et al., 2016. ([video](https://www.youtube.com/watch?v=5Mb_IguFDmQ), [demo](https://people.eecs.berkeley.edu/~kjamieson/hyperband.html))

### Others

