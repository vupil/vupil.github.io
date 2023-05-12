---
title: 'Chemistry-informed Transformers for Reaction Prediction and Retrosynthesis'
date: 2023-05-10
redirect_from: https://vipulmann.com/posts/2022/04/SMILES%20grammar%20transformers%20for%20reactions/
permalink: /posts/2022/04/SMILES grammar transformers for reactions/
tags:
  - artificial intelligence
  - retrosynthesis
  - computational chemisty
  - reaction prediction
---


<div style="text-align: justify">


<p>The transformer architecture has remarkably improved the accuracy of sequence modeling tasks (eg. language translation) but could they be used to model chemical reactions? Do chemical reactions have some similarity with natural language that allows for the use of powerful transformer-inspired architectures? How would the molecules be represented in such frameworks so that appropriate chemical structural information is captured? Are there other potential transformer-like architectures that could handle chemical representations better compared to the vanilla transformer model?</p>

<p>To use the transformer architecture, two requirements have to be satisfied -- first, chemicals participating in a reaction should be represented using text-based representations (akin to words in a sentence), and second, the reaction modeling problem needs to be formulated as a 'language translation' task. Thus, based on this analogy, participating chemicals are 'words' and left-hand-side of reactions are 'sentences' (in reactants language) that need to be 'translated' to the right-hand-side 'sentences' (in products language). Our series of works using this analogy (<a href='https://arxiv.org/abs/2305.03153' target="_blank">paper 4</a>, <a href='https://doi.org/10.1016/j.coche.2021.100749' target="_blank">paper 3</a>, <a href='https://doi.org/10.1016/j.compchemeng.2021.107533' target="_blank">paper 2</a>, <a href='https://doi.org/10.1002/aic.17190' target="_blank">paper 1</a>) first addressed the issue of using an appropriate chemical grammar-based representation followed by proposing a novel tree-transformer architecture that could perform the translation using molecular trees as input in a chemistry-aware manner.</p>

<p>The machine translation framework for reaction modeling is shown in the Figure 1 below. The forward translation (from reactants to products) is used to predict chemical reaction outcomes, and the inverse translation (from product to reactants) is used to solve the retrosynthesis problem. The first important question is how to represent the input and output molecules?</p>

<p style="text-align: center;"><img class="aligncenter size-full wp-image-123" src="/files/mt_framework.jpg" width="750" height="" /></p>
Figure 1: SMILES grammar-based representations for reaction prediction and retrosynthesis using machine translation framework. <br><br>

  <h3>Can we do better than the SMILES representation?</h3>
<p>The most commonly used representation is the SMILES representation where molecules are represented using a linear text-based notation. For instance, for say cyclopropane, the SMILES representation is C1CC1. While the SMILES representation is vastly used, it contains little explicitly encoded chemical structural information. On the other hand, the grammar parse tree shown in Figure 2 contains additional relevant information. For instance, it contains information such as the number of aromatic carbon atoms, the presence of a ring-structure, the alternating double bonds in the ring, the presence of an aliphatic oxygen atom, and finally the active hydrogen atom attached to the oxygen atom. Moreover, this information is represented in a hierarchical manner, with the broadest class of rules at the top and increasingly more specific ones toward the bottom of the parse-tree. We thus proposed a SMILES grammar-based representation based on these parse trees for molecules. We showed that these representations are better from a model performance as well as information theoretic standpoint, since the conditional entropy (or uncertainty) associated with it is the lowest, thus aiding data-driven approaches in modeling and discovering patterns efficiently.</p>

  <p style="text-align: center;"><img class="aligncenter size-full wp-image-123" src="/files/cyclopropane.jpeg" width="450" height="" /></p>
Figure 2: The SMILES grammar parse-tree obtained for cyclopropane with the SMILES representation as C1CC1.<br><br>

  <h3>Can we do better than the vanilla transformer architecture?</h3>
<p>The second important question to answer is can the transformer model be adapted to better handle hierarchical chemistry-informed molecular representations? This would allow for the entire grammar (instead of linearized SMILES grammar tree) to be input to the transformer architecture and preserve the structural hierarchy that is inherently encoded. To this end, we modified the transformer architecture and proposed a novel tree transformer architecture for modeling retrosynthesis problems as shown in Figure 3 below.</p>
  
<p style="text-align: center;"><img class="aligncenter size-full wp-image-123" src="/files/tree-transformer.png" width="450" height="" /></p>
Figure 3: The proposed tree transformer with SMILES grammar parse-trees as input and target sequence as output.<br><br>

<p>The tree transformer model comprises two major changes -- first, tree positional encoding that encodes positions in a tree capturing parent/child/sibling relationships representing the underlying hierarchy, and second, tree convolution operations that performs convolutions operations around nodes in the tree to capture contextual information. The tree convolution operations allow for structural information to be encoded in the latent space utilizing structural information to the fullest extent.</p>

<p><b>Results</b></p>
<p>The results on the forward prediction and the retrosynthesis prediction are shown below. Note that we only demonstrate the tree transformer approach on the retrosynthesis model but it could be easily applied for the forward prediction model just by reversing the direction of translation and should result in improved performance.</p>
 
<table>
  <caption>Table 1: <strong>Accuracy (%)</strong>: consolidated results for the forward prediction model (USPTO-MIT dataset) and retrosynthesis model (USPTO-50K dataset)</caption>
  <tr>
    <th>Model</th>
    <th>Top 1</th>
    <th>Top 2</th>
    <th>Top 3</th>
    <th>Top 5</th>
    <th>Top 10</th>
  </tr>
  <tr>
    <td>forward (grammar linearized)</td>
    <td>80.1</td>
    <td>86.3</td>
    <td>88.7</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>retrosynthesis (grammar tree, with class)</td>
    <td>51.0</td>
    <td>64.3</td>
    <td>70.0</td>
    <td>74.6</td>
    <td>79.1</td>
  </tr>
  <tr>
    <td>retrosynthesis (grammar tree, no class)</td>
    <td>41.6</td>
    <td>54.0</td>
    <td>60.4</td>
    <td>67.6</td>
    <td>73.1</td>
  </tr>
</table>

  
<table>
  <caption>Table 2: <strong>Incorrect syntax (%)</strong>: consolidated results for the forward prediction model (USPTO-MIT dataset) and retrosynthesis model (USPTO-50K dataset)</caption>
  <tr>
    <th>Model</th>
    <th>Top 1</th>
    <th>Top 2</th>
    <th>Top 3</th>
    <th>Top 5</th>
    <th>Top 10</th>
  </tr>
  <tr>
    <td>forward (grammar linearized)</td>
    <td>1.0</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>retrosynthesis (grammar tree, with class)</td>
    <td>1.5</td>
    <td>2.7</td>
    <td>4.0</td>
    <td>6.0</td>
    <td>9.8</td>
  </tr>
  <tr>
    <td>retrosynthesis (grammar tree, no class)</td>
    <td>1.3</td>
    <td>2.0</td>
    <td>2.6</td>
    <td>3.8</td>
    <td>6.0</td>
  </tr>
</table>


  
<p>Further results, detailed analyses, and additional chemistry-based statistics are presented in our published articles -- <a href='https://arxiv.org/abs/2305.03153' target="_blank">retrosynthesis tree transformer</a>, <a href='https://doi.org/10.1002/aic.17190' target="_blank">forward prediction</a>, <a href='https://doi.org/10.1016/j.compchemeng.2021.107533' target="_blank">information-theoretic analysis</a>, and <a href='https://doi.org/10.1016/j.coche.2021.100749' target="_blank">review article</a>.
</p>
