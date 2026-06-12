---
name: merge-feature-or-dependency-pr
description: Workflow command scaffold for merge-feature-or-dependency-pr in autoskills.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /merge-feature-or-dependency-pr

Use this workflow when working on **merge-feature-or-dependency-pr** in `autoskills`.

## Goal

Merges a pull request for a new feature or dependency update, often repeating the changes from the source branch.

## Common Files

- `src/pages/index.astro`
- `package.json`
- `pnpm-lock.yaml`
- `packages/autoskills/skills-map.ts`
- `packages/autoskills/skills-registry/elysiajs/SKILL.md`
- `packages/autoskills/skills-registry/index.json`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Merge the pull request branch into main
- Apply the same file changes as in the original feature or dependency branch
- Commit with a merge message referencing the PR

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.