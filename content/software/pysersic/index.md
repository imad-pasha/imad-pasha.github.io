+++
image = "pysersic-fit.png"
date = "2020-01-21"
title = "pysersic"
+++

![](pysersic.png)

## A Python package for determining galaxy structural properties via Bayesian inference, accelerated with jax

``pysersic`` is a Python package for fitting Sersic (and other) profiles to astronomical images using Bayesian inference. It is built using the jax framework with inference performed using the numpyro probabilistic programming library.

The code is hosted on GitHub and is available open source under the MIT license. 



The empirically derived Sérsic profile is the most common parametric form for the surface-brightness profile as it provides a reasonable approximation to nearly all galaxies, given the additional freedom of the Sérsic index over fixed-index profiles. Given the long history of Sérsic fitting codes with many available tools, the development of pysersic was largely motivated by two related factors, first and foremost of which was the desire to implement Sérsic fitting in a fully Bayesian context at speed. The ability to place the typical Sérsic fitting problem into a Bayesian context with runtimes that are not prohibitive (the traditional drawback of MCMC methods) has recently been unlocked by the second motivation: to leverage the `jax` library. `jax` utilizes just-in-time compilation to decrease computational runtimes, provides seamless integration with hardware accelerators such as graphics processing units (GPUs) for further improvements in performance, and enables automatic differentiation, facilitating gradient based optimization and sampling methods. Together, these features greatly increase speed and efficiency, especially when sampling or optimizing a large number of parameters.

- Code repo: [https://github.com/pysersic/pysersic](https://github.com/pysersic/pysersic)
- Docs: [https://pysersic.readthedocs.io/en/latest/](https://pysersic.readthedocs.io/en/latest/)
- arXiv: [https://arxiv.org/abs/2306.05454](https://arxiv.org/abs/2306.05454)
- JOSS: [https://doi.org/10.21105/joss.05703](https://doi.org/10.21105/joss.05703)

![](https://pysersic.readthedocs.io/en/latest/_images/example-fit_18_0.png)