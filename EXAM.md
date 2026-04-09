# Git & GitHub Proficiency Exam

**Rainbow IT — Internal Assessment**
**Duration:** 90 minutes
**Date:** April 9, 2026

---

## Rules

- **No direct pushes to `main`.** All changes to `main` must go through Pull Requests on GitHub.
- Use **conventional commit messages** throughout: `type(scope): description`
  - Examples: `feat(html): update header title`, `docs(readme): add project description`
  - Common types: `feat`, `fix`, `docs`, `style`, `refactor`, `chore`
- Each commit should be **atomic** — one logical change per commit.
- Use proper **branch naming conventions**: choose appropriate prefixes and descriptive names.
- Stage files **individually**. Do NOT use `git add .`

---

## Task 0 — Command Log (mandatory, ongoing)

Before you begin any git work, create a file called `COMMANDS.md` in the project root.

Throughout the exam, log **every git command** you run into this file, in order — one command per line, with an optional short comment explaining why.

**Rules for COMMANDS.md:**

- This file must **NEVER be committed**. It must remain untracked at all times.
- After the exam, submit this file to the examiner on Slack.

---

## Task 1 — Project Setup

1. Clone the repo using the URL provided by the examiner.
2. Enter the project directory.
3. Verify you are on the `main` branch.
4. Open `index.html` in a browser and confirm the page loads correctly.

*This task is not scored. It's just setup.*

---

## Task 2 — Feature: Update Header Title & Background Color

1. Create and switch to an appropriately named branch from `main`.
2. In `index.html`, change the header text from **"Rainbow IT"** to **"Rainbow IT - Team Dashboard"**.
3. Commit this change with a proper conventional commit message.
4. In `style.css`, change the body background color from `#f0f0f0` to `#e8f5e9`.
5. Commit this change separately with a proper conventional commit message.

> These must be **two separate commits** — one for the HTML change, one for the CSS change.

Do NOT open a PR for this branch yet. You will come back to it in Task 4.

---

## Task 3 — Feature: Add a New Team Member

1. Switch back to `main`.
2. Create and switch to an appropriately named branch from `main`.
3. In `app.js`, add `"Sabbir"` to the `members` array.
4. Commit with a proper conventional commit message.
5. Push the branch to the remote.
6. Open a Pull Request on GitHub into `main`.
7. Merge the PR — ensure a merge commit is created (not a squash or rebase merge).

---

## Task 4 — Rebase Workflow

1. Switch to the branch you created in Task 2.
2. Rebase it onto the updated `main` (which now includes the add-member merge from Task 3). After the rebase, your styling commits should sit on top of the latest `main`.
3. Push the branch to the remote.
4. Open a Pull Request on GitHub into `main` and merge it.

---

## Task 5 — Merge Conflict Resolution

There is a pre-existing branch in the repo called `feature/update-header-test`. This branch modifies the same header title and navbar color that you changed in Task 2.

If you try to open a PR from this branch into `main`, GitHub will report that it **cannot be automatically merged**. You must resolve the conflict locally first.

1. Check out the `feature/update-header-test` branch locally.
2. Merge `main` into it locally.
3. You **will** encounter merge conflicts. This is expected. Resolve them:
  - For the header title: keep your version from Task 2.
  - For the navbar color: keep the version from `feature/update-header-test`.
4. Stage the resolved files and commit the merge with a proper message.
5. Push the updated branch to the remote.
6. Open a Pull Request on GitHub into `main` and merge it.

---

## Task 6 — Documentation

1. Switch to `main` and pull the latest changes.
2. Create and switch to an appropriately named branch from `main`.
3. Create a `README.md` file with the following:
  - Project name: **Rainbow IT - Team Dashboard**
  - A one-line description of the project.
4. Commit with a proper conventional commit message.
5. Push the branch to the remote.
6. Open a Pull Request on GitHub into `main` and merge it.

---

## Submission

When you are done:

1. Run a command to view the full git log with graph and take a screenshot of the output.
2. Submit your `COMMANDS.md` file on Slack.
3. Notify the examiner that you are finished. The examiner will review your PRs on GitHub.

---

## Evaluation Criteria


| #   | Criteria            | Description                                                             |
| --- | ------------------- | ----------------------------------------------------------------------- |
| 1   | Branch naming       | Correct prefixes and descriptive names chosen for each task             |
| 2   | Commit messages     | Conventional format: `type(scope): description`                         |
| 3   | Atomic commits      | One logical change per commit; Task 2 must have 2 separate commits      |
| 4   | Rebase vs Merge     | Rebase used correctly in Task 4; merge commit used in Task 3            |
| 5   | PR workflow         | All merges to `main` done via Pull Requests; no direct pushes to `main` |
| 6   | Conflict resolution | Conflict resolved in the feature branch (Task 5) before opening the PR  |
| 7   | Selective staging   | `COMMANDS.md` must NOT appear in any commit                             |
| 8   | Command log         | `COMMANDS.md` is complete and submitted on Slack                        |


**Good luck!**