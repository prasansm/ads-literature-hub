# Indexing and retrieval

Ads retrieval reverses parts of conventional Search: a live query must match advertiser-authored keywords, targeting constraints, and structured ad objects under tight latency and recall requirements.

## Indexing and candidate generation

- [A Data Structure for Sponsored Search](https://www.microsoft.com/en-us/research/publication/a-data-structure-for-sponsored-search/) — Broder et al., *ICDE 2009*. Designs a specialized index for broad-match containment queries over a very large ad corpus. `seminal` `production`
- [The Anatomy of an Ad: Structured Indexing and Retrieval for Sponsored Search](https://research.google/pubs/the-anatomy-of-an-ad-structured-indexing-and-retrieval-for-sponsored-search/) — Chatterjee et al., *WWW 2010*. Shows how structured ad fields can improve sponsored-search indexing and retrieval. `seminal`
- [Global Optimization for Advertisement Selection in Sponsored Search](https://www.microsoft.com/en-us/research/publication/global-optimization-for-advertisement-selection-in-sponsored-search/) — Ghosh et al., *JCST 2015*. Studies candidate selection as a global optimization problem.
- [ProphetNet-Ads: A Looking Ahead Strategy for Generative Retrieval Models in Sponsored Search Engine](https://www.microsoft.com/en-us/research/publication/prophetnet-ads-a-looking-ahead-strategy-for-generative-retrieval-models-in-sponsored-search-engine/) — Qi et al., *NLPCC 2020*. Applies sequence generation to sponsored-search retrieval.
- [End-to-End Neural Matching Framework for E-Commerce Sponsored Search](https://arxiv.org/abs/1812.01190) — Zhang et al., 2018. Jointly learns semantic matching for product-ad retrieval.
- [Improving Retrieval in Sponsored Search by Leveraging Query Context Signals](https://arxiv.org/abs/2407.14346) — 2024. Uses contextual signals beyond the current query to improve retrieval. `recent`
- [MOBIUS: Towards the Next Generation of Query-Ad Matching in Baidu's Sponsored Search](https://arxiv.org/abs/2409.03449) — 2024. A modern industrial query-ad matching system. `recent` `production`

## Design questions to track

- Exact, phrase, broad, semantic, and generative matching
- Recall versus latency and index cost
- Targeting and policy filters before versus after retrieval
- Freshness, advertiser updates, and cold-start ads
- Retrieval calibration and candidate-source blending

[Back to the hub](../README.md)
