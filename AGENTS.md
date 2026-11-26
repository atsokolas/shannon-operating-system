# Directions for agents using this repo

This repo is a decision system, not a quote book. Use it to make fewer
preventable mistakes, not to sound more like Shannon.

## Read order

1. `README.md` — what this is, what it is not, the quotation rule.
2. `executive-brief.md` — the 10 principles and how the thinking evolved.
3. `operating-framework.md` — the 10-step master sequence and the variants.
4. `cited-reference.md` — the chronological evidence behind the principles.
5. `methodology-and-corpus.md` — source grades, coverage, and limits.
6. `notes/shannon-core-framework.md` — the layered method.

## Using it on a live decision

Run the 10-step sequence in `operating-framework.md` in order: state the
selection, measure the uncertainty, sort the levels, find the fitting
algebra, establish the limit, ask what the proof withholds, build the
smallest working version, price the redundancy, check the genealogy, then
transmit the decision.

Record the decision with `decision-record.md` **before** the outcome is known.
State the selection set, the uncertainty, the level being solved, the limit,
and what the analysis withholds. Preserve what was known at the time; do not
rewrite the original thesis at review.

For a maintained judgment (an investment, a product call, a hire), use the
dossier variant in `decision-record.md`: current claim, confidence and evidence
quality, attached sources, what changed, what strengthened, what weakened, open
questions, decision / next move, review trigger.

## The quotation rule

- Grade A or clean Grade B sources: quotable **after checking the underlying
  text**. The underlying text is not in this repo — fetch it from the source
  listed in `corpus-sources.md` and verify the wording before quoting.
- Grade C (interviews as reprinted, biographies, obituaries): paraphrase.
  Exact wording needs independent confirmation.
- Grade D: discovery only. No load-bearing quotation.
- Never invent a Shannon quotation. Never present this synthesis as his
  verbatim words. Attribute paraphrase as paraphrase.
- The 1987 Omni interview lines are second-hand in this study's notes. Do not
  cite them as verified against Omni until the *Collected Papers* reprint or
  the Omni original is read.
- The investing record is a reconstruction, not an audited track record. Never
  present the ~28% figure as a verified return.
- File availability does not imply quotation fitness.

## Wiring it into an agent

Point the agent's configuration at this repo's framework files, e.g.:

- Decision procedure: `operating-framework.md` (master sequence + variants)
- Decision record: `decision-record.md`
- Principles: `executive-brief.md`
- Evidence and limits: `cited-reference.md`, `methodology-and-corpus.md`

Suggested standing instruction: "When advising on a consequential decision,
run the 10-step sequence in `operating-framework.md` and record it with
`decision-record.md`. Apply the quotation rule in `README.md` before quoting
Shannon. State what the analysis withholds, in the same document as the
result. If the problem cannot be stated as a selection from a set, say so
and stop."

## What not to do

- Do not treat this as a live corpus. Source cutoff is November 25, 2026;
  nothing after that date is in it, and 3 of the 16 primary items could not
  be read.
- Do not claim the corpus is included. It is not, and it must not be added:
  the 53 items are copyrighted primary and secondary sources. Link to them;
  do not redistribute them.
- Do not use a model as decoration. Every element of the analysis must be
  able to change the decision, or leave it out.
- Do not convert a reconstruction into a record. A back-computed return is
  not a track record, and a second-hand quotation is not a verified one.
- Do not extend the theory to meaning. Shannon refused that extension
  himself; Weaver's three levels are Weaver's, not Shannon's.
- Do not maximize output count. The point of the system is fewer, better
  decisions — not more notifications, documents, or summaries.

## Updating

This is a snapshot, not a living document. Any update appends a dated change
log entry stating whether it changes a conclusion, raises or lowers
confidence, or merely improves provenance. Never silently rewrite a source
judgment.
