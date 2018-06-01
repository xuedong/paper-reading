# Numerical Optimization

## Summary

* [Convex Optimization](#convex-optimization)
* [Local Optimization](#local-optimization)
* [Global Optimization with Deterministic Approaches](#global-optimization-with-deterministic-approaches)
* [Global Optimization with Stochastic Approaches](#global-optimization-with-stochastic-approaches)

## Papers

### Convex Optimization

### Local Optimization

* **`L-BFGS`** [On the Limited Memory BFGS Method for Large Scale Optimization](https://pdfs.semanticscholar.org/171c/4f717089b70ac98f348f4d3497f1b440bdaf.pdf), D. Liu and J. Nocedal, 1989.
	- L-BFGS requires the knowledge of the derivatives.

### Global Optimization with Deterministic Approaches

* **`DIRECT`** [Lipschitzian Optimization without the Lipschitz Constant](https://link.springer.com/article/10.1007/BF00941892), D. Jones et al., 1993.
* **`CMA-ES`** [Adapting Arbitrary Normal Mutation. Distributions in Evolution Strategies: The Covariance Matrix Adaptation](https://ieeexplore.ieee.org/document/542381/), N. Hansen and A. Ostermeier, 1996.
	- CMA-ES is derivative-free.

### Global Optimization with Stochastic Approaches

* **`GP-UCB`** [Gaussian Process Optimization in the Bandit Setting: No Regret and Experimental Design](https://arxiv.org/abs/0912.3995), N. Srinivas et al., 2010.
	- GP-UCB invokes an UCB term to decide which point to sample next (acquisition function), and provides a regret bound of O(sqrt(gamma(T)T)), where gamma(T) is the maximum information gain between function values and noisy samples of the first T observations.
	- The guarantee of GP-UCB ensures sub-linear regret for some kernels of interest, however, it lacks of algorithm-independent lower bound.
* [A Tutorial on Bayesian Optimization of Expensive Cost Functions, with Application to Active User Modeling and Hierarchical Reinforcement Learning](https://arxiv.org/abs/1012.2599), E. Brochu et al., 2010.
	- Bayesian optimization is based on the famous Bayes rule. In principle, we assume some prior knowledge on the objective function f to be optimized. We then update to some posterior while gathering evidence along with all previous observations.
	- GP prior is one of the most investigated prior for BO. It can be considered as some "random function" while instead of returning a function value, it returns the mean and variance of a Gaussian distribution over the possible values of f at the current sampled point x.
	- Since GP is characterized by its mean function and covariance function, it is of great importance to choose the kernel/covariance function. Typical kernels are **`SE`** kernel (squared exponential) and **`Matérn`** kernel.
	- The next step is to choose some acquisition/utility function that we optimize over the GP, so that we can decide which point to sample next. Common acquisition functions include **`PI`** (probability of improvement), **`EI`** (expected improvement) and **`GP-UCB`**, etc. 
* [Maximizing Acquisition Functions for Bayesian Optimization](https://arxiv.org/abs/1805.10196), J. Wilson et al., 2018.
	- In this paper, the authors investigated two approaches for addressing BO's inner optimization problem, namely the differentiability of Monte Carlo integration and the submodularity of parallel querying.
* [Tight Regret Bounds for Bayesian Optimization in One Dimension](https://arxiv.org/abs/1805.11792), J. Scarlett, 2018.
	- The authors provide a lower bound of Omega(sqrt(T)) and an upper bound of O(sqrt(Tlog(T))) for BO over one dimensional functions under some mild assumptionson the kernel (e.g. SE and Matérn kernel satisfy these assumptions).
	- The lower bound provided is the first one in a noisy Bayesian setting.

