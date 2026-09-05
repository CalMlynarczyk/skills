# Evidence Standards for Ingredient Risk

How to say something true about whether an ingredient matters.

## Contents

- [Hazard vs. risk](#hazard-vs-risk)
- [Evidence tiers](#evidence-tiers)
- [Reading regulatory signals](#reading-regulatory-signals)
- [Dose anchors worth knowing](#dose-anchors-worth-knowing)
- [Hype vs. function](#hype-vs-function)
- [Failure modes in both directions](#failure-modes-in-both-directions)
- [Populations where the answer changes](#populations-where-the-answer-changes)
- [Writing a calibrated flag](#writing-a-calibrated-flag)

## Hazard vs. risk

Hazard is the capacity to cause harm under some conditions. Risk is the probability of harm under actual conditions of use. The gap between them is where nearly all bad ingredient commentary lives.

Risk ≈ hazard × exposure, where exposure includes:

- **Dose** — how much per use
- **Route** — ingested, dermal, inhaled, ocular. The same compound can be inert on skin and dangerous inhaled. Sodium lauryl sulfate is an eye irritant and a fine toothpaste ingredient.
- **Frequency and duration** — a once-a-year deck stain is not a daily moisturizer
- **Bioavailability** — whether it's absorbed at all. Many compounds pass through unabsorbed, and titanium dioxide's inhalation classification says nothing about eating it.
- **Form** — powder vs. solution vs. aerosol changes inhalation exposure by orders of magnitude

When an ingredient's alarming reputation comes from an exposure scenario that doesn't apply, say exactly that: the finding is real, and here's the exposure it required, and here's what this product delivers.

## Evidence tiers

Use these to label how much weight a claim can carry. State the tier plainly in the output — "animal studies only, at doses far above realistic exposure" is more informative than "some concerns have been raised."

**Tier A — Strong.** Systematic reviews and meta-analyses of human data, or convergent conclusions from independent regulatory bodies (EFSA, FDA, EPA, Health Canada, SCCS) that have reviewed the full dossier. Large well-designed RCTs or consistent large prospective cohorts.

**Tier B — Moderate.** Multiple independent human studies pointing the same direction, but with limitations — observational designs with plausible confounding, small trials, surrogate endpoints, or occupational-exposure data being extrapolated to consumer exposure.

**Tier C — Weak.** Animal studies only, especially at doses well above realistic human exposure. In vitro / cell culture findings. Single studies that haven't replicated. Human studies with serious methodological problems.

**Tier D — Speculative.** Mechanistic reasoning without outcome data ("it binds this receptor, therefore..."), structural similarity to a known-harmful compound, or claims tracing to advocacy scoring systems rather than primary literature.

Tier C and D findings are not worthless — they're how real signals start. But they justify "here's something being investigated," not "avoid this."

**Also note the direction of the gap.** Some ingredients have weak evidence of harm because they've been heavily studied and nothing was found. Others have weak evidence because almost nobody has looked. "No evidence of harm" and "evidence of no harm" are different statements and the distinction is worth making explicit.

## Reading regulatory signals

**IARC classifications rank confidence that something *can* cause cancer under some conditions, not how much cancer it causes.** Group 1 contains both plutonium and processed meat. Group 2A (probably carcinogenic) and 2B (possibly) are frequently reported as though they were potency rankings. When citing IARC, state what the classification means and, where known, the exposure level involved.

**Prop 65 warnings are triggered at thresholds set far below observed-effect levels**, and the litigation structure incentivizes over-warning. Their presence on a product is close to uninformative. Their absence is somewhat more informative.

**GRAS has a self-affirmation pathway** — a manufacturer can conclude an ingredient is safe with its own expert panel and, in many cases, without notifying FDA. So "GRAS" spans everything from exhaustively studied to lightly reviewed. Worth knowing when an ingredient's safety case rests on it.

**EPA registration on a disinfectant** means efficacy claims were reviewed against specified organisms under specified contact times. The contact time on the label is a real number from a real test, and most people don't observe it. That's frequently a more useful thing to tell someone than any ingredient flag.

**"Banned in Europe"** deserves a check rather than a citation. The EU regulates cosmetics on a hazard basis and the US on a risk basis, so divergence is often a philosophical difference, not new evidence. Sometimes the ban is a well-supported response to real data. Look at which.

**Absence of restriction is weak evidence for old ingredients.** Compounds grandfathered in decades ago haven't necessarily been reviewed under modern standards.

## Dose anchors worth knowing

Numbers convert vague worry into an answerable question. When they're relevant, look up the current values rather than reciting from memory — ADIs get revised, and EFSA and FDA sometimes differ.

Useful anchors to reach for:

- **ADI / TDI** (acceptable or tolerable daily intake) — typically the no-observed-adverse-effect level divided by a safety factor of 100. Comparing realistic consumption against the ADI usually resolves food additive questions decisively in one direction or the other.
- **UL** (tolerable upper intake level) for vitamins and minerals — the relevant anchor for fortified foods and supplements, where over-supplementation is a genuine and under-discussed risk.
- **Occupational exposure limits** (OSHA PEL, ACGIH TLV, NIOSH REL) for inhalation risk from cleaning products — set for 8-hour workday exposure, so consumer use is typically far below, but they give a scale.
- **LD50** — use cautiously and rarely. It measures acute lethality, not chronic risk, and it's routinely misused to make ordinary substances sound dangerous.
- **Concentration in the product** — a 0.1% ingredient in a product diluted 1:64 for mopping is a very different exposure from the same ingredient in a leave-on lotion.

## Hype vs. function

Ingredients that can't do what the packaging implies, usually because there isn't enough of them. This is the most commonly useful finding in an ingredient analysis and the one people are least equipped to spot on their own, because the ingredient *is* present — the label isn't lying, it's just letting the reader supply the wrong quantity.

### Detecting it

**Position in the list.** Everything is ordered by weight. Anything appearing after the fragrance, dye, or preservative is below roughly 1% and frequently below 0.1%. If the hero ingredient on the front of the package is sitting between the fragrance and the dye, that's the answer.

**Threshold doses.** The question is whether the ingredient needs a minimum concentration to do the advertised job. Many actives have reasonably well-established effective ranges — niacinamide, salicylic acid, benzoyl peroxide, zinc pyrithione, most antimicrobials. If the concentration can't plausibly reach it, the claim is decorative. Look up the range rather than guessing.

**The active ingredients panel.** In the US, anything making a drug claim must appear in a separate "Active Ingredients" panel with its concentration. If the ingredient the marketing is built around is down in the cosmetic list instead, the manufacturer is deliberately not making a regulated claim about it. That's informative.

**Claim wording.** "Contains," "with," "infused with," and "formulated with" carry no quantity commitment. "Clinically tested" often means tested for irritation, not efficacy. Compare against language that does commit: a stated percentage, an active ingredients panel, a CFU count, or a quantity per serving on a supplement facts panel.

**Whether it survives the product.** Some ingredients are functionally dead on arrival regardless of quantity — probiotics without a viability-at-expiry guarantee, heat-sensitive compounds in a pasteurized product, enzymes in a high-pH formulation that denatures them.

### Where it's legitimate

Low concentration is only evidence of hype when a threshold dose is required. Plenty of ingredients work exactly as intended at trace levels and flagging them is a false positive:

- Preservatives at 0.1% are doing their entire job
- Chelators, pH adjusters, and rheology modifiers work at fractions of a percent
- Enzymes in detergent are catalytic and effective at very low loading
- Fragrance and dye are supposed to be trace
- Micronutrient fortification is dosed to a daily value, not to weight
- Some pharmacologically active compounds genuinely work at low concentration

The test is not "is there very little of it" but "does the advertised effect require more than this."

### Common patterns

**Food and supplements** — protein or fiber claims met by isolates added specifically to hit a panel number; "made with real fruit" where the fruit is a juice concentrate below the sweetener; collagen, which is digested to constituent amino acids like any other protein; superfruit and botanical extracts at trace levels; proprietary blends that hide individual quantities precisely so this analysis can't be done; added vitamins in a product whose main contribution is sugar.

**Personal care** — the "contains argan oil / collagen / caffeine / hyaluronic acid" pattern where the ingredient sits at the end of the list; botanical extract stacks (a dozen plant names, collectively under 1%); "dermatologist recommended" as a claim with no regulatory content.

**Cleaning** — essential oils and plant extracts in a product where a conventional surfactant or quat does all the work; "with baking soda" in a formulation whose cleaning comes from the surfactant system; "plant-derived" surfactants that are molecularly identical to petroleum-derived equivalents; enzyme claims on a product without a functional enzyme system.

Report these the same way as risk flags — name the ingredient, say what it isn't doing, and say what would change the assessment. And note when the product still works fine despite the hype, which is usually the case. "The marketing is nonsense but the underlying formulation is solid" is a genuinely useful thing to tell someone.

## Failure modes in both directions

**Alarmist failures:**

- Treating chemical names as evidence of danger. Everything has a chemical name. Water is dihydrogen monoxide, and "ascorbic acid" is vitamin C.
- Appeal to nature. Natural origin predicts nothing about toxicity — botulinum, ricin, and aflatoxin are all natural, and citric acid from a fermenter is molecularly identical to citric acid from a lemon.
- Citing rodent studies at doses hundreds of times realistic exposure without noting the dose.
- Repeating advocacy-group hazard scores as if they were toxicological findings. Several popular scoring systems weight hazard without exposure and penalize data-poor ingredients, which produces scores that don't track real-world risk.
- "Contains a compound also found in [scary context]." Ingredient overlap is not equivalence of risk.
- Counting ingredients. A 30-ingredient list is not worse than a 6-ingredient list; it's often a more sophisticated formulation, and preservative systems exist because microbial growth in a shampoo bottle is a genuine hazard.

**Dismissive failures:**

- Treating regulatory approval as proof of safety at all exposures, for all populations, indefinitely.
- Ignoring the disclosure gaps — "fragrance," "proprietary blend," and inert-ingredient exemptions all hide real content.
- Overlooking cumulative exposure across many products in the same day.
- Dismissing sensitization and allergy because a compound isn't systemically toxic. Contact dermatitis from a preservative or fragrance allergen is real, common, and the most likely adverse outcome from most personal and household products.
- Missing the acute hazards while debating the chronic ones. Mixing incompatible cleaners, storing concentrates within reach of children, and detergent pod ingestion cause far more documented harm than any of the chronic-exposure ingredient debates.

## Populations where the answer changes

Consider these when the product or context makes them relevant, rather than reciting the whole list every time:

- **Pregnancy and nursing** — retinoids, high-dose vitamin A, certain solvents, alcohol, high-mercury fish, unpasteurized dairy
- **Infants and small children** — honey under 12 months (botulism), nitrate exposure, caffeine, ingestion risk from concentrated products and pods, higher dose-per-body-weight for everything
- **Asthma and reactive airways** — quaternary ammonium compounds, chlorine-releasing agents, fragrance and terpenes, aerosolized anything. Occupational data on cleaning-product-associated asthma is reasonably strong.
- **Contact allergy and eczema** — methylisothiazolinone, formaldehyde releasers, fragrance allergens (the EU's 26 labeled ones are a useful checklist), nickel, lanolin
- **Enzyme and metabolic conditions** — PKU and aspartame (phenylalanine), G6PD deficiency and certain oxidants, hereditary fructose intolerance, celiac and gluten, lactase deficiency
- **Sulfite sensitivity** — genuinely dangerous in a small asthmatic subset, and sulfites are widely used in wine, dried fruit, and processed potato
- **Kidney or liver impairment, or restricted diets** — potassium chloride in salt substitutes, phosphate additives, protein and sodium loads
- **Medication interactions** — grapefruit compounds, vitamin K and warfarin, high-dose supplements generally
- **Pets** — this is often overlooked and genuinely matters. Xylitol is severely toxic to dogs at low doses. Cats metabolize phenols and many essential oils poorly (pine oil, tea tree, citrus oils, phenolic disinfectants). Ethylene glycol is lethal and palatable. Cocoa mulch, alliums, grapes. If someone mentions a pet in the household and the product is relevant, raise it.

## Writing a calibrated flag

A well-formed flag reads like this:

> **Methylisothiazolinone** — preservative, prevents bacterial growth in the water phase. It's a well-documented contact sensitizer; the EU restricted it in leave-on cosmetics in 2017 after a sharp rise in patch-test-positive dermatitis cases, and it remains permitted in rinse-off products at low concentration. *Evidence: strong (Tier A) for sensitization in susceptible people; not a systemic toxicity concern.* Relevant if you have eczema, known preservative allergy, or a history of reacting to wet wipes or shampoos. If none of that applies to you, this is a non-issue in a rinse-off product.

Note what it does: names the function, states the concern precisely, gives the regulatory history as evidence rather than as a scare, tiers the evidence, separates the sensitization question from the toxicity question, and closes with the specific condition under which it matters — including permission to ignore it.

Compare to the version that isn't worth writing:

> **Methylisothiazolinone** — a preservative that has been linked to allergic reactions and is restricted in Europe. Some people prefer to avoid it.

Same ingredient, no information transferred.
