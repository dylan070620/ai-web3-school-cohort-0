# GitHub Setup

This repository is intended to become a public GitHub learning repo named:

`ai-web3-school-cohort-0`

## Current Status

- Local files are initialized.
- Local git repository is not initialized yet unless done manually later.
- GitHub remote is not created.
- GitHub CLI `gh` is not available in this terminal.

## Manual Confirmation Required

Before each of these operations, the learner must confirm:

- `git init`
- `git add`
- `git commit`
- GitHub repo creation
- Remote setup
- Push to GitHub

## If Using GitHub CLI Later

Suggested flow after `gh` is installed and logged in:

```bash
gh auth login
gh repo create ai-web3-school-cohort-0 --public --source=. --remote=origin
git add .
git commit -m "Initialize AI Web3 School learning repository"
git push -u origin main
```

Do not run these commands until the current repo contents are reviewed.

