# xingtu-bci · AI Collaboration Bad Case Index

> Under local construction, not published yet. Records mistakes made when people collaborate with AI. Each case = symptom → root cause → actionable prevention.

[![License: MIT](https://img.shields.io/badge/License-MIT-orange.svg)](./LICENSE) ![Status](https://img.shields.io/badge/status-local-lightgrey)

## In one line

Turn rework, misjudgments, leaks, and false successes from AI collaboration into reusable guardrails. One bad case = one lesson plus one actionable prevention — no platitudes.

## Core principle: mechanisms only, no entities

This is the hard line for this repo. The value of a bad case lies in the **judgment mechanism** (how we reasoned wrong, how to prevent it), not in **project entities** (which API, which repo, which person). Therefore:

- Include: failure patterns, root-cause categories, actionable prevention, judgment rules, self-check questions.
- Exclude: API/class names, internal repo names, internal domains, client names, personal names, business data, commit hashes, internal issue IDs.

If a de-identified case loses its sense of the scene, restore it by keeping the decision chain and timeline — not by keeping entities.

## Case source (SSoT)

Cases come from the maintainer's long-running bad-case index (symptom → root cause → prevention), all de-identified into general mechanisms:

- Fabricated third-party mechanisms / second-hand numbers used as evidence
- Concurrent write-overwrite / success receipts that do not mean results landed
- Same fact in multiple copies, each rotting independently
- False negatives from using grep to validate Chinese content
- Internal meta-information leaking into public text (AI-writing fingerprint)
- Boundary judgment when changing shared methods, and "adding is safer than modifying"

External projects, when referenced, are only compared by form and mechanism, marked `public-source` with source link and check date. Never presented as first-hand testing.

## Boundaries with neighboring repos

| Repo | Covers | Does not cover |
|---|---|---|
| `xingtu-agent` | Agent deployment cases and decision chains | Does not focus on collaboration mistakes |
| `xingtu-testting` | Problems and judgment in AI testing | Does not record collaboration-process failures |
| **xingtu-bci** (this repo) | AI collaboration failure patterns and guardrails | Not a testing methodology or Agent scenario retrospective |

## Core content

- **Bad case cards**: uniform template — symptom → root cause → prevention → evidence → de-identification check.
- **Guardrail list**: executable rules promoted from cases (when to become a script gate, hook, or hard rule).
- **Promotion path**: a case starts as "record only"; promote to a hard rule only when evidence is sufficient. Do not turn one lesson into a global ban lightly.

## Quick start

```bash
git clone <repo-url> xingtu-bci
cd xingtu-bci
# Template: cases/_TEMPLATE.md; collected cases: cases/public/
```

Before adding a case, read `cases/_TEMPLATE.md` and fill in the status label and evidence source.

## Case status labels

| Label | Meaning |
|---|---|
| `design` | Design or idea only, not verified |
| `public-source` | Compiled from public material, not tested here; needs link and check date |
| `verified` | Run locally with reproducible evidence |
| `production` | In production use |

## Contribution rules (hard gates)

1. De-identify entities: no API names, internal repo names, domains, personal names, client names, issue IDs, or commit hashes.
2. De-identify time: absolute dates become relative week numbers, to prevent reverse-engineering project cycles.
3. De-identify quantities: no locally identifying scale figures.
4. Label source and verification level of every number; second-hand data is not a criterion.
5. Every case must be actionable — "be careful next time" is not prevention; "enumerate all callers before changing" is.

## License

[MIT](./LICENSE) · 行途 XingTu

## Author

行途 XingTu (engineering byline) · WeChat: 行途技术手记
