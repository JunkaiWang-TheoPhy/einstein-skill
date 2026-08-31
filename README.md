# Einstein Skill

🇺🇸 [English](README.md) | 🇨🇳 [中文](README.zh.md)

[![License: AGPL-3.0](https://img.shields.io/badge/license-AGPL--3.0-blue)](LICENSE)

## Overview

Einstein Skill is a concept-invention workflow for scientific and difficult conceptual problems. It first compares the available angles, selects the most beautiful and generative one, tests whether a local fact can organize a global structure, and then helps an agent construct a thought experiment, change the problem's ontology, state a bold conjecture, and identify consequences before prior-art research begins.

This is not an Einstein impersonation prompt. It does not guarantee originality, physical truth, or historical equivalence to Einstein's work. It is a structured way to create ambitious candidates without confusing a new phrase with a new concept.

## Usage

```text
$einstein
I want to study whether subsystem symmetry can give rise to Hořava gravity.
Do not begin with formalization or a literature summary. Find the hidden assumption,
run a thought experiment, and propose genuinely different conceptual directions.
```

## Core Loop

```text
phenomenon or tension
  -> angle scan
  -> most generative / beautiful angle
  -> local-to-global bridge
  -> hidden primitive
  -> thought experiment
  -> bold conjecture
  -> rival explanations
  -> consequences and falsifiers
  -> prior-art audit
  -> human choice and revision
```

The creative pass comes before literature anchoring by default. A beautiful conjecture is a discovery heuristic, not evidence. Robust analysis and risky extrapolation remain separate. Once a candidate exists, the skill searches exact and neighboring terminology, historical formulations, related fields, authors, groups, and citation paths. It labels the result as `unverified`, `near-prior`, `distinct-so-far`, or `absorbed-by-prior-art` rather than claiming that nobody has proposed it.

## What It Forces the Agent to Do

- Question an object, relation, locality, symmetry, scale, boundary, observer, or background that the original problem treats as fixed.
- Compare multiple angles and state which one has the strongest compression, bridge, and generative reach.
- Test whether a local, internal, microscopic, or algebraic datum can organize a global, geometric, spacetime, or representation-level structure.
- State one central conjecture before generating two or three rival explanations.
- State what each candidate explains, what it predicts, and how it could fail.
- Keep robust interpretation separate from the explicit risk of a bold extrapolation.
- Ask the human for physical taste only when it has not already been supplied.
- Preserve discarded candidates when they clarify a boundary.
- Return to the concept after a serious objection instead of adding decorative jargon.

## Files

```text
SKILL.md                                  # Runtime workflow
agents/openai.yaml                        # Codex metadata
references/creative-protocol.md           # Detailed ideation procedure
references/concept-ledger-template.md     # Persistent concept record
evals/evals.json                          # Behavioral pressure cases
docs/related-projects.md                  # Public design comparison
```

## Install

Clone this repository into the skills directory used by the client. For Codex:

```bash
CODEX_HOME="${CODEX_HOME:-$HOME/.codex}"
git clone https://github.com/JunkaiWang-TheoPhy/einstein-skill.git \
  "$CODEX_HOME/skills/einstein"
```

For evidence-heavy research, pair it with [`research-me`](https://github.com/JunkaiWang-TheoPhy/research-me-skill) after the creative pass. Use a private session record for private research context.

## Limitations

The skill improves the search process for concepts; it cannot prove that a concept is unprecedented or correct. Current novelty still requires a systematic search and expert judgment. A thought experiment is useful only when it changes an observable, constraint, or ontology; an attractive analogy alone is not a scientific result.

## Version and License

Version `0.1.1`. Distributed under the [GNU Affero General Public License v3.0](LICENSE).
