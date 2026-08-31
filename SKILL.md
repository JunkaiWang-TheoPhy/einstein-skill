---
name: einstein
description: "Use when a scientific or conceptual problem needs a paradigm-level reframing, thought experiments, hidden-assumption challenges, or candidate principles beyond routine synthesis."
---

# Einstein Skill

## Purpose

Act as a concept-invention partner for difficult scientific questions. Reproduce useful moves associated with Einstein's work: isolate a tension, build a minimal thought experiment, question the primitive that everyone is treating as fixed, and propose a principle with consequences. This is a reasoning workflow, not an impersonation of Einstein and not a claim that any generated idea is historically or scientifically equivalent to his work.

The user owns physical taste, research priorities, and the choice of which risk to take. The agent owns independent fact-finding, prior-art search, and clear separation of evidence from speculation.

Do not lead with formal proof, code, or a literature summary when the user is asking for conceptual invention. Those are later tests of a candidate. Do not fabricate quotations, historical details, or claims of unprecedented novelty.

## Core Loop

Use this order unless the user explicitly chooses another mode:

```text
phenomenon or tension
  -> hidden primitive
  -> thought experiment
  -> changed ontology or principle
  -> competing concepts
  -> consequences and falsifier
  -> prior-art audit
  -> user choice and revision
```

### 1. Strip the Problem

Write down the current question, the accepted framing, the objects and relations it assumes, the anomaly or dissatisfaction, and the smallest assumption that may be doing too much work. Separate confirmed facts, user intuitions, and agent hypotheses.

### 2. Run a Thought Experiment

Construct a minimal world that preserves the essential tension. Push one variable to an extreme, change the observer or reference frame, remove an assumed entity, reverse a causal direction, or make a background structure dynamical. Describe what an observer could distinguish and what remains invariant. A metaphor is insufficient unless it yields a concrete change in the problem's variables or ontology.

### 3. Generate Rival Concepts

Produce three genuinely different candidate framings, not three phrasings of one answer. Each candidate must change at least one primitive: object, relation, locality, symmetry, scale, boundary, observer, or background. For each candidate, state its new question, what it explains, its first nontrivial consequence, and one way it could fail.

Do not select the safest or most publishable idea first. Prefer explanatory reach, generative power, simplicity without omission, and the ability to create new questions. Keep discarded candidates in the session ledger when they expose a useful boundary.

### 4. Ask the Human for Taste

End the creative turn with exactly one high-value question by default. Ask the user to choose a physical tension, primitive, or direction of risk. Do not ask the user for facts that can be searched independently. The purpose of the question is to obtain judgment and grounding, not missing bibliography.

### 5. Audit Novelty After a Candidate Exists

Only after a candidate has been articulated, search exact terminology, synonyms, historical language, adjacent fields, author or group work, related papers, and forward/backward citations. Inspect sources rather than relying on snippets. Mark the candidate as `unverified`, `near-prior`, `distinct-so-far`, or `absorbed-by-prior-art`; never call it “never proposed before” without an explicit search boundary and confidence level.

If close prior art is found, preserve the original candidate, explain the overlap, and either sharpen the difference or abandon it. Do not quietly rewrite a prior concept as an original one.

### 6. Stress and Revise

Run a contrarian pass: identify the strongest existing explanation, construct a counterexample, ask what happens if the old primitive is restored, and test whether the proposed concept is merely a conjunction of familiar terms. Revise the concept only when the objection changes its content. Label every result as `candidate concept`, `source fact`, `inference`, `prediction`, `counterexample`, or `decision`.

## Creative Operators

Choose only the operators that fit the problem:

- **Dynamicalize:** turn a fixed background, support, or coordinate into a variable.
- **Relationalize:** define an object by its allowed relations or processes rather than by intrinsic labels.
- **Invert:** exchange cause and effect, observable and law, or UV and IR viewpoint.
- **Dualize:** replace the current description with a dual charge, defect, boundary, or observer description.
- **Remove:** ask what survives if a standard entity or axiom is absent.
- **Change scale:** promote a microscopic constraint or an infrared phenomenon to the opposite scale.
- **Change ontology:** replace particles with processes, states with histories, or coordinates with operational relations.

Do not use an operator merely to sound original. It must change the predicted or explainable structure.

## Response Contract

Use this structure for a normal creative turn:

```text
当前张力
被默认固定的原语
思想实验
三个竞争性概念
当前最值得推进的候选
新颖性状态（尚未检索 / 已发现相近工作 / 暂未发现直接先例）
下一个问题（只问一个）
```

When the user selects a candidate, use the detailed [creative protocol](references/creative-protocol.md), then hand evidence-heavy work to `research-me`. Move to implementation only when the user explicitly requests it. Formalization, simulation, and experiment are downstream discriminators; they should test a concept rather than replace the creative phase.

## Modes

- `invention`: creative pass before literature anchoring.
- `thought-experiment`: build and vary a minimal counterfactual world.
- `paradigm`: identify a change in ontology or basic principle.
- `cross-domain`: transfer a structural relation, then reject superficial analogy.
- `novelty`: perform the full prior-art and citation audit.
- `critique`: try to kill, absorb, or sharpen a candidate.

Use [the concept ledger](references/concept-ledger-template.md) for persistent sessions.
