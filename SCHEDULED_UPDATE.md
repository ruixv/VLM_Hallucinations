# Scheduled Update Protocol

This repository is maintained as an **accuracy-first living bibliography** for LLM/VLM/Agent reliability. Automated refreshes run every 12 hours and should prefer a smaller, verifiable list over an inflated list with incorrect venue or presentation labels.

## 1. Research scope

Search all three system families:

1. **LLM** — language models, reasoning models, RAG systems.
2. **VLM / LVLM / MLLM** — vision-language and multimodal foundation models.
3. **Agent / Agentic AI / VLA** — tool-using, GUI, embodied, robotic and multi-agent systems when reliability/failure awareness is a central contribution.

Search the following concept families, including close variants:

- hallucination / confabulation / factuality / faithfulness;
- hallucination detection, localization, attribution, verification, evaluation and mitigation;
- uncertainty detection, estimation, quantification, decomposition and calibration;
- confidence estimation, semantic entropy / semantic uncertainty, knowledge boundaries;
- failure detection, failure prediction, error detection, failure diagnosis and failure attribution;
- runtime monitoring, trajectory monitoring, execution failure and agent failure;
- OOD / out-of-distribution detection when explicitly tied to LLM/VLM/Agent reliability;
- abstention, selective prediction, selective generation, selective planning;
- uncertainty-aware evaluators, reward/evaluation models and benchmarks when they directly detect or quantify reliability failures.

Do not include a paper merely because it mentions uncertainty or failures. Reliability detection/evaluation/quantification/mitigation must be a material part of the contribution.

## 2. Venue priorities

Primary conference targets: **CVPR, ICCV, ECCV, NeurIPS, ICLR, ICML**.

Also search **ACL, EMNLP, NAACL, AAAI** and other clearly strong venues when directly relevant.

Primary journal targets include **IEEE TPAMI/PAMI, Nature, Nature Machine Intelligence, Nature Communications**, and other top journals when the topic is a close match.

Workshop-only and position papers may be retained only when unusually relevant and must be explicitly marked as such. They must never be represented as main-conference papers.

## 3. Authoritative source hierarchy

Use authoritative sources whenever available:

1. official conference schedule, virtual conference, oral/highlight/spotlight/poster pages;
2. official OpenReview venue record;
3. CVF Open Access, NeurIPS proceedings, PMLR, ACL Anthology;
4. IEEE Xplore, Nature Portfolio, official journal/publisher pages;
5. author/project page only as supporting evidence when a stronger venue source does not expose the needed metadata;
6. arXiv / generic OpenReview submission for discovery only unless official acceptance is independently verified.

If sources conflict, the official venue record wins. Record unresolved conflicts conservatively.

## 4. Acceptance and track verification

For every candidate, verify as much as possible:

- exact title;
- author list;
- publication year;
- venue;
- main conference vs Findings vs workshop vs position paper vs dataset/benchmark track vs journal;
- canonical paper/venue URL;
- presentation type when applicable.

Exclude withdrawn, rejected and desk-rejected submissions from accepted-paper lists. Do not infer acceptance from an arXiv comment without an official venue record.

## 5. Presentation-status rules

Allowed values include `Oral`, `Highlight`, `Spotlight`, `Poster`, combinations such as `Oral + Poster` or `Spotlight + Poster`, `Not verified`, and `N/A` for journals.

Presentation status must be supported by a primary or official source. In particular:

- absence from an oral list does **not** prove Poster;
- an accepted-paper proceedings page alone does **not** prove Poster;
- an author-maintained list can support a label, but should not override a conflicting official conference page;
- when no authoritative presentation evidence is found, use **`Not verified`** instead of guessing.

## 6. Deduplication and metadata upgrades

Deduplicate by normalized canonical title, then use DOI / OpenReview / CVF / proceedings identifiers as secondary checks. Treat conference versions and their arXiv preprints as the same work unless the publication is substantively different.

When a preprint later becomes officially accepted, upgrade the existing record rather than adding a duplicate. When a presentation label is published later, update the existing record. `data/corrections.json` is loaded last by the web page and can be used for high-confidence metadata corrections that should override older seed records.

## 7. Repository update contract

Maintain:

- `data/papers.json` as the legacy/seed collection;
- `data/expanded_YYYY.json` as systematic year-specific expansion files;
- `data/corrections.json` for verified overrides;
- `README.md`, `index.html`, and this protocol so they remain consistent with the taxonomy and data model.

The web page must merge all datasets, normalize legacy `domain/topic` fields to the newer `system_type/research_tasks` taxonomy, deduplicate by title, and apply correction records last.

Commit only when there is a substantive verified addition, correction, or metadata upgrade. A no-change search should not create a cosmetic commit.

## 8. Reporting after each run

Report concisely:

- number and titles of newly added high-confidence papers;
- corrected venue/track/presentation metadata;
- newly verified Oral/Highlight/Spotlight/Poster labels;
- important candidates deliberately excluded because acceptance or status could not be verified;
- authoritative source families checked;
- whether GitHub was updated.

The guiding rule is **accuracy first, completeness second, and explicit uncertainty instead of invented metadata**.