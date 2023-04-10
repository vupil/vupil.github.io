---
title: 'grammar2vec: Molecular property prediction'
date: 2022-04-11
permalink: /posts/2022/04/Molecular property prediction using grammar2vec/
tags:
  - artificial intelligence
  - property prediction
  - computational chemisty
  - machine learning 
---
<div style="text-align: justify">

Ever wondered how to inject chemistry knowledge into machine learning models to accurately predict properties of molecules? How would a molecule be represented before it is input to an ML model? How could the representation be made more chemistry-aware and ensure it is complete and accurate? Do natural language processing methods have anything to do with such representations?

We developed a framework called grammar2vec, similar to word2vec for words that I'm sure most of us are familiar with thanks to the famous King - Man + Woman = Queen example.  Word2vec is an unsupervised representation learning approach that learns dense vectors for representing words that also capture their underlying semantics and meaning to a large extent. Grammar2vec is the molecular equivalent of word2vec and Grammar2vec generates a high dimensional numeric vector representation for molecules. These numeric molecular representations are similarly learnt in an unsupervised manner, while capturing their semantics to a large extent. A natural question that arises then is -- how to represent the molecule textually as the basis for generating representation using grammar2vec?

To answer this question, let's look at a common text-based representation of molecules called the SMILES representation. For instance, for say benzene, the SMILES representation would be xxxx where x1 indicates this, x2 indicates this, and so on. While these representations are great in representing underlying chemistry succinctly, they miss out on explicit chemistry information about the nature of chains, bonds, atoms, and so on. To address this, we parse the SMILES string using its underlying grammar to automatically generate a parse-tree that assigns hierarchical structure the SMILES representation and the intermediate nodes provide useful chemistry-based meta information. For instance, the same benzene molecule would be represented as shown in the below tree. And when this molecular grammar tree is traversed in a depth-first manner, we get a sequential representation that is an inline text-based representation just like SMILES string but contains a lot more chemistry-information compared to SMILES. 

Therefore, using the sequential grammar representation, we generate dense vector embeddings that are used to represent a given molecule, irrespective of the property that needs to be predicted. Details on the implementation could be found in our published article. 

The dense molecular representations are used as features for a given ML model with the property of interest to be predicted as the target variable. This allows for any suitable model depending on the dataset size, problem formulation, and target property of interest to be used with grammar2vec-based molecular representations. Moreover, we demonstrated that the models built using these features are chemistry-aware in the sense that correlated properties have correlated feature importances. The model performance was benchmarked on boiling point and critical temperature datasets, and we observed that the R-squared values (a measure of goodness of regression model) were 0.98 and 0.99 respectively. 

Thus, in summary, the developed models were hybrid due to a combination of chemistry and machine learning-based features, interpretable due to their correlation with underlying chemistry, and accurate in predicting the properties of interest. Further details could be found in the published article at: https://doi.org/10.1016/j.fluid.2022.113531
  
  
</div>
  

