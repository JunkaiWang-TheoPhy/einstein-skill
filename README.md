# Einstein Skill

<p align="center">
  <a href="README.md">🇺🇸 English</a> |
  <a href="README.zh.md">🇨🇳 中文</a>
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-AGPL--3.0-blue" alt="License: AGPL-3.0"></a>
</p>

<p align="center">
  <img src="assets/einstein-laboratory-banner.png" alt="Albert Einstein studying a test tube in a sepia laboratory">
</p>

## The Story

### The tension

AI systems can be very good at local analysis: derive a consequence, summarize a paper, or optimize a calculation. Theory building asks for a different move. A theorist may see several valid angles and care most about the one that explains why two descriptions belong together. For example: why might an internal global charge spectrum have anything to do with a spacetime representation? A flat answer can list the two topics and still miss the question.

### The insight

The valuable leap is often a local-to-global bridge. Local, internal, microscopic, or algebraic data may organize a global, geometric, spacetime, or representation-level structure. The bridge can be wrong. Its value is that it compresses previously separate facts, makes a connection feel less accidental, and creates a new consequence worth trying to break.

### The response

Einstein Skill makes that theory choice explicit. It scans the available angles, selects the one with the strongest combination of compression and generative reach, runs a thought experiment, states one bold conjecture, and only then produces rival explanations and a prior-art audit. Robust analysis and risky extrapolation stay separate. The human supplies physical taste and the acceptable risk; the agent supplies search, comparison, and evidence boundaries.

### The boundary

This is not an Einstein impersonation prompt. It does not guarantee originality, physical truth, or historical equivalence to Einstein's work. It encodes a disciplined way to keep a beautiful conjecture alive long enough to test it without confusing elegance with evidence.

## Research Basis

The design is motivated by the following verified sources. They motivate the workflow; they do not establish that this Skill improves scientific discovery.

| Design question | Reference | What it contributes |
| --- | --- | --- |
| What capability is missing between prediction and theory building? | [Shalyt, Regev, Soljačić, and Kaminer, *Can AI Follow In Einstein's Footsteps?* (2026)](https://arxiv.org/abs/2607.27794) | Frames asking the right questions, inventing principles, and proposing falsification tests as a missing part of paradigm-level physics discovery. |
| What fails when LLM research ideas are evaluated? | [Si, Yang, and Hashimoto, *Can LLMs Generate Novel Research Ideas?* (2024)](https://arxiv.org/abs/2409.04109) | Reports a controlled human study and identifies weaknesses in self-evaluation and diversity, supporting explicit human taste and rival generation. |
| How can generated research ideas be evaluated? | [Guo et al., *IdeaBench* (2024)](https://arxiv.org/abs/2411.02429) | Separates dimensions such as novelty, feasibility, and insight instead of treating “new” as a single self-reported score. |
| What is the historical anchor for principle-first theory construction? | [A. Einstein, *Zur Elektrodynamik bewegter Körper* (1905)](https://doi.org/10.1002/andp.19053221004) | Primary source anchor for the historical paper behind the Einstein reference in this Skill's name. |

### References

1. Michael Shalyt, Nathan Regev, Marin Soljačić, and Ido Kaminer, “Can AI Follow In Einstein's Footsteps?”, arXiv:2607.27794 (2026). [arXiv record](https://arxiv.org/abs/2607.27794).
2. Chenglei Si, Diyi Yang, and Tatsunori Hashimoto, “Can LLMs Generate Novel Research Ideas? A Large-Scale Human Study with 100+ NLP Researchers”, arXiv:2409.04109 (2024). [arXiv record](https://arxiv.org/abs/2409.04109).
3. Sikun Guo et al., “IdeaBench: Benchmarking Large Language Models for Research Idea Generation”, arXiv:2411.02429 (2024). [arXiv record](https://arxiv.org/abs/2411.02429).
4. A. Einstein, “Zur Elektrodynamik bewegter Körper”, *Annalen der Physik* (1905). [Publisher record and DOI](https://doi.org/10.1002/andp.19053221004).

## Workflow Overview

The workflow begins with a theoretical choice, then turns that choice into a candidate that can be challenged:

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
assets/einstein-laboratory-banner.png # Generated README cover image
SKILL.md                                  # Runtime workflow
agents/openai.yaml                        # Codex metadata
references/creative-protocol.md           # Detailed ideation procedure
references/concept-ledger-template.md     # Persistent concept record
evals/evals.json                          # Behavioral pressure cases
docs/related-projects.md                  # Public design comparison
.github/PULL_REQUEST_TEMPLATE.md          # Story-first PR structure and references
docs/pull-request-story-and-references.md # PR narrative and citation standard
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

Version `0.1.2`. Distributed under the [GNU Affero General Public License v3.0](LICENSE).
