# Skills

A collection of [Agent Skills](https://agentskills.io/specification) — reusable instructions that give an AI agent a calibrated, structured way to handle a specific kind of task, instead of relying on whatever it improvises in the moment.

## What's here

| Skill | Description |
|---|---|
| [`ingredient-analysis`](skills/ingredient-analysis) | Reads an ingredient list (food, drink, supplement, cosmetic, cleaning product, or other household item) and gives a verdict: what's genuinely worth worrying about, what's on the label for marketing, evidence-graded flags, and what the minor ingredients are actually doing. |
| [`product-comparison`](skills/product-comparison) | Compares two or more products — ingredients, materials, specs, features, cost per unit of what matters — and names which one to get and why. Delegates to `ingredient-analysis` for the per-product depth on ingredient-driven products. |
| [`contract-terms-analysis`](skills/contract-terms-analysis) | Reads a contract, terms of service, lease, warranty, subscription agreement, or offer letter and gives a verdict: what's standard boilerplate, what's worth pushing back on, how enforceable each flagged clause actually is, and what the routine legal language is doing. |

Each skill lives in `skills/<name>/`, with a `SKILL.md` describing when and how to use it, and a `references/` folder of material the skill reads on demand rather than keeping loaded up front.

## Using these skills

**Claude Code:** clone this repo and symlink (or copy) the skill directories you want into `~/.claude/skills/` (available in every project) or a project's `.claude/skills/` (scoped to that project):

```sh
git clone https://github.com/CalMlynarczyk/skills.git
cd skills
ln -s "$(pwd)/skills/ingredient-analysis" ~/.claude/skills/ingredient-analysis
ln -s "$(pwd)/skills/product-comparison" ~/.claude/skills/product-comparison
ln -s "$(pwd)/skills/contract-terms-analysis" ~/.claude/skills/contract-terms-analysis
```

**skills.sh:** this repo uses the flat `skills/<name>/SKILL.md` layout that [skills.sh](https://www.skills.sh/) scans for, so it's installable there too:

```sh
npx skills add CalMlynarczyk/skills
```

**Any other agent that implements the [Agent Skills spec](https://agentskills.io/specification):** point it at a `skills/<name>` directory directly — `SKILL.md` plus its `references/` folder is a complete, self-contained skill.

## Repository structure

```
skills/
  ingredient-analysis/
    SKILL.md
    references/
  product-comparison/
    SKILL.md
    references/
    assets/
  contract-terms-analysis/
    SKILL.md
    references/
```

See `AGENTS.md` for details on the conventions these skills follow and guidance for extending the collection.

## License

MIT — see [LICENSE](LICENSE).

