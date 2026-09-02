# Ads Knowledge Hub

A curated learning path for engineers entering advertising systems, especially those coming from Search, ranking, recommendations, or machine learning.

Advertising systems sit at the intersection of:

- Information retrieval and ranking
- Probability and large-scale machine learning
- Auction theory and mechanism design
- Budget allocation and constrained optimization
- Experimentation and causal inference
- Contextual bandits and online learning

## Contents

- [Start here](#start-here)
- [Metrics and equations](#metrics-and-equations)
- [Online courses](#online-courses)
- [Foundational papers](#foundational-papers)
- [Official references](#official-references)

## Start here

If you have limited time, begin with these five papers:

1. [Internet Advertising and the Generalized Second-Price Auction](https://pubs.aeaweb.org/doi/10.1257/aer.97.1.242)
2. [Ad Click Prediction: A View from the Trenches](https://research.google/pubs/ad-click-prediction-a-view-from-the-trenches/)
3. [Entire Space Multi-Task Model for Post-Click Conversion Rate](https://arxiv.org/abs/1804.07931)
4. [Counterfactual Reasoning and Learning Systems](https://www.jmlr.org/papers/v14/bottou13a.html)
5. [The Unfavorable Economics of Measuring the Returns to Advertising](https://academic.oup.com/qje/article-abstract/130/4/1941/1914592)

And these three courses:

1. [Introduction to Digital Advertising — University of Colorado Boulder](https://www.coursera.org/learn/introduction-to-digital-advertising)
2. [Game Theory II: Advanced Applications — Stanford and UBC](https://www.coursera.org/learn/game-theory-2)
3. [Introduction to A/B Testing — Udacity/Google](https://www.udacity.com/course/ab-testing--ud257)

## Metrics and equations

Let:

- `I` = impressions
- `K` = clicks
- `C` = conversions
- `S` = advertiser spend
- `V` = conversion value

| Metric | Equation | Interpretation |
|---|---:|---|
| CTR | `K / I` | Clicks per impression |
| CVR | `C / K` | Post-click conversions per click |
| Conversion probability per impression | `C / I = pCTR x pCVR` | Joint click-and-conversion probability |
| CPM | `1000 x S / I` | Cost per thousand impressions |
| CPC | `S / K` | Cost per click |
| CPA | `S / C` | Cost per conversion |
| ROAS | `V / S` | Conversion value per unit of spend |
| RPM | `1000 x platform revenue / I` | Platform revenue per thousand impressions |
| Win rate | `auctions won / auctions entered` | Auction competitiveness |
| Fill rate | `impressions served / eligible opportunities` | Inventory utilization |
| Frequency | `impressions / reached users` | Exposures per reached user |

### Simplified ranking objectives

For CPC bidding:

```text
score = pCTR x CPC bid x quality
```

For CPA bidding:

```text
score = pCTR x pCVR x CPA bid x quality
```

For conversion-value optimization:

```text
expected value per impression
  = pCTR x pCVR x E[conversion value | conversion]
```

For incremental-value optimization:

```text
incremental conversion probability
  = P(conversion | ad shown, context)
  - P(conversion | ad not shown, context)
```

### Funnel decomposition

```text
opportunities
  -> eligible
  -> participated
  -> won
  -> rendered
  -> viewable
  -> clicked
  -> converted
```

A useful diagnostic identity is:

```text
conversions
  = opportunities
  x eligibility rate
  x win rate
  x render rate
  x pCTR
  x pCVR
```

## Online courses

### Advertising domain and metrics

- [Introduction to Digital Advertising — University of Colorado Boulder](https://www.coursera.org/learn/introduction-to-digital-advertising) — Payment models, metrics, formats, programmatic advertising, DSPs, SSPs, and the advertising ecosystem.
- [Digital Advertising — Coursera](https://www.coursera.org/learn/digital-advertising) — Beginner overview of SEM, bidding, campaign structure, social advertising, and campaign optimization.
- [Digital Marketing Analytics — O.P. Jindal Global University](https://www.coursera.org/learn/digital-marketing-analytics) — Funnels, KPIs, programmatic advertising, attribution, Google Ads, and web analytics.
- [Marketing Analytics with Meta](https://www.coursera.org/learn/marketing-analytics-with-facebook/) — A/B tests, brand lift, conversion lift, marketing mix modeling, and campaign analysis.

### Auctions and mechanism design

- [Game Theory — Stanford and UBC](https://www.coursera.org/learn/game-theory-1) — Strategic behavior, Bayesian games, equilibria, and keyword-auction examples.
- [Game Theory II: Advanced Applications — Stanford and UBC](https://www.coursera.org/learn/game-theory-2) — Mechanism design, VCG, first- and second-price auctions, revenue equivalence, and optimal auctions.
- [Game Theory with Engineering Applications — MIT OpenCourseWare](https://ocw.mit.edu/courses/6-254-game-theory-with-engineering-applications-spring-2010/pages/syllabus/) — Rigorous engineering-oriented treatment of Bayesian games, auction formats, revenue, efficiency, and mechanism design.
- [Topics in Game Theory — MIT OpenCourseWare](https://ocw.mit.edu/courses/14-147-topics-in-game-theory-fall-2009/) — Graduate material on market design, auction theory, and matching mechanisms.

### Experimentation and causality

- [Introduction to A/B Testing — Udacity/Google](https://www.udacity.com/course/ab-testing--ud257) — Metrics, experimental design, analysis, policy, and ethics.
- [Causal Inference — Columbia University](https://www.coursera.org/learn/causal-inference) — Potential outcomes, randomization inference, propensity scores, matching, and inverse-probability weighting.
- [Designing, Running, and Analyzing Experiments — UC San Diego](https://www.coursera.org/learn/designexperiments) — Practical experimental design and statistical analysis.

### Bandits and reinforcement learning

- [Decision Making and Reinforcement Learning](https://www.coursera.org/learn/dmrol) — Multi-armed bandits, epsilon-greedy exploration, UCB, MDPs, and reinforcement learning.
- [Reinforcement Learning Specialization — University of Alberta](https://www.coursera.org/specializations/reinforcement-learning) — Four-course treatment of bandits, value functions, policy methods, prediction, and control.

### Machine learning and ranking supplements

- [Google Machine Learning Crash Course](https://developers.google.com/machine-learning/crash-course/) — Logistic regression, classification, embeddings, categorical features, production ML, and fairness.
- [Google Recommendation Systems](https://developers.google.com/machine-learning/recommendation/) — Candidate generation, scoring, re-ranking, embeddings, and large-scale recommendation architecture.

## Foundational papers

### Surveys and orientation

- [Introduction to Computational Advertising](https://aclanthology.org/P08-5001.pdf) — Broder, 2008. A compact map of sponsored search, contextual advertising, and behavioral targeting.

### Auction and marketplace foundations

- [Internet Advertising and the Generalized Second-Price Auction](https://pubs.aeaweb.org/doi/10.1257/aer.97.1.242) — Edelman, Ostrovsky, and Schwarz, *AER 2007*. The canonical GSP auction paper.
- [Position Auctions](https://people.ischool.berkeley.edu/~hal/Papers/2006/position.pdf) — Varian, *International Journal of Industrial Organization 2007*. Equilibria and empirical behavior of position auctions.
- [AdWords and Generalized Online Matching](https://people.eecs.berkeley.edu/~vazirani/pubs/adwords.pdf) — Mehta et al., *JACM 2007*. Online allocation under advertiser budgets and the `1 - 1/e` result.
- [Sponsored Search Auctions with Markovian Users](https://arxiv.org/abs/0805.0766) — Aggarwal et al., 2008. Examination, abandonment, and interactions among ads on a page.
- [Algorithmic Methods for Sponsored Search Advertising](https://arxiv.org/abs/0805.1759) — Survey of market mechanisms and algorithms for sponsored search.

### CTR and response prediction

- [Predicting Clicks: Estimating the Click-Through Rate for New Ads](https://doi.org/10.1145/1242572.1242643) — Richardson, Dominowska, and Ragno, *WWW 2007*. Cold-start pCTR prediction using ad, query, and advertiser features.
- [Ad Click Prediction: A View from the Trenches](https://research.google/pubs/ad-click-prediction-a-view-from-the-trenches/) — McMahan et al., *KDD 2013*. FTRL-Proximal, sparse features, calibration, confidence, and production lessons.
- [Practical Lessons from Predicting Clicks on Ads at Facebook](https://quinonero.net/Publications/predicting-clicks-facebook.pdf) — He et al., *ADKDD 2014*. GBDT plus logistic regression, normalized entropy, calibration, sampling, and freshness.
- [Simple and Scalable Response Prediction for Display Advertising](https://people.csail.mit.edu/romer/papers/TISTRespPredAds.pdf) — Chapelle, Manavoglu, and Rosales, *ACM TIST 2014*. Large-scale click and conversion prediction.
- [Field-Aware Factorization Machines for CTR Prediction](https://doi.org/10.1145/2959100.2959134) — Juan et al., *RecSys 2016*. Sparse, field-aware feature interactions.
- [Wide & Deep Learning for Recommender Systems](https://arxiv.org/abs/1606.07792) — Cheng et al., 2016. Combining memorization and generalization.
- [DeepFM](https://www.ijcai.org/proceedings/2017/0239.pdf) — Guo et al., *IJCAI 2017*. Joint factorization-machine and neural-network architecture.
- [Deep Interest Network for CTR Prediction](https://www.kdd.org/kdd2018/accepted-papers/view/deep-interest-network-for-click-through-rate-prediction) — Zhou et al., *KDD 2018*. Candidate-dependent representations of user interests.

### Conversion prediction and delayed feedback

- [Modeling Delayed Feedback in Display Advertising](https://dblp.org/rec/conf/kdd/Chapelle14.html) — Chapelle, *KDD 2014*. Conversion delay, censoring, and immature negative labels.
- [Handling Many Conversions per Click in Modeling Delayed Feedback](https://research.google/pubs/handling-many-conversions-per-click-in-modeling-delayed-feedback/) — Varadaraja et al., *ADKDD 2021*. Multiple conversions and long-tailed, changing delays.
- [Entire Space Multi-Task Model for Post-Click Conversion Rate](https://arxiv.org/abs/1804.07931) — Ma et al., *SIGIR 2018*. Sample-selection bias, sparsity, and joint `pCTR x pCVR` modeling.
- [Modeling Labels for Conversion Value Prediction](https://research.google/pubs/modeling-labels-for-conversion-value-prediction/) — Varadaraja and Guruganesh, *ADKDD 2021*. Non-binary conversion values, scale, and outliers.

### Bidding, allocation, budgets, and pacing

- [Budget Optimization in Search-Based Advertising Auctions](https://arxiv.org/abs/cs/0612052) — Feldman et al., *ACM EC 2007*. Advertiser bid optimization under a budget constraint.
- [Budget Pacing for Targeted Online Advertisements at LinkedIn](https://www0.cs.ucl.ac.uk/staff/w.zhang/rtb-papers/linkedin-pacing.pdf) — Agarwal et al., *KDD 2014*. Global pacing layered over local auction decisions.
- [Bid Optimization in Broad-Match Ad Auctions](https://research.google/pubs/bid-optimization-in-broad-match-ad-auctions/) — Even-Dar et al., 2009. Bid optimization when keywords match multiple queries.
- [Handling Forecast Errors While Bidding for Display Advertising](https://research.google/pubs/handling-forecast-errors-while-bidding-for-display-advertising/) — Lang, Moseley, and Vassilvitskii, *WWW 2012*. Robust bidding under forecast uncertainty.

### Experimentation, attribution, and incrementality

- [Counterfactual Reasoning and Learning Systems: The Example of Computational Advertising](https://www.jmlr.org/papers/v14/bottou13a.html) — Bottou et al., *JMLR 2013*. Causal reasoning, importance weighting, policy-generated data, and feedback loops.
- [The Unfavorable Economics of Measuring the Returns to Advertising](https://academic.oup.com/qje/article-abstract/130/4/1941/1914592) — Lewis and Rao, *QJE 2015*. Why advertising lift requires enormous experiments.
- [Ghost Ads: Improving the Economics of Measuring Online Ad Effectiveness](https://journals.sagepub.com/doi/10.1509/jmr.15.0297) — Johnson, Lewis, and Nubbemeyer, *Journal of Marketing Research 2017*. Auction-aware experimental control groups.
- [A Comparison of Approaches to Advertising Measurement](https://www.kellogg.northwestern.edu/faculty/gordon_b/files/fb_comparison.pdf) — Gordon et al., *Marketing Science 2019*. Observational estimates versus randomized advertising experiments.
- [A Causal Framework for Digital Attribution](https://research.google/pubs/a-causal-framework-for-digital-attribution/) — Kelly, Vaver, and Koehler, 2018. Attribution framed as a causal decision problem.
- [Incrementality Bidding and Attribution](https://arxiv.org/abs/2208.12809) — Lewis and Wong. Connecting causal lift, bidding, attribution, and experimentation.
- [Robust Causal Inference for Incremental ROAS with Randomized Paired Geo Experiments](https://research.google/pubs/robust-causal-inference-for-incremental-return-on-ad-spend-with-randomized-paired-geo-experiments/) — Chen and Au, *Annals of Applied Statistics 2022*.
- [Bias Correction for Paid Search in Media Mix Modeling](https://research.google/pubs/bias-correction-for-paid-search-in-media-mix-modeling/) — Chen et al., 2018. Search-ad targeting bias in observational media-mix models.

### Contextual bandits and policy evaluation

- [A Contextual-Bandit Approach to Personalized News Article Recommendation](https://arxiv.org/abs/1003.0146) — Li, Chu, Langford, and Schapire, *WWW 2010*. LinUCB, contextual exploration, and offline replay evaluation.
- [Contextual Multi-Armed Bandits for Causal Marketing](https://arxiv.org/abs/1810.01859) — Contextual Thompson sampling and off-policy evaluation for marketing treatments.
- [Improved Online Learning Algorithms for CTR Prediction in Ad Auctions](https://research.google/pubs/improved-online-learning-algorithms-for-ctr-prediction-in-ad-auctions/) — Feng, Liaw, and Zhou, *ICML 2023*. CTR learning, UCB mechanisms, regret, and strategic advertiser behavior.

## Official references

- [Google Ads: CTR definition](https://support.google.com/google-ads/answer/2615875?hl=en)
- [Google Ads: Ad Rank definition](https://support.google.com/google-ads/answer/1752122?hl=en)
- [Google Ads: Bidding overview](https://support.google.com/google-ads/faq/10286469?hl=en)
- [Google Ads: Impression share](https://support.google.com/google-ads/answer/2497703?hl=en-419)
- [Google Ads: Search campaign performance metrics](https://support.google.com/google-ads/answer/9451527?hl=en)
- [IAB Click Measurement Guidelines](https://www.iab.com/guidelines/click-measurement-guidelines/)
- [IAB Ad Impression Measurement Guidelines](https://www.iab.com/guidelines/ad-impression-measurement-guidelines-us-global/)
- [IAB/MRC Retail Media Measurement Guidelines](https://www.iab.com/wp-content/uploads/2024/01/IAB_Retail_Media_Measurement_Guidelines_January2024.pdf)

## Contributing

Suggestions are welcome. When adding a resource, include:

- A stable link to the original paper, publisher, course, or official documentation
- Authors and publication venue where applicable
- One sentence explaining why the resource matters
- The most relevant section of this README

Avoid adding promotional blog posts when a primary paper or official source is available.
