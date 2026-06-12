---
name: dependency-update
description: Workflow command scaffold for dependency-update in autoskills.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /dependency-update

Use this workflow when working on **dependency-update** in `autoskills`.

## Goal

Updates one or more dependencies to a new version, ensuring the lockfile is in sync.

## Common Files

- `package.json`
- `pnpm-lock.yaml`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Update the version of a dependency in package.json
- Regenerate or update pnpm-lock.yaml to reflect the new dependency version
- Commit both files with a message indicating the dependency change

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.