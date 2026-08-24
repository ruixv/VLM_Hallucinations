# Scheduled Update Protocol

This repository is maintained with an **accuracy-first 12-hour research update cycle**.

## Search scope

Every run should search for new or newly verified work in:

- **CVPR / ICCV / ECCV**
- **NeurIPS / ICLR / ICML**
- **IEEE Transactions on Pattern Analysis and Machine Intelligence (TPAMI / PAMI)**
- **Nature** and relevant **Nature Portfolio** journals
- arXiv / OpenReview may be used for *discovery*, but must not be treated as proof of conference or journal acceptance unless the official venue record confirms it.

Primary concepts and aliases:

- LLM hallucination, factuality, faithfulness, factual error, knowledge hallucination
- VLM / LVLM / MLLM / multimodal hallucination
- object hallucination, visual hallucination, visual grounding failure
- hallucination detection, evaluation, benchmark, attribution, mechanism
- hallucination mitigation, decoding, steering, intervention, alignment, RAG, verification
- multimodal reasoning hallucination, modality conflict, visual evidence reliance

## Source priority

Use authoritative sources in this order whenever possible:

1. Official conference / journal pages and proceedings
2. Official OpenReview venue records
3. CVF Open Access for CVPR / ICCV
4. NeurIPS or PMLR proceedings
5. IEEE Xplore / Nature Portfolio article pages
6. arXiv only for discovery or supplementary metadata
7. Project pages / GitHub only for code links, never as the sole acceptance proof

## Acceptance and presentation verification

Do **not** infer acceptance from a preprint title, author CV, Google Scholar snippet, lab news page, or citation metadata alone.

For each paper, explicitly verify:

- exact title
- authors
- venue and year
- main conference / findings / workshop / datasets-and-benchmarks track, where relevant
- presentation status: `Oral`, `Highlight`, `Spotlight`, `Poster`, or `Not verified`

Only assign Oral / Highlight / Spotlight / Poster when the official venue or OpenReview record states it. If no authoritative presentation label is found, store `Not verified`.

Withdrawn, rejected, desk-rejected, workshop-only, and unverified submissions must never be mislabeled as top-conference accepted papers.

## Deduplication

Normalize titles by case, punctuation, whitespace, and common Unicode variants. Prefer DOI / OpenReview ID / arXiv ID when available. If the same work moves from preprint to an accepted venue, update the canonical record rather than create a duplicate.

## Update targets

When verified changes are found:

1. Update `data/papers.json`.
2. Update the `meta.last_updated` timestamp and `meta.paper_count`.
3. Keep `index.html` compatible with the current schema.
4. Update `README.md` when scope, statistics, or important curation rules change.
5. Commit with a concise message such as `Update hallucination papers: 2026-08-25 AM`.

If no substantive verified change is found, do not create a noise commit.

## Quality control

Before committing a new record, ask:

- Is this paper genuinely about hallucination/factuality/faithfulness rather than merely mentioning the term?
- Is the claimed venue supported by an official source?
- Is the presentation type supported by an official source?
- Is the paper already in the database under another title/version?
- Is the URL stable and authoritative?
- Are the domain (`LLM` vs `VLM`) and topic tags reasonable?

Accuracy has priority over paper count and update speed.
