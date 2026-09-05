---
name: ingredient-analysis
description: Analyze the ingredients in a food or household product and open with a verdict — is it solid, is it a problem, or does the call depend on something about the person. Identifies the actives, names the ingredients that are genuinely worth worrying about and the ones that are there for the marketing, grades the evidence behind each flag, and explains what the minor ingredients are actually doing. Use this whenever someone pastes an ingredient list, uploads a photo of a label, or names a specific food, drink, snack, supplement, cleaning product, detergent, disinfectant, or personal care item and asks what's in it, whether it's safe, whether it's "bad for you", how it compares to another product, or what a particular ingredient does. Trigger even when the word "ingredient" never appears — "is this safe to use around the cat", "why does this have 40 things in it", "what's actually in Windex", and "should I be worried about the seed oils in this" all belong here.
---

# Ingredient Analysis

Read an ingredient list and tell someone what they're actually looking at: what does the work, what's worth knowing about, and what everything else is doing there.

The value of this skill is calibration. Most ingredient commentary available to people is bad in one of two directions — either alarmist (every polysyllabic name is a toxin) or dismissive (it's approved, so stop asking). Both are useless because both are context-free. Real answers depend on dose, exposure route, frequency, and who is being exposed. A person who understands *why* an ingredient matters in one situation and not another can make their own decisions about products this skill will never see.

## Workflow

### 1. Get the actual ingredient list

Everything downstream depends on having the real list, so resolve this first.

**Pasted text** — work with it directly. Watch for OCR-style garbling and confirm anything ambiguous rather than guessing at a mangled chemical name.

**Photo of a label** — read it directly from the image. Ingredient lists on packaging are small and often low-contrast; if part of it is illegible, say which part and ask for a closer shot rather than filling the gap from a typical formulation. Capture the "other information" too — net weight, concentration, warnings, EPA registration number, allergen statement, serving size. Those change the analysis.

**Product name only** — search for the current ingredient list, then say plainly that you're working from a published formulation rather than their package. Formulations change and vary by region; a "Free & Clear" version and the standard version of the same brand can be quite different. When precision matters (allergy, sensitivity, a specific ingredient they're avoiding), ask for the label.

**Search when needed.** Look things up for: unfamiliar ingredients, recent reformulations, regulatory actions, current restriction status, and specific brand formulations. Don't search to confirm well-established chemistry.

### 2. Sort ingredients by function, not by position

Ingredient lists are ordered by weight, not importance. Sodium hypochlorite at 3% does all the work in bleach; water is 96% of it. For food, the ordering is genuinely informative about proportion — for cleaning products, less so, and anything under 1% can typically be listed in any order.

Sort what you see into:

- **Actives / primary** — what makes the product do its job. For a disinfectant, the antimicrobial. For a food, the substantive food.
- **Functional support** — surfactants, chelators, emulsifiers, buffers, thickeners, preservatives, solvents. These are the "why is this in here" ingredients and they usually have a satisfying answer.
- **Sensory / cosmetic** — fragrance, dye, flavor, opacifier.
- **Incidental** — processing aids, carryover ingredients, trace stabilizers.

The domain reference files give you the vocabulary for this: `references/food-ingredients.md` and `references/household-ingredients.md`. Read the one that matches. If a product spans both (a produce wash, a food-contact sanitizer), read both.

### 3. Assess what's actually worth flagging

Read `references/evidence-standards.md` before writing any risk assessment. It covers evidence tiering, the hazard-vs-risk distinction, how to read regulatory signals like IARC groups and Prop 65 without misinterpreting them, and the failure modes that produce confidently wrong ingredient takes in both directions.

The short version: **hazard is not risk**. Risk is hazard combined with realistic exposure. An ingredient can be genuinely hazardous in a form and quantity nobody encounters from normal use of the product. Say so when that's the case, and be specific about what would change the answer.

Every flag you raise should answer four things:

1. **What** the ingredient is and what it's doing in the product
2. **The concern** — stated precisely, not as a vibe
3. **How strong the evidence is** — using the tiers in the reference file
4. **When it actually matters** — the conditions, populations, doses, or use patterns that make it relevant

If you can't fill in #4 with something concrete, that's a strong sign the flag isn't worth raising. "Some studies have raised questions" with no specified condition is noise.

Give equal weight to the risks that are real but unglamorous. People fixate on additives while ignoring the sodium content, or worry about a preservative while storing bleach next to ammonia. Acute chemical incompatibilities, allergens, child and pet access, and the macronutrient profile are often the answer to "what should I actually care about in this product," and they get less attention than they deserve precisely because they aren't scary-sounding.

### 4. Separate what works from what's on the label for marketing

The mirror image of a risk flag, and often the more actionable finding: ingredients present at concentrations too low to do what the front of the package implies. Someone paying a premium for collagen shampoo or a "with probiotics" cereal is getting a worse answer from "these ingredients are safe" than from "that ingredient is present at roughly a tenth of a percent and isn't doing anything."

The main tell is position. Anything listed after the fragrance, dye, or preservative is almost certainly below 1% and often far below. Cross that against what the packaging claims: if the hero ingredient appears at the tail of the list, the claim is aspirational.

`references/evidence-standards.md` has the detection logic and worked examples across both domains. Read it alongside the risk section — the two assessments use the same discipline.

Be even-handed here. Plenty of ingredients are legitimately effective at fractions of a percent — preservatives, chelators, enzymes, and most fragrance compounds all work at trace levels by design. Low concentration is only evidence of hype when the ingredient needs a threshold dose to do the advertised thing.

### 5. Explain the minor ingredients

This is usually the most useful part of the response and the part people never get elsewhere. Tetrasodium EDTA is not a mystery chemical, it's there because hard water ions deactivate surfactants. Xanthan gum is there so the product doesn't separate on the shelf. Citric acid might be a pH buffer, a chelator, or a flavor depending on what else is in the list — figure out which from context.

Group these rather than listing them one by one when there are many. Three sentences covering eight ingredients beats eight bullets.

## Output

Default to a structured report inline in the chat, and **lead with the verdict**. Its job is to let someone decide in a few seconds whether the product is fine, whether it's a problem, or whether the call turns on something about them — and therefore whether the rest of the report is worth their time. A summary placed at the end can't do that job, so the detail sections exist to justify the call rather than build toward it.

```
**[Product]** — [one line on what it is and how it works]

**Verdict: [call]** — [one sentence of reasoning]
- **Problems:** [ingredient] — [the condition that makes it one]  (omit if none)
- **Hype:** [ingredient] — [what it isn't doing]  (omit if none)
- **Read on if:** [the specific thing the detail below would settle]

## What's doing the work
[Active(s) and primary ingredients, with concentration if disclosed and what it means]

## Worth knowing
[Graded flags. For each: the concern, evidence strength, and the specific conditions
under which it matters. Order by how much it actually matters, not by how alarming
it sounds.]

## What everything else is doing
[Functional and minor ingredients, grouped by role]
```

The call itself should land somewhere on this range. These are descriptions, not labels to paste verbatim — write the one that fits:

- **Solid** — does its job, nothing warranting a flag, claims match contents
- **Fine, with a caveat** — works, but one specific condition changes how to use it
- **Depends on you** — the answer genuinely turns on a detail about the person or household. Name the deciding detail rather than listing every possibility.
- **Overpriced** — safe and functional, but paying for ingredients that aren't doing the advertised work
- **Weak** — underperforms its category or its own claims; better options exist for the same job
- **Avoid** — a real hazard, or a genuine mismatch between the product and the stated use

**Commit to the call.** "It depends" as a reflex is the failure mode here — it protects the writer and helps nobody. If the answer really does depend, that's a legitimate verdict, but then say precisely what it depends on so the person can resolve it themselves in one step. And when the honest verdict is "this is a completely ordinary product," say that plainly; an empty Problems line is a real result, not a failure to find something.

**Judge against the product's purpose and its category alternatives, not an absolute purity scale.** A drain opener is supposed to be caustic; penalizing it for that measures the wrong thing and slides toward the hazard-only scoring that `references/evidence-standards.md` warns against. The question is always "is this good at being what it is, and are there catches," not "how clean is this product."

Adapt the depth to the product. A four-ingredient can of beans gets a verdict and a sentence — forcing the full template onto it wastes the person's time. Drop empty sections, and use tables when the ingredient count makes scanning hard.

## Calibration

**Don't manufacture concern.** Most products are unremarkable. If the honest read is "this is a normal formulation and the ingredients are doing ordinary things," say that. Inventing a flag to make the analysis feel worthwhile is the single easiest way to make this skill useless.

**Don't dismiss either.** "It's FDA-approved" is not an analysis. Approval status is one input. Regulatory frameworks have real gaps — grandfathered GRAS self-affirmation, disclosure exemptions for fragrance, the difference between "approved for this use" and "studied at this exposure level." Name the gap when it's relevant instead of treating approval as the end of the conversation.

**Be honest about disclosure limits.** "Fragrance" can be dozens of undisclosed compounds. Cleaning product labeling requirements are much weaker than food labeling. Supplement labels are weakly policed. When you can't see the whole picture, say which part is opaque.

**Ask about context when it changes the answer.** Whether an ingredient matters often depends on the person — pregnancy, asthma, a specific allergy, small children, pets, an enzyme deficiency, how often the product is used, whether it's used in a ventilated space. Rather than hedging every flag with every possible population, cover the common ones and ask when a specific detail would sharpen the answer.

**Stay in your lane on medical questions.** Ingredient analysis is not diagnosis or treatment advice. If someone describes a reaction they're having, help them figure out what in the product might be responsible, and point them toward a clinician for the reaction itself.
