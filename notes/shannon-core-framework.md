# Claude Shannon — Core Framework (Working Notes)

These are source notes, not the final synthesis. Claims are provisional until
checked across the full chronological corpus. Every quotation below was read
in the source named; grades follow the hierarchy in
`methodology-and-corpus.md`.

## The method: find the algebra, then let it work

- Shannon's signature move, visible first in the 1937 master's thesis, is to
  take a domain run by craft and intuition and find the algebra that fits it.
  Relay design becomes Boolean algebra: a circuit is a set of equations, and
  synthesis is manipulation of those equations until the fewest letters
  remain. "This calculus is shown to be exactly analogous to the Calculus of
  Propositions used in the symbolic study of logic." [Source: Shannon, "A
  Symbolic Analysis of Relay and Switching Circuits," MIT master's thesis,
  1937; published *Trans. AIEE*, 1938]
- The same move, applied to a second field, produced the 1940 genetics
  thesis: a non-associative, commutative algebra in which a population
  distribution over linked loci is a symbol, random mating is
  multiplication, and recombination enters through the multiplication table.
  It was original, correct, and ignored — including by Shannon himself, who
  never published it and wrote nothing further on genetics. [Source: Shannon,
  "An Algebra for Theoretical Genetics," MIT PhD thesis, 1940; DSpace record
  http://hdl.handle.net/1721.1/11174 — metadata read, PDF unreadable in this
  pass; secondary corroboration in Soni & Goodman, *A Mind at Play*]
- The pattern is: identify the atomic choices, measure them, prove what is
  possible in the limit, and admit what the proof does not give. The 1948
  paper does this for communication; the 1949 paper does it for secrecy; the
  1950 paper does it for chess. Each paper contains a passage saying what it
  does not solve.

## Selection from a set as the primitive

- In every domain Shannon treats, the primitive is a choice from a set of
  possibilities: a message selected from a set, a key selected from a set, a
  move selected from the legal set, a switch open or closed. Information is
  the measure of that selection, logarithmic after Hartley. "The fundamental
  problem of communication is that of reproducing at one point either exactly
  or approximately a message selected at another point." [Source: Shannon,
  "A Mathematical Theory of Communication," *Bell System Technical Journal*,
  1948]
- Entropy H = −Σ p log p is derived axiomatically (Theorem 2), not asserted.
  The bit is Tukey's word, adopted by Shannon: "If the base 2 is used the
  resulting units may be called binary digits, or more briefly bits, a word
  suggested by J. W. Tukey." [Source: Shannon, 1948]
- The counting device recurs across domains: the ~2^{HN} typical sequences
  (1948); the residue classes of messages under a pure cipher (1949); the
  ~10^120 variations of a chess game (1950). Counting the set is the analysis.

## Meaning separated from mechanism

- The 1948 paper delimits itself in the first pages: "These semantic aspects
  of communication are irrelevant to the engineering problem." The theory is
  about selection among possibilities, not about what the message means.
  [Source: Shannon, 1948]
- Weaver's 1949 essay does the opposite: it defines communication in the
  widest sense — "all of the procedures by which one mind may affect
  another" — sorts the problems into three levels (A technical, B semantic,
  C effectiveness), and argues the Level A theory overlaps the higher levels
  more than one would naively suspect. Weaver's framing is how most
  non-engineers first met the theory. [Source: Weaver, "Recent Contributions
  to the Mathematical Theory of Communication," in Shannon & Weaver, *The
  Mathematical Theory of Communication*, 1949]
- Shannon spent the rest of his life refusing Weaver's extension. In 1989:
  "Meaning is a pretty hard thing to get a grip on… I don't think it is all
  that easy to encompass that in a mathematical form." [Source: Shannon,
  interview with John Horgan, *Scientific American*, Jan 1990, as reprinted
  by the author] The theory's popular career and its author's own account of
  it diverge from 1949 onward. Know which level you are solving — and whose
  extension you are using.

## Existence without construction

- The channel coding theorem (Theorem 11, 1948) is proved by averaging over
  random codes: information can be sent at any rate up to capacity C with
  arbitrarily small error. Shannon stresses what the proof does not give:
  "The demonstration of Theorem 11, while not a pure existence proof, has
  some of the deficiencies of such proofs. An attempt to obtain a good
  approximation to ideal coding by following the method of the proof is
  generally impractical. In fact, apart from some rather trivial cases and
  certain limiting situations, no explicit description of a series of
  approximation to the ideal has been found." And: "Probably this is no
  accident but is related to the difficulty of giving an explicit construction
  for a good approximation to a random sequence." The only explicit
  near-ideal code in the paper is Hamming's, credited to Hamming. [Source:
  Shannon, 1948]
- The same honesty appears in 1959: eleven years later, the error-exponent
  paper grinds out bounds rather than constructions, leaves the reliability
  function exact only above a critical rate, and calls its own algebra
  "unusually tedious." [Source: Shannon, "Probability of Error for Optimal
  Codes in a Gaussian Channel," *BSTJ*, 1959]
- The rule: a limit theorem tells you what is possible; it does not hand you
  the machine. Ideal coding also needs long delay: "In general, ideal or
  nearly ideal encoding requires a long delay in the transmitter and
  receiver." [Source: Shannon, 1948]

## Perfect secrecy and its price

- Secrecy is communication theory with an adversary. A secrecy system is a
  family of reversible transformations, one per key, and the enemy is assumed
  to know the system — "pessimistic and hence safe… one must expect his
  system to be found out eventually." [Source: Shannon, "Communication
  Theory of Secrecy Systems," *BSTJ*, 1949]
- Perfect secrecy (Theorem 6) requires at least as many keys as messages:
  "The amount of uncertainty we can introduce into the solution cannot be
  greater than the key uncertainty." With known source statistics, compress
  first, then Vernam: "a bit of key completely conceals a bit of message
  information." [Source: Shannon, 1949]
- With a finite key, the unicity distance ≈ H(K)/D — about 30 letters for
  simple substitution on English. Redundancy is what makes a solution
  possible at all. [Source: Shannon, 1949]
- Practical design is confusion and diffusion: simple ciphers separated by a
  mixing transformation, so "the redundancy has been both diffused and
  confused by the mixing transformation F." The five criteria for a good
  system are mutually incompatible — by Shannon's own admission argued
  vaguely: "This reasoning is too vague to be conclusive, but the general
  idea seems quite reasonable." [Source: Shannon, 1949]

## Minimalism: the smallest thing that still does the job

- The 1937 thesis asks for the fewest relay contacts; the hardest
  series-parallel functions (XOR and its negation) need 3·2^(n−1) − 2
  elements, but only 4(n−1) with general circuits. Minimality is proved for
  series-parallel circuits only; for general circuits "the function
  requiring the most elements using any type of circuit has not as yet been
  determined." [Source: Shannon, 1937]
- The 1956 paper asks the same question of Turing machines: a universal
  machine can be built with one tape and only two internal states, and one
  state is impossible. "Our main result is to show that a universal Turing
  machine can be constructed using one tape and having only two internal
  states." The state–symbol product becomes the measure of size, and Shannon
  ends on an open problem: "An interesting unsolved problem is to find the
  minimum possible state-symbol product for a universal Turing machine."
  [Source: Shannon, "A Universal Turing Machine with Two Internal States,"
  *Automata Studies*, 1956]
- Minimalism is a research style, not a slogan: find the boundary, prove it
  sharp, and leave the open problem stated.

## Build it to know it

- Theseus (1950) is Shannon's first built learning machine: a 5×5 maze, a
  magnetised wooden mouse, ~75–110 relays under the floor remembering the
  direction the mouse last left each square. First run by trial and error;
  second run direct to the goal; on a changed maze it revises its memory.
  Shannon's own summary of its abilities: "(1) solve problems by trial and
  error, (2) repeat the solutions without the errors, (3) add and correlate
  new information to a partial solution, (4) forget a solution when it is no
  longer applicable." [Source: Shannon, "Computers and Automata," *Proc.
  IRE*, 1953; Kyoto Prize lecture, 1985]
- The 1953 paper also prints his own defeat: his penny-matching machine lost
  55–45 to Hagelbarger's. The machine is aimed "more nearly at Poe's method
  of play than von Neumann's" — it wins because humans cannot be random.
  [Source: Shannon, "A Mind-Reading (?) Machine," Bell Labs memo, 1953;
  Shannon, 1953]
- The chess paper (1950) is a design study, not a program: Type A search is
  "both slow and a weak player" (over 16 minutes per move at three-ply);
  Type B is a sketch; no program was ever built by Shannon. "The chief
  weakness is that the machine will not learn by mistakes." [Source: Shannon,
  "Programming a Computer for Playing Chess," *Philosophical Magazine*, 1950]
- The workshop habit continues for decades: juggling machines, the
  Ultimate Machine (Minsky's idea; Shannon built versions), THROBAC, the
  wearable roulette computer with Thorp (1960–61). The machines are the
  experiments; the papers are the reports.

## Play as method

- "I've always pursued my interests without much regard for financial value
  or value to the world. I've spent lots of time on totally useless things."
  [Source: Shannon, interview with John Horgan, *Scientific American*, Jan
  1990, as reprinted by the author]
- Kyoto, 1985: "Building devices like chess-playing machines and juggling
  machines, even as a 'shumi,' might seem a ridiculous waste of time and
  money, but I think the history of science has shown that valuable
  consequences often proliferate from simple curiosity." [Source: Shannon,
  Kyoto Prize lecture, 1985]
- The juggling theorem, (F+D)·H = (V+D)·N, developed in the 1970s, written
  c. 1980, published 1993: a bookkeeping identity turned into a machine.
  Shannon could himself juggle no more than four balls. [Source: Shannon,
  "Scientific Aspects of Juggling," 1993; *Scientific American*, "The
  Mathematics of Juggling"]
- Play is not the opposite of the theory. Theseus, the penny-matching
  machine, the chess paper, and the juggling theorem are the same habit:
  build a small working system, watch it, and let the observation discipline
  the theory.

## Credit generously; print your defeats

- The papers are generous with attribution: Boole and Huntington (1937);
  Nyquist, Hartley, Wiener, Fano, Hamming (1948); Gaines, Givierge, von
  Neumann and Morgenstern, Hopf (1949); von Neumann–Morgenstern, de Groot,
  Fine (1950). The mind-reading memo credits Hagelbarger in its first
  sentence.
- The 1982 oral history is the counterweight: Shannon denies, repeatedly and
  flatly, that Wiener modelled information as a random process ("He was far
  more a stepping stone for me than was Norbert Wiener" — of Hartley), denies
  the von Neumann entropy anecdote ("I'm quite sure that it didn't happen
  between von Neumann and me"), and dates the stochastic-source idea to 1941.
  The interview is evidence about how Shannon wanted his work understood,
  not a neutral chronology: his memory demonstrably fails on checkable points
  in the same interview. [Source: Shannon, oral history, Robert Price, IEEE
  History Center Interview #423, 28 July 1982]
- The Kelly authorship question is genuinely unresolved: Kelly published the
  1956 paper alone; Shannon was colleague, sounding board, and in-house
  referee; Poundstone leans toward co-discovery, James Case's review leans
  toward Kelly-alone authorship with Shannon's help. Do not write "Shannon
  co-discovered the Kelly criterion" as settled fact. [Source: Kelly, "A New
  Interpretation of Information Rate," *BSTJ*, 1956; Poundstone, *Fortune's
  Formula*, 2005; Case, *SIAM News*, 2006]

## Investing: temperament, concentration, and a reconstruction

- Poundstone reconstructs Shannon's personal stock portfolio as returning
  about 28% a year from the late 1950s through 1986 — a retrospective
  estimate from surviving records, not an audited track record. No audited
  statements, no fund record, and no continuous return series exist in any
  source consulted. Period endpoints vary between retellings. The comparison
  with Buffett's ~27% (1965–1995) is Poundstone's construction, not a
  like-for-like horse race. [Source: Poundstone, *Fortune's Formula*, 2005,
  via secondary quotation]
- The mechanism was not Kelly and not the Demon: plain concentrated
  buy-and-hold. Three stocks — Teledyne, Motorola, Hewlett-Packard — made up
  98% of the portfolio (1981 snapshot); Teledyne alone was nearly 80%, cost
  basis 88 cents split-adjusted, ~$300 by 1986. Poundstone himself says the
  record had "little to do with Kelly's formula." Shannon admired Teledyne's
  Henry Singleton as a capital allocator — the man, not a formula. [Source:
  Poundstone, 2005, via secondaries]
- Shannon's Demon is an unpublished MIT talk (c. 1967 is an inference from
  Shannon's 1987 remark, not a dated record), never published, name coined
  later by an unknown hand. The mathematics is settled — a double-then-halve
  round trip multiplies a 50–50 rebalanced portfolio by 1.125 — but Shannon
  reportedly said he did not use it himself: "the commissions would kill
  you" (anecdotal, Grade D). [Source: Poundstone, 2005, via secondaries]
- No evidence was found that Shannon served on MIT's endowment or investment
  committee. Do not claim an endowment role.

## The turn away, and the prediction record

- After 1959 Shannon published little on information theory. In 1989 he
  denied having tired of it: "It's not that I was tired of it. It's that I
  was working on a different thing… I was playing around with machines to do
  computations. That's been more of my interest than information theory
  itself. The intelligent-machine idea." He added that he continued working
  on information theory but "considered most of his results unworthy of
  publication." [Source: Shannon, Horgan interview, 1989–1990]
- Kyoto, 1985: "by 2001 AD we will have machines which can walk as well, see
  as well, and think as well as we do." Wrong on the date by decades, right
  on the direction. [Source: Shannon, Kyoto Prize lecture, 1985]
- The 1953 "generalized" learning program — teach a machine "in much the
  same way as a child is taught" — "would need to be based on some entirely
  new ideas" and "progress appears to be held up." A correct diagnosis of the
  gap, still open in 1953 terms. [Source: Shannon, 1953]
- Stage fright kept him out of his own field's meetings for decades; he
  nearly backed out of the 1973 Shannon Lecture. He retired as Donner
  Professor in 1978, and died February 24, 2001, after a long illness with
  Alzheimer's disease. [Sources: MIT News obituary, 2001; *New York Times*
  obituary, Feb 27, 2001]

## Provisional synthesis

Shannon's system is best understood as a layered method, not a set of
slogans:

1. Find the algebra that fits the domain.
2. Reduce the problem to selection from a set; measure the selection.
3. Separate meaning from mechanism; solve the level you are on.
4. Prove what is possible in the limit; state what the proof withholds.
5. Seek the smallest thing that still does the job.
6. Build the machine; let the build test the theory.
7. Let curiosity choose the problem; keep score honestly.
8. Credit others generously; print your defeats.
9. Distrust neat genealogies; check priority against the record.
10. Concentrate on what you understand; never mistake a reconstruction for
    a record.

This ordering is provisional and will be tested against the full
chronological corpus.
