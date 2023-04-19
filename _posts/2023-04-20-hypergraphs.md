---
title: 'The Network of Organic Chemistry -- hypergraphs, evolution, statistics, and AI applications'
date: 2023-04-11
permalink: /posts/2022/04/Hypergraph network of organic chemistry/
tags:
  - artificial intelligence
  - graph theory
  - computational chemisty
  - machine learning 
---

<div style="text-align: justify">


<p>Imagine we create a huge, single network of organic chemistry reactions where each uniques molecule is represented as a node and molecules that take part in a reaction are connected with directed edges. Such a network would be representative of the current reaction chemistry knowledge. Obviously, some nodes would be highly connected (common/reactive/efficient chemicals) than others (rare chemicals); but are there other interesting statistics and properties of this network that could shed some light on how reaction chemistry is structured? If we create such networks at different points in history, how have the statistics evolved over time? Can we extrapolate evolution of these properties over time to predict possible future trajectories? Are there any AI applications of such networks apart from merely satisying scientific curiosity?</p>

<p>To answer these questions accurately and consistently, the network representation has to be right. A directed graph is a natural choice with directed edges between reactant molecules and product molecules for each reaction. However, this is not efficient and introduces suprious edges. We therefore used hypergraphs for this study, a generalization of graphs where each (hyper) edge could connect any number of reactants to products and not just two. We computed statistics of this huge hypergraph of organic chemistry, studied its time evolution, and used random walks on the hypergraph to generate embeddings that are used in reaction classification. We show that the hypergraph representation is flexible, preserves reaction context, and uncovers hidden insights that are otherwise not apparent in a traditional directed graph representation of chemical reactions.</p>

<p>Consider four example reactions (R1, R2, R3, R4) involving five different molecules (A, B, C, D, E). The hypergraph representation for this is shown the figure below. Notice that each hyperedge represents a unique reaction and the annotations indicate the 'role' of a molecule as 'reactant (R)' or 'product (P)'. We create hypergraph networks using a standard reactions datset containing reactions reported from 1976-2016 with 487,724 reactions in total. We divided the data ino three regimes -- before 1985, 1985-2005, and after 2005, to study the time evolution of various graph-theoretic network statistics.</p>


<p style="text-align: center;"><img class="aligncenter size-full wp-image-123" src="/files/hypergraph-example.png" width="400" height="" /> &nbsp; &nbsp; &nbsp; &nbsp; <img class="aligncenter size-full wp-image-123" src="/files/hypergraph-entire.png" width="400" height="" /></p>
Figure 1: (left) Hypergraph-based representation where an entire reaction is represented using a single hyperedge and the annotations indicate the vertex ‘roles’ as product (P) or reactant (R) (right) Top-100 largest communities (cluster) in the network of organic chemistry showing clear regions of high and low densities along with an island community disconnected from the rest of the network.<br><br>


