# Week 1 AI Concept Cards

Status: draft

## LLM

What it is:

- A large language model predicts likely next tokens from the context it can see.
- It is strong at language understanding, code generation, summarization, and rough reasoning.

When to use:

- Explaining concepts.
- Drafting code or notes.
- Summarizing documents.
- Turning messy thoughts into structure.

Risk:

- It can confidently invent facts, links, APIs, or references.
- Important facts must be verified with external sources or actual execution.

## Prompt

What it is:

- A prompt is the current task instruction given to the model.
- It tells the model what role to play, what output to produce, and what constraints to follow.

When to use:

- One-off explanations.
- Drafting notes.
- Generating checklists.
- Asking the model to transform or critique content.

Risk:

- A prompt alone does not create reliable execution.
- If the task needs state, tools, logs, or verification, a prompt is not enough.

## Workflow

What it is:

- A workflow is a predefined process with fixed steps.
- The model may be one node in the process, but the route is mostly designed by humans.

When to use:

- Repeatable tasks.
- Course note generation.
- Proof-of-work packaging.
- Data cleaning with fixed steps.

Risk:

- It can be too rigid when the next step depends on unknown intermediate results.

## Agent

What it is:

- An Agent uses a model to plan, choose tools, observe results, and decide the next action across multiple steps.

When to use:

- Open-ended tasks.
- Multi-tool tasks.
- Tasks where intermediate results decide the next step.
- Long-running learning or research workflows.

Risk:

- More autonomy means more risk.
- Agents need guardrails, tracing, state management, and human confirmation for sensitive actions.

## Tool Use

What it is:

- Tool use lets a model call external functions, APIs, browsers, files, terminals, or other systems.

When to use:

- Fetching current data.
- Running tests.
- Reading files.
- Calling APIs.
- Updating a repo.

Risk:

- Wrong tool, wrong parameters, or wrong target can cause bad outputs or unsafe actions.
- High-risk actions need human confirmation.

## AI Coding

What it is:

- AI coding tools help read code, generate code, explain libraries, run commands, and maintain a repo.

When to use:

- Learning unfamiliar code.
- Creating prototypes.
- Writing boilerplate.
- Debugging errors.

Risk:

- The model can produce code that runs but is insecure, brittle, or conceptually wrong.
- Human review, tests, and small commits are still required.

## My Current Understanding

- Prompt is best for asking.
- Workflow is best for fixed processes.
- Agent is best when the path depends on tool results.
- The closer AI gets to execution, the more I need logs, verification, permissions, and human confirmation.

