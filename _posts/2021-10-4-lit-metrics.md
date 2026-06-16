---
layout: post
title: Econometrics Literature
date: 2021-10-4 9:00:00 --0000
permalink: /posts/lit-metrics/
---

This blog post continuously updates with papers in econometrics. Please let me know if you have any questions. You can get in touch with me by email. My email can be obtained through the "About" section of the blog.

This blog post has been updated on 9-28-2025.

* TOC
{:toc}

### Causal Inference
[Roth (2022)](https://doi.org/10.1257/aeri.20210236): Pretest with Caution: Event-Study Estimates after Testing for Parallel Trends
- AERI
- This paper points out two limitations to the test for parallel trends
    - Conventional pretests may have low power, meaning that preexisting trends that produce meaningful bias in the treatment effects estimates may not be detected with substantial probability
    - Conditioning the analysis on the result of a pre-trends test induces distortions to estimation and inference from pretesting. In other words, the draws of the data that survive a pretest are a selected sample from the true data-generationg process (DGP)

[Goodman-Bacon (2021)](https://drive.google.com/file/d/1gUg7INdzM9A1d1OqCFZjLg9a-BAxMBzf/view): Difference-in-Differences with Variation in Treatment Timing
- Journal of Econometrics

[Angrist (2021)](https://www.nber.org/papers/w29726): Empirical Strategies in Economics: Illuminating the Path from Cause to Effect
- Nobel lecture
- LATE/IV

[Pischke (2021)](https://voxeu.org/article/natural-experimenters-nobel-laureates-david-card-joshua-angrist-and-guido-imbens): Natural experiments in labour economics and beyond: The 2021 Nobel laureates David Card, Joshua Angrist, and Guido Imbens

[Mogstad, Torgovitsky & Walters (2021)](https://pubs.aeaweb.org/doi/pdfplus/10.1257/aer.20190221): The Causal Interpretation of Two-Stage Least Squares with Multiple Instrumental Variables
- Empirical researchers often combine multiple instrumental variables (IVs) for a single treatment using two-stage least squares (2SLS). When treatment effects are heterogeneous, a common justification for including multiple IVs is that the 2SLS estimand can be given a causal interpretation as a positively weighted average of local average treatment effects (LATE). This justification requires the well-known monotonicity condition.
- They show that with more than one instrument, this condition can only be satisfied if choice behavior is effectively homogeneous.
- Based on this finding, they consider the use of multiple IVs under a weaker, partial monotonicity condition. They characterize empirically verifiable sufficient and necessary conditions for the 2SLS estimand to be a positively weighted average of LATEs under partial monotonicity.
- They apply these results to an empirical analysis of the returns to college with multiple instruments. They show that the standard monotonicity condition is at odds with the data. Nevertheless, their empirical checks reveal that the 2SLS estimate retains a causal interpretation as a positively weighted average of the effects of college attendance among complier groups.

[Broderick, Giordano & Meager (2021)](https://arxiv.org/pdf/2011.14999.pdf): An Automatic Finite-Sample Robustness Metric: Can Dropping a Little Data Change Conclusions?
- They found a way to assess the robustness of regression results by removing a small number of observations
    - They invented a framework for selecting observations to remove such that they have the largest impact on the regression result
        - This method is called Approximate Maximum Influence Perturbation
- For the observations selected, the metric records the lower bound of the difference between the original estimator and the new estimator. Therefore, as long as the metric indicates a violation of robustness, the original estimator should be re-examined

[Liu, Poirier & Shiu (2021)](https://arxiv.org/abs/2105.12891): Identification and Estimation of Average Partial Effects in Semiparametric Binary Response Panel Models
- The paper point-identify APE in binary response panel models under an index sufficiency assumption on the unobserved heterogeneity
- Three-step semiparametric estimator:
    - Estimate the common parameters
    - Estimate the conditional expectation of the outcomes given the indices and a generated regressor that depends on first-step estimates
    - Avg derivatives of this conditional expectation to obtain a partial mean that estimates the APE

[Feng (2021)](https://drive.google.com/file/d/1Kddkh705vk-1uhq0y5xYXWNdTabmclcN/view): Causal Inference in Possibly Nonlinear Factor Models
- Treatment effects models with noisily measured confounders
    - Noisy measurements are associated with the underlying latent confounders through an unknown, possibily nonlinear factor structure
        - The main building block is a local principal subspace approximation procedure that combines K-nearest neighbors matching and principal component analysis

[Kwon (2021)](https://soonwookwon.github.io/files/Soonwoo_Kwon_JMP.pdf): Optimal Shrinkage Estimation of Fixed Effects in Linear Panel Data Models
- The set of shrinkage estimators in comparison includes conventional estimators
- Compared to conventional estimators, the optimal estimator allows the fixed effect to vary with time and to be serially correlated. It also does not require distributional assumptions.
- Optimized R package, FEShR

[Agarwal, Shah, Shen (2021)](https://arxiv.org/pdf/2006.07691.pdf): Synthetic Interventions
- If there are M groups and N trials, how to reduce the number of trials per group and achieve similar estimation results
- Uses synthetic control methods

[Butcher, Moran & Watson (2021)](https://www.nber.org/system/files/working_papers/w29520/w29520.pdf?utm_campaign=PANTHEON_STRIPPED&amp%3Butm_medium=PANTHEON_STRIPPED&amp%3Butm_source=PANTHEON_STRIPPED): IMMIGRANT LABOR AND THE INSTITUTIONALIZATION OF THE U.S.-BORN ELDERLY
- Shift-share instrument

[Arkhangelsky, Athey, Hirshberg, Imbens & Wager (2021)](https://pubs.aeaweb.org/doi/pdfplus/10.1257/aer.20190159): Synthetic Difference-in-Differences
- Applicable when treatment starts in the same time period for every unit
- [R Package](https://github.com/synth-inference/synthdid)

#### IV
[Borusyak, Hull, and Jaravel (2024)](https://www.doi.org/10.3386/w33236): A Practical Guide to Shift-Share Instruments
- Present the core logic of both many exogenous shifts or many exogenous shares

[Mikusheva & Shapiro (2022)](https://pubs.aeaweb.org/doi/pdfplus/10.1257/jep.36.1.177): Isaiah Andrews, 2021 John Bates Clark Medalist
- Weak instruments

#### RCT
[Xiong, Chin, Taylor, Athey (2022)](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=lg_0u-0AAAAJ&citation_for_view=lg_0u-0AAAAJ:9ZlFYXVOiuMC): small sample size

[Nie, Imbens & Wager (2021)](https://arxiv.org/pdf/2112.04723.pdf): Covariate Balancing Sensitivity Analysis for Extrapolating Randomized Trials across Locations

#### Regression Discontinuity
[Cattaneo, Keele & Titiunik (2021)](https://arxiv.org/pdf/2110.08410.pdf): Covariate Adjustment in Regression Discontinuity Designs

#### Synthetic control
[Cattaneo, Feng, Palomba & Titiunik (2022)](https://arxiv.org/pdf/2202.05984.pdf): scpi: Uncertainty Quantification for Synthetic Control Estimators
- package for Python, R, and Stata

#### Peer Effects Model
[Li & Wager (2022)](https://arxiv.org/pdf/2202.05356.pdf): Network Interference in Micro-Randomized Trials
- When an individual's outcome could depend on other individuals' treatments and outcomes

Solvsten (2021): Estimation and Inference in a Peer Effects Model with Heteroskedasticity

#### Clustering
- [Abadie, Athey, Imbens & Wooldridge (2021)](https://economics.mit.edu/faculty/abadie/papers): Clustering Adjustments to Standard Errors
    - Liang-Zeger (cluster) vs Eiker-Huber-White (heterogeneity-robust) variances - can be inaccurate
    - proposed estimator is more accurate
        - In cross-sectional settings where there are many clusters
    - Takeaway: should think about sampling and assignment mechanism

#### Misc
- [Graham, Hirano, Imbens (2021)](https://doi.org/10.1017/S0266466621000372): the ET Interview: Professor Gary Chamberlain
    - Econometric Theory
    - Summary: multivariable regression resulted from the siblings work, probably inspired the individual fixed effects.

#### Mixture Models
- [Kwon & Mbakop (2021)](https://wpsites.ucalgary.ca/eric-mbakop/wp-content/uploads/sites/32/2020/06/Revision.pdf): Estimation of the Number of Components of Non-parametric Multivariate Finite Mixture Models
    - Published in: Annals of Statistics
    - Propose a novel estimator for the number of mixture components (denoted by M) in a non-parametric finite mixture model
    - Setting: The analyst has repeated observations of K >= 2 variables that are conditionally independent given a finitely supported latent variable with M support points
    - Condition: an integral operator T that is identified from the data has rank equal to M (under a mild assumption on the joint distribution of the observed and latent variables)
    - Propose: an estimator of M which consists of a thresholding rule that counts the number of singular values of a consistent estimator of T that are greater than a data-driven threshold.
    - Prove: 
        - Their estimator of M is consistent
        - Establish non-asymptotic results which provide finite sample performance guarantees for their estimators
    - Monte Carlo study which shows that their estimator performs well for samples of moderate size

#### Kernel Density Estimation
[Cattaneo, Chandak, Jansson & Ma (2022)](https://arxiv.org/pdf/2204.10375.pdf): lpcde: Local Polynomial Conditional Density Estimation and Inference
- Published in the R Journal and ArXiv
- This paper discusses the R package lpcde, which stands for local polynomial conditional density estimation
- It implements the kernel-based local polynomial smoothing methods introduced in [Cattaneo, Chandak, Jansson, and Ma (2022)]()

[Cattaneo, Feng & Underwood (2022)](https://arxiv.org/pdf/2201.05967.pdf): Uniform Inference for Kernel Density Estimators with Dyadic Data

#### Policy evaluation
- [Arkhangelsky & Korovkin (2021)](https://arxiv.org/pdf/1905.13660.pdf): On Policy Evaluation with Aggregate Time-Series Shocks
    - New algorithm for estimating treatment effects
        - When exogenous variation comes from aggregate time-series shocks
    - Estimator combines data-driven unit-level weights with a time-series model
    - Use the unit weights to control for unobserved aggregate confounders
    - Use the time-series model to extract the quasi-random variation from the observed shock

- [Cattaneo and Titiunik (2024)](https://arxiv.org/pdf/2402.11640.pdf): Protocols for Observational Studies: An Application to Regression Discontinuity Designs
    - How to craft a pre-analysis plan.

### Machine Learning
- [Chetverikov and Sørensen (2025)](https://doi.org/10.1086/736770): Selecting Penalty Parameters of High Dimensional M-Estimators Using Bootstrapping after Cross Validation
    - New method for selecting penalty parameters for lasso regressions
    - Verified using policing ratial bias data

- [Montiel Olea, Ke, and Nesbit (2021)](http://www.joseluismontielolea.com/papers.html): Robust Machine Learning Algorithms for Text Analysis
    - Standard text analysis methods have flat regions
    - Use Bayesian methods to remove the problem

#### Causal Random Forest
- [Sverdrup, et al (2026)](https://cloud.r-project.org/web/packages/grf/vignettes/grf_guide.pdf): An introduction to grf
    - Gives technical background for the R package that handles causal random forest
    - Gives two examples


### Partial Identification
[Manski (2022)](https://faculty.wcas.northwestern.edu/~cfm754/identification_statistical_decision_theory.pdf): IDENTIFICATION AND STATISTICAL DECISION THEORY
- Uses sampling to randomize choice when partial identification in statistical decision theory requires criteria such as minimax regret.


[Cattaneo, Cheung, Ma & Masatlioglu (2021)](https://arxiv.org/pdf/2110.10650.pdf): Attention Overload
- They introduce an Attention Overload Model that captures the idea that alternatives compete for the decision marker's attention, and hence the attention frequency each alternative receives decreases as the choice problem becomes larger.
- Using this nonparametric restriction on the random attention formation, they show that a fruitful revealed preference theory can be developed, and provide testable implications on the observed choice behavior that can be used to partially identify the decision maker's preference.
- They also provide novel partial identification results on the underlying attention frequency, thereby offering the first nonparametric identification result of (a feature of) the random attention formation mechanism in the literature.
- Building on their partial identification results, for both preferences and attention frequency, they develop econometric methods for estimation and inference.
    - The procedures remain valid even in settings with large number of alternatives and choice problems.
- They also provide a software package in R implementing their empirical methods, and illustrate them in a simulation study.


### Short-term vs long-term estimation
[Imbens, Kallus, Mao & Wang (2022)](https://arxiv.org/pdf/2202.07234.pdf): Long-term Causal Inference Under Persistent Confounding via
Data Combination

### Discrete choice estimation
[Christensen, Moon, and Schorfheide (2022)](https://arxiv.org/pdf/2204.11748.pdf): Optimal Discrete Decisions when Payoffs are Partially Identified
- Published in ArXiv
- This paper derives optimal statistical decision rules for discrete choice problems when the decision maker is unable to discriminate among a set of payoff distributions.
- The decision maker must confront both model uncertainty (about the identity of the true payoff distribution) and statistical uncertainty (the set of payoff distributions must be estimated)
- Efficient-robust decision rules, which minimize maximum risk or regret over the set of payoff distributions and which use the data to learn efficiently about features of the set of payoff distributions germane to the choice problem, are optimal and can dominate seemingly natural alternatives.

### Social network modeling
[Lewbel, Qu, and Tang (2022)](https://doi.org/10.1086/722090): Social Networks with Unobserved Links
- JPE just accepted
- Point identify and estimate linear social network models without observing any network links
- Required data consist of many small networks of individuals, such as classrooms or villgaes, with individuals that are each only observed once
