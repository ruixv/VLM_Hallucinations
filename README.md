# LLM / VLM / Agent Reliability Papers

A living, accuracy-first bibliography for **hallucination, uncertainty, and failure awareness** in modern foundation models.

**Web page:** https://ruixv.github.io/VLM_Hallucinations/  
**Repository:** https://github.com/ruixv/VLM_Hallucinations

## Scope

The collection covers **LLMs**, **VLM/LVLM/MLLMs**, and **agents/agentic systems**, with emphasis on hallucination detection/evaluation/mitigation, uncertainty estimation/calibration/confidence/reliability, failure/OOD/error detection, abstention and selective prediction.

Priority venues include **CVPR, ICCV, ECCV, NeurIPS, ICLR, ICML, ACL, EMNLP, NAACL, AAAI, IEEE TPAMI/PAMI, IEEE TMM**, and highly relevant Nature Portfolio journals including **Nature, Nature Machine Intelligence, Nature Communications, and Scientific Reports** when directly on-topic. Other strong venues are included only when justified by topical relevance and source quality.

## Current coverage

The systematic refresh through **2026-09-05** adds eight newly verified NeurIPS 2025 records that were not present in the repository. All eight have official NeurIPS virtual presentation pages and are therefore verified as **Poster**:

- **On Epistemic Uncertainty of Visual Tokens for Object Hallucinations in Large Vision-Language Models** — uncertainty analysis and hallucination mitigation.
- **Poison as Cure: Visual Noise for Mitigating Object Hallucinations in LVMs** — object-hallucination mitigation via visual perturbation.
- **Grounding Language with Vision: A Conditional Mutual Information Calibrated Decoding Strategy for Reducing Hallucinations in LVLMs** — calibrated decoding and visual grounding.
- **The Curse of Multi-Modalities: Evaluating Hallucinations of Large Multimodal Models across Language, Visual, and Audio** — multimodal hallucination benchmark/evaluation.
- **GLSim: Detecting Object Hallucinations in LVLMs via Global-Local Similarity** — training-free hallucination detection.
- **Mitigating Hallucination in VideoLLMs via Temporal-Aware Activation Engineering** — VideoLLM hallucination mitigation.
- **ViCrit: A Verifiable Reinforcement Learning Proxy Task for Visual Perception in VLMs** — hallucination localization/critic training.
- **Auditing Meta-Cognitive Hallucinations in Reasoning Large Language Models** — reasoning-chain hallucination auditing and detection.

The September 4 increment remains available in `data/expanded_2026_09_04.json`.

The September 3 increment remains available in `data/expanded_2026_09_03.json` and `data/expanded_2026_09_03_pm.json`. The September 2 increment remains available in `data/expanded_2026_09_02.json`, and the September 1 increment remains available in `data/expanded_2026_09_01.json`.

Conference presentation labels remain conservative: no Oral/Highlight/Spotlight/Poster designation is inferred without an authoritative presentation source. Journal records use `N/A`.

## Data layout

- `data/papers.json` — canonical seed collection.
- `data/expanded_2023.json` … `data/expanded_2026.json` — year-level expansion records.
- dated files such as `data/expanded_2026_08_25.json` … `data/expanded_2026_09_05.json` — high-confidence additions and corrections from systematic refreshes.
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