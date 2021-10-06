---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
sitemap: true
---
### Overview

|_Journal Publications_|
|:-|
|**Vipul Mann**, Venkat Venkatasubramanian. Retrosynthesis Prediction using Grammar-based Neural Machine Translation: An Information-Theoretic Approach. _Computers & Chemical Engineering_. (2021), doi: [10.1016/j.compchemeng.2021.107533](https://doi.org/10.1016/j.compchemeng.2021.107533)| 
|**Vipul Mann**, Venkat Venkatasubramanian. Predicting Chemical Reaction Outcomes: A Grammar Ontology-based Transformer Framework. _AIChE Journal_. (2021), doi: [10.1002/aic.17190](https://doi.org/10.1002/aic.17190)|
|**Vipul Mann**, Abhishek Sivaram, Laya Das, Venkat Venkatasubramanian. Robust and Efficient Swarm Communication Topologies for Hostile Environments. _Swarm and Evolutionary Computation_. (2021), doi: [10.1016/j.swevo.2021.100848](https://doi.org/10.1016/j.swevo.2021.100848) |
|**Vipul Mann**, Deepak Maurya, Arun Kumar Tangirala, and Shankar Narasimhan. Optimal Filtering and Residual Analysis in Errors-in-variables Model Identification. _Industrial and Engineering Chemistry Research_. (2020), doi: [10.1021/acs.iecr.9b04561](https://pubs.acs.org/doi/10.1021/acs.iecr.9b04561), [codebase (MATLAB implementation)](https://github.com/vupil/Optimal-Filtering-EIV-DIPCA)

|_Conferences_|
|:-|
|**Vipul Mann**, Venkat Venkatasubramanian. A Formal Grammar-Based Machine Learning Approach for Predicting Reaction Outcomes. _2020 Virtual AIChE Annual Meeting_. (2020), [Virtual AIChE Annual Meeting 2020](https://www.aiche.org/academy/conferences/aiche-annual-meeting/2020/proceeding/paper/477c-formal-grammar-based-machine-learning-approach-predicting-reaction-outcomes) |
|**Vipul Mann**, Abhishek Sivaram, Laya Das, Venkat Venkatasubramanian. Optimal Communication Topologies for Particle Swarm Optimization under Hostile Environments. _2020 Virtual AIChE Annual Meeting_. (2020), [Virtual AIChE Annual Meeting 2020](https://www.aiche.org/academy/conferences/aiche-annual-meeting/2020/proceeding/paper/339j-optimal-communication-topologies-particle-swarm-optimization-under-hostile-environments) |
|**Vipul Mann**, Arun Kumar Tangirala, and Shankar Narasimhan. Linear Dynamic Model Identification and Data Reconciliation using Dynamic Iterative PCA (DIPCA). _AIChE 2017 Spring Meeting and 13th Global Congress on Process Safety_. (2017), [AIChE 2017 Spring Meeting](https://aiche.confex.com/aiche/s17/webprogram/Paper481511.html) |


***

## Journal Publications

### Retrosynthesis Prediction using Grammar-based Neural Machine Translation: An Information-Theoretic Approach
#### _Vipul Mann, Venkat Venkatasubramanian_  | April 2021 | [doi: 10.26434/chemrxiv.14410442.v1](https://doi.org/10.26434/chemrxiv.14410442.v1)

<font size="3"><b>Abstract</b><br>
<ul> <li> Retrosynthetic prediction is one of the main challenges in chemical synthesis that requires identifying reaction pathways and precursor molecules for synthesizing a target molecule. This requires a search over the space of plausible chemical reactions that often results in complex, multi-step, branched synthesis trees for even moderately complex organic reactions. Here, we propose an approach that performs single-step retrosynthesis prediction using SMILES grammar-based representations in a neural machine translation framework. Information-theoretic analyses of such grammar-representations reveal that they are both superior and well-suited for machine learning tasks due to their underlying redundancy and high information capacity compared to purely character-based representations. We report the top-1 prediction accuracy of 43.8% (top-5 measure of 61.4%) and syntactic validity of 95.6% (top-5 measure of 91.6%) on a standard reaction dataset. Comparing our model's performance with previous work that used purely character-based SMILES representations demonstrate improved accuracy and reduced grammatically invalid predictions.</li>
</ul>
</font>

### Predicting Chemical Reaction Outcomes: A Grammar Ontology-based Transformer Framework  
#### _Vipul Mann, Venkat Venkatasubramanian_  | January 2021 | [doi: 10.1002/aic.17190](https://doi.org/10.1002/aic.17190), [article](../files/16992231.pdf)

<font size="3"><b>Abstract</b><br>
<ul> <li> Discovering and designing novel materials is a challenging problem as it often requires searching through a combinatorially large space of potential candidates, typically requiring great amounts of effort, time, expertise, and money. The ability to predict reaction outcomes without performing extensive experiments is, therefore, important. Toward that goal, we report an approach that uses context‐free grammar‐based representations of molecules in a neural machine translation framework. This involves discovering the transformations from the source sequence (comprising the reactants and agents) to the target sequence (comprising the major product) in the reaction. The grammar ontology‐based representation hierarchically incorporates rich molecular‐structure information, ensures syntactic validity of predictions, and overcomes over‐parameterization in complex machine learning architectures. We achieve an accuracy of 80.1% (86.3% top‐2 accuracy) and 99% syntactic validity of predictions on a standard reaction dataset. Moreover, our model is characterized by only a fraction of the number of training parameters used in other similar works in this area.</li>
</ul>
</font>

  
###  Robust and Efficient Swarm Communication Topologies for Hostile Environments  
#### _Vipul Mann, Abhishek Sivaram, Laya Das, Venkat Venkatasubramanian_  | Februrary 2021 | [doi: 10.1016/j.swevo.2021.100848](https://doi.org/10.1016/j.swevo.2021.100848)

<font size="3"><b>Abstract</b><br>
<ul>
  <li>Swarm Intelligence-based optimization techniques rely strongly on information communicated among agents during the search. These algorithms are generally used for solving challenging problems where the search function landscape, typically highly nonlinear, is not adequately known a priori and there are multiple local optima that could result in premature convergence for many algorithms. Furthermore, in certain applications, the search environment is hostile in the sense that the agents, and/or their communication channels, could get disrupted during the search, thereby adversely impacting the search performance. Such disruptions change the communication topology of the agents and hence the information available to them, ultimately influencing the performance of the algorithm. Here, we present a study of the impact of loss of agents on performance as a function of the initial network configuration. We use particle swarm optimization to optimize an objective function with multiple sub-optimal regions in a hostile environment and study its performance for a range of network topologies with loss of agents. The results reveal interesting trade-offs between efficiency, robustness, and overall performance for different topologies that are analyzed to discover general features of networks that maximize performance. We observe that small-world networks perform well under hostile conditions.</li>
</ul>
</font>

### Optimal Filtering and Residual Analysis in Errors-in-Variables Model Identification
#### _Vipul Mann, Deepak Maurya, Arun Kumar Tangirala, Shankar Narasimhan_  | January 2020 | [doi:10.1021/acs.iecr.9b04561](https://pubs.acs.org/doi/abs/10.1021/acs.iecr.9b04561) | [codebase (MATLAB implementation)](https://github.com/vupil/Optimal-Filtering-EIV-DIPCA)

<font size="3"><b>Abstract</b><br>
<ul>
  <li> Dynamic model identification from time series data is a critical component of process control, monitoring, and diagnosis. An important adjunct of model identification is the derivation of filtered estimates of the variables and consequent one-step-ahead prediction errors (residuals) which are very useful for model assessment and iterative model identification. In this work, we present an optimal filtering and residual generation method for the errors-in-variables (EIV) scenario, wherein both the input and output variable measurements are contaminated with errors. The main idea is to combine an EIV-identification strategy with the EIV-Kalman filter (EIV-KF) that is known to provide optimal filtered estimates and residuals of both inputs and outputs for a linear dynamical process in the EIV case. In this work, we combine the EIV-KF with the dynamic iterative principal component analysis (DIPCA) approach that has been recently developed for EIV model identification. This work assumes prominence in that the optimally generated residuals are critical to the tasks of model assessment, fault detection, and diagnosis. The use of residuals in model assessment and reidentification is illustrated in this article, while pointing out that the use of DIPCA alone leads to nonunique filtered estimates and hence nonunique residuals. We remark that the proposed method can be used with any other EIV identification technique.</li>
</ul>
</font>


***

## Conference Publications

### A Formal Grammar-Based Machine Learning Approach for Predicting Reaction Outcomes
#### _Vipul Mann, Venkat Venkatasubramanian_ | November 2020 | [Virtual AIChE Annual Meeting 2020](https://www.aiche.org/academy/conferences/aiche-annual-meeting/2020/proceeding/paper/477c-formal-grammar-based-machine-learning-approach-predicting-reaction-outcomes)  

<font size="3"><b>Abstract</b><br>
<ul>
  <li> Prediction of reaction outcomes without performing time-consuming experiments offers several invaluable advantages -- reducing experimentation costs due to elimination of highly improbable reactions, lowering the time to hypothesis-validation-and-correction, enabling high-throughput experimentation for complex reactions, and allowing significantly more time for analyzing the results. In recent years, machine learning techniques have been successfully applied in this area that, either directly or indirectly, address one or more of the above issues. A few areas of application include discovery of novel molecules with desired properties, understanding structure-property relationships, identifying catalysts for better reaction catalysis, and data-driven modeling of chemical reaction kinetics. The success of machine learning methods could largely be attributed to their inherent proficiency in capturing complex non-linear dependencies between various factors that govern the reaction systems. Here, we present an approach for predicting the most likely product of a reaction based on a given set of reactants and agents (catalysts, reaction medium). The structural properties of reactants and the product molecules are encoded based on a formal grammar, akin to context-free grammars (CFG) in the area of natural language processing (NLP), that essentially gives rise to a parse-tree representation of the molecule. This representation is used in a convolutional neural network architecture to model the structural transformations from a set of reactants to the most likely product of the reaction. The proposed framework could be used for rapid experimentation and analysis of reaction outcomes, especially if the molecules involved are less-known and structurally novel. In addition, the latent space of the neural network architecture could also be used to discover insights on the transformations from reactants to products in a given reaction under different conditions.</li>
</ul>
</font>

### Optimal Communication Topologies for Particle Swarm Optimization Under Hostile Environments
#### _Vipul Mann, Abhishek Sivaram, Laya Das, Venkat Venkatasubramanian_ | November 2020 | [Virtual AIChE Annual Meeting 2020](https://www.aiche.org/academy/conferences/aiche-annual-meeting/2020/proceeding/paper/339j-optimal-communication-topologies-particle-swarm-optimization-under-hostile-environments)  

<font size="3"><b>Abstract</b><br>
<ul>
  <li>A class of nature-inspired optimization techniques called swarm intelligence methods involves a systematic exploration and exploitation of the search-space through efficient information exchange between the constituent agents. Such algorithms are common in areas where the optimization problems are inherently difficult due to a lack of complete information about the function landscape, due to the presence of several local minima that could result in premature convergence, and more importantly due to the presence of hostile environments that could result in a partial loss of swarm agents during the exploration phase. Such hostile environments could be seen in applications involving the design of communication channels for efficient information dissemination to a target group, targeted drug-delivery where drug molecules search for the affected site before diffusing, and high-value target localization with a network of drones communicating among themselves. In this work, we study the impact of the loss of agents on the performance of such algorithms as a function of the initial communication topology. We use particle swarm optimization (PSO) to optimize an objective function with multiple sub-optimal regions in a hostile environment and study its performance for a range of network topologies under hostile conditions. The presence of a hostile environment results in changes in the swarm communication topologies during the search-space exploration resulting in varying performances for different initial network configurations. The results reveal interesting relationships between graph-theoretic properties and the algorithmic performance based on which general properties of networks that maximize performance are identified. Moreover, networks with small-world properties are seen to maximize performance under hostile conditions and outperform the standard network topologies. Although the findings of this work are based on performance of the PSO algorithm, the results are fairly generalizable, and should extend to algorithms that rely on efficient communication between agents while searching for an optimal solution.</li>
</ul>
</font>

### Linear Dynamic Model Identification and Data Reconciliation using Dynamic Iterative PCA (DIPCA)
#### _Vipul Mann, Arun Kumar Tangirala, Shankar Narasimhan_ | March 2017 | [AIChE Spring Meeting 2017](https://www.aiche.org/conferences/aiche-spring-meeting-and-global-congress-on-process-safety/2017/proceeding/paper/172a-linear-dynamic-model-identification-and-data-reconciliation-using-dynamic-iterative-pca-dipca)  

<font size="3"><b>Abstract</b><br>
<ul>
  <li> Identification of input-output models from data is of utmost relevance in chemical process industries and has applications in process monitoring, control and fault diagnosis. Input-output data used in such identification exercises often has measurement errors in both the variables. Model identification under such conditions translates to solving an errors-in-variables (EIV) problem which is difficult to solve using classical system identification techniques. A recently proposed method - Dynamic Iterative Principal Component Analysis (DIPCA) uses PCA framework to identify the process order, delay, model parameters, and
error variances. DIPCA, however, has certain shortcomings under small sample conditions which limit its practical applications. In this work, we address these shortcomings, namely ambiguity in order determination under small sample cases and arbitrary selection of stacking lag which leads to sub-optimal parameter estimates. We define a metric called ’d-selective eigenvalue ratio’, or d-SEVR that sharply identifies the true order even for small sample cases. We also demonstrate the existence of an optimal stacking lag corresponding to the lowest error in estimation of error-covariance matrix. Finally, we use the identified model to obtain reconciled estimates of variables using Kalman Filter.</li>
    </ul>
    </font>
