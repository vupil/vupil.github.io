---
layout: archive
title: "CV"
permalink: /experience/
author_profile: true
---


### Education and Training

|Time|Degree|School|
|:-|:-|:-|
|09/2019 - Present | Ph.D. Candidate, Chemical Engineering | Columbia University
|05/2017|Master of Technology (Dual Degree), Chemical Engineering | Indian Institute of Technology Madras
|05/2016|Bachelor of Technology (Dual Degree), Chemical Engineering |Indian Institute of Technology Madras


### Publications and Presentations

|Publications|
|:-|
|**Vipul Mann**, Abhishek Sivaram, Laya Das, Venkat Venkatasubramanian. Robust and Efficient Swarm Communication Topologies for Hostile Environments. _Swarm and Evolutionary Computation, March 2020_, **Submitted**|
|**Vipul Mann**, Deepak Maurya, Arun Kumar Tangirala, and Shankar Narasimhan. Optimal Filtering and Residual Analysis in Errors-in-variables Model Identification. _Industrial and Engineering Chemistry Research (2020)_, January 2020 ([PDF](../files/iecr_paper1.pdf))|
|**Vipul Mann**, Arun Kumar Tangirala, and Shankar Narasimhan. Linear Dynamic Model Identification and Data Reconciliation using Dynamic Iterative PCA (DIPCA). _AIChE 2017 Spring Meeting and 13th Global Congress on Process Safety_, March 2017|

### Teaching

|Time|Role|Course|Affiliation|
|:-|:-|:-|:-|
|Fall 2019|Teaching Assistant|Math Methods in Chemical Engineering (Graduate)|Columbia University|
|Spring 2017|Teaching Assistant| Introduction to Statistical Hypothesis Testing (Graduate)| IIT Madras|
|Fall 2016|Teaching Assistant|Applied Time Series Analysis (Graduate)|IIT Madras|

### Professional Service

|Time|Role|Organization|
|:-|:-|:-|
|02/2020 - Present|Reviewer|Journal of Computers and Chemical Engineering|

### Technical Strengths

|Category|Skills|
|:-|:-|
|Language           |Python, R, MATLAB, SQL, HTML, and LaTeX|
|Simulation         |SimuLink and Aspen HYSYS|

### Projects

<font size="2"><b>Modeling Enhanced Enzyme Diffusion in the Presence of Substrates</b><br>
Advisor: Prof. Kyle Bishop | Sep 2019 - Nov 2019  
<ul>
<li>Modeled enhanced enzyme diffusion using a Bayesian data analysis framework in Python; used enzyme trajectories data obtained from single molecule imaging techniques for tracking enzyme movements </li>
<li> Evaluated possibility of anisotropic diffusion through a statistical hypothesis test using F-test on displacements </li>
<li>Proposed Markov-Chain Monte Carlo (MCMC) simulations combined with k-means clustering for modeling diffusion for the different enzyme oligomerization forms; obtained probabilistic distributions capturing uncertainty in the estimates </li>
<li> Demonstrated significant variations in diffusion coefficients across the possible oligomerization states of the enzyme </li>
</ul>
</font>

<font size="2"><b>Machine Learning for Sports Analytics with ESPN-cricinfo</b><br>
Advisor: Prof. Raghunathan Rengaswamy | Nov 2018 - March 2019
<ul>
<li> Used ESPN's ball-by-ball historical dataset for cricket matches in the past 15 years to build a machine learning tool for predicting match scores, quantifying impactful match events, and generating 'smart statistics' for players </li>
<li> Implemented a recurrent neural network (RNN) and evaluated its performance in modeling the game dynamics </li>
<li> Built modules in Python for performing optimal balls-allocation between bowlers and batsmen, estimating wicket probability at a given state, and estimating match-win probabilities by factoring in both historical data and current </li>
<li> Combined all the modules together to build an interactive match-simulation tool with quantification of impactful events </li>
<li> This tool was used by ESPN-cricinfo during the Indian Premiere League 2019 and ICC World Cup 2019 worldwide </li>
</ul>
</font>

<font size="2"><b>Anomaly Detection and Prediction for Aluminum Smelting Operations</b><br>
Advisor: Prof. Raghunathan Rengaswamy | July 2018 - Oct 2018
<ul>
<li> Built an L1 trend-extraction routine in Python with built-in hyperparameter estimation module for a piecewise linear trend extraction on any general time-series signal; core of the algorithm uses CVXOPT for optimization </li>
<li> Implemented a fuzzy variant of C-means clustering on the estimated linear trends to identify sub-optimal, or anomalous operating regimes through clustering of the operating regimes based on a pre-defined optimality criterion </li>
<li> Performed subspace angle comparisons between principal vectors to assess cluster separations and derive process insights </li>
<li> Integrated all the three modules as a Python package and shipped to the end user with Sphinx generated documentation </li>
</ul>
</font>

<font size="2"><b>Optimal Filtering using PCA based Dynamic Models</b><br>
Advisor: Prof. Arun Tangirala and Prof. Shankar Narasimhan | June 2016 - May 2017
<ul>
<li> Studied and implemented a novel identification technique called dynamic iterative principal component analysis (DIPCA) in MATLAB that takes in process data and estimates model order, parameters, and measurement error variances </li>
<li> Proposed a layered optimal data reconciliation and model validation approach based on an errors-in-variables Kalman-filter to handle dynamic input-output variables that the principal component analysis (PCA) framework is unable to handle </li>
<li> Demonstrated efficacy of this approach on a physical 'two-tank liquid level' case study in obtaining noise-free variable estimates and performing a selective model validation similar to residual analysis in classical system identification </li>
</ul>
</font>

<font size="2"> <b>Historical Data Mining and System Identification</b><br>
Advisor: Dr. Kaushik Ghosh, ASEA Brown Boveri (ABB) Research Centre | May 2015 - Aug 2015
<ul>
<li> Implemented a novel segment identification algorithm in MATLAB to identify 'good regions' in historical databases </li>
<li> Comparatively analyzed an iterative-autoregressive exogenous (ARX) algorithm with the existing system identification algorithm at ABB; proposed changes to make the algorithm more robust towards high noise conditions </li>
<li> Proposed unification of segment identification and iterative ARX algorithms for use in ABB's model identification toolbox </li>
</ul>
</font>

<font size="2"> <b>SARIMA modeling and Speech Data Analysis using Spectrogram</b><br>
Advisor: Prof. Arun Tangirala | July 2015 - Dec 2015
<ul>
<li> Modeled monthly measles cases reported in New York City for the last 44 years using R as a Seasonal ARIMA model </li>
<li> Implemented spectrogram approach in R to separate noise from an overlapping amplitude and frequency modulated signal </li>
</ul>
</font>
