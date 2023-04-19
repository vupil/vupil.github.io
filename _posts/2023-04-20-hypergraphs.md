---
title: 'The Network of Organic Chemistry -- network statistics, insights, and AI applications'
date: 2023-04-11
permalink: /posts/2022/04/Hypergraph network of organic chemistry/
tags:
  - artificial intelligence
  - graph theory
  - computational chemisty
  - machine learning 
---

<div style="text-align: justify">


<p>Imagine we create a huge, single network of organic chemistry reactions where each uniques molecule is represented as a node and molecules that take part in a reaction are connected with directed edges. Such a network would be representative of the current reaction chemistry knowledge. Obviously, some nodes would be highly connected (common/reactive/efficient chemicals) than others (rare chemicals); but are there other interesting statistics and properties of this network that could shed some light on how reaction chemistry is structured? If we create such networks at different points in history, how have the statistics evolved over time?  Do chemistry networks also exhibit 'small-world' behavior? Can we extrapolate evolution of these properties over time to predict possible future trajectories? Are there any AI applications of such networks apart from merely satisying scientific curiosity?</p>

<p>To answer these questions accurately and consistently, the network representation has to be right. A directed graph is a natural choice with directed edges between reactant molecules and product molecules for each reaction. However, this is not efficient and introduces suprious edges. We therefore used hypergraphs for this study, a generalization of graphs where each (hyper) edge could connect any number of reactants to products and not just two. We computed statistics of this huge hypergraph of organic chemistry, studied its time evolution, and used random walks on the hypergraph to generate embeddings that are used in reaction classification. We show that the hypergraph representation is flexible, preserves reaction context, and uncovers hidden insights that are otherwise not apparent in a traditional directed graph representation of chemical reactions.</p>

<p>Consider four example reactions (R1, R2, R3, R4) involving five different molecules (A, B, C, D, E). The hypergraph representation for this is shown the figure below. Notice that each hyperedge represents a unique reaction and the annotations indicate the 'role' of a molecule as 'reactant (R)' or 'product (P)'. We create hypergraph networks using a standard reactions datset containing reactions reported from 1976-2016 with 487,724 reactions in total. We divided the data ino three regimes -- before 1985, 1985-2005, and after 2005, to study the time evolution of various graph-theoretic network statistics.</p>


<p style="text-align: center;"><img class="aligncenter size-full wp-image-123" src="/files/hypergraph-example.png" width="300" height="" /> &nbsp; &nbsp; &nbsp; &nbsp; <img class="aligncenter size-full wp-image-123" src="/files/hypergraph-entire.png" width="300" height="" /></p>
Figure 1: (left) Hypergraph-based representation where an entire reaction is represented using a single hyperedge and the annotations indicate the vertex ‘roles’ as product (P) or reactant (R) (right) Top-100 largest communities (cluster) in the network of organic chemistry showing clear regions of high and low densities along with an island community disconnected from the rest of the network.<br><br>
  
  
<h3>Network statistics and chemistry inferences</h3>
<p><b>Degree distribution:</b> The degree of a node in a graph is its number of incoming or outgoing edges. Degree distributions provide a general sense of the network structure and its connectivity pattern. Generating a degree distribution involves computing the degree (or number of edges) for each node and estimating the underlying probabilistic distribution that they follow. The incoming (product role) degree distribution for the hypergraph for the three time regimes is shown below.</p>

<p style="text-align: center;"><img class="aligncenter size-full wp-image-123" src="/files/degree-dist.png" width="300" height="" /></p>

<p>The degree distribution follows a scale-free (or power-law) distribution pointing towards existence of preferential linking meaning new nodes attach to existing nodes with probability proportinal to their degree. This implies that chemistry growth is largely driven by a relatively small set of highly important molecules that are highly connected (higher degree, k) and they have a higher likelihood of playing a central role in the discovery of new reactions. The scale-free parameter, alpha, has been increasing over time, indicating towards the accelerated growth nature of chemistry. A high alpha is attributed to higher initial attractiveness, meaning that isolated nodes (new chemicals) have higher non-zero probability of connection. Since the initial attractiveness is the highest and much different in regime 3 (after 2005) than the other two regimes, it could be inferred that in the recent years, there has been an emphasis on the rewiring of existing reactions to create connections between previously disconnected nodes, or the synthesis of rarer molecules -- both possible due to significant advances in computational and experimental chemistry. It becomes clear from the analysis on average shortest path length that the major driver of chemistry evolution in the recent years is the rewiring of existing reactions.</p>
  
<p style="text-align: center;"><img class="aligncenter size-full wp-image-123" src="/files/avg-path.png" width="300" height="" /></p>

  
<p><b>Average path length:</b> The average separation between the molecules (vertices) in terms of number of reactions (edges) is captured by the average path length of the network. We study average path length as a function of the number of nodes in the network using time-based step-forward sampling using 1%, 5%, 10%, 20%, 50% and 100% of the network in each regime. We observe that across both the representations, the average path length between the nodes decreases exponentially as the number of nodes in the networks is increased. Moreover, in both the cases, the average path lengths for the time regimes 1 and 2 are very similar to each other but the average path length for regime 3 is significantly higher than those in other two across all values of N. The phenomenon of decreasing path length as number of nodes is increased has been reported in the literature as network densification where the network grows more and more dense over time.</p>
  
<p>The average all pairs shortest distance for the hypergraph could be interpreted as separation between nodes (or molecules) in terms of number of reaction, since each hyperedge corresponds to a unique reaction and hence, there exists a one-to-one mapping between reactions and hyperedges. We observe that the network of organic chemistry is much more compact than previously understood with nearly 3.25 degrees of separation between molecules, pointing towards an even stronger small-world nature than previously observed with five degrees of separation (based on directed-graph based studies). In addition, in regime 3, we observe a significant upward shift of average separation across all values of N, suggesting that in the recent years, the discovery of complex chemistry has led to the synthesis of molecules via complex routes that has led to a relative increase in their average separation. However, as is evident by the exponentially decreasing average path length as the network grows (higher values of N) across all time regimes, the network exhibits the phenomenon of densification. Network densification takes place primarily due to the creation of links between existing nodes in the network rather than by the addition (or discovery) of new nodes and is characterized by shrinking diameter. Such densification suggests that chemistry has been evolving mostly based on the rewiring of existing reactions (edges) rather than the discovery of completely new molecules (nodes addition), that has brought the molecules closer to each other over time.</p>
  
  

  
