# AGENTS.md

This file provides guidance to GenAI agents when working with code in this repository.

## What this repository is

A collection of GenAI Agent Skills — no build, no tests, no application code. Each skill is a directory under `skills/` containing a `SKILL.md` (the skill's instructions, loaded into context when triggered) and a `references/` folder of markdown files the skill reads on demand for deeper detail it doesn't need up front. There is no compiler, linter, or test suite to run; the "correctness" of this repo is the quality and consistency of the prose in `SKILL.md` and its references.

## Repository layout

```
skills/
  <skill-name>/
    SKILL.md              # required: frontmatter + instructions
    references/*.md       # optional: on-demand lookup material
```

Currently: `skills/ingredient-analysis` and `skills/product-comparison`.

## SKILL.md structure

Every `SKILL.md` starts with YAML frontmatter:

```yaml
---
name: skill-name              # kebab-case, matches the directory name
description: >
  What the skill does, then an explicit list of trigger phrasings —
  including ones that don't contain the obvious keyword.
---
```

The `description` is what a future Claude uses to decide whether a skill applies to a given request, so it must enumerate non-obvious trigger phrasings, not just restate the skill's name (see both existing skills for the pattern: e.g. ingredient-analysis triggers on "is this safe to use around the cat", product-comparison triggers on "talk me out of the expensive one").

The body follows a consistent shape across skills:

1. **One-line restatement** of the skill's job, then a short paragraph naming the specific failure mode the skill exists to avoid (e.g. ingredient-analysis's "alarmist vs. dismissive" framing; product-comparison's "two teardowns stapled together" framing). This framing paragraph is load-bearing — it's what keeps the skill's output calibrated rather than generic, so preserve it when editing.
2. **`## Workflow`** — numbered steps in the order the analysis should actually happen (establish scope/decision → gather substance → assess → structure findings). Steps reference `references/*.md` inline at the point they're needed rather than front-loading all reference material.
3. **`## Output`** — a literal template (in a fenced code block) the response should follow, plus a short list of the possible verdicts/calls with one line each on when to use them. Every template leads with a verdict/pick line first, details after — these skills are built around "commit to a call up front, justify it below," not narrative build-up.
4. **`## Calibration`** — explicit failure modes to avoid, usually paired opposites (e.g. "don't manufacture concern" / "don't dismiss either"). This section is where the skill's judgment calls are pinned down; don't remove it during trims.

## References

`references/*.md` files hold domain material a skill needs but shouldn't keep in the always-loaded `SKILL.md` body: ingredient vocabularies, evidence-grading rubrics, spec-reading guidance. `SKILL.md` points to them by relative path (`references/evidence-standards.md`) with a sentence on when to read which one — keep that pointer text accurate when adding, renaming, or splitting reference files.

Skills can depend on each other: `product-comparison` explicitly delegates per-product ingredient analysis to the `ingredient-analysis` skill rather than re-deriving it ("Run the `ingredient-analysis` skill on each product... That skill owns the per-product depth; this one owns the comparison"). When adding a skill that overlaps an existing one's territory, prefer this delegation pattern over duplicating logic.

## Distribution: skills.sh discovery

This repo is laid out as `skills/<name>/SKILL.md` — a flat layout — which is one of the layouts [skills.sh](https://www.skills.sh/) scans for directly (it also checks a catalog layout `skills/<category>/<name>/SKILL.md`, and reads `.claude-plugin/marketplace.json` / `plugin.json` if present). No repo restructuring or top-level manifest is required just to be discoverable; skills.sh indexes public repos by scanning for `SKILL.md` files rather than requiring a submission step.

What discovery quality actually depends on is the frontmatter, per the [Agent Skills spec](https://agentskills.io/specification):

- `name` — lowercase letters, numbers, and hyphens only; no leading/trailing/consecutive hyphens; ≤64 chars; **must exactly match the parent directory name**. Both existing skills already satisfy this.
- `description` — non-empty, ≤1024 chars. This is the only thing a browsing human or a routing agent sees before opening the file, so treat it as index copy, not just an in-session trigger list (both existing skills are already written this way — see the SKILL.md structure section above).
- `license` (optional) — a license name or pointer to a bundled license file. This repo has a root `LICENSE` (MIT) but no skill currently declares `license: MIT` in its frontmatter; adding it makes the license visible to tools that only look at the skill directory in isolation (e.g. once a skill is vendored or copied elsewhere).
- `compatibility` (optional) — only add this if a skill assumes something about its runtime (a required tool, network access, a specific host product). Neither current skill needs it — both are pure-reasoning skills with no execution dependency.
- `metadata` (optional) — free-form string map (e.g. `author`). Not required for discovery, but harmless to add.

## Distribution: Agent Plugin readiness

This repo is not yet a Claude Code plugin (no `.claude-plugin/` directory). Converting it is additive, not a restructure:

- A plugin needs a manifest at `.claude-plugin/plugin.json`. Only `name` is required; worth setting `version`, `description`, `author`, `license`, and `repository` too since those are what render in a plugin listing.
- The default plugin skill path is `skills/`, scanned automatically — which is exactly this repo's existing layout. No file moves needed; adding `.claude-plugin/plugin.json` at the root is sufficient to make this a valid single plugin bundling both skills.
- Once packaged, skills are namespaced as `<plugin-name>:<skill-name>` (e.g. a plugin named `product-research` would expose `/product-research:ingredient-analysis`). The plugin `name` becomes part of the public invocation surface, so it's worth deciding deliberately rather than defaulting to the repo name.
- If this becomes a multi-plugin **marketplace** rather than a single installable plugin, that needs a separate `.claude-plugin/marketplace.json` at the root listing each plugin with its `source` and `skills` paths (see `anthropics/skills`'s `.claude-plugin/marketplace.json` for the shape). For a repo this size (one plugin, two skills), a single `plugin.json` is the simpler fit unless the intent is specifically to host multiple independently-installable plugins.
- The two distribution goals don't conflict: skills.sh reads `.claude-plugin/plugin.json` / `marketplace.json` directly when present, and otherwise falls back to scanning `skills/`. Adding plugin manifests later won't break skills.sh discovery of this repo, and doesn't require touching any existing `SKILL.md`.

## Working on this repo

- Changes here are almost entirely edits to `SKILL.md` / `references/*.md` prose. There's no code path to run — validate a change by rereading it against the frontmatter's trigger list and the workflow/output/calibration structure above, not by executing anything.
- Keep frontmatter `description` fields comprehensive: they're the only thing used for skill routing, so a trigger phrasing left out is a real gap, not a style nit.
- New skills should follow the four-section body shape (framing → Workflow → Output → Calibration) already established by both existing skills, including a literal output template in a fenced code block.
- Keep skill directory names and their `name` frontmatter in sync (see Distribution sections above) — this is enforced by the Agent Skills spec and by how Claude Code namespaces skills inside a plugin, not just a style preference.
