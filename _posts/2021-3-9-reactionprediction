## Do we really need to perform reactions experiments in chemistry laboratories?

We have all heard the following prophesies at least once during the last couple of years -- "Machines are going to replace humans in all the tasks that you could imagine?", "Artificial Intelligence is going to solve all the problems (and invent several others) that the human civilization currently suffers from", and my personal favorite "You throw anything at the *ML software* and it'll spit out the correct answer; it's like magic." Though all of these (scandalous) statements have some truth in them, they are not at all useful at addressing the question that a non-ML scientist has lurking at the back of his mind --  could she be replaced as conveniently by machines as they claim?

The short answer to this is no, or in fact I should say never. The could never be *completely* replaced by a mere machine learning algorithm, no matter how complex they are and how many billions of training parameters does it have. After all, the intelligence part of AI is still artificial and the more you look into it, the more is the realization that they are not even close to even fractionally mimic the capabilities of the human mind.

If you're still not convinced and want a longer version of the above, read on. Though the central question that I try to answer here is whether a human chemist could be replaced by machine learning-based systems, but the same in my opinion applies to all the engineering and scientific disciplines. The premise for this post is based on our recent work where we developed a chemistry-informed ML system that predicts the outcomes of organic chemical reactions, without requiring a chemist (or non-chemist) to perform any laboratory experiments whatsoever. The <a href='#paperlink'>full article</a><sup>1</sup> describes this approach in much more technical detail than I would be covering in this post. If you or your institution does not have access to the journal, please reach out to me and I would be happy to share the full-text pdf version of the article.


#### Organic Chemical Reactions
Organic reactions are those that primarily involve organic compounds, consisting of molecules that are predominantly composed of carbon(C) and hydrogen(H) atoms, with the optional presence of certain other elements such as oxygen(O), nitrogen(N), chlorine(Cl), bromine(Br), and so on. A vast majority of the compounds on earth are hydrocarbons with their vast abundance playing a significant role in global and local phenomena. Such reactions often occur through a series of reactions that are highly dependent on the type of molecules under consideration and the reaction environment, often giving rise to extremely complex compounds in just a few steps. Moreover, the selectivity of the products change significantly as the reaction conditions change. As a result of these factors, organic chemistry poses several challenges if one were to use computation methods for modeling them, with little or no prior incorporation of chemistry information.

Here are two reactions that demonstrate how simple and complex organic reactions could become, depending on the participating compounds.

Ethene to ethane.

Image from: https://onlinelibrary.wiley.com/doi/full/10.1002/anie.201605460


#### Conventional Reaction Prediction approaches
Conventionally, the majority of the reaction prediction is guided by the existing reaction mechanisms that define how a molecule gets manipulated based on the expected class of reaction that it might follow which is followed by an experimental validation of the predictions if there are multiple competing reactions for the same set of starting compounds that might give rise to multiple different products. As we had seen earlier, the process gets extremely complicated quickly as more complex compounds are involved, making the prediction process extremely dependent on the experience of the chemist. This clearly indicates towards the challenges of this process, apart from the dire (relative) shortage of the expert experience chemists in the scientific community -- first, the predictions are highly subject to the person selecting the reactions based on their subjective knowledge which may lead to disagreement and impede formalization, second, the reaction mechanisms and the predicted products would be highly biased towards those that are already known to the chemist, or preexisting in the literature, ensuring that there aren't enough novel compounds and reactions identified during such exercises.

[insert chemistry cartoon here]


The dictionary-based computational methods that makes use of the entire library of known reactions, their properties, all the possible compounds known irrespective of their rarity, and gets rid of the human bias in making such predictions work better than humans. However, these systems fail to generalize and predict novel compounds or identify novel chemical reactions that may not have been seen yet since they are just the manifestation of all the chemistry knowledge in the scientific community, which without doubt is not complete. This is the primary motivation behind using machine learning algorithms -- the power of predicting beyond the knowledge that it acquired during the training stage. Again, machine learning to the rescue! Isn't it amazing as to how apparently useful they seem to be, yet we all despise them because of their lack of transparency from a human's perspective? Isn't this our limitation to understand the systems that work so well and make predictions on data points outside the training set as well with a fairly high-degree of accuracy? I'll defer this discussion to a later post and stick to the reaction prediction problem in the interest of the attention deficit of most readers (including myself!).


#### Machine translation and Reaction prediction
Our motivation to use a machine translation approaches to the reaction prediction framework came into existence because of the stark similarities between the natural language that we use to communicate in our daily lives and the language of chemistry that the chemists use in their daily lives (in addition to natural language, of course!). Just as natural language has sentences and words as the atomic units in a sentence that convey a given meaning, the language of chemistry analogously has molecular representations (H2O, CO2, C2H5OH) with the individual characters being the atomic units that convey information on the constituent elements and their stoichiometry. Thus, using a machine translation framework made complete sense and we hypothesized that this would open a new direction in chemistry.

However, a detailed literature survey made us realize that most human think alike and no idea is truly novel -- there were a couple of papers (but not too many) that talked about the exact same framework that could be used for modeling reactions. Figure {} provides an overview of this framework. This was both heartening as well as disheartening -- the former because we got immediate validation of our work which truly had started a new direction in reaction prediction and is in fact is the current state of the art, but also the latter because we were just a couple of years late to have seen this analogy. We anyway focused on the former, the validation part and taking inspiration from it, thought of contributing to this area with another breakthrough. We believed the breakthrough would come with the same analogy between natural and chemistry language that we had envisaged.


[insert image from Molecular Transformer]


The natural extension to this is another analogy that tie the two areas together -- grammatical rules that formalize the construction of sentences (molecular representations) from their respective atomic units. All the existing works in the area of reaction prediction have ignored this stark analogy that fundamentally defines the structure of the high-level constructs from the lower-level units. We hypothesized that the inclusion of such information in the machine translation frameworks would significantly aid the model in *learning* the grammar, instead of hoping it to learn (or memorize) it based on the training set. Moreover, such a grammar-based framework would ensure that the predictions made using such a framework would be highly likely to follow the grammar-rules themselves and therefore be syntactically correct, i.e. water is more likely to be predicted as H2O instead of 2HO or OH2, though all of them have the same stoichiometry.

The grammar rules for natural language and for a text-based representation of molecules (SMILES notation) are shown in the Figure {}.


In order to incorporate such grammar rules, we replaced the text-based representation of molecules with newer representations that incorporate the underlying structure. Without going too much into technical details, imagine that each of the text-based representations are obtained by following a set of grammatical rules that are applied sequentially to obtain the corresponding tokens. These rules and their sequential application could be represented using a tree as shown in the following figures. The grammar production rules are extracted from these trees by parsing them in the indicated manner, which now become the new representations that incorporate all the additional structural and grammatical information underlying the molecule.

[insert two figures: propene and cyclopropane]


When used in a machine translation framework depicted in Figure {}, we obtained extremely promising results that demonstrate the superiority of this with respect to the other frameworks.

[table with comparison with other works]

A comparison with the human organic chemists indicate that this model beats them across all the reaction classes. Moreover, the incorrect predictions are still very close to the actual product of the reaction.

[image 1: plot]
[image 2: incorrect predictions]


Therefore, clearly the incorporation of grammar has achieve significant improvements over traditional approaches:
[the three bullet points from the paper]

#### What does this mean?
Coming back to the question -- does the rapid development and improvement of such systems eventually replace the human experts and obviate the years of hard-earned experience? 














<p id='paperlink'><i>
1. Mann, V. and Venkatasubramanian, V. (2021), Predicting Chemical Reaction Outcomes: A Grammar Ontology‐based Transformer Framework. AIChE J. Accepted Author Manuscript e17190. <a href="https://doi.org/10.1002/aic.17190">https://doi.org/10.1002/aic.17190</a></i></p>
