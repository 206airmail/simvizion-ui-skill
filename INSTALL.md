# Installation and updating

This is a directory-based agent skill; its entry point is `SKILL.md` at the repository root.

## Install via Git

```bash
git clone https://github.com/206airmail/simvizion-ui-skill.git .agents/skills/simvizion-ui
```

## Update via Git

```bash
git -C .agents/skills/simvizion-ui pull --ff-only
```

If the skill directory has local modifications, `pull --ff-only` may fail. Commit, discard, or move local changes before updating; keep official changes in this repository rather than editing installed copies.

## Use outside Git-managed agent directories

Clone it to any location the agent can access, then explicitly point the agent at the cloned `SKILL.md` and have it load the task-relevant reference files.

## Publishing

1. Create an empty GitHub repository (for example, `simvizion-ui-skill`).
2. Upload these repository-root files without an extra enclosing folder.
3. Set the default branch to `main`.
4. Create a `v1.3.0` tag after the initial release has been verified.
5. Verify installation commands point to `206airmail/simvizion-ui-skill`.
