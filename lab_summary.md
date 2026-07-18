# Prompt Engineering Lab — Summary

Tested three tasks (sentiment classification, data extraction, product description) across v1 (zero-shot) and v3 (tuned) prompts at 15 runs each.

Sentiment improved from **43% to 93% consistency**, with the underlying label itself never wrong across five diverse test messages including sarcasm — only a cosmetic "Sentiment:" prefix remains unresolved.

Extraction improved from **14% to 100% consistency** on the base case and held 100% JSON validity across all four stress-test variations, though a genuine schema gap was found: messages with multiple orders dropped consistency to 79%, splitting across three different resolution strategies.

Product description held 0% raw text consistency by design (creative task) in both v1 and v3, but **v3 locked structural format to 100%**, **cut average length by ~75%**, and eliminated fabricated numeric specs — with one new price-triggered fabrication pattern discovered under stress testing.

**Key lesson:** text-uniqueness is a good consistency proxy for narrow tasks (sentiment, extraction) but a misleading one for creative generation, where structure, length, and hallucination control are the metrics that actually matter.