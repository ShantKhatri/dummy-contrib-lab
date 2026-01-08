# Contributing Guidelines

Failure to follow these guidelines may result in your Pull Request being closed without review.

## Contribution Workflow

This section guides you through the process of contributing to this project via a Pull Request.

### 1. Fork the Repository
First, fork the repository to your own GitHub account. This creates a copy of the repository under your user.
*   Go to the main project repository on GitHub.
*   Click the "Fork" button in the top right corner.

### 2. Clone Your Fork
Clone your forked repository to your local machine:
```bash
git clone https://github.com/YOUR_USERNAME/PROJECT_NAME.git
cd PROJECT_NAME
```
Replace `YOUR_USERNAME` and `PROJECT_NAME` with your GitHub username and the repository name.

### 3. Keep Your Fork Up-to-Date
Before creating a new branch, sync your local `main` branch with the upstream `main` branch to ensure you have the latest changes:
```bash
git remote add upstream https://github.com/ORIGINAL_OWNER/PROJECT_NAME.git
git checkout main
git pull upstream main
git push origin main
```

### 4. Create a New Branch
Always create a new branch for your changes. This keeps your work organized and isolated. Use a descriptive branch name following the "Branch Naming" guidelines below.
```bash
git checkout -b feat/your-feature-name main
# Or for a bug fix:
# git checkout -b fix/issue-description main
```

### 5. Open an Issue (Recommended)
Before starting significant work, it's highly recommended to open an issue to discuss your proposed changes. This helps ensure your contribution aligns with the project goals and avoids duplicate efforts.

### 6. Make Your Changes
Implement your changes on your new branch.

### 7. Commit Your Changes
Commit your changes with clear, descriptive commit messages following the "Commit Messages" guidelines. Aim for a single logical commit per PR if possible, or squash multiple related commits before opening the PR.
```bash
git add .
git commit -m "feat: add amazing new feature"
```

### 8. Push to Your Fork
Push your local branch to your forked repository on GitHub:
```bash
git push origin feat/your-feature-name
```

### 9. Open a Pull Request (PR)
Once your changes are pushed:
*   Go to your forked repository on GitHub.
*   You should see a prompt to "Compare & pull request" from your newly pushed branch.
*   Click that button or navigate to the "Pull requests" tab and click "New pull request".
*   **Fill out the PR template completely:** Provide a clear title, a detailed description of your changes, and reference any related issues (e.g., "Closes #123" or "Fixes #456").
*   Ensure your PR addresses a single logical change.

### 10. PR Review and Merge
*   Project maintainers will review your PR. They may ask for changes or clarifications.
*   Respond to comments promptly and make requested changes.
*   Once approved, your PR will be merged into the `main` branch.

## Branch Naming
- feat/<short-description>
- fix/<short-description>
- docs/<short-description>

Examples:
- feat/update-readme
- fix/typo-placeholder

## Commit Messages
Use Conventional Commits:

- feat: add new feature
- fix: fix a bug
- docs: documentation only changes
- chore: maintenance tasks

## Good example:
docs: improve README clarity


## Commit History
- Squash commits if needed
- One PR = one logical change

## Pull Requests
- Must reference an Issue
- Must fill out the PR template completely
- Vague descriptions will result in closure

## Communication
- Do not ask "Can I work on this?"
- Do not ask questions already answered in docs
- Be precise and respectful of reviewer time
