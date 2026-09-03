# LLM / VLM / Agent Reliability Papers

A living, accuracy-first bibliography for **hallucination, uncertainty, and failure awareness** in modern foundation models.

**Web page:** https://ruixv.github.io/VLM_Hallucinations/  
**Repository:** https://github.com/ruixv/VLM_Hallucinations

## Scope

The collection covers **LLMs**, **VLM/LVLM/MLLMs**, and **agents/agentic systems**, with emphasis on hallucination detection/evaluation/mitigation, uncertainty estimation/calibration/confidence/reliability, failure/OOD/error detection, abstention and selective prediction.

Priority venues include **CVPR, ICCV, ECCV, NeurIPS, ICLR, ICML, ACL, EMNLP, NAACL, AAAI, IEEE TPAMI/PAMI, IEEE TMM**, and highly relevant Nature Portfolio journals including **Nature, Nature Machine Intelligence, Nature Communications, and Scientific Reports** when directly on-topic. Other strong venues are included only when justified by topical relevance and source quality.

## Current coverage

The systematic refresh through **2026-09-03** adds five newly verified high-confidence records that were not present in the repository:

- **Accuracy and hallucinations in AI-generated medication dosing calculations: a sequential explanatory mixed-methods evaluation** — Scientific Reports 2026; evaluates hallucination frequency, numerical accuracy, reasoning errors, and reliability of ChatGPT, Gemini, and DeepSeek on standardized medication-dosing calculations.
- **Understanding New-Knowledge-Induced Factual Hallucinations in LLMs: Analysis and Interpretation** — Findings of ACL 2026; analyzes how learning unfamiliar knowledge induces and propagates factual hallucinations and studies attention-based mechanisms and mitigation.
- **Dynamic PMI-Guided Contrastive Decoding Reduces Hallucination in Large Language Models: A Unified Framework of Fine-Grained Input Transformations** — Findings of ACL 2026; proposes training-free contrastive decoding for hallucination mitigation and improved factuality/reasoning robustness.
- **Principled Detection of Hallucinations in Large Language Models via Multiple Testing** — Findings of ACL 2026; formulates hallucination detection as calibrated hypothesis testing with conformal p-values and controlled false-alarm rate.
- **MARCH: Multi-Agent Reinforced Check for Hallucination** — ACL 2026 Main Conference, Long Paper; uses specialized Solver/Proposer/Checker agents and multi-agent reinforcement learning for RAG hallucination verification and mitigation.

The September 2 increment remains available in `data/expanded_2026_09_02.json` and contains seven previously verified records spanning VLM hallucination detection, LLM uncertainty, RAG faithfulness/reliability, hallucination mitigation, and conversational failure evaluation. The September 1 increment remains available in `data/expanded_2026_09_01.json` and contains ten previously verified records spanning hallucination detection/mitigation, uncertainty/calibration, failure detection, and abstention.

Conference presentation labels remain conservative: no Oral/Highlight/Spotlight/Poster designation is inferred without an authoritative presentation source. Journal records use `N/A`.

## Data layout

- `data/papers.json` — canonical seed collection.
- `data/expanded_2023.json` … `data/expanded_2026.json` — year-level expansion records.
- dated files such as `data/expanded_2026_08_25.json` … `data/expanded_2026_09_03_pm.json` — high-confidence additions and corrections from systematic refreshes.
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