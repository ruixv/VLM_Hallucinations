# LLM / VLM / Agent Reliability Papers

A living, accuracy-first bibliography for **hallucination, uncertainty, and failure awareness** in modern foundation models.

**Web page:** https://ruixv.github.io/VLM_Hallucinations/  
**Repository:** https://github.com/ruixv/VLM_Hallucinations

## Scope

The collection covers **LLMs**, **VLM/LVLM/MLLMs**, and **agents/agentic systems**, with emphasis on hallucination detection/evaluation/mitigation, uncertainty estimation/calibration/confidence/reliability, failure/OOD/error detection, abstention and selective prediction.

Priority venues include **CVPR, ICCV, ECCV, NeurIPS, ICLR, ICML, ACL, EMNLP, NAACL, AAAI, IEEE TPAMI/PAMI, IEEE TMM**, and highly relevant Nature Portfolio journals including **Nature, Nature Machine Intelligence, Nature Communications, and Scientific Reports** when directly on-topic. Other strong venues are included only when justified by topical relevance and source quality.

## Current coverage

The systematic refresh through **2026-09-02** adds six high-confidence official ACL/EACL proceedings records that were not present in the repository:

- **HALP: Detecting Hallucinations in Vision-Language Models without Generating a Single Token** — EACL 2026 Main Conference · Long Paper; pre-generation hallucination-risk prediction from VLM internal representations, with implications for abstention and selective routing.
- **Prompting the Unknown: Understanding Response Uncertainty in Large Language Models** — Findings of ACL 2026; theoretical and empirical analysis of prompt informativeness and response uncertainty.
- **PretrainRL: Alleviating Factuality Hallucination of Large Language Models at the Beginning** — Findings of ACL 2026; pretraining-stage factuality intervention for hallucination mitigation.
- **Fine-Grained Detection of Context-Grounded Hallucinations Using LLMs** — Findings of ACL 2026; fine-grained context-grounded hallucination detection and error characterization.
- **HalluGuard: Evidence-Grounded Small Reasoning Models to Mitigate Hallucinations in Retrieval-Augmented Generation** — Findings of ACL 2026; evidence-grounded RAG hallucination detection/guardrailing.
- **Faithfulness-Aware Uncertainty Quantification for Fact-Checking the Output of Retrieval-Augmented Generation** — Findings of ACL 2026; faithfulness-aware uncertainty quantification and factual-error detection for RAG.

The September 1 increment remains available in `data/expanded_2026_09_01.json` and contains ten previously verified records spanning hallucination detection/mitigation, uncertainty/calibration, failure detection, and abstention.

Conference presentation labels remain conservative: no Oral/Highlight/Spotlight/Poster designation is inferred without an authoritative presentation source. Journal records use `N/A`.

## Data layout

- `data/papers.json` — canonical seed collection.
- `data/expanded_2023.json` … `data/expanded_2026.json` — year-level expansion records.
- dated files such as `data/expanded_2026_08_25.json` … `data/expanded_2026_09_02.json` — high-confidence additions and corrections from systematic refreshes.
- `data/corrections.json` — higher-confidence metadata corrections and override records.
- `index.html` — GitHub Pages browser; it merges all loaded sources and deduplicates by normalized canonical title, with later correction records overriding earlier metadata.

## Presentation labels

Exactly one highest verified presentation label is stored per conference paper:

- **Oral**
- **Highlight**
- **Spotlight**
- **Poster**
- **Not verified**

The precedence is **Oral > Highlight > Spotlight > Poster > Not verified**. Combination labels are normalized to the highest status only: `Oral + Poster → Oral`, `Highlight + Poster → Highlight`, and `Spotlight + Poster → Spotlight`. Poster is treated as the base presentation format and is never appended to a higher-prestige designation.

A paper is never inferred to be a poster simply because it is not listed as an oral. Journals use `N/A`.

## Verification policy

We prioritize official conference schedules/virtual pages, official OpenReview venue records, CVF Open Access, NeurIPS proceedings, PMLR, ACL Anthology, IEEE Xplore, Nature Portfolio, and official publisher/proceedings pages. arXiv and generic OpenReview submissions may be used for discovery, but are not sufficient by themselves to claim venue acceptance.

Withdrawn, desk-rejected, and rejected submissions are excluded from accepted-paper lists. Workshop, Findings, Student Research Workshop, Dataset/Benchmark, Industry, and other non-main tracks are explicitly distinguished when retained.

## Automated refresh

Each refresh searches for new papers and metadata changes, verifies venue/track/presentation status against authoritative sources, normalizes presentation labels, deduplicates records, and commits only when there is a substantive verified addition or correction.

See [`SCHEDULED_UPDATE.md`](SCHEDULED_UPDATE.md) for the detailed protocol.

## Corrections

Accuracy is more important than maximizing raw paper count. If you find an incorrect venue, track, author list, presentation type, duplicate, or missing high-confidence paper, please open an issue or submit a correction with an authoritative source.