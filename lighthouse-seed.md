# The Lighthouse Network — Seed Document

**An application of Janus-Facing Architecture: a witnessed knowledge commons, carried by civic hubs.**

Network Theory Applied Research Institute

This document is held to Janus-Facing Architecture in full. It names roles and mechanisms, never the software that fills them; every invariant of the parent architecture binds here without restatement, and where this document and JFA disagree, either this document is fixed or JFA is amended in the open. Its normative companion is **lighthouse-weight-tiers.md**, the full tier specification; this document summarizes the tiers and does not duplicate them — a mirror is a second source of truth, born drifting.

**Vocabulary, mapped to JFA roles.** A **hub** is a civic institution — a library, a school, or any organization running the software — holding two JFA roles in one deployable package: the **orchestrator** (JFA's coordinator/operator role: the member-facing app, the hub's own append-only log, its adjudication duties) and the **witness** (countersigning *other* hubs' checkpoints). **LBTAS** is the covenant's assessment scale — harm-surfacing, Leveson-derived; its expansion is pending definition (open problem 2). An **anchor** is a commitment of structural facts and hashes to the witnessed record. An **attestation** is a hub's signed claim that a run physically occurred on its premises — occurrence, never truth. A **hub-unit** is the unit of corroboration count: the hub, never the account. A **stand-in label** marks any guarantee running below its structural floor.

---

## Part I — what Lighthouse is

Lighthouse is a knowledge commons in which empirical facts are captured **alongside the procedures that test them**, from claimants of academic and nonacademic background alike, anchored to a witnessed record through local hubs where the public can discuss, replicate, and contest in community. It instantiates JFA Part VI: a witnessed record can anchor any empirical or commercial claim; anchored, a claim becomes citable, and the covenant rates the claimant the same way it rates a trading partner. The same rails that make trade trustworthy make knowledge trustworthy.

The name is the discipline. A lighthouse does not certify a safe route; it makes the hazard visible and leaves navigation to the ship. Lighthouse illuminates claims — their procedures, their replications, their disputes, their claimants' standing — and never issues a verdict on truth. Flag, never finding; anchor, never certify.

What it must not become, inherited verbatim: a rating agency for truth, an ad market where visibility is bought, a credentialing monopoly. Discovery stays federated, cited, and contestable.

## Part II — the claim model

The atomic knowledge object is a bound triple: **fact claim, procedure, result**, anchored as a claim, never asserted as fact.

- The ledger commits structural facts and references only — content hashes of the three artifacts, claim type, procedure-version identifier, timestamp, pseudonymous claimant reference, hub reference. **No PII in the commons**, ever.
- The artifacts themselves — procedure text, data — enter the AGPL contribution commons, content-addressed, served by hubs. Provenance is inbound = outbound; a contribution cannot be reclaimed.
- Knowledge claims, replications, and their disputes are **typed relations**, distinct from trade and adjudication signals. No reader may collapse them.
- Replications bind to the **procedure version** they ran. A refinement is a new anchor citing the old; standing accrues per version with the chain visible.
- Every anchor is answerable; challenges are first-class edges; a claimant's silence accrues dwell — readable, never auto-adjudicated. An artifact gone unretrievable renders as artifact-dark; the anchor never erases.

## Part III — the covenant applied

LBTAS rates **claimants, never claims**. A claim accrues standing only through the corroboration structure of Part V; a person accrues standing only through conduct.

- The full distribution ships, never an average; the lowest rating is the breach itself. A fabrication never dissolves into a comfortable volume of good work.
- **Concordance is data; breach is conduct.** An inconsistent replication is a concordance fact — consistent, inconsistent, inconclusive — never an accusation, and it is never routed as a harm claim. Only conduct enters the covenant pipeline: fabrication, misrepresentation of what was run, a false attestation. **Disagreement is never breach.** This channel separation is what keeps harm claims from becoming the weapon of scientific dispute.
- The covenant is symmetric: every claim is answerable, dismissals annotate, and a later breach annotates a claimant's anchors without erasing them — a fabricator can have said something true, and replications of their claims stand on their own record.
- No truth authority anywhere: no "verified true" from any hub, any center, any scan, any model. A machine reading aid explains; it never certifies.

## Part IV — the hub architecture

One package, two roles, two keys, **always pointed outward**.

- Every hub runs the orchestrator and the witness, but **no institution witnesses its own log**. Library A's checkpoints are countersigned by School B and Library C; A returns the favor on theirs. Witness keys are pairwise-distinct and never the operator's own — a fused orchestrator-witness at one institution is the self-attesting operator the record layer exists to prevent.
- A harm claim against a hub **files at a neighboring hub's witness**, upstream, with the operator absent from its own claim's birth. Wherever two hubs federate, the filing-liveness gap closes.
- **Launch floor: two independent hubs.** A single-hub pilot is conformant only under the stand-in label; it cannot present itself as federation.
- **Venue, never gate.** The record and the market live in the protocol, below any hub's app. A member refused or mistreated at Library A walks into School B's app with standing and liquidity intact. That portability — not any hub's goodwill — is what makes hubs venues rather than gatekeepers.
- Hub independence is read structurally: pairwise-distinct control, with common operator, common controller, and shared administrative parent excluded. **A county library system's ten branches are one unit.** The witness relation is *not* a control relation — hubs that countersign each other's logs remain independent corroborators, or small federations would strangle at birth.
- Target market: libraries and schools, with members logging into their hub's mobile or web app. Under AGPL-3.0, any institution may enter the knowledge-commons orchestration market; copyleft plus the legibility ladder keeps that market contestable, not merely open.

## Part V — weight tiers, by reference

Normative text lives in the companion specification. The shape: **T0 Anchored** (existence is the floor, never evidence) → **T1 Cited** (renders the discovery graph; citation counts size nothing, permanently) → **T2 Replicated in-hub** (executability; all same-hub replications collapse to one hub-unit) → **T3 Replicated cross-hub** (corroboration counted in independent-hub units, held per concordance category — "consistent at four hubs, inconsistent at one" ships exactly so) → **T4 Attested** (a hub's institutional key stakes its standing on *occurrence, never truth*; minting cost is bodies and afternoons, linear).

Four disciplines bind across tiers: version binding; concordance-is-data-breach-is-conduct; **eligibility, never sizing** — tier status gates whether a claim may enter the economy inflow, and never sizes a payout; and no collapsed rendering — no score, no stars, no verified badge, every tier shipped with its receipt.

## Part VI — the Sybil posture

Managed until it does not pay, never solved: the two tools that could solve it — a global identity authority and a purchase wall — are the two things the architecture refuses. Four moves:

1. **Corroboration counts hubs, not accounts.** Same-controller exclusion at every tier; ten sock accounts at one library collapse into one hub's worth of structure.
2. **Physical presence is the per-unit cost.** Attestation makes the strongest tier cost bodies and afternoons, linearly, with no scale economies — dishonesty priced above its yield, not prevented.
3. **The too-clean scan.** Closed citation subgraphs, mutual-admiration rings, and suspiciously scatter-free concordance across "independent" hubs are flag material — a contestable flag, never a removal, because false positives land on small honest niche communities, and the natural contestation venue is the hub floor itself.
4. **Rewards sequenced behind the switch.** At launch, weight sizes nothing: no ranking, no inflow. The graph accumulates in the witnessed record — rings built early are wasted effort and permanently visible to retro-scanning. Weight then switches on as a governed, witnessed policy change, for cross-hub and attested tiers only. Sybil-before-citation-weight, satisfied by ordering rather than perfection.

Named residue: one human genuinely attending N hubs (linear cost is the defense); real-human collusion rings spanning hubs (fraud — covenant territory, each adjudicated instance a breach that never averages away); remote members' tier reach (open problem 3); cold-start corroboration thinness (stand-in labels carry the honesty).

## Part VII — the economy inflow

Anchored, corroborated knowledge becomes R&D input for products and services in JFA economies — a cultivar's yield, a tool's failure mode, a method's cost curve, flowing from the commons into real exchange.

- Tier status gates **eligibility** for the inflow; the threshold — T3-plus, or T4-only at the switch — is governed, witnessed policy, not tier definition. Payout sizing belongs to the real exchange it funds, which carries the trade friction the tiers cannot.
- **No paid placement, ever.** A vendor's claims about its own products anchor, replicate, and get disputed like anyone else's; the covenant and the scan police them, never a listing fee.
- The JFA economy invariants bind wholesale: the unit earned, never bought; non-redeemable; denomination is not redemption; and a completed regulatory read before any credit phase.

## Part VIII — development order

Build bottom-up; the order is the argument. Each stage ships with its stand-in labels honest.

1. **Stage 0 — the federated record.** Two-hub pilot: per-hub append-only logs, cross-witnessed monotonic checkpoints, consistency proofs, filing-at-the-neighbor. This is JFA's own highest-leverage build (open problem 2) wearing Lighthouse's clothes; nothing above it reads honestly until it is real.
2. **Stage 1 — anchoring and discovery.** T0 and T1: the claim triple, the typed citation graph, artifact serving from the AGPL commons. Sizing nothing.
3. **Stage 2 — replication and concordance.** T2 and T3: hub-unit counting, concordance distributions, dwell rendering. Receipts and rules-as-diffable-policy-data ship *here*, as launch features — legibility is a build deliverable, not polish.
4. **Stage 3 — attestation.** T4: hub institutional keys, occurrence discipline, the staff-exclusion rule, false-attestation feeding the operator-conduct read.
5. **Stage 4 — the inflow switch.** Only after the regulatory read and only for cross-hub and attested tiers, as a governed, witnessed policy change.

## Part IX — open problems

1. **The record-examination interface is undesigned.** Members examining the record through their hub's app inherits the legibility ladder whole — decisions explaining themselves at point of use, rules living as diffable data, policy versions witnessed, machine reading aids that never become oracles. This is the next design conversation, and it is named here rather than routed around.
2. **LBTAS awaits its definition.** This document treats it as the covenant's harm-surfacing, Leveson-derived assessment scale; the expansion and any Lighthouse-specific adaptation of the scale's levels are unwritten.
3. **Geographic exclusion.** A community with no participating hub cannot reach T4 and reaches T3 only through distant registration. Traveling attestation days and partner-hub arrangements are candidate design-arounds; silent acceptance is not.
4. **Hub capture beyond the scan.** Real institutions can collude; the answer is adjudication plus the operator-conduct read, both of which depend on federation being real — this problem rests on Stage 0 exactly as JFA's problem 4 rests on its problem 2.
5. **Everything in JFA Part VII binds here.** Problems 2, 4, 7, and 8 especially. Lighthouse's hub-as-witness design is a proposed lever on problem 8 — civic institutions as long-lived, publicly accountable, mutually independent witnesses — to be proven in deployment, not assumed.

## The standard

A system is Lighthouse only if all seven hold; failing one, it is different software wearing the vocabulary.

1. Claims are anchored as claims; no center, scan, hub, or model holds a verdict on truth.
2. Hubs are venues, never gates: the record and the market live below any hub's app, and a member leaves one hub for another with standing and liquidity intact.
3. No institution witnesses its own log; two independent hubs is the federation floor, and anything less carries the stand-in label.
4. Corroboration is counted in independent-hub units, never accounts; citation counts size nothing, permanently.
5. Distributions ship whole — concordance beside volume, harm beside praise — never a collapsed score or a verified badge, and every rendering carries its receipt.
6. Concordance is data and breach is conduct; disagreement is never breach.
7. Weight gates eligibility and never sizes payout; every reward sits behind a governed, witnessed switch, sequenced Sybil-first.

---

While implementing, the tension protocol is in force: on noticing a constraint being reframed for convenience, a stand-in shipping unlabeled, or an open problem being routed around — stop, name the tension, attach it to the invariant or problem, and propose the minimal conformant move. Surface it; do not absorb it.

*This document is free documentation under the project's AGPL-3.0 commons; it is meant to be read, reimplemented, and contested.*
