# Ranking and response prediction

This layer estimates user response and combines it with advertiser value, quality, constraints, and marketplace objectives.

## CTR and relevance

- [Predicting Clicks: Estimating the Click-Through Rate for New Ads](https://doi.org/10.1145/1242572.1242643) — Richardson, Dominowska, and Ragno, *WWW 2007*. Early work on cold-start pCTR using ad, query, and advertiser features. `seminal`
- [Ad Click Prediction: A View from the Trenches](https://research.google/pubs/ad-click-prediction-a-view-from-the-trenches/) — McMahan et al., *KDD 2013*. FTRL-Proximal, sparse features, calibration, and production lessons. `seminal` `production`
- [Practical Lessons from Predicting Clicks on Ads at Facebook](https://quinonero.net/Publications/predicting-clicks-facebook.pdf) — He et al., *ADKDD 2014*. GBDT plus logistic regression, normalized entropy, calibration, sampling, and freshness. `production`
- [Simple and Scalable Response Prediction for Display Advertising](https://people.csail.mit.edu/romer/papers/TISTRespPredAds.pdf) — Chapelle, Manavoglu, and Rosales, *ACM TIST 2014*. Large-scale click and conversion prediction.
- [Similarity Models for Ad Relevance Measures](https://www.microsoft.com/en-us/research/publication/similarity-models-for-ad-relevance-measures/) — *NIPS MLOAD 2010*. Studies semantic similarity signals for ad relevance.
- [Leveraging Bidding Graphs for Advertiser-Aware Relevance Modeling in Sponsored Search](https://www.microsoft.com/en-us/research/wp-content/uploads/2021/11/2021.findings-emnlp.191.pdf) — *Findings of EMNLP 2021*. Adds advertiser behavior to semantic relevance modeling.

## Feature interaction and deep ranking

- [Field-Aware Factorization Machines for CTR Prediction](https://doi.org/10.1145/2959100.2959134) — Juan et al., *RecSys 2016*. Field-aware sparse feature interactions.
- [Wide & Deep Learning for Recommender Systems](https://arxiv.org/abs/1606.07792) — Cheng et al., 2016. Combines memorization and generalization.
- [DeepFM](https://www.ijcai.org/proceedings/2017/0239.pdf) — Guo et al., *IJCAI 2017*. Joint factorization-machine and neural-network architecture.
- [Deep Interest Network for Click-Through Rate Prediction](https://arxiv.org/abs/1706.06978) — Zhou et al., *KDD 2018*. Candidate-dependent user-interest representations.

## Conversion and value prediction

- [Modeling Delayed Feedback in Display Advertising](https://dblp.org/rec/conf/kdd/Chapelle14.html) — Chapelle, *KDD 2014*. Models conversion delay, censoring, and immature negative labels.
- [Entire Space Multi-Task Model for Post-Click Conversion Rate](https://arxiv.org/abs/1804.07931) — Ma et al., *SIGIR 2018*. Addresses sample-selection bias and sparsity by jointly modeling CTR and CVR. `seminal`
- [Handling Many Conversions per Click in Modeling Delayed Feedback](https://research.google/pubs/handling-many-conversions-per-click-in-modeling-delayed-feedback/) — Varadaraja et al., *ADKDD 2021*. Handles multiple conversions and long-tailed delays.
- [Modeling Labels for Conversion Value Prediction](https://research.google/pubs/modeling-labels-for-conversion-value-prediction/) — Varadaraja and Guruganesh, *ADKDD 2021*. Covers non-binary value, scale, and outliers.

## Multi-objective ranking

- [Optimizing Multiple Performance Metrics with Deep GSP Auctions for E-commerce Advertising](https://arxiv.org/abs/2012.02930) — 2020. Joint optimization of multiple marketplace metrics.
- [Ranking with Multiple Objectives](https://arxiv.org/abs/2410.12139) — 2024. General methods and tradeoffs for multi-objective ranking. `recent`

[Metrics and scoring equations](../resources/metrics-and-equations.md) · [Back to the hub](../README.md)
