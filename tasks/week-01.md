# Week 01 Tasks

Goal: build shared AI and Web3 language, complete one testnet operation chain, and record a minimal AI x Web3 crossover workflow.

Last updated: 2026-05-19

## WCB Platform Sync

Last synced: 2026-05-19 via WCB Agent API read-only calls.

- Program: AI x Web3 School
- Program ID: `cmnx791nl008sru0167pzp4ki`
- Task track ID: `cmoy1hces012app01kp9ci5gb`
- API key storage: local `.env` only, ignored by Git.
- Platform writes performed: none.

Current WCB status summary:

- Submitted: 13 tasks.
- Not started: 24 tasks.
- Total tasks returned: 37.
- Points endpoint was not available through agent calls.

Important WCB IDs for remaining core work:

- AI interactive learning artifact: `cmp3jyqgx07san301erpv124n`
- Minimal smart contract interaction: `cmp3jyr3h07sgn301jpcjoma9`
- AI x Web3 minimal flowchart: `cmp3jyrc507sin301kjhy1mwf`
- Week 1 Proof-of-Work Pack: `cmp3jyrjn07skn301qopx9rwe`
- AI x Web3 learning summary: `cmp3jyrq307smn301bmk31xc2`
- Industry follow list: `cmpaouccj010hmj01515rw0qz`

## Required Tasks

### Task 01: AI Concept Cards

Status: done

WCB status: SUBMITTED

Create short concept cards for:

- LLM
- prompt
- workflow
- agent
- tool use
- AI coding

Proof:

- `notes/week-01-ai-concept-cards.md`
- Commit: `c027818 Add AI concept cards in learner voice`

Done when:

- [x] Each concept explains what it is.
- [x] Each concept explains when to use it.
- [x] Each concept includes at least one risk or limitation.

### Task 02: Learning Agent Setup

Status: done

WCB status: SUBMITTED

Record how the learning agent helped initialize this repo and which operations required human confirmation.

Proof:

- `logs/week-01-learning-agent-setup.md`
- GitHub repo link.
- Commit hash.
- Commit: `ac700cc Complete learning agent setup log`

Done when:

- [x] Repo initialized.
- [x] GitHub repo published.
- [x] Agent setup log completed.
- [x] Safety boundary written clearly.

### Task 03: AI Interactive Learning Artifact

Status: in progress

WCB status: NOT_STARTED

Create a small interactive or semi-interactive artifact about one Week 1 concept.

Recommended topic:

- Wallet, signature, transaction, and Gas lifecycle quiz.

Possible formats:

- Markdown quiz.
- Concept card page.
- CLI quiz.
- Flowchart.
- Minimal HTML page.

Proof:

- File in `demos/`.
- README note explaining what AI generated, what I reviewed, and what may be unreliable.

Current proof:

- `demos/week-01-transaction-lifecycle-quiz.md`

Done when:

- [x] Quiz draft exists.
- [x] Questions cover wallet, signature, Gas, human confirmation, and explorer verification.
- [ ] Add a short review note explaining what AI generated, what I checked, and what may still be unreliable.

### Task 04: Web3 Concept Cards

Status: done

WCB status: SUBMITTED

Create short concept cards for:

- account
- address
- wallet
- mnemonic
- private key
- signature
- transaction
- Gas
- smart contract
- testnet
- block explorer

Proof:

- `notes/week-01-web3-concept-cards.md`
- Commit: `698c1d1 Add Web3 concept cards in learner voice`

Done when:

- [x] Private key and mnemonic risks are explained.
- [x] Signature and transaction are distinguished.
- [x] Wallet confirmation and block explorer verification are connected.

### Task 05: Testnet Transaction

Status: done

WCB status: SUBMITTED

Complete one testnet transaction with a test wallet.

Proof:

- `logs/week-01-testnet-transaction.md`
- Commit: `0e75a57 Record Sepolia testnet transactions`

Record:

- [x] Testnet name.
- [x] Public wallet address.
- [x] Transaction hash.
- [x] Status.
- [x] Gas used or fee.
- [x] Block height.
- [x] Block explorer link.
- [x] Problems encountered.

Safety:

- [x] No mnemonic or private key is recorded.
- [x] No real funds are used.

Completed transactions:

- Faucet transfer: `0x905c98746fadaf7748a3ab61e97a9bc1ed860a140c248e20e983f77293ec42e8`
- OKX Wallet to MetaMask transfer: `0xf2d0538039ad29f7a12c152fe6c5044566d801c011a3c6b7fa2cf824394a8cf6`

### Task 06: Minimal Smart Contract Interaction

Status: done

WCB status: NOT_STARTED

Deploy or call one minimal smart contract on a testnet.

Recommended path:

- Use Remix first for speed.
- Use Foundry later when the basic chain is clear.

Proof:

- `logs/week-01-minimal-contract.md`

Record:

- [x] Contract source or ABI location.
- [x] Contract address.
- [x] One read result.
- [x] One write transaction hash.
- [x] Explorer link.
- [x] What wallet confirmed.

Completed proof:

- Contract: `Mytoken`
- Contract address: `0x95cCA7900A1dbA13814430a6eD4993ABbb4E951D`
- Deploy transaction: `0xec287300f40b20a0df26f1ea54e01a2b3894438f19e02576e8030e839b724810`
- Read: `_getbalance()` returned `1000000000000000000000000`
- Write: `mint(address,uint256)` transaction `0xdf8f064399d2ce71d667cf5c693037c37643a93892c8c6885e5bdff3af7ccc6e`

### Task 07: EOA, Smart Account, Multi-Sig Comparison

Status: optional

WCB status: NOT_STARTED

Compare EOA, smart account, and multi-sig from the perspective of permissions and AI automation risk.

Proof:

- `notes/week-01-account-models.md`

### Task 08: AI x Web3 Minimal Flowchart

Status: in progress

WCB status: NOT_STARTED

Draw the minimal crossover process:

AI generates -> human reviews -> wallet confirms -> chain executes -> explorer verifies -> GitHub records.

Proof:

- `demos/week-01-ai-web3-flow.md`

Must include:

- [x] Human confirmation nodes.
- [x] Failure points.
- [x] Recovery actions.
- [x] Things the Agent must not do.
- [ ] Final review and include in Week 1 proof-of-work pack.

### Task 09: Week 1 Proof-of-Work Pack

Status: todo

WCB status: NOT_STARTED

Assemble all Week 1 proof into one submission note.

Proof:

- `submissions/week-01-proof-of-work.md`

Must include:

- Repo link.
- Commit links or hashes.
- Learning agent log.
- AI concept notes.
- Web3 concept notes.
- Testnet transaction proof.
- Contract interaction proof.
- Minimal crossover flow.
- Security and privacy checklist.

### Task 10: Limited Web3 Assistant Workflow

Status: optional

WCB status: NOT_STARTED

Design a restricted Web3 assistant or small workflow.

Proof:

- `demos/week-01-limited-web3-assistant.md`

Must state:

- What it can help with.
- What it cannot do.
- Where human confirmation is mandatory.
- How logs and recovery work.

### Task 11: AI x Web3 Learning Summary

Status: todo

WCB status: NOT_STARTED

Publish a Week 1 learning summary.

Proof:

- `notes/week-01-learning-summary.md`

Suggested structure:

- What I understood.
- What I built.
- What I verified on-chain.
- What still feels unclear.
- What Week 2 should build on.

### Task 12: Industry Follow List

Status: optional

WCB status: NOT_STARTED

Build a small AI x Web3 information source list.

Proof:

- `resources.md`

Record:

- 5 to 10 people, projects, or sources.
- Why they matter.
- What I want to learn from them.
