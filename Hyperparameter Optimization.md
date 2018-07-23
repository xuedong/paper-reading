# Hyperparameter Optimization

## Papers

* **`Hyperband`** [Hyperband: A Novel Bandit-Based Approach to Hyperparameter Optimization](https://arxiv.org/abs/1603.06560), L. Li et al., 2016. ([video](https://www.youtube.com/watch?v=5Mb_IguFDmQ), [demo](https://people.eecs.berkeley.edu/~kjamieson/hyperband.html))
	- This paper treats the hyper-parameter tuning problem as a non-stochastic infinitely many-armed bandit problem. It consists of several brackets that contains different number of configurations, and uses Sequential Halving as subroutine in each bracket with the same budget.
* **`BOHB`** [BOHB: Robust and Efficient Hyperparameter Optimization at Scale](https://arxiv.org/abs/1807.01774), S. Falkner et al., 2018.
	- Bayesian optimization (in particular, TPE) combined with Hyperband.

