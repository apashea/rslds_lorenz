# rslds_lorenz
Experimental code using the `ssm` library for inferring discrete regimes and latent nonlinear dynamics from masked, noisy, high-dimensional time series using the rSLDS model and Lorenz attractor simulation.

This code implements a demonstration of a Recurrent Switching Linear Dynamical System (rSLDS) model for inferring discrete latent states and continuous dynamics from high-dimensional, masked, noisy observations simulated from the Lorenz attractor system. It begins by generating a time series trajectory from the three-dimensional Lorenz system, simulates high-dimensional binary observation data using a Bernoulli Generalized Linear Model (i.e. highly lossy), and applies a block mask to a portion of the observed time series to introduce missing data, emulating aspects of the experiment in (Linderman et. al, 2017). An rSLDS model from the Linderman Lab’s `ssm` library is then configured and fit to the masked observations, implementing variational EM and structured mean-field inference. The notebook visualizes the true Lorenz attractor, the nonlinear latent trajectory colored by inferred discrete regime, discrete regime time-series (highlighting the masked region), observed and true event probabilities, and inferred event probabilities and uncertainties. The workflow illustrates the power of rSLDS models for recovering interpretable latent dynamics and discrete state structure in partially observed, nonlinear, and noisy time series, relevant for neuroscience and dynamical systems applications.

See also:
- Linderman, S., Johnson, M., Miller, A., Adams, R., Blei, D. &amp; Paninski, L.. (2017). Bayesian Learning and Inference in Recurrent Switching Linear Dynamical Systems. <i>Proceedings of the 20th International Conference on Artificial Intelligence and Statistics</i>, in <i>Proceedings of Machine Learning Research</i> 54:914-922 Available from https://proceedings.mlr.press/v54/linderman17a.html.
- https://github.com/lindermanlab/ssm


