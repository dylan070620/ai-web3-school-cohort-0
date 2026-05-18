# LLM API Experiments

Use this folder for first LLM API calls and prompt experiments.

## First Experiment

Goal:

- Send one prompt to an LLM API from Python.
- Receive a response.
- Print a short result.

## Safety

- Put real keys in `.env` only.
- Commit `.env.example`, not `.env`.
- Do not paste API keys into daily notes.

## Agent Bridge

After the first API call works, evolve it into:

1. A function that accepts a question.
2. A tool that loads on-chain data.
3. A small Agent loop that decides when to call the tool.

