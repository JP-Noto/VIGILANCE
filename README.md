# VIGILANCE

**For the human to concentrate where they have value.**

> Founding maxim: "The human concentrated where they have value, the system vigilant everywhere."

`Status: Public Draft · Corpus: 0.1.2 · Rank: test bench · License: CC BY-NC-SA 4.0`

> **Stage of this work: test bench** (gate 2 passed on 2026-09-06, signed decision; the hypothesis remains the form, and the drill remains to be run). One practitioner, one instrumented process, one measurement
> (a quote, control included, goes from 65-90 minutes to 25). Nothing replicated, nothing
> proven. "Proven" would require a series; no series exists yet. Negative results will be
> published like the others.

French documents are authoritative: [README.fr.md](README.fr.md) prevails in case of divergence.

## The observation

Two ways to control work, and both fail as volume grows. Exhaustive human review does not scale:
it manufactures the rubber stamp, the human who signs without seeing. Sampling scales: it lets
the needle through.

## The principle: control by exception

The system checks 100% of the flow against explicit rules; the human handles only what falls
outside, with the authority to decide. Three ingredients, all necessary:

1. **Explicit rules of "normal"**: written, versioned, contestable. Not a model's fuzzy
   judgment: controls you can read.
2. **Total verification by the system**: every line, every time. AI makes exhaustive vigilance
   affordable.
3. **The human on exceptions only**: and every judged exception enriches the rules.
   Organizational learning, not statistical.

Coverage is total and human attention is real: the combination that neither exhaustive review
nor sampling offers.

## Permanent surveillance? No: two regimes

The question comes early, and it is legitimate: if the system verifies everything, is this
permanent surveillance? No. Control has two regimes, each on its own object, and nothing
runs between the two.

**The flow, first**: everything the system produces or lets in, unit by unit. A supplier
quote arriving and checked line by line, a write into the price reference, an updated
record, a document leaving toward a third party: each unit of this flow is a « passage ».

- **At the passage**: at every unit produced. One hundred percent of the flow, at every
  passage (V2), on a single write path where deterministic guards decide within a latency
  budget (V6). Triggered by the act, never between two acts: as long as nothing is
  produced, nothing runs.
- **On the patrol** (la ronde): periodically, on the global state. The asynchronous review
  by agentic judgment observes what no passage can see: the link that rots, the file
  changed off the path, the global invariant that came undone.

A permanent control would add no guarantee: between two acts, nothing changes through the
path; what changes off the path is precisely an anomaly the patrol observes. It would add
cost and noise, which the economy of attention refuses. The limit is declared: between two
patrols, an off-path change stays invisible; that is why the single path is a rule (V6.1),
being off the path is an anomaly in itself.
## What the corpus measures

- **The exception rate.** Too high: rules too strict, or a sick process. Zero: rules too loose,
  or a decorative human.
- **The human correction rate on exceptions**: does the human decide, or stamp?
- **Rule enrichment over time**: yesterday's exceptions become tomorrow's controls.

## What would invalidate the concept

On a real instrumented process: if control by exception lets through more consequential
anomalies than the exhaustive human review it replaces, at equal or greater human time, the
concept falls. The criterion is published before the measurement series, and it will not move
to please them.

**What the corpus does not promise.** VIGILANCE economizes attention against ordinary
drift: the error, the omission, the slide. It is not a security device. Security assumes an
active adversary, one who reads the rules in order to defeat them; this corpus promises
nothing against that adversary, and the fields that deal with it are named in the
[WHITEPAPER](WHITEPAPER.md) (related work) and in [LINEAGE](LINEAGE.md). And a second
boundary: **vigilance applies to what is produced and how — never to
people**. Quality control of deliverables is not surveillance of those who make them: that
use belongs to another regime, and this corpus does not equip it. The corpus’s health
measures read rules and processes, never people
([Health measures](fiches/MESURES-DE-SANTE.md)).

## Where it comes from

Born on real ground on 2026-08-06: a second pair of human eyes replaced by five mechanical
controls on supplier quotes. First run on a real document the next day: nine exceptions surfaced,
two
of them invisible at price level (which would have delivered product A instead of product B),
and an unwritten trade rule brought to light. First measurement on 2026-09-04: one quote,
control included, from 65-90 minutes to 25. The dated detail lives in [LINEAGE](LINEAGE.md).

## The family

This corpus is the fifth of a family, and each layer has its role:

| Layer | Governs |
|---|---|
| A host AI OS (third-party) | the system: laws, files, loops, boundaries |
| [LIVING REFERENCE](https://github.com/JP-Noto/LIVING-REFERENCE) | the status of knowledge: what is validated, what is canon |
| [WORKING REFERENCE](https://github.com/JP-Noto/WORKING-REFERENCE) | how the reference serves the work: what reaches the call, served and sealed |
| [MYSTANCE](https://github.com/JP-Noto/MYSTANCE) | the human's place: the tuned relationship, skill growth, sovereignty |
| [SOUNDNESS](https://github.com/JP-Noto/SOUNDNESS) | the birth of document-extracted knowledge: the record grounded in its source piece |
| **VIGILANCE** | the economy of human attention: control by exception, the human on exceptions only |

VIGILANCE carries the link between the layers: it consumes its elders' references, it does not
redefine them. The doctrine is independent of any host OS and any model, present or future;
an independence by construction, the corpora being text; the operational proof is on the
bench. The family is
operated by the [ONDE AI R&D](https://github.com/JP-Noto/ONDE) laboratory.

## The documents

| Document | Role |
|---|---|
| [SPEC](SPEC.md) | normative: terms, five claims, rule families V1-V7, boundaries, falsification R1-R4; it prevails |
| [WHITEPAPER](WHITEPAPER.md) | the why of every ingredient, the founding case with its evidence ranks, related work |
| [LINEAGE](LINEAGE.md) | the debts declared before writing, and the dated internal genealogy |
| [fiches/](fiches/index.md) | nine practitioner sheets: the claim, the gesture, the example, what the sheet does not promise |
| [research/](research/DRILL-PROTOCOLE.md) | the drill: an adversarial bench protocol, pre-registered before any measurement |
| [profiles/](profiles/DEVIS.md) | one declared application profile per field (the quote-control profile, de-branded) |
| [README.fr.md](README.fr.md) | the authoritative French original |
| [CHANGELOG](CHANGELOG.md) · [CITATION.cff](CITATION.cff) · [LICENSE](LICENSE.md) · [CONTRIBUTING](CONTRIBUTING.md) | versions, citation, license, state of contributions |
