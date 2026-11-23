# LLM / VLM / Agent Reliability Papers

A living, accuracy-first bibliography for **hallucination, uncertainty, and failure awareness** in modern foundation models.

**Web page:** https://ruixv.github.io/VLM_Hallucinations/  
**Repository:** https://github.com/ruixv/VLM_Hallucinations

## Scope

The collection covers **LLMs**, **VLM/LVLM/MLLMs**, and **agents/agentic systems**, with emphasis on hallucination detection/evaluation/mitigation, uncertainty estimation/calibration/confidence/reliability, failure/OOD/error detection, abstention and selective prediction.

Priority venues include **CVPR, ICCV, ECCV, NeurIPS, ICLR, ICML, ACL, EMNLP, NAACL, AAAI, IEEE TPAMI/PAMI, IEEE TMM**, and highly relevant Nature Portfolio journals including **Nature, Nature Machine Intelligence, Nature Communications, and Scientific Reports** when directly on-topic. Other strong venues are included only when justified by topical relevance and source quality.

## Current coverage

The systematic refresh through **2026-10-28** adds **44 unique verified records** to the loaded bibliography. It backfills previously verified NeurIPS 2025 poster records, adds newly indexed **EMNLP 2026 Findings** on uncertainty calibration, answerability, hallucination detection, multimodal mitigation and agent reliability, and fills missed ACL/EACL and CVPR 2026 Main/Findings records.

Representative additions include:

- **FLOW-ABSTAIN: Modeling the Answerable Manifold for Query-Aware Abstention in Large Language Models** — EMNLP Findings of EMNLP 2026; abstention, answerability estimation, OOD detection.
- **Towards Reliable Truth-Aligned Uncertainty Estimation in Large Language Models** — EMNLP Findings of EMNLP 2026; uncertainty estimation, confidence calibration, hallucination detection.
- **Hallucination as Exploit: Evidence-Carrying Multimodal Agents** — EMNLP Findings of EMNLP 2026; agent failure detection, hallucination mitigation, evidence verification.
- **Two Pathways to Truthfulness: On the Intrinsic Encoding of LLM Hallucinations** — ACL Main Conference · Long Paper; hallucination detection, truthfulness representation, knowledge-boundary analysis.
- **A unified multi-domain framework for hallucination detection and reliability evaluation in large language models** — Scientific Reports Journal Article; hallucination detection, reliability evaluation, adversarial robustness.
- **Overthinking Causes Hallucination: Tracing Confounder Propagation in Vision Language Models** — CVPR Findings Track; hallucination detection, uncertainty analysis, reasoning failure analysis.

The update also adds the Scientific Reports article *A unified multi-domain framework for hallucination detection and reliability evaluation in large language models* (published 2026-10-15), and the Nature article *Training language models to be warm can reduce accuracy and increase sycophancy* (published 2026-04-29). Journal records use N/A for presentation.

The eight newly backfilled NeurIPS 2025 papers added from official virtual pages are recorded as **Poster**. New ACL/EMNLP/CVPR records remain **Not verified** unless an official presentation page supports a label. The legacy **Oral + Poster** value for *Semantic Uncertainty* is normalized to **Oral**; two existing NeurIPS 2025 seed records are upgraded to **Poster** from official virtual pages.

## Data layout

- `data/papers.json` — canonical seed collection.
- `data/expanded_2023.json` … `data/expanded_2026.json` — year-level expansion records.
- dated files such as `data/expanded_2026_08_25.json` … `data/expanded_2026_10_28.json` — high-confidence additions and corrections from systematic refreshes.
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
### 2026-11-18 verified additions

Two additional official EMNLP 2026 Findings papers are indexed in `data/expanded_2026_11_18.json`: **ToolHACE: A Dataset for Detecting Hallucinations in Tool-Based LLM Responses** (tool-augmented agent hallucination benchmark) and **DynHD: Hallucination Detection for Diffusion Large Language Models via Denoising Dynamics Deviation Learning**. Both have official ACL Anthology proceedings records; presentation status is **Not verified**. Other candidates require cross-file deduplication before inclusion.

### 2026-11-19 verification

Added **Dynamic Alignment Compensation for Hallucination Mitigation in Large Vision-Language Models** (Kairong Yu, Zixin Zhu, Le Yu, Hongwei Wang), **EMNLP 2026 Findings**, DOI `10.18653/2026.findings-emnlp.161`, official [ACL Anthology](https://aclanthology.org/2026.findings-emnlp.161/). The paper is stored in `data/expanded_2026_11_18.json` with `presentation: Not verified` because no official presentation label was established. Cross-file deduplication also confirmed that other screened ACL/EMNLP candidates were already represented in earlier expansion or correction files.

### 2026-11-19 additional official proceedings backfill

Five previously unlisted EMNLP 2026 papers are added in `data/expanded_2026_11_19.json`: **Agentic Uncertainty Quantification** (Findings), **INTRYGUE** (Main Conference), **When Response Variation Does Not Indicate Uncertainty** (Main Conference), **CHARM** (Findings), and **K-FinHallu** (Findings). Titles, author lists and venue/track were verified against their individual ACL Anthology records. All have `presentation: Not verified` pending explicit authoritative presentation evidence. The canonical seed `data/papers.json` remains unchanged.

### 2026-11-20 official proceedings verification

Three records were added to `data/expanded_2026_11_20.json`: **Exploring Agentic Tool-Calling Decisions via Uncertainty-Aligned Reinforcement Learning** (EMNLP 2026 Findings), **LLM Abstention Can Be a Prompt Artifact, in Addition to Genuine Uncertainty** (EMNLP 2026 Main Conference), and **Overview of SHROOM-Visions 2026** (UncertaiNLP workshop shared-task overview, **not** EMNLP Main). Official ACL Anthology metadata and DOIs were checked; all presentation labels remain **Not verified**. Previously indexed FLOW-ABSTAIN, Sieve and Sage, and related candidates were not duplicated.

### Additional official EMNLP Main papers — 2026-11-20

Three further official EMNLP 2026 Main Conference papers are included in `data/expanded_2026_11_20_pm.json`: **Beyond the Final Layer** (multilingual LLM calibration), **The Mirage of Calibrated Confidence** (VLM reasoning-trajectory confidence reliability), and **OmniHalluc-L** (multimodal hallucination benchmarking and perturbation calibration). Their official ACL Anthology records were checked; presentation status remains **Not verified**. These are separate from the earlier three November 20 additions.

### 2026-11-21 official EMNLP Main additions

Four ACL Anthology-verified EMNLP 2026 Main Conference papers were added in `data/expanded_2026_11_21.json`: **PropUQ-MAS** (uncertainty propagation in LLM multi-agent systems), **Last Step Matters** (long-horizon agent failure prediction), **HaluMem** (memory-system hallucination benchmark), and **Perceive, Localize, Reflect** (evidence-anchored MLLM multi-agent debate). All use the conservative presentation label **Not verified**. `data/papers.json` remains the canonical seed database.

### 2026-11-21 supplementary verified papers

Added **9 deduplicated official proceedings papers** in `data/expanded_2026_11_21_pm.json`: 4 EMNLP Main papers (AWA-RL search-agent abstention; ACA-RL missing-premise reasoning; RiskEval verbal confidence versus decisions; agent memory for unanswerable questions), 3 EMNLP Findings papers (Agent-Trident; hallucination-aware multi-agent RAG; OmniHallu), and 2 CVPR Main papers (Unstitching the Chimera; Thinking in Uncertainty). Official ACL Anthology/CVF sources verified venue and author metadata. Presentation is **Not verified** for all nine; no unverified Oral/Highlight/Spotlight/Poster was inferred. The canonical `data/papers.json` seed remains unchanged.

### 2026-11-22 verified EMNLP additions

Added three official proceedings papers in `data/expanded_2026_11_22.json`: **DualStake** (EMNLP 2026 Main; agent evidence/answer confidence calibration), **From Answers to Interpretations** (EMNLP 2026 Findings; ambiguity-induced aleatoric uncertainty), and **Tracking Truth Through Layers** (EMNLP 2026 Findings; TemHal cross-layer hallucination detection). Cross-file title checks found no prior records. Each is `Not verified` for presentation; no conference-presentation label was inferred. `data/papers.json` remains the canonical seed.

- **2026-11-22 supplemental verification:** Added *A Comprehensive Analysis for Visual Object Hallucination in Large Vision-Language Models* (Jing et al., EMNLP 2026 Findings), officially indexed at [ACL Anthology](https://aclanthology.org/2026.findings-emnlp.115/). Presentation: Not verified. The existing `data/expanded_2026_11_22.json` now contains four papers.

### 2026-11-23: verified agent reliability additions

Three official ACL Anthology records added in `data/expanded_2026_11_23.json`: **Ask or Assume? Uncertainty-Aware Clarification-Seeking in Coding Agents** (EMNLP 2026 Findings), **How to Speculate about Uncertainty in Agentic Coding? A Draft-Model Gate Method** (EMNLP 2026 Industry Track), and **SVR-MAD: A Bayesian-Inspired Framework for Posterior-Guided Multi-Agent Debate** (EMNLP 2026 Findings). All are marked `Not verified` for presentation; the Industry Track is not mislabeled as Main Conference.

### 2026-11-23 PM: verified EMNLP Main Conference backfill

Three additional official proceedings records were added in `data/expanded_2026_11_23_pm.json`: **AgentHallu** (agent hallucination step attribution), **LexAgentHallu** (legal-agent hallucination benchmark), and **Teaching LLMs to Abstain via Fine-Grained Semantic Confidence Reward** (confidence-based abstention). All are EMNLP 2026 Main Conference papers with presentation `Not verified`. Sources: [AgentHallu](https://aclanthology.org/2026.emnlp-main.925/), [LexAgentHallu](https://aclanthology.org/2026.emnlp-main.2121/), [Teaching LLMs to Abstain](https://aclanthology.org/2026.emnlp-main.243/).

## Verified additions — 2026-11-24

- **Breaking the Illusion: When Positive Meets Negative in Multimodal Decoding** — CVPR 2026 Main Conference, pp. 4210–4220; Yubo Jiang et al. The proposed Positive-and-Negative Decoding (PND) strengthens visual evidence while penalizing language-prior-driven hallucinations. Presentation: **Not verified**. [Official CVF record](https://openaccess.thecvf.com/content/CVPR2026/html/Jiang_Breaking_the_Illusion_When_Positive_Meets_Negative_in_Multimodal_Decoding_CVPR_2026_paper.html). Stored in `data/expanded_2026_11_24.json` after cross-file title deduplication; seed database unchanged.
