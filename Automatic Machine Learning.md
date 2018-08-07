# Automatic Machine Learning

## Summary

* [Hyperparameter Optimization](#hyperparameter-optimization)
* [Model Search](#model-search)
* [Meta Learning](#meta-learning)

## Papers

### Hyperparameter Optimization

* **`Hyperband`** [Hyperband: A Novel Bandit-Based Approach to Hyperparameter Optimization](https://arxiv.org/abs/1603.06560), L. Li et al., 2016. ([video](https://www.youtube.com/watch?v=5Mb_IguFDmQ), [demo](https://people.eecs.berkeley.edu/~kjamieson/hyperband.html))
	- This paper treats the hyper-parameter tuning problem as a non-stochastic infinitely many-armed bandit problem. It consists of several brackets that contains different number of configurations, and uses Sequential Halving as subroutine in each bracket with the same budget.
* **`BOHB`** [BOHB: Robust and Efficient Hyperparameter Optimization at Scale](https://arxiv.org/abs/1807.01774), S. Falkner et al., 2018.
	- Bayesian optimization (in particular, TPE) combined with Hyperband.

### Model Search

* [Towards Automated Deep Learning: Efficient Joint Neural Architecture and Hyperparameter Search](https://arxiv.org/abs/1807.06906), A. Zela et al., 2018.

### Meta Learning

* **`Reverse-HG`** [Bilevel Programming for Hyperparameter Optimization and Meta-Learning](https://arxiv.org/abs/1806.04910), L. Franceschi et al., 2018.
