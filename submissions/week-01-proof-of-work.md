# Week 1｜Proof-of-Work Pack

Status: final

## Repo

- Main learning repo: https://github.com/dylan070620/ai-web3-school-cohort-0
- Restricted Web3 assistant repo: https://github.com/dylan070620/bootcamp-proof-generator_dz
- Restricted Web3 assistant live demo: https://bootcamp-proof-generator-dz.vercel.app

## What I Completed This Week

This week I moved from scattered AI / Web3 knowledge into a more complete learning workflow:

1. Set up a public GitHub learning repo.
2. Used Codex as my learning agent to plan, record, and review Week 1 work.
3. Wrote AI concept cards in my own words.
4. Wrote Web3 concept cards in my own words.
5. Completed real Sepolia testnet transactions.
6. Deployed and interacted with my own ERC20 contract on Sepolia.
7. Built an interactive transaction lifecycle quiz.
8. Compared EOA, smart accounts, and multi-sig accounts.
9. Designed and deployed a restricted Web3 assistant: Bootcamp Proof Generator.
10. Recorded security boundaries for AI agent + Web3 workflows.

## Proof Index

| Area | Proof |
| --- | --- |
| Learning repo | [README](../README.md) |
| Personal plan | [learning-plan.md](../learning-plan.md) |
| Learning agent setup | [week-01-learning-agent-setup.md](../logs/week-01-learning-agent-setup.md) |
| AI concept cards | [week-01-ai-concept-cards.md](../notes/week-01-ai-concept-cards.md) |
| Web3 concept cards | [week-01-web3-concept-cards.md](../notes/week-01-web3-concept-cards.md) |
| Testnet transaction | [week-01-testnet-transaction.md](../logs/week-01-testnet-transaction.md) |
| Minimal smart contract interaction | [week-01-minimal-contract.md](../logs/week-01-minimal-contract.md) |
| Transaction lifecycle quiz | [week-01-transaction-lifecycle-quiz.md](../demos/week-01-transaction-lifecycle-quiz.md) |
| EOA / smart account / multi-sig comparison | [week-01-account-models.md](../notes/week-01-account-models.md) |
| AI x Web3 minimal flow | [week-01-ai-web3-flow.md](../demos/week-01-ai-web3-flow.md) |
| Restricted Web3 assistant workflow | [week-01-limited-web3-assistant.md](../demos/week-01-limited-web3-assistant.md) |
| Daily log 2026-05-20 | [2026-05-20.md](../daily/2026-05-20.md) |
| Daily log 2026-05-21 | [2026-05-21.md](../daily/2026-05-21.md) |

## Commit Proof

- `c027818` Add AI concept cards in learner voice
- `698c1d1` Add Web3 concept cards in learner voice
- `0e75a57` Record Sepolia testnet transactions
- `ac700cc` Complete learning agent setup log
- `4d24036` Record minimal ERC20 contract interaction
- `432b333` Complete transaction lifecycle quiz artifact
- `5c8974b` Add May 20 daily learning log
- `14e7a52` Add account model comparison notes
- `9bd106b` Add May 21 daily learning log
- `b8bcd79` Add AI Web3 proof generator flow
- `d875759` Record limited Web3 assistant workflow

## Learning Agent

- Tool used: Codex
- Main role: planning, repo maintenance, note organization, concept review, proof drafting, safety checklist generation.
- Setup proof: [week-01-learning-agent-setup.md](../logs/week-01-learning-agent-setup.md)

What AI helped with:

- Turned Week 1 requirements into a learning plan and task tracker.
- Helped ask me questions so I could explain concepts in my own words.
- Helped organize my answers into bilingual notes.
- Helped structure proof records and markdown submissions.
- Helped check that no private key, mnemonic, API key, `.env`, or sensitive secret was committed.

What required human confirmation:

- GitHub repo creation and pushes.
- Wallet confirmations.
- Sepolia transaction sending.
- ERC20 deployment.
- ERC20 mint transaction.
- WCB submissions.
- Any action involving signatures, authorization, transfers, contract writes, or public publishing.

## AI Basics

Proof: [week-01-ai-concept-cards.md](../notes/week-01-ai-concept-cards.md)

Concepts covered:

- LLM
- Prompt
- Workflow
- Agent
- Tool use
- AI coding

My main understanding:

An LLM is good at generating likely text from context, but it is not a reliable source of truth by itself. Prompting can guide one response, workflow can organize fixed steps, and an agent can plan and use tools across steps. The closer AI gets to execution, the more important guardrails, logs, verification, and human confirmation become.

## Web3 Basics

Proof: [week-01-web3-concept-cards.md](../notes/week-01-web3-concept-cards.md)

Concepts covered:

- Account
- Address
- Wallet
- Mnemonic
- Private key
- Signature
- Transaction
- Gas
- Smart contract
- Testnet
- Block explorer

My main understanding:

A wallet is not just a login account. It manages keys and gives the user an interface to sign, send transactions, and interact with contracts. Private keys and mnemonics must never be exposed. Transaction hashes and block explorers are the basic way to verify what actually happened on-chain.

## Testnet Transaction Proof

Proof: [week-01-testnet-transaction.md](../logs/week-01-testnet-transaction.md)

Network: Sepolia

Completed transactions:

- Faucet transaction: `0x905c98746fadaf7748a3ab61e97a9bc1ed860a140c248e20e983f77293ec42e8`
- OKX Wallet to MetaMask transfer: `0xf2d0538039ad29f7a12c152fe6c5044566d801c011a3c6b7fa2cf824394a8cf6`

Explorer links:

- https://sepolia.etherscan.io/tx/0x905c98746fadaf7748a3ab61e97a9bc1ed860a140c248e20e983f77293ec42e8
- https://sepolia.etherscan.io/tx/0xf2d0538039ad29f7a12c152fe6c5044566d801c011a3c6b7fa2cf824394a8cf6

What I learned:

- A transaction has a sender, receiver, value, status, gas, block number, and transaction hash.
- The explorer is the source I should check instead of trusting only wallet UI or AI summaries.
- Wallet actions must be manually reviewed before confirmation.

## Smart Contract Interaction Proof

Proof: [week-01-minimal-contract.md](../logs/week-01-minimal-contract.md)

Network: Sepolia

Contract:

- Contract name: `Mytoken`
- Token name: `BoWei Token`
- Symbol: `BVB`
- Contract address: `0x95cCA7900A1dbA13814430a6eD4993ABbb4E951D`
- Deploy transaction: `0xec287300f40b20a0df26f1ea54e01a2b3894438f19e02576e8030e839b724810`
- Mint transaction: `0xdf8f064399d2ce71d667cf5c693037c37643a93892c8c6885e5bdff3af7ccc6e`

Explorer links:

- Contract: https://sepolia.etherscan.io/address/0x95cCA7900A1dbA13814430a6eD4993ABbb4E951D
- Deploy tx: https://sepolia.etherscan.io/tx/0xec287300f40b20a0df26f1ea54e01a2b3894438f19e02576e8030e839b724810
- Mint tx: https://sepolia.etherscan.io/tx/0xdf8f064399d2ce71d667cf5c693037c37643a93892c8c6885e5bdff3af7ccc6e

Read interaction:

- Function: `_getbalance()`
- Result: `1000000000000000000000000`
- Human-readable result: `1,000,000 BVB`

Write interaction:

- Function: `mint(address,uint256)`
- Amount: `1000000000000000000`
- Human-readable amount: `1 BVB`
- This required manual wallet confirmation and gas.

What I learned:

- A read call does not change chain state.
- A write transaction changes chain state and requires wallet confirmation.
- Contract deployment is also an on-chain transaction.
- Logs and events help verify what happened.

## AI Interactive Learning Artifact

Proof: [week-01-transaction-lifecycle-quiz.md](../demos/week-01-transaction-lifecycle-quiz.md)

Artifact: Transaction Lifecycle Quiz

It helps a learner review:

- Wallet control
- Signature risk
- Gas
- Human confirmation
- Transaction hash
- Block explorer verification
- Read call vs write transaction
- AI agent safety boundary

AI helped draft the quiz structure, but I reviewed it against my own Sepolia transfer and ERC20 interaction records.

## Account Model Comparison

Proof: [week-01-account-models.md](../notes/week-01-account-models.md)

Compared:

- EOA
- Smart account
- Multi-sig account

My main understanding:

EOA is like one person holding one key. Smart account is like a wallet with rules. Multi-sig is like a team vault. For AI x Web3, the important question is not only whether AI can execute, but who defines the permission boundary and which changes must be manually confirmed.

My current safety model:

**Low-risk execution can be automated inside predefined limits, but permission-boundary changes must be manually confirmed.**

## AI x Web3 Minimal Crossover

Proof: [week-01-ai-web3-flow.md](../demos/week-01-ai-web3-flow.md)

Project idea: Bootcamp Proof Generator

Workflow:

1. User selects network.
2. User enters tx hash.
3. App reads public transaction data.
4. App reads transaction receipt.
5. App explains the transaction in plain language.
6. App generates copyable markdown proof.
7. User reviews explorer link and proof.
8. User submits proof manually.

Safety boundary:

- No wallet connection.
- No private key.
- No mnemonic.
- No signing.
- No authorization.
- No transaction sending.
- No invented tx hash, explorer link, or chain data.

## Restricted Web3 Assistant

Proof: [week-01-limited-web3-assistant.md](../demos/week-01-limited-web3-assistant.md)

Live demo: https://bootcamp-proof-generator-dz.vercel.app

Repo: https://github.com/dylan070620/bootcamp-proof-generator_dz

What it does:

- Reads public testnet transaction data.
- Explains transaction status and details.
- Generates bootcamp proof markdown.

What it does not do:

- It does not connect to a wallet.
- It does not request private keys or mnemonics.
- It does not sign transactions.
- It does not send transactions.
- It does not change on-chain state.

Why this matters:

This is a safer first step for AI x Web3. Instead of giving an agent execution power, I built a read-only assistant that helps users understand and verify public on-chain data.

## Security And Privacy Checklist

- [x] No private key included.
- [x] No mnemonic included.
- [x] No real API key included.
- [x] No `.env` file included.
- [x] No sensitive screenshots included.
- [x] Wallet actions were manually confirmed.
- [x] Contract writes were manually confirmed.
- [x] WCB writes require manual confirmation.
- [x] Explorer links were checked on the correct network.
- [x] AI outputs were reviewed against actual chain data.
- [x] Public repo only contains safe learning proof.

## Week 1 Reflection

What I understand now:

- LLMs are useful for explanation, drafting, and coding help, but their outputs must be verified.
- A workflow is more reliable than a loose prompt when the task has fixed steps.
- Agents become risky when they move from explanation into execution.
- Wallets, signatures, transactions, gas, contracts, and explorers form one chain of on-chain action and verification.
- AI x Web3 needs strong permission boundaries.

What I built:

- A learning repo.
- AI and Web3 concept cards.
- A transaction lifecycle quiz.
- A Sepolia ERC20 deployment and interaction record.
- An account model comparison note.
- A Bootcamp Proof Generator design.
- A deployed read-only Bootcamp Proof Generator prototype.

What I verified on-chain:

- A Sepolia faucet transfer.
- A Sepolia wallet transfer.
- An ERC20 contract deployment.
- An ERC20 read call.
- An ERC20 mint transaction.

What still feels unclear:

- How to use Foundry for a full deploy workflow.
- How to design safe session keys and account abstraction rules.
- How to make AI-generated transaction explanations more reliable.
- How to verify complex contract calls beyond basic receipt fields.

What I want to learn in Week 2:

- More practical wallet and payment flows.
- Safer agent permission design.
- Better chain data parsing.
- How to connect a restricted assistant to real user workflows without giving it dangerous permissions.

## Final Submission Link

Recommended WCB submission link:

https://github.com/dylan070620/ai-web3-school-cohort-0/blob/main/submissions/week-01-proof-of-work.md
