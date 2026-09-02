# Query and ad understanding

This layer interprets user intent and advertiser intent, normalizes entities and concepts, and generates useful rewrites or representations before matching.

## Sponsored-search papers

- [Optimizing Relevance and Revenue in Ad Search: A Query Substitution Approach](https://www.microsoft.com/en-us/research/publication/optimizing-relevance-and-revenue-in-ad-search-a-query-substitution-approach/) — Broder et al., *SIGIR 2008*. Uses offline query substitution plus fast online matching while balancing relevance and revenue. `seminal`
- [Interpreting Advertiser Intent in Sponsored Search](https://www.microsoft.com/en-us/research/publication/interpreting-advertiser-intent-in-sponsored-search/) — Azimi et al., *KDD 2015*. Uses organic search evidence to understand advertiser keywords and intent.
- [Diversity Driven Query Rewriting in Search Advertising](https://www.microsoft.com/en-us/research/publication/diversity-driven-query-rewriting-in-search-advertising/) — Yao et al., *KDD 2021*. Learns diverse close-variant rewrites with reinforcement learning. `production`
- [Bid Keyword Suggestion in Sponsored Search Based on Competitiveness and Relevance](https://www.microsoft.com/en-us/research/publication/bid-keyword-suggestion-in-sponsored-search-based-on-competitiveness-and-relevance/) — Zhang et al., *Information Processing & Management 2014*. Frames keyword recommendation around both semantic relevance and marketplace competition.
- [A Concept Knowledge-Driven Keywords Retrieval Framework for Sponsored Search](https://arxiv.org/abs/2102.10560) — Yang et al., 2021. Uses concept knowledge to expand keyword retrieval and improve coverage.

## Transferable adjacent reading

Modern Search work on spelling, segmentation, entity linking, semantic parsing, dense representations, and query rewriting transfers directly—but Ads adds advertiser intent, policy eligibility, commercial value, and auction feedback.

[Back to the hub](../README.md)
