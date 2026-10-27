# SimVizion UI Design System

**Family Resemblance, Not Uniformity.** A desktop-first visual design language for Rust, Tauri, Electron, native desktop, and related web applications.

Design every application for its purpose. Make every application unmistakably SimVizion.

## What's new in v1.3

v1.3 strengthens **visual confidence without decorative excess**: purposeful headline-lime metrics, readable-secondary text, responsive dashboard typography, an intermediate unified content-card surface, contextual density, and required whole-screen visual review. Equal peer categories stay equally prominent. All improvements preserve the original compact technical-editor defaults.

## Install for coding agents

The repository root contains `SKILL.md`, with supporting specifications in `references/`, implementation examples in `examples/`, and visual references in `assets/`.

### Install into a project

Run from your project root:

```bash
git clone https://github.com/206airmail/simvizion-ui-skill.git .agents/skills/simvizion-ui
```

To update the skill later:

```bash
git -C .agents/skills/simvizion-ui pull --ff-only
```

For Windows PowerShell, use the same commands (Git must be installed).

Other agents may use another skill directory, such as `.claude/skills/simvizion-ui` or `.codex/skills/simvizion-ui`, depending on their host's skill-discovery conventions.

### Pin a known version

Once a version tag exists, clone and check out that tag:

```bash
git clone https://github.com/206airmail/simvizion-ui-skill.git .agents/skills/simvizion-ui
git -C .agents/skills/simvizion-ui checkout v1.3.0
```

To update from a pinned version, deliberately check out a newer published tag. An ordinary `git pull` will not advance a detached tag checkout.

## Tell an agent to use the skill

> Read `.agents/skills/simvizion-ui/SKILL.md` and follow the references it identifies for the current task. Preserve family resemblance without copying another application's layout.

## Source of truth

- `SKILL.md`: mission, design authority, workflow, and reference routing.
- `references/`: canonical detailed design rules.
- `QUICK_REFERENCE.md`: convenience summary; not a competing specification.
- `examples/`: illustrative implementation guidance.
- `VISUAL_REFERENCE.md` and `assets/`: visual references, not compulsory layouts.

## Release practice

1. Change the skill and applicable canonical references.
2. Synchronize `QUICK_REFERENCE.md`, examples, and implementation tokens.
3. Check internal links and inspect representative UI states.
4. Commit and tag versions, for example `v1.2.0`, `v1.3.0`.
5. Update consuming projects with `git pull --ff-only`, or switch to the new tag for pinned installs.

This repository is intended to store the **skill source**, not a shared runtime UI framework. It does not require applications to use identical layouts or technologies.
