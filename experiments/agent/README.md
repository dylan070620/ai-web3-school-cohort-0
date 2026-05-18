# Agent Experiments

Use this folder to build from a simple LLM call toward a tool-using Agent.

## Minimal Agent Shape

- Goal: what the Agent is trying to do.
- Input: user question or wallet address.
- Tools: functions the Agent can call.
- Reasoning loop: decide, call tool, observe, respond.
- Output: concise analysis.

## First Agent Idea

Wallet activity analyst:

1. User enters a public wallet address.
2. Tool fetches recent transactions.
3. Python structures the data.
4. LLM summarizes behavior.
5. Agent returns beginner-friendly insights and caveats.

## Safety

- Do not analyze private wallets without consent.
- Use public test data while learning.
- Redact addresses in public notes if needed.

