# Lighthouse Weight Tiers — Draft Specification

Held to Janus-Facing Architecture. A tier is a **structural fact about corroboration**, never a verdict about truth. Tiers are counted in **independent-hub units**: the hub, not the account, is the unit of count, with independence read structurally and common-control hubs excluded. Tier definitions are **policy, not mechanism** — they live as diffable policy data and commit to the witnessed record with plain-language changelog entries, so "what tier rules were in force when this rendered?" always has a witnessed answer. Every rendering that shows a tier carries a receipt: which replications, which hubs, which concordance distribution, which tier-policy version. Knowledge claims and their replications are **typed relations**, distinct from trade and adjudication signals; no reader may blur them.

---

## T0 — Anchored

A knowledge claim exists in the witnessed record as a bound triple — **fact claim, procedure, result** — committed by a claimant in good standing, at a hub, under the record layer's ordinary discipline: append-only, independently witnessed, monotonic. The anchor commits **structural facts and references only**: content hashes of the three artifacts, a claim type, a procedure-version identifier, a timestamp, a pseudonymous claimant reference, a hub reference. The artifacts themselves — the written procedure, the data — enter the AGPL contribution commons, content-addressed and served by hubs; the ledger holds hashes.

- Anchoring is gated by the covenant: standing decides **whether** an account may anchor, never how much or how visibly.
- Existence is the floor, never evidence. A reader may infer that this claim, with this procedure, existed at this time from an account then in good standing. A reader may NOT infer review, plausibility, or truth.
- Every anchor is answerable. Anyone may anchor a challenge referencing it; the claimant's silence accrues dwell — a readable fact, never an auto-adjudicated one.
- An artifact that becomes unretrievable does not erase the anchor; the claim renders as artifact-dark, another readable fact.
- A claimant's later covenant breach **annotates their anchors, never erases them**. A fabricator can have said something true; replications of their claims stand on their own record.

Gaming surface: mass minting. Defense: T0 sizes nothing, every anchor is answerable exposure under the covenant, and a hub may rate-limit anchoring as local, published policy.

## T1 — Cited

Other anchors reference the claim. Citations are **typed edges** — extends, uses-procedure, disputes, mentions — and the edge types are policy data. Citation renders the **discovery graph**: it is how claims are found, browsed, and contested across hubs.

- Citation counts MUST NOT enter weight, ranking-for-reward, or eligibility — **permanently**, not pending anything. Citations are and will remain nearly free to mint; a signal that costs nothing can weight nothing.
- A *disputes* edge is first-class and renders beside *extends*. The graph never nets.
- Discovery surfaces MUST render provenance — who cites, from which hub — so a citation ring is legible as a shape. The too-clean scan reads closed subgraphs as flag material; a flag is contestation input, never removal.

A reader may infer attention and connectivity. A reader may NOT infer corroboration. Citation finds claims; it never confirms them.

## T2 — Replicated in-hub

An account other than the claimant, registered at the **claimant's own hub**, ran a specific procedure version and anchored a **replication**: procedure-version reference, their own result hash, and their **concordance declaration** — consistent, inconsistent, or inconclusive — which is their own answerable claim, contestable like any anchor.

- All same-hub replications **collapse to one hub-unit** regardless of account count. The collapse is the Sybil defense: sock accounts buy nothing, and the metric holds without any controller-detection.
- The claimant's own accounts are excluded; where common control of accounts is structurally visible it is excluded too — but the collapse rule, not detection, carries the guarantee.
- T2 contributes structure and rendering, never eligibility. Its function is the on-ramp: it proves the procedure is **runnable by hands other than its author's**, and it surfaces procedural defects cheaply, before cross-hub effort is spent.

A reader may infer executability and local interest. A reader may NOT infer independent confirmation — a shared hub means shared equipment, shared social gravity, shared blind spots.

## T3 — Replicated cross-hub

Anchored replications exist from hubs **structurally independent** of the claimant's. The tier carries a count in hub-units — the number of distinct independent hubs with at least one anchored replication — held **per concordance category**: "consistent at four hubs, inconsistent at one" ships exactly so, permanently. This is the no-averaging rule applied to knowledge.

- Independence is read structurally at the hub level: pairwise-distinct control. Common operator, common controller, shared administrative parent — excluded. **A county library system's ten branches are one unit.**
- The witness relation is not a control relation. Hubs that countersign each other's checkpoints remain independent corroborators; otherwise federation partners could never corroborate each other, and small networks would strangle at birth.
- A hub is a countable unit only while its own record is honestly witnessed — two or more independent witnesses, none its own keys. A new hub's replications run under the **stand-in label** until its witnessing is real: staged recognition, exactly as at the governance layer.
- Real replication scatters. Too-perfect concordance across supposedly independent hubs is itself scan-flag material — the wash-trade signature translated to knowledge.
- An unanswered inconsistency accrues dwell on the original claim — readable, never an auto-downgrade.

Gaming surface: minted hubs, since AGPL means anyone may stand one up. Defense: unit status is earned structurally — witnessed record, control exclusion, stand-in until federated — so a fake hub costs what a real hub costs.

## T4 — Attested

A hub anchors, under its own institutional key, an **occurrence attestation**: this procedure version ran on these premises, on this date, in this session, by this account reference. **Occurrence, never truth** — the hub attests the event it directly hosted, not the finding. The replicator's result and concordance declaration remain their own separate, linked anchor.

- A false attestation is the hub's own covenant breach — adjudicable, read as structure, feeding the operator-conduct read that governs hub standing. The attestation has teeth because an institution's standing is behind it.
- Counted in hub-units like T3: many attested runs at one hub are one unit. Run count renders as detail and sizes nothing.
- **Attestation is a service, never a permission.** A hub may decline to host or attest any procedure — scheduling, supervision, and ordinary duty-of-care are hub-local, published policy — and a declined claim loses nothing elsewhere: it anchors at T0, travels the graph at T1, corroborates cross-hub at T3. The venue's ordinary care does safety work without any center becoming a truth or content authority.
- A hub MUST NOT attest runs by accounts under its own control — its operator, its staff acting as the hub. Employment is a control relation at this tier; a self-attested unit is the fox counting hens: it counts zero and carries the label.
- The tier's minting cost is **bodies and afternoons** — linear in hubs, no scale economies. That linearity, not any identity check, is the Sybil economics.

A reader may infer that independent institutions staked their standing on the event occurring. A reader may NOT infer the result is correct — only that faking it now costs real institutions real afternoons, multiplied.

---

## Disciplines that bind across tiers

- **Version binding.** A replication binds to the procedure version it ran. A refined procedure is a new anchor citing the old; weight accrues per version, with the chain visible. Otherwise weight gathers on v1 while v2 quietly ships beneath it.
- **Concordance is data; breach is conduct.** An inconsistent replication is a concordance fact, not an accusation, and it is never routed as a harm claim. Only conduct — fabrication, misrepresentation of what was run, a false attestation — enters the covenant's claim pipeline. **Disagreement is never breach.** Keeping the two channels separate is what keeps harm claims from becoming the weapon of scientific dispute.
- **Eligibility, never sizing.** Tier status gates whether a claim is eligible for the economy inflow; the threshold — T3-plus, or T4-only at the switch — is governed policy, not tier definition. Payout sizing belongs to the real exchange it funds, which carries the trade friction the tiers cannot.
- **No collapsed rendering.** No single score, no stars, no "verified" badge. A tier renders with its receipt: the replications, the hubs, the concordance distribution, the policy version in force.

## Requests to refuse or flag

- *"Show the claim's overall score."* → Rebuilds the average the covenant forbids. Ship the distribution.
- *"Boost ranking by citation count."* → T1 sizes nothing, permanently.
- *"Let the hub attest its own staff's runs."* → Self-attestation wearing an institutional key.
- *"Let hubs charge for faster or higher-tier placement."* → Reputation sold. Attestation scheduling is hub policy; tier standing is never purchasable.
- *"Auto-downgrade on an inconsistent replication."* → Concordance is data. Render it; never adjudicate it by clock or count.
- *"Mark the claim verified at T4."* → The truth authority in a nicer coat. Occurrence, never truth.
- *"Fold trade reputation into knowledge weight."* → Blurs typed relations. A good merchant is not thereby a good claimant.

## Named residue

Geographic exclusion: communities with no participating hub cannot reach T4, and reach T3 only through distant registration — a gap to design around (traveling attestation days, partner-hub arrangements), never to accept silently. Cold-start: thin hub counts early mean thin corroboration; stand-in labels carry the honesty until federation thickens. Real-human collusion rings spanning hubs remain possible at linear cost; they are fraud — covenant territory — and each adjudicated instance is a breach that never averages away.
