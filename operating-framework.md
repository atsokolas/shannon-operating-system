# The Shannon Operating Framework

This is a practical decision system derived from the study. It is not a
substitute for domain expertise. It is a way to apply expertise more
reliably — by turning a hard problem into a measurable one, stating the
limit, and building the smallest thing that tests the theory.

## The master sequence

### 1. State the selection

- What is being chosen, from what set, by whom?
- What are the possible messages, moves, keys, or designs — and which ones
  are actually available?
- Who is the sender, who is the receiver, and what is the channel between
  them?

Write the decision as a selection from a set. If the set cannot be stated,
analysis has begun too early.

### 2. Measure the uncertainty

- How much is unknown, and in what form? What is the entropy of the
  situation — how many possibilities remain live?
- What single observation would reduce the uncertainty most?
- What is already known, and what is merely assumed to be known?

Do not confuse the volume of information with its content. A long message
can carry little information, and a short one can carry much.

### 3. Sort the levels

Weaver's three levels, used with Shannon's caution:

- **A — technical.** Can the symbols be transmitted accurately? Can the
  thing be built, computed, or executed at all?
- **B — semantic.** Do the symbols convey the intended meaning? Does the
  receiver understand what the sender meant?
- **C — effectiveness.** Does the received meaning affect conduct as desired?
  Does the decision change what actually happens?

Name the level you are solving. A Level A solution does not settle a Level B
problem, and a Level C failure is not evidence that the Level A engineering
was wrong.

### 4. Find the fitting algebra

- What formal structure does this domain obey? What are its atoms, its
  operations, its invariants?
- Can the problem be rewritten as equations, and the equations manipulated
  until the fewest terms remain?
- Which existing theory fits — and where does the fit break?

If no algebra fits, say so. Forcing a domain into the wrong formalism is
worse than working without one.

### 5. Establish the limit

- What is possible in principle, and what is impossible? What is the
  capacity of this channel — the fastest rate, the best achievable error, the
  smallest machine that still does the job?
- What would a perfect solution require, and what does it cost?
- Where is the boundary sharp, and where is it only bounded?

A limit theorem is a boundary, not a machine. Record the boundary before
discussing implementation.

### 6. Ask what the proof withholds

- Does the argument prove existence, or give a construction? If existence
  only, what is the construction problem, and who has solved it?
- What delay, cost, or complexity does the ideal solution require?
- Which of the desiderata are mutually incompatible, and which one are you
  sacrificing?
- What did the analysis assume that the real situation violates?

State the withholding in the same document as the result. A proof that hides
its own limits is a sales pitch.

### 7. Build the smallest working version

- What is the Theseus for this problem — the smallest mechanism whose
  behavior tests the theory?
- What would you observe if the theory is right, and what if it is wrong?
- Can the build be small enough to finish, and honest enough to fail?

Understanding that stays in the head is untested. If the machine loses the
tournament you staged, print the score.

### 8. Price the redundancy

- What margin, error-correction, or reserve does this decision need, and
  what does it cost?
- How much intercepted evidence would it take for an adversary — or reality
  — to uniquely determine the outcome? What is the unicity distance of your
  position?
- Where is redundancy wasteful, and where is it the only thing standing
  between you and ruin?

Redundancy is not inefficiency. It is the price of surviving noise.

### 9. Check the genealogy

- Whose work are you standing on? Name the debts in the first pages, not
  the footnotes.
- Which priority claims are you relying on, and what does the record actually
  show?
- What would change your mind — what fact, if true, falsifies the preferred
  view?
- What is the strongest opposing case, stated as its best advocate would?

Distrust neat genealogies. A story about who begat what is not evidence.

### 10. Transmit the decision

Before the outcome is known, record the decision in a form the future can
decode without equivocation:

- the selection set, the uncertainty, and the level being solved;
- the limit, and what the analysis withholds;
- the smallest version built, and what it did;
- the conditions that would change the decision, and the review date.

At review, separate decision quality from outcome quality. A good decision
can have a bad outcome — noise is real — and a bad decision can have a good
outcome. Preserve what was known at the time; do not rewrite the original
thesis.

## One-page decision record

```text
Decision:
Deadline / owner:
Reversibility:

Selection set (what is being chosen, from what):
Uncertainty (what is unknown; what would reduce it most):
Level: technical / semantic / effectiveness

Fitting algebra / model:
Limit (what is possible in principle; what is impossible):
What the analysis withholds (existence vs. construction; delay; cost):
Smallest version built (or: why none):
Redundancy priced (margin; unicity distance):

Genealogy (debts; priority claims checked):
Strongest opposing case:
What would change my mind:

Decision and size:
Conditions / tripwires:
Review date:
Confidence range:
```

## Communication and information variant

For any message, system, or interface:

- Define the source, transmitter, channel, receiver, and destination. Name
  the noise.
- Measure before compressing: what is the entropy of what must actually be
  conveyed, and what is redundancy that can be removed — or redundancy that
  must be kept as error-correction?
- State the capacity: what rate can this channel actually carry, and what
  happens above it?
- Separate the levels: a Level A success (accurate transmission) is not a
  Level B success (understood meaning) or a Level C success (changed
  conduct).
- Price the delay: ideal performance that requires unbounded delay is not
  ideal performance.

## Investment variant

### Selection and uncertainty

- What is the selection set — the actual alternatives, not the ones in the
  headlines?
- What is unknown, and what single fact would reduce the uncertainty most?
- Which level are you solving: the technical (can this business do what it
  claims?), the semantic (do you understand what it actually does?), or the
  effectiveness (will owning it change your outcome as desired)?

### Limit and withholding

- What is the best achievable outcome in principle, and what does the
  analysis withhold? A back-computed return is not a track record.
- Distinguish a system from a temperament: concentration in a business you
  understand is a decision; a reconstructed 28% is not evidence for a
  method.
- State the concentration explicitly: how much of the portfolio is one bet,
  and what happens if that bet is wrong?

### Rebalancing

- Rebalancing harvests volatility only if the round trip survives costs.
  Price the commissions, taxes, and attention before assuming the premium.
- Shannon's Demon is mathematics, not a system he used. Do not present it as
  one.

### Decision discipline

- State why the market may be wrong.
- State why you may be wrong.
- Size for knowledge and downside, not excitement.
- Establish thesis-breakers; do not convert every disappointment into "long
  term."
- Record the decision before the outcome, with the conditions that would
  change it.

## Building and product variant

- Define the consequential user decision or job; do not begin with features.
- Identify the selection the user actually faces, and measure the uncertainty
  before adding information.
- Build the smallest working version and watch it behave. A prototype that
  cannot fail cannot teach.
- State what the design does not do, in the same document as what it does.
- Incentivize maintained truth: sources, changed evidence, uncertainty, and
  correction.
- Run a pre-mortem for hallucination, stale context, privacy, permissioning,
  automation error, and false confidence.
- Prefer a narrow, high-value workflow with accumulated proprietary context
  over generic AI surface area.
- Preserve a "too hard / insufficient evidence" state. A system forced to
  answer every query will manufacture certainty.

For each dossier, keep:

```text
Current claim
Confidence and evidence quality
Attached sources
What changed
What strengthened
What weakened
Open questions
Decision / next move
Review trigger
```

## AI assistants and automation variant

Before automating:

- What selection is being made, and what is the uncertainty?
- What happens when the automation is wrong — and how quickly is the error
  detected?
- Can it make an external commitment, spend money, publish, delete, or
  expose private information?
- Are sources and transformations auditable?
- Is stale context visibly dated?
- Does the output contain fact, inference, and recommendation as separate
  layers?
- When a claim rests on a reconstruction, does the output say so? When a
  quotation is second-hand, does it say so? When a source could not be read,
  does it say so?
- Which action requires human approval?

Automate reversible collection and maintenance aggressively. Gate
consequential external actions. Optimize for fewer high-quality decisions, not
more notifications.

## Weekly practice

Once a week:

1. Review one consequential decision before knowing its result.
2. State one problem as a selection from a set, and measure the uncertainty.
3. Find one belief you have not seriously tried to disprove.
4. Identify one place where meaning and mechanism are being confused.
5. Name one limit your current plan assumes away — and price it.
6. Build one small thing that tests a belief, or admit you have not.
7. Remove one commitment that increases noise or distraction risk.

The purpose is not to sound more like Shannon. It is to make fewer
preventable mistakes, and to know, when a problem is solved, exactly what was
solved and what was not.
