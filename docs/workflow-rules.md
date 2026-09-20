# Git Workflow & Collaboration Rules

This document outlines the version control standards, branching models, and pull request guidelines enforced in this repository.

---

## 1. Branching Strategy

We follow a feature-branch workflow to maintain a clean and stable `main` branch.

### Branch Naming Conventions
- **New Features:** `feature/short-description` (e.g., `feature/add-git-cheatsheet`)
- **Bug Fixes:** `fix/issue-description` (e.g., `fix/typo-in-readme`)
- **Documentation:** `docs/topic-name` (e.g., `docs/workflow-rules`)
- **Maintenance/Refactoring:** `chore/task-name` (e.g., `chore/update-ci-pipeline`)

---

## 2. Commit Guidelines

We enforce **Conventional Commits** to keep our project history clean and readable.

### Format
`type(scope): concise description in lower case`

### Common Types
- `feat`: A new feature or document
- `fix`: A bug fix or error correction
- `docs`: Documentation-only changes
- `chore`: Maintenance tasks, config changes, or non-code updates

### Rules
1. Keep commits **atomic** (one logical change per commit).
2. Write present-tense, imperative commit messages (e.g., "add workflow guide" instead of "added workflow guide").

---

## 3. Pull Request (PR) Process

Direct pushes to the `main` branch are strictly prohibited. All changes must arrive via Pull Requests.

### Submission Steps
1. **Create a Branch:** Cut a new branch off the latest `main`.
2. **Make & Commit Changes:** Follow the commit guidelines above.
3. **Open a PR:** Fill out the automated `PULL_REQUEST_TEMPLATE.md`.
4. **Peer Review:** Assign at least one collaborator to review the code.
5. **Address Feedback:** Push fix commits directly to the feature branch.
6. **Merge:** Use **Squash and Merge** or **Rebase and Merge** to maintain a linear history on `main`.

---

## 4. Conflict Resolution

When merge conflicts occur:
1. Pull the latest `main` into your local feature branch.
2. Resolve conflicts manually inside your editor (Zed / VS Code).
3. Verify changes locally before committing the conflict resolution.
4. Push the resolved branch back to GitHub to update the PR.
