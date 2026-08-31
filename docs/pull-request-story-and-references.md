# Pull Request Story and References Standard

## Principle

A pull request is a narrative research and engineering artifact. It should let a reviewer understand why the change exists, what insight motivated it, what evidence supports it, and what remains uncertain before asking them to inspect the implementation.

Technical correctness remains necessary, but a file list is not an explanation. The story comes first; the implementation inventory comes second.

## Required Story

Write the opening in this order:

1. **Tension:** the problem, contradiction, missing capability, or decision that created the need for the change.
2. **Insight or hypothesis:** the new understanding, conceptual bridge, or design choice.
3. **Intervention:** what was changed and why it is the appropriate response.
4. **Evidence:** tests, measurements, source inspection, experiments, or observed behavior.
5. **Consequence:** what the change now makes possible or what question it sharpens.
6. **Limits and next step:** uncertainty, failed paths, scope boundary, and the next decision.

Do not open with a chronological account of commands or a file-by-file changelog. Do not turn a speculative hypothesis into a fact merely because the implementation passes tests.

## Literature References

Scientific, research, and conceptual pull requests must include a claim-to-source map and references. Each important claim should point to the source that actually supports it, not to a paper that only shares broad vocabulary.

For each reference:

- verify existence and metadata using an authoritative record such as the publisher, DOI, arXiv, INSPIRE-HEP, Crossref, or an official repository;
- inspect the abstract or relevant passage;
- record a stable URL or identifier and the access date when the source is central;
- explain overlap and meaningful difference for the closest prior work when novelty is discussed;
- never treat a failed exact-phrase search as evidence of originality.

Pure maintenance, formatting, or infrastructure changes may omit literature, but the PR must state why external research does not apply. This exception prevents decorative citations while keeping research claims auditable.

## Evidence Boundary

Keep these statuses separate:

- **Fact:** directly supported by repository evidence or a cited source.
- **Inference:** a reasoned interpretation of those facts.
- **Hypothesis:** a proposal that still needs testing or literature comparison.
- **Open risk:** a known way the claim or implementation could fail.

Tests establish the behavior they cover. They do not, by themselves, establish scientific novelty, physical truth, or the generality of a theory.

## Review Checklist

- [ ] The story appears before technical details.
- [ ] The central insight is stated in plain language.
- [ ] Evidence is connected to the claims it supports.
- [ ] Literature references are verified and relevant when research claims are present.
- [ ] Limitations and next steps are explicit.
