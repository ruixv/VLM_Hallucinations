# LLM / VLM / Agent Reliability Papers

A living, accuracy-first bibliography for **hallucination, uncertainty, and failure awareness** in modern foundation models.

**Web page:** https://ruixv.github.io/VLM_Hallucinations/  
**Repository:** https://github.com/ruixv/VLM_Hallucinations

## Scope

The collection covers **LLMs**, **VLM/LVLM/MLLMs**, and **agents/agentic systems**, with emphasis on hallucination detection/evaluation/mitigation, uncertainty estimation/calibration/confidence/reliability, failure/OOD/error detection, abstention and selective prediction.

Priority venues include **CVPR, ICCV, ECCV, NeurIPS, ICLR, ICML, ACL, EMNLP, NAACL, AAAI, IEEE TPAMI/PAMI, IEEE TMM**, and highly relevant Nature Portfolio journals. Other strong venues are included only when directly on-topic.

## Current coverage

The systematic refresh through **2026-08-31** now includes six high-confidence ACL/EACL 2026 additions verified from the official ACL Anthology:

- **Reducing Hallucinations in LLMs via Factuality-Aware Preference Learning** — Findings of ACL 2026; hallucination mitigation, factuality-aware preference optimization, and OOD reliability.
- **Answering the Wrong Question: Reasoning Trace Inversion for Abstention in LLMs** — ACL 2026 Main Conference · Long Paper; abstention/selective prediction, reasoning failure detection, and hallucination mitigation.
- **Knowing When to Abstain: Medical LLMs Under Clinical Uncertainty** — EACL 2026 Main Conference · Long Paper; uncertainty estimation, calibration/reliability, and abstention under clinical uncertainty.
- **Harmful Factuality: LLMs Correcting What They Shouldn’t** — Findings of EACL 2026; a source-faithfulness failure mode where models replace source content with factually correct but unfaithful information, plus a simple mitigation.
- **The Unintended Trade-off of AI Alignment: Balancing Hallucination Mitigation and Safety in LLMs** — Findings of EACL 2026; analyzes truthfulness/refusal coupling and proposes a mitigation that preserves refusal behavior while reducing hallucination pressure.
- **Decomposed Prompting Does Not Fix Knowledge Gaps, But Helps Models Say “I Don’t Know”** — Findings of ACL 2026; disagreement-based uncertainty/error detection and training-free abstention for closed-book QA.

An initially rediscovered paper, **Efficient Hallucination Detection in Automatic Code Generation**, was not counted as new because it was already present in `data/corrections.json`; the refresh therefore preserves title-level deduplication rather than inflating the bibliography.

Conference presentation labels remain conservative: no Oral/Highlight/Spotlight/Poster designation is inferred without an authoritative presentation source. Journal records use `N/A`.

## Data layout

- `data/papers.json` — canonical seed collection.
- `data/expanded_2023.json` … `data/expanded_2026.json` — year-level expansion records.
- `data/expanded_2026_08_25.json` … `data/expanded_2026_08_31.json` — dated high-confidence additions and corrections from systematic refreshes.
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