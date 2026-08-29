# LLM / VLM / Agent Reliability Papers

A living, accuracy-first bibliography for **hallucination, uncertainty, and failure awareness** in modern foundation models.

**Web page:** https://ruixv.github.io/VLM_Hallucinations/  
**Repository:** https://github.com/ruixv/VLM_Hallucinations

## Scope

The collection covers three system families:

- **LLM** — large language models, reasoning models, RAG systems.
- **VLM / LVLM / MLLM** — vision-language and multimodal large language models.
- **Agent / Agentic AI / VLA** — tool-using agents, GUI agents, embodied agents, robot/VLA policies, and multi-agent systems when the paper explicitly studies reliability or failure awareness.

And the following research themes:

- hallucination **detection, localization, evaluation, attribution, and mitigation**;
- **uncertainty detection / estimation / quantification**, confidence, calibration, semantic uncertainty, knowledge boundaries;
- **failure detection / prediction / diagnosis / attribution**, runtime monitoring, OOD/error detection;
- **abstention, selective prediction / selective generation**, reliability-aware planning and evaluation;
- benchmarks and evaluation methods directly targeting these reliability failures.

The main venue priority is **CVPR, ICCV, ECCV, NeurIPS, ICLR, ICML**, with additional coverage of ACL/EMNLP/NAACL/AAAI and highly relevant top journals such as **IEEE TPAMI, Nature, Nature Machine Intelligence, Nature Communications**, plus other strong venues when the work is directly on-topic.

## Current coverage

The systematic refresh through **2026-08-29** added four further high-confidence ACL 2026 omissions verified from the official ACL Anthology: **Calibration-Aware Policy Optimization for Reasoning LLMs** (ACL 2026 Long Paper), **Every Response Counts: Quantifying Uncertainty of LLM-based Multi-Agent Systems through Tensor Decomposition** (ACL 2026 Long Paper), **NeuroSym-Cal: Bridging the Reasoning-Execution Gap in Code Generation via Hierarchical Calibration** (Findings of ACL 2026), and **LatentRefusal: Latent-Signal Refusal for Unanswerable Text-to-SQL Queries** (Findings of ACL 2026). These extend the collection's coverage of calibration, uncertainty-aware reasoning, multi-agent uncertainty, selective generation, refusal, and failure detection without relaxing the presentation-verification policy.

Conference presentation labels remain conservative: no Oral/Highlight/Spotlight/Poster designation is inferred without an authoritative presentation source. Journal records use `N/A`.

The web page computes the current unique-paper count after title-level deduplication across all loaded data files, so metadata upgrades and correction records do not inflate the displayed count.

Data layout:

- `data/papers.json` — original seed collection;
- `data/expanded_2023.json` … `data/expanded_2026.json` — systematic year-level expansion records;
- `data/expanded_2026_08_25.json` and `data/expanded_2026_08_26.json` — additional ACL 2026 papers verified in recent refreshes;
- `data/expanded_2026_08_26_pm_a.json` — ACL 2026 additions on black-box uncertainty estimation and reflective hallucination detection;
- `data/expanded_2026_08_26_pm_vista.json` — ACL 2026 VISTA multi-turn hallucination evaluation record;
- `data/expanded_2026_08_27.json` — ACL/EACL/Nature Portfolio additions verified through the 2026-08-28 refresh;
- `data/expanded_2026_08_29.json` — ACL 2026 calibration, multi-agent uncertainty, selective generation, and refusal additions verified on 2026-08-29;
- `data/corrections.json` — higher-confidence metadata corrections plus newly verified additions that should override older seed records;
- `index.html` — GitHub Pages browser that merges and deduplicates all records at load time.

## Presentation labels

Presentation status is deliberately conservative and uses **one normalized highest-status label per paper**:

- **Oral** — explicitly verified from an official conference oral schedule/page or equivalent primary record.
- **Highlight / Spotlight** — explicitly verified from the official venue record.
- **Poster** — explicitly verified from an official conference/virtual poster page or official OpenReview venue record.
- **Not verified** — the paper itself is verified as accepted/published, but no authoritative presentation-status evidence was found in the current pass.
- **N/A** — journal article or another venue where conference presentation type does not apply.

The precedence is **Oral > Highlight > Spotlight > Poster > Not verified**. If a conference record describes a paper as both a higher-status presentation and a poster, only the higher-status label is retained: `Oral + Poster → Oral`, `Highlight + Poster → Highlight`, and `Spotlight + Poster → Spotlight`. Poster is treated as the base presentation format and is not appended to a more selective designation.

A paper is **never inferred to be a poster simply because it is not listed as an oral**, and a third-party list does not override an official conference record.

## Verification policy

We prioritize, in order, official conference schedules/virtual pages, official OpenReview venue records, CVF Open Access, NeurIPS proceedings, PMLR, ACL Anthology, IEEE Xplore, Nature Portfolio, and official publisher/proceedings pages. arXiv and generic OpenReview submissions are useful for discovery, but are not sufficient by themselves to claim acceptance at a target venue.

Withdrawn, desk-rejected, or rejected submissions are excluded from accepted-paper lists. Workshop and position papers may be retained only when strongly relevant and are explicitly marked by track so that they are not confused with main-conference papers.

## Automated refresh

The collection is re-checked **every 12 hours**. Each run searches for new papers and metadata changes, verifies venue/track/presentation status against authoritative sources, normalizes presentation labels to the highest verified status, deduplicates records, and updates this repository only when there is a substantive verified change.

See [`SCHEDULED_UPDATE.md`](SCHEDULED_UPDATE.md) for the detailed protocol.

## GitHub Pages

If Pages is not already enabled: **Settings → Pages → Deploy from a branch → `master` → `/ (root)`**. The site can then be served at https://ruixv.github.io/VLM_Hallucinations/.

## Corrections

Accuracy is more important than maximizing the raw paper count. If you find a wrong venue, track, author list, presentation type, duplicate, or missing high-confidence paper, please open an issue or submit a correction with an authoritative source.