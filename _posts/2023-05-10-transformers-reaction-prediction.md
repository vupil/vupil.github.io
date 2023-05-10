---
title: 'Chemistry-informed Transformers for Reaction Prediction and Retrosynthesis based on SMILES grammar'
date: 2023-54-10
permalink: /posts/2022/04/SMILES grammar transformers for reactions/
tags:
  - artificial intelligence
  - retrosynthesis
  - computational chemisty
  - reaction prediction
---

<div style="text-align: justify">


<p>The transformer architecture has remarkably improved the accuracy of sequence modeling tasks (eg. language translation) but could they be used to model chemical reactions? Do chemical reactions have some similarity with natural language that allows for the use of powerful transformer-inspired architectures? How would the molecules be represented in such frameworks so that appropriate chemical structural information is captured? Are there other potential transformer-like architectures that could handle chemical representations better compared to the vanilla transformer model?</p>

<p>To use the transformer architecture, two requirements have to be satisfied -- first, chemicals participating in a reaction should be represented using text-based representations (akin to words in a sentence), and second, the reaction modeling problem needs to be formulated as a 'language translation' task. Thus, based on this analogy, participating chemicals are 'words' and left-hand-side of reactions are 'sentences' (in reactants language) that need to be 'translated' to the right-hand-side 'sentences' (in products language). Our series of works using this analogy first addressed the issue of using an appropriate chemical grammar-based representation followed by proposing a novel tree-transformer architecture that could perform the translation using molecular trees as input in a chemistry-aware manner.</p>

<p>The machine translation framework-based problem modeling is shown in the Figure 1 below. The forward translation (from reactants to products) is used to predict chemical reaction outcomes, and the inverse translation (from product to reactants) is used to solve the retrosynthesis problem. The first important question is how to represent the input and output molecules?</p>

<p style="text-align: center;"><img class="aligncenter size-full wp-image-123" src="/files/mt_framework.jpg" width="750" height="" /></p>
Figure 1: SMILES grammar-based representations for reaction prediction and retrosynthesis using machine translation framework. <br><br>

<p><b>Can we do better than SMILES representation? </b></p>
<p>The most commonly used representation is the SMILES representation where molecules are represented using a linear text-based notation. For instance, for say cyclopropane, the SMILES representation is C1CC1. While the SMILES representation is vastly used but contains little explicitly encoded chemical structural information. On the other hand, the grammar parse tree shown in Figure 2 contains additional relevant information. For instance, it contains information such as the number of aromatic carbon atoms, the presence of a ring-structure, the alternating double bonds in the ring, the presence of an aliphatic oxygen atom, and finally the active hydrogen atom attached to the oxygen atom. Moreover, this information is represented in a hierarchical manner, with the broadest class of rules at the top and increasingly more specific ones toward the bottom of the parse-tree. We thus proposed a SMILES grammar-based representation based on these parse trees for molecules. We showed that these representations are better from a model performance as well as information theoretic standpoint, since the conditional entropy (or uncertainty) associated with it is the lowest, thus aiding data-driven approaches in modeling and discovering patterns efficiently.</p>

  <p style="text-align: center;"><img class="aligncenter size-full wp-image-123" src="/files/cyclopropane.jpeg" width="450" height="" /></p>
Figure 2: The SMILES grammar parse-tree obtained for cyclopropane with the SMILES representation as C1CC1.<br><br>

<p><b>Can we do better than the vanilla transformer architecture?</b></p>
<p>The second important question to answer is can the transformer model be adapted to better handle hierarchical chemistry-informed molecular representations? This would allow for the entire grammar (instead of linearized SMILES grammar tree) to be input to the transformer architecture and preserve the structural hierarchy that is inherently encoded. To this end, we modified the transformer architecture and proposed a novel tree transformer architecture for modeling retrosynthesis problems as shown in Figure xx</p>

<p>To answer this question, let's look at a common text-based representation of molecules called the SMILES representation. For instance, for say propene, the SMILES representation would be 'CC=C' where each 'C' indicates the presence of an aliphatic carbon atom and '=' indicates the presence of a double-bond between two C atoms. While these representations are great in representing underlying chemistry succinctly, they miss out on <i>explicit structural information</i> such as the nature of chains, type of bonds and atoms, and so on. To explicitly include such structural information in a molecule's text-based representation, we combine the SMILES representation with the underliyng SMILES grammar. We parse the SMILES string using its underlying grammar to assign a hierarchical structure to the SMILES representation, called a grammar parse-tree. In this grammar parse-tree, the intermediate nodes provide useful chemistry-based structural meta information. For instance, the same propene molecule would be represented as shown in the hierarchical tree in Figure 2. And when this molecular grammar tree is traversed in a depth-first manner, we get a sequential representation that is an inline text-based representation just like SMILES string but also contains the intermediate structural information embedded in the parse tree. This sequential grammar-based representation for propene would be "1, 3, 2, 4, 6, 15, 17, 6, 15, 17, 13, 6, 15, 17", comprising a sequence of production rules at each step/node in the SMILES grammar parse-tree. Therefore, using the sequential grammar representation, we generate dense vector embeddings using a word2vec-like framework that are used to represent a given molecule, irrespective of the property that needs to be predicted. Details on the implementation could be found in our <a href='https://doi.org/10.1016/j.fluid.2022.113531' target="_blank">published article</a>. </p>

<p>The tree transformer model comprised two major changes -- first, tree positional encoding that encodes positions in a tree capturing parent/child/sibling underlying hierarchy, and second, tree convolution operations that performs convolutions operations around nodes in the tree to capture contextual information. The tree convolution operations allow for structural information to be encoded in the latent space utilizing structural information to the fullest extent.</p>

<p>The results on the forward prediction and the retrosynthesis prediction are shown below. Note that we only demonstrate the tree transformer approach on the retrosynthesis model but it could be easily applied for the forward prediction model just by reversing the direction of translation and should result in improved performance.</p>

<p style="text-align: center;"><img class="aligncenter size-full wp-image-123" src="/files/gram-tree.jpg" width="300" height="" /> &nbsp; &nbsp; &nbsp; &nbsp; <img class="aligncenter size-full wp-image-123" src="/files/grammar2vec-dist.jpg" width="300" height="" /></p>
Figure 2: (left) The parse-tree obtained for propene (SMILES representation: CC=C) using SMILES grammar productions rules. The productions are extracted from the parse tree in a depth-first manner, resulting in the grammar representation for propene to be 1, 3, 2, 4, 6, 15, 17, 6, 15, 17, 13, 6, 15, 17 ; (right) A histogram of the 32-dimensional molecular descriptors for all molecules in our dataset<br><br>

