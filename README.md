# LLM / VLM Hallucination Papers

A curated, continuously updated research index for **LLM hallucination** and **VLM / MLLM hallucination**, with emphasis on top-tier conferences and journals.

> **Accuracy-first policy.** A paper is added only after its bibliographic identity and venue are verified against an authoritative source. Presentation labels such as **Oral / Highlight / Spotlight / Poster** are shown only when an official conference page, OpenReview venue record, or equivalent authoritative source explicitly supports the label. Otherwise the website displays **Not verified** rather than guessing.

## Scope

Priority venues include:

- Vision: **CVPR, ICCV, ECCV**
- Machine learning: **NeurIPS, ICLR, ICML**
- Journals: **IEEE TPAMI**, **Nature** and relevant Nature Portfolio journals
- Closely related top-tier work may be included when it directly advances hallucination understanding, evaluation, detection, grounding, factuality, or mitigation.

The index covers both:

- **VLM / MLLM hallucination**: object hallucination, visual grounding failures, modality conflict, multimodal reasoning hallucination, decoding/intervention/alignment methods, benchmarks and metrics.
- **LLM hallucination**: factuality, faithfulness, knowledge errors, detection, attribution, retrieval/verification, representation editing, decoding and training-time mitigation.

## Website

The static site is served by `index.html` and reads the canonical dataset from `data/papers.json`.

Features include full-text search and filtering by domain, venue, year, presentation type, and topic; official-source links; verification status; and update timestamps.

After enabling GitHub Pages for the repository root, the expected URL is:

`https://ruixv.github.io/VLM_Hallucinations/`

## Data schema

Each record stores:

- title and authors
- year, venue and track
- domain (`LLM` or `VLM`)
- topic tags
- presentation (`Oral`, `Highlight`, `Spotlight`, `Poster`, or `Not verified`)
- authoritative source URL and source type
- last verification date

## Update policy

The project is designed for a **12-hour update cycle**. Each run should:

1. Search recent authoritative conference/proceedings/journal sources plus arXiv/OpenReview for discovery.
2. Separate *new preprints/submissions* from *verified accepted papers*.
3. Verify venue and presentation labels from official sources before promoting them into the top-venue list.
4. Deduplicate by normalized title and, where available, DOI/arXiv/OpenReview identifier.
5. Update `data/papers.json`, `README.md` statistics / latest additions, and any derived webpage metadata.
6. Commit only substantive, verified changes.

See [`SCHEDULED_UPDATE.md`](SCHEDULED_UPDATE.md) for the detailed protocol.

## Current status

The repository was initialized on **2026-08-24** with an accuracy-first seed set verified from CVF Open Access, official OpenReview venue records, and NeurIPS proceedings. The first seed is intentionally conservative; subsequent scheduled passes should broaden historical coverage of LLM hallucination and top-journal papers without lowering verification standards.

## Contributing / corrections

If a venue, presentation label, title, or source is inaccurate, please open an issue with an authoritative link. Corrections should take priority over adding new papers.
