---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
sitemap: true
---
## Journal Publications

### Predicting Chemical Reaction Outcomes: A Grammar Ontology-based Transformer Framework  
_Vipul Mann, Venkat Venkatasubramanian_  | September 2020 | [doi: 10.26434/chemrxiv.12985892](https://chemrxiv.org/articles/preprint/Predicting_Chemical_Reaction_Outcomes_A_Grammar_Ontology-based_Transformer_Framework/12985892)

#### Abstract
Discovering and designing novel materials is a challenging problem as it often requires searching a combinatorially large space of potential candidates. Evaluation of all candidates experimentally is typically infeasible as it requires great amounts of effort, time, expertise, and money. The ability to predict reaction outcomes without performing extensive experiments is, therefore, important. Towards that goal, we report an approach that uses context-free grammar (CFG) based representations of molecules in a neural machine translation framework. We formulate the reaction-prediction task as a machine translation problem that involves discovering the transformations from the source sequence (comprising the reactants and agents) to the target sequence (comprising the major product) in the reaction. The grammar ontology-based representation of molecules hierarchically incorporates rich molecular structure information that, in principle, should be valuable for modeling chemical reactions. We achieve an accuracy of 80.1% on a standard reaction dataset using a model characterized by only a fraction of the number of training parameters in other sequence-to-sequence models based works in this area. Moreover, 99% of the predictions made on the same reaction dataset were found to be syntactically valid. We conclude that CFGs-based ontological representations could be an efficient way of incorporating structural information, ensuring chemically valid predictions, and overcoming overfitting in complex machine learning architectures employed in reaction prediction tasks.

---
###  Robust and Efficient Swarm Communication Topologies for Hostile Environments  
_Vipul Mann, Abhishek Sivaram, Laya Das, Venkat Venkatasubramanian_  | March 2020 | [arXiv:2008.09575](https://arxiv.org/abs/2008.09575)

#### Abstract
Swarm Intelligence-based optimization techniques combine systematic exploration of the search space with information available from neighbors and rely strongly on communication among agents. These algorithms are typically employed to solve problems where the function landscape is not adequately known and there are multiple local optima that could result in premature convergence for other algorithms. Applications of such algorithms can be found in communication systems involving design of networks for efficient information dissemination to a target group, targeted drug-delivery where drug molecules search for the affected site before diffusing, and high-value target localization with a network of drones. In several of such applications, the agents face a hostile environment that can result in loss of agents during the search. Such a loss changes the communication topology of the agents and hence the information available to agents, ultimately influencing the performance of the algorithm. In this paper, we present a study of the impact of loss of agents on the performance of such algorithms as a function of the initial network configuration. We use particle swarm optimization to optimize an objective function with multiple sub-optimal regions in a hostile environment and study its performance for a range of network topologies with loss of agents. The results reveal interesting trade-offs between efficiency, robustness, and performance for different topologies that are subsequently leveraged to discover general properties of networks that maximize performance. Moreover, networks with small-world properties are seen to maximize performance under hostile conditions.

---
### Optimal Filtering and Residual Analysis in Errors-in-Variables Model Identification
_Vipul Mann, Deepak Maurya, Arun Kumar Tangirala, Shankar Narasimhan_  | January 2020 | [doi:10.1021/acs.iecr.9b04561](https://pubs.acs.org/doi/abs/10.1021/acs.iecr.9b04561) | [codebase (MATLAB implementation)](https://github.com/vupil/Optimal-Filtering-EIV-DIPCA)

#### Abstract
Dynamic model identification from time series data is a critical component of process control, monitoring, and diagnosis. An important adjunct of model identification is the derivation of filtered estimates of the variables and consequent one-step-ahead prediction errors (residuals) which are very useful for model assessment and iterative model identification. In this work, we present an optimal filtering and residual generation method for the errors-in-variables (EIV) scenario, wherein both the input and output variable measurements are contaminated with errors. The main idea is to combine an EIV-identification strategy with the EIV-Kalman filter (EIV-KF) that is known to provide optimal filtered estimates and residuals of both inputs and outputs for a linear dynamical process in the EIV case. In this work, we combine the EIV-KF with the dynamic iterative principal component analysis (DIPCA) approach that has been recently developed for EIV model identification. This work assumes prominence in that the optimally generated residuals are critical to the tasks of model assessment, fault detection, and diagnosis. The use of residuals in model assessment and reidentification is illustrated in this article, while pointing out that the use of DIPCA alone leads to nonunique filtered estimates and hence nonunique residuals. We remark that the proposed method can be used with any other EIV identification technique.


## Conference Publications

### A Formal Grammar-Based Machine Learning Approach for Predicting Reaction Outcomes
_Vipul Mann, Venkat Venkatasubramanian_ | November 2020 | [Virtual AIChE Annual Meeting 2020](https://aiche.confex.com/aiche/2020/meetingapp.cgi/Paper/605838)  

#### Abstract
Prediction of reaction outcomes without performing time-consuming experiments offers several invaluable advantages -- reducing experimentation costs due to elimination of highly improbable reactions, lowering the time to hypothesis-validation-and-correction, enabling high-throughput experimentation for complex reactions, and allowing significantly more time for analyzing the results. In recent years, machine learning techniques have been successfully applied in this area that, either directly or indirectly, address one or more of the above issues. A few areas of application include discovery of novel molecules with desired properties, understanding structure-property relationships, identifying catalysts for better reaction catalysis, and data-driven modeling of chemical reaction kinetics. The success of machine learning methods could largely be attributed to their inherent proficiency in capturing complex non-linear dependencies between various factors that govern the reaction systems. Here, we present an approach for predicting the most likely product of a reaction based on a given set of reactants and agents (catalysts, reaction medium). The structural properties of reactants and the product molecules are encoded based on a formal grammar, akin to context-free grammars (CFG) in the area of natural language processing (NLP), that essentially gives rise to a parse-tree representation of the molecule. This representation is used in a convolutional neural network architecture to model the structural transformations from a set of reactants to the most likely product of the reaction. The proposed framework could be used for rapid experimentation and analysis of reaction outcomes, especially if the molecules involved are less-known and structurally novel. In addition, the latent space of the neural network architecture could also be used to discover insights on the transformations from reactants to products in a given reaction under different conditions.

### Linear Dynamic Model Identification and Data Reconciliation using Dynamic Iterative PCA (DIPCA)
_Vipul Mann, Arun Kumar Tangirala, Shankar Narasimhan_ | March 2017 | [AIChE Spring Meeting 2017](https://www.aiche.org/conferences/aiche-spring-meeting-and-global-congress-on-process-safety/2017/proceeding/paper/172a-linear-dynamic-model-identification-and-data-reconciliation-using-dynamic-iterative-pca-dipca)  

#### Abstract
Identification of input-output models from data is of utmost relevance in chemical process industries and has applications in process monitoring, control and fault diagnosis. Input-output data used in such identification exercises often has measurement errors in both the variables. Model identification under such conditions translates to solving an errors-in-variables (EIV) problem which is difficult to solve using classical system identification techniques. A recently proposed method - Dynamic Iterative Principal Component Analysis (DIPCA) uses PCA framework to identify the process order, delay, model parameters, and
error variances. DIPCA, however, has certain shortcomings under small sample conditions which limit its practical applications. In this work, we address these shortcomings, namely ambiguity in order determination under small sample cases and arbitrary selection of stacking lag which leads to sub-optimal parameter estimates. We define a metric called ’d-selective eigenvalue ratio’, or d-SEVR that sharply identifies the true order even for small sample cases. We also demonstrate the existence of an optimal stacking lag corresponding to the lowest error in estimation of error-covariance matrix. Finally, we use the identified model to obtain reconciled estimates of variables using Kalman Filter.

      <!-- Show static HTML/CSS as a placeholder in case js is not enabled - javascript include will override this if things work -->
      <style type="text/css" media="screen">
  .gr_custom_container_ {
    /* customize your Goodreads widget container here*/
    border: 1px solid gray;
    border-radius:10px;
    padding: 10px 5px 10px 5px;
    background-color: #FFF;
    color: #000;
    width: 300px
  }
  .gr_custom_header_ {
    /* customize your Goodreads header here*/
    border-bottom: 1px solid gray;
    width: 100%;
    margin-bottom: 5px;
    text-align: center;
    font-size: 120%
  }
  .gr_custom_each_container_ {
    /* customize each individual book container here */
    width: 100%;
    clear: both;
    margin-bottom: 10px;
    overflow: auto;
    padding-bottom: 4px;
    border-bottom: 1px solid #aaa;
  }
  .gr_custom_book_container_ {
    /* customize your book covers here */
    overflow: hidden;
    height: 60px;
      float: left;
      margin-right: 4px;
      width: 39px;
  }
  .gr_custom_author_ {
    /* customize your author names here */
    font-size: 10px;
  }
  .gr_custom_tags_ {
    /* customize your tags here */
    font-size: 10px;
    color: gray;
  }
  .gr_custom_rating_ {
    /* customize your rating stars here */
    float: right;
  }
</style>

      <div id="gr_custom_widget_">
          <div class="gr_custom_container_">
    <h2 class="gr_custom_header_">
    <a style="text-decoration: none;" rel="nofollow" href="https://www.goodreads.com/review/list/48237749-vipul-mann?shelf=read&amp;utm_medium=api&amp;utm_source=custom_widget">Vipul Mann&#39;s books</a>
    </h2>
      <div class="gr_custom_each_container_">
          <div class="gr_custom_book_container_">
            <a title="The Man Who Solved the Market: How Jim Simons Launched the Quant Revolution" rel="nofollow" href="https://www.goodreads.com/review/show/3462347174?utm_medium=api&amp;utm_source=custom_widget"><img alt="The Man Who Solved the Market: How Jim Simons Launched the Quant Revolution" border="0" src="https://i.gr-assets.com/images/S/compressed.photo.goodreads.com/books/1567623099l/43889703._SY75_.jpg" /></a>
          </div>
          <div class="gr_custom_rating_">
            <span class=" staticStars notranslate" title="liked it"><img alt="liked it" src="https://www.goodreads.com/images/layout/gr_red_star_active.png" /><img alt="" src="https://www.goodreads.com/images/layout/gr_red_star_active.png" /><img alt="" src="https://www.goodreads.com/images/layout/gr_red_star_active.png" /><img alt="" src="https://www.goodreads.com/images/layout/gr_red_star_inactive.png" /><img alt="" src="https://www.goodreads.com/images/layout/gr_red_star_inactive.png" /></span>
          </div>
          <div class="gr_custom_title_">
            <a rel="nofollow" href="https://www.goodreads.com/review/show/3462347174?utm_medium=api&amp;utm_source=custom_widget">The Man Who Solved the Market: How Jim Simons Launched the Quant Revolution</a>
          </div>
          <div class="gr_custom_author_">
            by <a rel="nofollow" href="https://www.goodreads.com/author/show/3118998.Gregory_Zuckerman">Gregory Zuckerman</a>
          </div>
      </div>
      <div class="gr_custom_each_container_">
          <div class="gr_custom_book_container_">
            <a title="Bird by Bird: Some Instructions on Writing and Life" rel="nofollow" href="https://www.goodreads.com/review/show/3170379755?utm_medium=api&amp;utm_source=custom_widget"><img alt="Bird by Bird: Some Instructions on Writing and Life" border="0" src="https://i.gr-assets.com/images/S/compressed.photo.goodreads.com/books/1394996112l/12543._SY75_.jpg" /></a>
          </div>
          <div class="gr_custom_rating_">
            <span class=" staticStars notranslate" title="really liked it"><img alt="really liked it" src="https://www.goodreads.com/images/layout/gr_red_star_active.png" /><img alt="" src="https://www.goodreads.com/images/layout/gr_red_star_active.png" /><img alt="" src="https://www.goodreads.com/images/layout/gr_red_star_active.png" /><img alt="" src="https://www.goodreads.com/images/layout/gr_red_star_active.png" /><img alt="" src="https://www.goodreads.com/images/layout/gr_red_star_inactive.png" /></span>
          </div>
          <div class="gr_custom_title_">
            <a rel="nofollow" href="https://www.goodreads.com/review/show/3170379755?utm_medium=api&amp;utm_source=custom_widget">Bird by Bird: Some Instructions on Writing and Life</a>
          </div>
          <div class="gr_custom_author_">
            by <a rel="nofollow" href="https://www.goodreads.com/author/show/7113.Anne_Lamott">Anne Lamott</a>
          </div>
      </div>
      <div class="gr_custom_each_container_">
          <div class="gr_custom_book_container_">
            <a title="Chaos: Making a New Science" rel="nofollow" href="https://www.goodreads.com/review/show/3002597349?utm_medium=api&amp;utm_source=custom_widget"><img alt="Chaos: Making a New Science" border="0" src="https://i.gr-assets.com/images/S/compressed.photo.goodreads.com/books/1327941595l/64582._SY75_.jpg" /></a>
          </div>
          <div class="gr_custom_rating_">
            <span class=" staticStars notranslate" title="it was amazing"><img alt="it was amazing" src="https://www.goodreads.com/images/layout/gr_red_star_active.png" /><img alt="" src="https://www.goodreads.com/images/layout/gr_red_star_active.png" /><img alt="" src="https://www.goodreads.com/images/layout/gr_red_star_active.png" /><img alt="" src="https://www.goodreads.com/images/layout/gr_red_star_active.png" /><img alt="" src="https://www.goodreads.com/images/layout/gr_red_star_active.png" /></span>
          </div>
          <div class="gr_custom_title_">
            <a rel="nofollow" href="https://www.goodreads.com/review/show/3002597349?utm_medium=api&amp;utm_source=custom_widget">Chaos: Making a New Science</a>
          </div>
          <div class="gr_custom_author_">
            by <a rel="nofollow" href="https://www.goodreads.com/author/show/10401.James_Gleick">James Gleick</a>
          </div>
      </div>
      <div class="gr_custom_each_container_">
          <div class="gr_custom_book_container_">
            <a title="Mossad: The Greatest Missions of the Israeli Secret Service" rel="nofollow" href="https://www.goodreads.com/review/show/3002595359?utm_medium=api&amp;utm_source=custom_widget"><img alt="Mossad: The Greatest Missions of the Israeli Secret Service" border="0" src="https://i.gr-assets.com/images/S/compressed.photo.goodreads.com/books/1347981678l/13623874._SY75_.jpg" /></a>
          </div>
          <div class="gr_custom_rating_">
            <span class=" staticStars notranslate"><img src="https://www.goodreads.com/images/layout/gr_red_star_inactive.png" /><img alt="" src="https://www.goodreads.com/images/layout/gr_red_star_inactive.png" /><img alt="" src="https://www.goodreads.com/images/layout/gr_red_star_inactive.png" /><img alt="" src="https://www.goodreads.com/images/layout/gr_red_star_inactive.png" /><img alt="" src="https://www.goodreads.com/images/layout/gr_red_star_inactive.png" /></span>
          </div>
          <div class="gr_custom_title_">
            <a rel="nofollow" href="https://www.goodreads.com/review/show/3002595359?utm_medium=api&amp;utm_source=custom_widget">Mossad: The Greatest Missions of the Israeli Secret Service</a>
          </div>
          <div class="gr_custom_author_">
            by <a rel="nofollow" href="https://www.goodreads.com/author/show/289426.Michael_Bar_Zohar">Michael Bar-Zohar</a>
          </div>
      </div>
      <div class="gr_custom_each_container_">
          <div class="gr_custom_book_container_">
            <a title="THINK STRAIGHT: Change Your Thoughts, Change Your Life" rel="nofollow" href="https://www.goodreads.com/review/show/2808866605?utm_medium=api&amp;utm_source=custom_widget"><img alt="THINK STRAIGHT: Change Your Thoughts, Change Your Life" border="0" src="https://i.gr-assets.com/images/S/compressed.photo.goodreads.com/books/1511333835l/36640169._SY75_.jpg" /></a>
          </div>
          <div class="gr_custom_rating_">
            <span class=" staticStars notranslate" title="liked it"><img alt="liked it" src="https://www.goodreads.com/images/layout/gr_red_star_active.png" /><img alt="" src="https://www.goodreads.com/images/layout/gr_red_star_active.png" /><img alt="" src="https://www.goodreads.com/images/layout/gr_red_star_active.png" /><img alt="" src="https://www.goodreads.com/images/layout/gr_red_star_inactive.png" /><img alt="" src="https://www.goodreads.com/images/layout/gr_red_star_inactive.png" /></span>
          </div>
          <div class="gr_custom_title_">
            <a rel="nofollow" href="https://www.goodreads.com/review/show/2808866605?utm_medium=api&amp;utm_source=custom_widget">THINK STRAIGHT: Change Your Thoughts, Change Your Life</a>
          </div>
          <div class="gr_custom_author_">
            by <a rel="nofollow" href="https://www.goodreads.com/author/show/14204065.Darius_Foroux">Darius Foroux</a>
          </div>
      </div>
  <br style="clear: both"/>
  <center>
    <a rel="nofollow" href="https://www.goodreads.com/"><img alt="goodreads.com" style="border:0" src="https://www.goodreads.com/images/widget/widget_logo.gif" /></a>
  </center>
  <noscript>
    Share <a rel="nofollow" href="https://www.goodreads.com/">book reviews</a> and ratings with Vipul Mann, and even join a <a rel="nofollow" href="https://www.goodreads.com/group">book club</a> on Goodreads.
  </noscript>
  </div>

      </div>
      <script src="https://www.goodreads.com/review/custom_widget/48237749.Vipul%20Mann's%20bookshelf:%20read?cover_position=&cover_size=&num_books=5&order=&shelf=&sort=&widget_bg_transparent=" type="text/javascript" charset="utf-8"></script>
