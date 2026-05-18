# Week 1 Learning Agent Setup Log

Status: draft

## Tool Path

Primary learning agent tool:

- Codex in the local workspace.

GitHub repo:

- https://github.com/dylan070620/ai-web3-school-cohort-0

## What The Agent Helped With

- Read the AI x Web3 School Learning Agent prompt.
- Align the repo structure with the Handbook and course goals.
- Generate initial files:
  - `README.md`
  - `profile.md`
  - `learning-plan.md`
  - `daily/`
  - `tasks/`
  - `handbook-feedback/`
  - `submissions/`
- Update Week 1 tasks based on the course schedule.
- Clean up old future-facing folders and API/private-key templates after review.

## What Required Human Confirmation

- Writing the first repo files.
- Running `git init`.
- Creating the GitHub repository.
- Adding `origin`.
- Pushing `main` to GitHub.

## Commit Proof

- Initial commit: `4cdd1e8 Initialize AI Web3 School learning repository`
- Week 1 plan update: `28698d5 Update Week 1 course-aligned learning plan`

Note:

- The Week 1 cleanup commit should remove old secret placeholder files, old templates, old generic experiment folders, and Hackathon placeholders from the public repo.

## Safety Boundaries

The Agent should not:

- See or store private keys.
- See or store mnemonics.
- Auto-sign wallet messages.
- Auto-send transactions.
- Auto-approve token allowances.
- Push public changes without review.

The Agent may help:

- Draft notes.
- Generate checklists.
- Explain concepts.
- Prepare commands.
- Review public transaction data.
- Organize proof-of-work.

## Reflection

The useful pattern is not "let AI do everything." The useful pattern is:

AI drafts -> I review -> I approve sensitive actions -> I verify output -> I record proof.
