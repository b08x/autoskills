```markdown
# autoskills Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns used in the `autoskills` repository, a TypeScript project built with the Astro framework. You'll learn about file naming, import/export styles, commit conventions, and the main workflows for dependency management and pull request merges. This guide also covers the project's approach to testing and provides handy commands for common tasks.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `skillsMap.ts`, `skillsRegistry.ts`

### Import Style
- Use **relative imports** for modules within the project.
  - Example:
    ```typescript
    import { getSkill } from './skillsRegistry';
    ```

### Export Style
- Use **named exports** rather than default exports.
  - Example:
    ```typescript
    // skillsRegistry.ts
    export function getSkill(name: string) { ... }
    ```

### Commit Patterns
- Commit messages use prefixes such as `feat` and `chore`.
- Average commit message length is around 56 characters.
  - Example: `feat: add ElysiaJS skill to registry`

## Workflows

### Dependency Update
**Trigger:** When a dependency needs to be updated (often via Dependabot or manually)  
**Command:** `/update-dependency`

1. Update the version of the dependency in `package.json`.
2. Regenerate or update `pnpm-lock.yaml` to reflect the new dependency version.
3. Commit both files with a message indicating the dependency change.
   - Example commit message: `chore: bump astro to v3.0.0`

**Files involved:**
- `package.json`
- `pnpm-lock.yaml`

### Merge Feature or Dependency PR
**Trigger:** When a pull request for a new feature or dependency update is approved and ready to merge  
**Command:** `/merge-pr`

1. Merge the pull request branch into `main`.
2. Ensure all file changes from the feature or dependency branch are applied.
3. Commit with a merge message referencing the PR.
   - Example commit message: `feat: merge PR #42 - add ElysiaJS skill`

**Files commonly involved:**
- `src/pages/index.astro`
- `package.json`
- `pnpm-lock.yaml`
- `packages/autoskills/skills-map.ts`
- `packages/autoskills/skills-registry/elysiajs/SKILL.md`
- `packages/autoskills/skills-registry/index.json`
- `src/icons/elysia.svg`

## Testing Patterns

- Test files follow the pattern `*.test.*` (e.g., `skillsRegistry.test.ts`).
- The specific testing framework is not specified, but tests are colocated with source files or in parallel directories.
- Example test file name: `skillsMap.test.ts`

## Commands

| Command           | Purpose                                                   |
|-------------------|-----------------------------------------------------------|
| /update-dependency| Update dependencies and sync lockfile                     |
| /merge-pr         | Merge an approved feature or dependency pull request      |
```
