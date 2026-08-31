# Related Projects and Design Notes

Reviewed: 2026-08-31

Einstein Skill is a new workflow package. The projects below are reference points, not dependencies and not claims that the same scientific capability has already been solved.

## Existing Einstein Skill

[nuwa-skills/einstein-skill](https://github.com/nuwa-skills/einstein-skill) is a public MIT-licensed skill that distills thought experiments, first-principles reasoning, reference-frame switching, counter-intuitive thinking, and cross-domain analogy. Its own examples are useful as a style baseline.

Einstein Skill keeps that useful vocabulary but changes the acceptance contract: a thought experiment must change an observable, constraint, or ontology; a candidate must have a consequence and a falsifier; and novelty remains unverified until a later search. This public repository is an independent implementation and does not copy its text.

## Hypothesis-Generation Systems

[Google AI Co-Scientist](https://research.google/blog/accelerating-scientific-breakthroughs-with-an-ai-co-scientist/) uses scientific debate, ranking tournaments, and evolution to generate and improve hypotheses. [Hypothesis Generation](https://labs.google/science/) exposes a related multi-agent research experiment.

[LLNL Open AI Co-Scientist](https://github.com/llnl/open-ai-co-scientist) is an open implementation with generation, reflection, ranking, evolution, proximity, and meta-review components.

These systems motivate the idea of competing candidates and iterative revision. Einstein Skill differs in sequencing: it starts with an unanchored conceptual pass so that literature does not define the entire search space, then performs a prior-art audit.

[HypoGeniC and HypoRefine](https://github.com/ChicagoHAI/hypothesis-generation) provide data-driven and literature-aware hypothesis-generation approaches. They are relevant for the later evidence phase, while Einstein Skill focuses on changing the problem's primitives before retrieval.

## Automated Discovery Systems

[FunSearch](https://github.com/google-deepmind/funsearch) and [AlphaEvolve](https://deepmind.google/blog/alphaevolve-a-gemini-powered-coding-agent-for-designing-advanced-algorithms/) show how language-model proposals can be combined with evolutionary search and explicit evaluators. They are strongest when the representation and objective are already defined. They do not by themselves solve the problem of inventing the representation or the scientific question.

[AI Scientist](https://github.com/SakanaAI/AI-Scientist) and [AI Scientist-v2](https://github.com/SakanaAI/AI-Scientist-v2) demonstrate end-to-end idea, experiment, analysis, and paper loops, mainly in machine learning. Their repositories warn that the system executes model-written code and should be isolated. They are useful workflow references, not evidence that an agent can independently create a new physical ontology.

## Evaluation of Idea Generation

[IdeaBench](https://arxiv.org/abs/2411.02429) treats research-idea generation as an evaluable task with dimensions such as novelty and feasibility. [Can LLMs Generate Novel Research Ideas?](https://arxiv.org/abs/2409.04109) highlights the difficulty of judging novelty even with expert evaluators. These limitations are why this skill never uses the model's own declaration of originality as proof.

## Design Decisions

1. Separate invention from retrieval so the first search result does not become the concept.
2. Require a changed primitive and a new consequence to distinguish concepts from names.
3. Keep rival ideas alive long enough to obtain human physical taste.
4. Treat novelty as a bounded audit result, never as a global negative claim.
5. Use research tools and formal or numerical tools after a candidate exists, as discriminators rather than as substitutes for imagination.

## Verification Trail

The public source pages above were inspected on 2026-08-31. The comparison records design features and stated limitations; it does not endorse the scientific conclusions of any referenced system.
