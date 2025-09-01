# Monte Carlo Guided Diffusion (MCGdiff)

This repository contains an experimental (partial) implementation of the algorithm introduced in the paper:  

> **Monte Carlo guided Diffusion for Bayesian linear inverse problems**  
> Gabriel Cardoso, Yazid Janati El Idrissi, Sylvain Le Corff and Eric Moulines (2023).

📄 [Paper link](https://arxiv.org/abs/2308.07983)

**Abstract :**

> Ill-posed linear inverse problems arise frequently in various applications, from computational
photography to medical imaging. A recent line of research exploits Bayesian inference with
informative priors to handle the ill-posedness of such problems. Amongst such priors, scorebased generative models (SGM) have recently been successfully applied to several different
inverse problems. In this study, we exploit the particular structure of the prior defined by
the SGM to define a sequence of intermediate linear inverse problems. As the noise level
decreases, the posteriors of these inverse problems get closer to the target posterior of the
original inverse problem. To sample from this sequence of posteriors, we propose the use of
Sequential Monte Carlo (SMC) methods. The proposed algorithm, $\texttt{MCGdiff}$, is shown to be
theoretically grounded and we provide numerical simulations showing that it outperforms
competing baselines when dealing with ill-posed inverse problems in a Bayesian setting.

It was developed as part of a **Simulation methods for generative models** during the Master 2 program in Data Science and Applied Mathematics at Sorbonne University. This work was carried out in collaboration with two other students: Sarah OUAHAB and Sheïma MEBARKA, as part of the course project.

---

## 📌 Project Overview  

Monte Carlo Guided Diffusion (MCGdiff) is a novel method for solving **Bayesian linear inverse problems** using **score-based generative models (SGMs)** as priors. 

The algorithm combines:  

- **Diffusion models** (forward and reverse stochastic processes)  
- **Sequential Monte Carlo (SMC)** sampling  
- **Bayesian inference** for posterior approximation  

The objective is to recover a latent signal or image from incomplete or noisy linear observations, while ensuring **theoretical guarantees** on the approximation of the posterior distribution.  

This implementation focuses on:  

- Reproducing the noiseless and noisy versions of MCGdiff as described in the paper.  
- Applying the method to toy datasets (e.g., Gaussian Mixture Models) and image-like data (MNIST).  
- Exploring extensions with classifier guidance and autoencoder-based guidance.  


### 📊 Results

- Particle-based approximation of the posterior distributions
- Recovery of missing dimensions in synthetic datasets
- Application to MNIST digits with guidance
- The results qualitatively reproduce the behavior described in the paper, although differences may arise due to implementation details and hyperparameter choices.


### ✨ Future Work

- Improve training of diffusion priors for complex datasets,
- Explore scalability to high-dimensional real-world inverse problems,
- Compare against other state-of-the-art methods (DDRM, DPS, SMCdiff).

---

### 📚 References

- Cardoso G., El Idrissi Y.J., Le Corff S. and Moulines E. (2023). Monte Carlo guided Diffusion for Bayesian linear inverse problems. arXiv:2308.07983.

### ⚙️ Repository Structure  

```{r, eval=FALSE}
# Repository tree

├── noiseless_implementation.ipynb                                                     # Main notebook with implementation and experiments
├── Monte_Carlo_guided_Diffusion_for_Bayesian_linear_inverse_problems.pdf              # Original paper
└── README.md                                                                          # Project documentation and references
