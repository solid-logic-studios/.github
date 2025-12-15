# Contributing to Solid Logic Studios

Welcome to the team. This document outlines the engineering standards and workflows for all Solid Logic Studios repositories.

As we are building a foundation for a future consultancy, we treat every commit as if it is for a paying client.

## 1. Core Engineering Principles
All code submitted to this organization must adhere to our core philosophies:
* **SOLID:** Apply the 5 principles. If a class is doing too much, break it down.
* **DRY:** distinct functionality should exist in exactly one place. Abstract reusable logic into utilities or hooks.
* **Type Safety:** `any` is strictly forbidden. Use proper interfaces and types.

## 2. Git Workflow
We use a **Feature Branch** workflow. Direct commits to `main` are forbidden (except for simple documentation updates).

### Branch Naming Convention
Branches must be named with a prefix describing the type of change:
* `feat/short-description` (New features)
* `fix/short-description` (Bug fixes)
* `refactor/short-description` (Code restructuring without behavior changes)
* `chore/short-description` (Build tasks, dependency updates)
* `docs/short-description` (Documentation only)

**Example:** `feat/add-squash-scoring-logic`

### Commit Messages
We follow **Conventional Commits** to automate changelogs in the future.
Format: `<type>: <description>`

* `feat: allow user to update profile picture`
* `fix: resolve api timeout on heavy load`
* `style: format code with prettier`

## 3. Pull Request (PR) Process
Since we are on the GitHub Free Tier, we rely on the **Honor System** for code reviews.

1.  **Draft PRs:** Open a PR as "Draft" if you want early feedback.
2.  **Ready for Review:** Mark as "Ready" only when:
    * Linting passes locally.
    * You have self-reviewed the code.
    * Relevant tests are added/updated.
3.  **The "Review" Rule:** Do not merge your own PR until the other person has commented with a "LGTM" (Looks Good To Me) or an official Approval.
4.  **Squash & Merge:** When merging, use "Squash and Merge" to keep the `main` history clean.

## 4. Coding Standards (TypeScript/Node)
* **Async/Await:** Prefer `async/await` over `.then()` chains.
* **Variables:** Use `const` by default. Use `let` only when reassignment is necessary. Never use `var`.
* **Naming:**
    * `camelCase` for variables and functions.
    * `PascalCase` for Classes, Interfaces, and React Components.
    * `UPPER_SNAKE_CASE` for constants.

## 5. Definition of Done
A feature is considered "Done" when:
1.  Logic is implemented.
2.  Code respects SOLID/DRY principles.
3.  No linting errors.
