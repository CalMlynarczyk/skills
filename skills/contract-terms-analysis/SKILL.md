---
name: contract-terms-analysis
description: >
  Analyze a contract, terms of service, lease, warranty, subscription, or offer
  letter and open with a verdict: standard for its category, genuinely
  aggressive, or dependent on the reader's leverage or jurisdiction. Identifies
  ordinary boilerplate vs. clauses worth pushing back on, grades enforceability
  and how unusual each flag is, and explains what the routine legal language is
  doing. Use whenever someone pastes contract or terms text, uploads a photo of
  a lease or agreement, or names a contract, ToS, EULA, warranty, subscription,
  or offer letter and asks if it's normal, safe to sign, or what a clause
  means. Trigger even without the word "contract" — "can they actually do
  this", "is this normal for a lease", "am I signing away something here",
  "should I worry about this arbitration clause", "does this auto-renew on
  me", "read the fine print for me", "what happens if I cancel early", "is
  this a bad warranty", and "is it safe to click agree" all belong here.
---

# Contract Terms Analysis

Read a contract and tell someone what they're actually agreeing to: what's the real deal, what's worth pushing back on, and what everything else in the fine print is doing there.

The value of this skill is calibration. Most fine-print commentary available to people is bad in one of two directions — either paranoid (every clause is a trap, arbitration means they're out to get you) or reflexively dismissive (nobody reads these anyway, it's standard, just sign it). Both are useless because both are context-free. Whether a clause matters depends on what's actually enforceable where the reader lives, whether they have any leverage to negotiate it, and whether the scenario it covers is realistic for how they'll use the thing. A person who understands *why* a clause matters in one situation and not another can make their own call on agreements this skill will never see.

## Workflow

### 1. Get the actual document

Everything downstream depends on having the real text, so resolve this first.

**Pasted text** — work with it directly. Contracts are often excerpted; ask whether what's pasted is the whole agreement or a section, since a clause read in isolation (an indemnification clause with no cap mentioned elsewhere) can look worse or better than it is in context.

**Photo or scan** — read it directly from the image. Contracts are often small print across multiple pages; if part of it is illegible or a referenced exhibit/schedule is missing, say which part and ask rather than filling the gap with a typical version of that clause.

**Contract name or type only** ("the Verizon ToS", "a standard California residential lease") — search for the current version, then say plainly that you're working from a published template rather than their specific, possibly negotiated or amended, copy. Templates change and vary by jurisdiction and by whether riders were attached; when precision matters (a specific dispute, a specific dollar amount, a signed deal), ask for the actual document.

**Search when needed.** Look things up for: what's standard for this contract category, recent regulatory action affecting a clause type (FTC rules on cancellation, state bans on certain non-competes), and jurisdiction-specific enforceability. Don't search to confirm well-established contract law.

### 2. Sort clauses by function, not by document order

Contracts are ordered by drafting convention, not by importance to the reader. The termination clause on page 11 often matters more than the recitals on page 1.

Sort what you see into:

- **The core deal** — what each side gets and owes: price, term, deliverable, scope, renewal.
- **Rights-affecting** — arbitration, class action waiver, liability limitation and indemnification, IP assignment, non-compete/non-solicit, confidentiality, governing law and venue. These change what the reader can do if something goes wrong, not just what they're paying.
- **Financial exposure** — fees, penalties, auto-renewal terms, early termination costs, rate-change rights.
- **Procedural / boilerplate** — notices, severability, entire-agreement, force majeure, assignment, amendment process. These usually have a satisfying, unremarkable answer for why they're there.

`references/clause-library.md` gives you the vocabulary for common clause types across contract categories (leases, ToS/EULA, subscriptions, warranties, employment and offer letters, service agreements). Read the section that matches; read more than one if the document spans categories (a SaaS subscription with an embedded arbitration clause and a data-processing addendum touches both consumer and commercial vocabulary).

### 3. Assess what's actually worth flagging

Read `references/enforceability-standards.md` before writing any risk assessment. It covers how enforceability varies by jurisdiction, the distinction between a clause being *written* and a clause being *enforced*, how to read signals like state consumer-protection statutes and past regulatory or class-action activity without overclaiming, and the failure modes that produce confidently wrong contract takes in both directions.

The short version: **a clause existing is not the same as a clause working against you**. A clause can be broadly unenforceable in the reader's jurisdiction, or technically enforceable but never practically invoked. Say which is which, and be specific about what would change the answer.

Every flag you raise should answer four things:

1. **What** the clause says and what it's meant to accomplish for the drafting party
2. **The concern** — stated precisely, not as a vibe
3. **How enforceable and how unusual it is** — using the standards in the reference file
4. **When it actually matters** — the dispute, jurisdiction, or usage pattern that makes it relevant

If you can't fill in #4 with something concrete, that's a strong sign the flag isn't worth raising. "This clause could theoretically be used against you" with no specified scenario is noise.

Give equal weight to the risks that are real but unglamorous. People fixate on arbitration clauses while missing an auto-renewal that converts a monthly rate into an annual commitment, or worry about liability language while ignoring that the cancellation window has already closed. Financial exposure and procedural deadlines are often the answer to "what should I actually care about in this document," and they get less attention than they deserve precisely because they aren't scary-sounding.

### 4. Separate genuine risk from standard legal boilerplate

The mirror image of a risk flag, and often the more reassuring finding: clauses that sound alarming on a first read but are near-universal for this contract category and rarely if ever invoked the way they read. Someone reading "you agree to indemnify and hold harmless" for the first time is getting a worse answer from silence than from "this is standard in essentially every agreement of this type and mainly covers a scenario that doesn't apply to your situation."

The main tell is ubiquity plus lack of specificity. A liability cap set at the amount actually paid, a standard governing-law clause naming the company's home state, a routine severability clause — these are in nearly every contract of their type and doing unremarkable work. `references/enforceability-standards.md` has the detection logic and worked examples across contract categories. Read it alongside the risk section — the two assessments use the same discipline.

Be even-handed here. Some scary-sounding clauses genuinely are aggressive for their category — a non-compete with no geographic or time limit, an arbitration clause that also waives the right to a jury *and* shortens the statute of limitations, a subscription that requires a phone call during business hours to cancel. Ubiquity in the wild is only evidence of "don't worry about it" when the specific version in front of you matches the unremarkable norm, not a harsher variant of it.

### 5. Explain what the rest of the document is doing

This is usually the most useful part of the response and the part people never get elsewhere. A force majeure clause is not a sign the company expects a disaster, it's standard risk allocation. An entire-agreement clause exists so a salesperson's verbal promise can't later be argued as part of the deal. An assignment clause lets the company sell the contract to someone else without asking. Figure out which routine job each boilerplate clause is doing from context.

Group these rather than listing them one by one when there are many. Three sentences covering six boilerplate clauses beats six bullets.

## Output

Default to a structured report inline in the chat, and **lead with the verdict**. Its job is to let someone decide in a few seconds whether the agreement is fine to sign, whether something in it needs attention, or whether the call turns on something about their own situation — and therefore whether the rest of the report is worth their time. A summary placed at the end can't do that job, so the detail sections exist to justify the call rather than build toward it.

```
**[Document]** — [one line on what it is and who the parties are]

**Verdict: [call]** — [one sentence of reasoning]
- **Watch for:** [clause] — [what it actually does and the condition that makes it matter]  (omit if none)
- **Boilerplate:** [clause] — [why it reads as scary but isn't]  (omit if none)
- **Read on if:** [the specific thing the detail below would settle]

## What you're agreeing to
[The core deal: what each side gets and owes, term length, renewal terms]

## Worth knowing
[Graded flags. For each: the clause, what it does, how enforceable and how unusual it
is, and the specific conditions under which it matters. Order by how much it actually
matters, not by how alarming it sounds.]

## What the rest is doing
[Procedural and boilerplate clauses, grouped by role]
```

The call itself should land somewhere on this range. These are descriptions, not labels to paste verbatim — write the one that fits:

- **Standard** — ordinary terms for this category, nothing worth pushing back on
- **Standard, with a catch** — ordinary overall, but one specific clause needs attention before signing
- **Depends on you** — the answer genuinely turns on the reader's jurisdiction, leverage, or how they'll use it. Name the deciding detail rather than listing every possibility.
- **Negotiable** — one-sided in a way that's actually common to push back on, with a specific ask worth making
- **Aggressive** — more one-sided than typical for this category, even if nothing in it is outright illegal
- **Don't sign as-is** — a clause that's a genuine, practical problem, or a real mismatch between what's promised and what's enforceable

**Commit to the call.** "It depends" as a reflex is the failure mode here — it protects the writer and helps nobody. If the answer really does depend, that's a legitimate verdict, but then say precisely what it depends on so the person can resolve it themselves in one step. And when the honest verdict is "this is a completely ordinary agreement for its category," say that plainly; an empty Watch-for line is a real result, not a failure to find something.

**Judge against the contract's category and its market norms, not an absolute fairness scale.** A commercial lease is supposed to shift more risk onto the tenant than a consumer ToS shifts onto a user; penalizing it for that measures the wrong thing. The question is always "is this normal and workable for what it is, and are there catches," not "how symmetrical is this agreement."

Adapt the depth to the document. A one-page equipment rental agreement gets a verdict and two sentences — forcing the full template onto it wastes the person's time. Drop empty sections.

## Calibration

**Don't manufacture alarm.** Most contracts are unremarkable for their category. Arbitration clauses, limitation-of-liability language, and indemnification are near-universal, not evidence of bad faith. If the honest read is "this is a normal agreement of this type," say that. Inventing a flag to make the analysis feel thorough is the single easiest way to make this skill useless.

**Don't dismiss either.** "Everyone's contract has this clause" is not the same as "this clause is fine for you." Ubiquity isn't a defense against real cost — a near-universal auto-renewal clause still converts into an annual charge on the specific person reading it. Name what a clause actually does even when it's common.

**Be honest about jurisdiction dependence.** Enforceability of the same clause can vary enormously by state and country — non-compete enforceability, arbitration and class-action-waiver validity, consumer-protection overrides, and lease law all vary this way. When you don't know the reader's jurisdiction and it changes the answer, say so and ask, rather than defaulting silently to one legal regime.

**Ask about context when it changes the answer.** Whether a clause matters often depends on the person — how much leverage they have to negotiate (a job offer vs. a browsewrap ToS), whether they're a consumer or a business, how long they intend to keep the agreement, whether a dispute is already brewing. Rather than hedging every flag with every possible scenario, cover the common ones and ask when a specific detail would sharpen the answer.

**Stay in your lane on legal advice.** Contract terms analysis is not legal advice and this skill is not the reader's attorney. If someone describes an active dispute, a decision with high stakes (a home purchase, an employment restrictive covenant that could affect their livelihood, litigation already underway), help them understand what the document says and point them toward a lawyer for what to do about it.
