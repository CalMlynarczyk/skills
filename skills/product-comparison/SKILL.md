---
name: product-comparison
description: Compare two or more products on what they are actually made of and what they actually do — ingredients, materials, specs, features, and cost per unit of the thing that matters — and name which one to get. Use this whenever someone is choosing between products: foods, drinks, supplements, cosmetics and personal care, cleaning products, home goods, furniture, tools, appliances, or consumer electronics. Trigger even when the word "compare" never appears — "is the store brand as good as the name brand", "which of these two sunscreens should I get", "talk me out of the expensive one", "what's the difference between X and Y", "worth upgrading from my current one", and "best X for daily use" all belong here. Also use when only one product is named but the real question is whether something else would serve better.
---

# Product Comparison

Decide between products by looking at what they are made of and what they can do, then say which one to get and why.

The value here is the comparison layer, not the teardowns. Two thorough single-product analyses stapled together is the most common way this goes wrong: symmetric, complete, and useless, because it leaves the reader doing the actual work of figuring out which differences matter. A good comparison is asymmetric on purpose — most attributes are ties and get one line, and the two or three attributes that actually decide it get the space. The reader should be able to stop after the first six lines and be right.

## Workflow

### 1. Establish what's being decided

Before gathering anything, pin down the decision, because the same two products can have different winners depending on the job.

- **The job.** Sunscreen for a daily commute and sunscreen for a day of open-water swimming are different decisions with the same candidates. A drill for hanging pictures twice a year is not a drill for framing a deck.
- **Replace or add.** "Which of these is better" and "is this better than what I already have" need different answers. The second has a much higher bar — switching costs are real and the incumbent gets to keep its accessories, refills, and learned habits.
- **Hard constraints.** Budget ceiling, physical dimensions, ecosystem lock-in, an allergy, a household member or pet, a lease that forbids drilling. These filter candidates rather than scoring them, so establish them before doing analysis on products that are already out.

Infer what you can from context and memory rather than interrogating. One question is fine when the answer genuinely changes the winner; three questions before any analysis is a worse experience than a good comparison with its assumptions stated plainly.

### 2. Fix the candidate set

**Named products** — compare those, and say so if an obvious candidate is missing from their set. Adding one uninvited option with a sentence on why it's in the running is usually welcome; replacing their list with your own is not.

**A category, not products** ("best sunscreen for daily use") — pick three or four candidates yourself and open by saying why those. The selection criteria matter as much as the comparison: span the meaningful range (a budget option, the category default, a premium option, and any genuinely different approach) rather than four variations of the same thing. Say plainly what you excluded and why, because "I didn't consider it" and "I considered it and it lost" are very different signals.

**Products that aren't in the same class** — say so early rather than forcing a table. When someone asks whether a $40 immersion blender beats a $400 stand mixer, the honest answer is that they solve overlapping but different problems, and the useful move is to name which jobs go to which. Don't fake comparability by finding attributes both happen to have.

### 3. Set the criteria and state the assumptions

Criteria come from the person: what they've said in this conversation, what's in their stated preferences and profile, and what they've cared about in past comparisons. Apply that context rather than defaulting to a generic scoring frame — someone with a dog, a small kitchen, or a strong preference for repairable hardware has a different winner than the average buyer.

State the assumptions compactly at the top of the output, in the **Assuming** line. This exists so a wrong assumption gets corrected in one reply instead of invalidating the whole analysis silently. Ask up front only when a preference would actually flip the winner and you can't infer it — otherwise assume, label the assumption, and note what changes if it's wrong.

Be careful about criteria the person never mentioned. Environmental impact, brand ethics, and resale value are legitimate factors, but inserting them uninvited quietly substitutes your priorities for theirs. Include them when they're decisive or when the person's stated values point that way, and label them as an addition when you do.

### 4. Gather the substance

**Ingredient-driven products** — foods, drinks, supplements, cosmetics, personal care, cleaning products. Run the `ingredient-analysis` skill on each product to get the actives, the evidence-graded flags, and the hype detection. That skill owns the per-product depth; this one owns the comparison. Don't re-derive its analysis, and don't flatten its findings into a single quality rating — a comparison needs the reasoning behind each flag so it can weigh flags against each other.

**Feature-driven products** — devices, appliances, tools, furniture, home goods. Read `references/materials-and-specs.md` for how to read spec sheets, what materials and construction details predict about longevity, which certifications carry information, and where published specs mislead.

**Most products are both.** A water filter has a media chemistry and a flow rate. A mattress has foam composition and a warranty. A frying pan is a coating question and a thermal mass question. Cover both axes when both bear on the decision.

**Sourcing.** Search for current formulations, specs, recalls, reformulations, and price. Say which numbers came from a label or manufacturer spec sheet versus a third-party test versus your own estimate, because those have very different reliability and the person deserves to know which parts of the table to trust. Manufacturer specs are marketing documents: they are accurate about what they measure and silent about what they don't.

**Asymmetric information is a finding.** When one product publishes full disclosure and another doesn't, that's a real difference, not a gap in your research. Say so rather than quietly comparing the well-documented product against your guesses about the other.

### 5. Build the comparison on aligned rows

Tables are how a comparison becomes checkable. The discipline that makes them work: **one attribute per row, the same attribute for every product, in the same units.** A table where each column lists whatever that manufacturer chose to advertise looks like a comparison but can't be read across, which is exactly the failure it's supposed to prevent.

| | Product A | Product B |
|---|---|---|
| Active | Zinc oxide 18% | Avobenzone 3% + homosalate 10% |
| Cost per use | $0.34 | $0.19 |
| Water resistance | 80 min | 40 min |
| Disclosure | Full | Fragrance undisclosed |

Normalize cost to the unit that reflects the decision — per wash, per gram of protein, per mL of active, per year of expected service life — and show the raw price too, since that's the number that has to clear the budget. Cost per unit is where genuinely surprising results tend to live, and it's the most common thing a person can't easily compute standing in a store.

Numbers belong in the table where real data exists: concentrations, capacities, dimensions, measured performance, warranty length, price per unit. Don't invent scores for things that don't have them — no 8/10 for "build quality", no weighted composite total. A composite score buries the weighting where nobody can argue with it and gives the arbitrary parts of the analysis the same authority as the measured parts. Better to show the real numbers and say which ones drove the call.

When an attribute the person cares about has no reliable data, keep the row and put "not disclosed" or "no independent testing" in the cell. Dropping it makes the comparison look more resolved than it is, and quietly rewards whichever product publishes least.

### 6. Find what actually separates them

Sort every difference into three buckets, and spend your output budget accordingly:

- **Decisive** — differs between products and matters for this person's job. This is the comparison. Usually two or three attributes.
- **Real but minor** — differs, but not enough to move the decision. One line each, or grouped.
- **Ties** — the same in every way that matters. Say so explicitly and briefly. Naming ties is not filler; it's what stops someone from re-litigating a difference that doesn't exist, and it's how they know the winner didn't win on a technicality.

Watch for the streetlight effect: the attributes that are easy to measure (megapixels, thread count, milligrams of a headline ingredient) get treated as decisive because there's a number, while the attributes that decide satisfaction (does it fit the space, is it annoying to clean, does the app require an account) get skipped because they don't tabulate. Push against that.

### 7. Flag deal-breakers separately from catches

A deal-breaker disqualifies a product for this person regardless of how it scores elsewhere — an allergen, an incompatibility with something they already own, a size that doesn't fit, a subscription requirement, a documented safety issue. These belong at the top, not buried in a row, because they end the analysis for that product rather than contributing to it.

A catch is a real drawback that doesn't disqualify: shorter warranty, annoying refill design, a flag from `ingredient-analysis` that matters only under conditions that don't apply here. Keep the two categories apart. Blurring them either alarms people out of a fine product or buries something that should have ended the conversation.

### 8. Call it

Name the winner and defend it in a sentence. When the answer genuinely depends on something unresolved, that's a legitimate verdict — but then name the single deciding detail so the person can settle it themselves in one step, rather than listing every branch. "Get A unless you're washing in cold water, in which case B" is a decision. "It depends on your priorities" is not.

If it's a tie, say it's a tie and tell them to buy the cheaper or more available one. That's a real result and often the most useful one, since it releases them from a decision they were treating as consequential.

## Output

Inline in the chat by default, structured like this. For comparisons big enough to be reference material — five or more products, or something they'll take shopping — offer a saved file at the end rather than assuming.

```
**[The decision]** — [what's being chosen, for what job]

**Pick: [product]** — [one sentence of why]
**Assuming:** [criteria being applied and where they came from]
- **Deal-breakers:** [product] — [what disqualifies it]  (omit if none)
- **Flips if:** [the one condition that changes the answer]

## What separates them
[Aligned-row table. Every product gets the same rows in the same units.]

## Where it's decided
[The two or three attributes driving the call, with the evidence behind each.]

## Where they're the same
[The ties, briefly.]

## Catches
[Per-product drawbacks that don't disqualify but should be known before buying.]
```

Adapt the depth to the decision. Two nearly identical pantry staples get a verdict, a four-row table, and a line — running the full template on them wastes the reader's time and implies the choice matters more than it does. Drop empty sections.

## Calibration

**Don't manufacture differentiation.** Many products in a category are genuinely equivalent, and store brands are frequently the same formulation from the same plant. If the honest read is "these are the same product at different prices," lead with that. Inventing a tiebreaker to justify the analysis is the fastest way to make this skill untrustworthy.

**Don't let price anchor the analysis.** Expensive products are not automatically better and cheap ones are not automatically smarter buys. Both reflexes are common enough that they're worth checking your own reasoning against — the finding that the premium option is genuinely worth it is just as valid as the finding that it isn't, and both need evidence.

**Judge each product against the job, not against a purity scale.** A product optimized for a use case the person doesn't have shouldn't be penalized in the abstract, but it also shouldn't win on capabilities they'll never touch. Extra capability has a cost — in price, size, complexity, or maintenance — and paying it for nothing is a real loss.

**Be explicit about what would change the answer.** New information should update the call cheaply. When the person can resolve an assumption in one reply, tell them which one and what it would change.

**Stay in scope on health and safety questions.** Ingredient flags come from `ingredient-analysis` with their evidence tiers intact; don't upgrade a weak flag into a deal-breaker because it makes for a cleaner verdict. If someone describes a reaction or a medical condition driving the choice, help with the product question and point them to a clinician for the condition itself.
