# Week 1 Demo: Transaction Lifecycle Quiz

Status: done

## Purpose

This is a minimal interactive learning artifact for Week 1.

It helps a beginner review the basic lifecycle of a Web3 transaction:

1. A wallet prepares a signature or transaction.
2. The human reviews the wallet details.
3. The transaction is signed and broadcast.
4. The chain executes the transaction.
5. The result is verified with a block explorer.

The demo is written as a Markdown quiz. A learner can answer each question before opening the reference answer. This is not a production app, but it is interactive enough for learning because it accepts the learner's own answer and compares it with a reviewed explanation.

## How To Use

1. Read one question.
2. Write your own answer in the `My answer` field.
3. Compare it with the `Reference answer`.
4. Use the `Check` section to decide whether your answer is complete.
5. If your answer is incomplete, rewrite it in your own words.

## Example Interaction

Input from learner:

```text
My answer: A transaction hash is like the ID of a transaction. I can use it to check whether the transaction succeeded.
```

Output / feedback:

```text
Good. Add one more point: the block explorer can also show status, block height, Gas, timestamp, from/to address, and logs.
```

## Quiz

### 1. What does a wallet mainly control?

A. A normal username and password.

B. Private keys and signing authority.

C. The block explorer database.

My answer:

```text

```

Reference answer:

- B.
- A wallet mainly manages private keys and provides an interface for signing messages, sending transactions, and interacting with dApps.
- The wallet itself is not the account. The account is controlled by the private key.

Check:

- Did you mention private keys?
- Did you mention signing or transaction authority?
- Did you avoid writing any real private key or mnemonic?

### 2. Is a signature always harmless?

A. Yes, it is just login.

B. No, it may authorize a specific message, permission, or action.

My answer:

```text

```

Reference answer:

- B.
- A signature is not just "clicking login". It proves control of an address or authorizes a specific message/action.
- In Web3, a user must read what the wallet asks them to sign.

Check:

- Did you distinguish normal login-style signing from higher-risk authorization?
- Did you mention human review before signing?

### 3. What does Gas pay for?

A. On-chain computation and transaction execution resources.

B. A monthly wallet subscription.

C. The price of the token being transferred.

My answer:

```text

```

Reference answer:

- A.
- Gas pays for computation and storage changes executed by the network.
- A failed transaction can still consume Gas because validators still executed or attempted the computation.

Check:

- Did you explain Gas as execution cost?
- Did you avoid confusing Gas with token price?

### 4. What should happen before a transaction is signed?

A. AI should approve it automatically.

B. The human should review the wallet details and confirm intentionally.

My answer:

```text

```

Reference answer:

- B.
- The human should check the network, contract or recipient address, action type, estimated fee, and expected result.
- AI can help explain the operation, but AI should not auto-confirm wallet actions.

Check:

- Did you mention network?
- Did you mention address or contract?
- Did you mention that the human must confirm?

### 5. What proves whether a transaction succeeded?

A. The model says it probably worked.

B. The block explorer shows status, block height, Gas, and transaction details.

My answer:

```text

```

Reference answer:

- B.
- A transaction hash is the public identifier used to look up a transaction.
- The block explorer can show status, block height, timestamp, Gas, from/to address, contract logs, and event data.

Check:

- Did you mention transaction hash?
- Did you mention explorer verification?
- Did you mention status or block height?

### 6. What is the difference between a read call and a write transaction?

My answer:

```text

```

Reference answer:

- A read call only reads current chain state and does not change the blockchain.
- A write transaction changes chain state, needs wallet confirmation, is broadcast to the network, and costs Gas.
- In my ERC20 task, `_getbalance()` was a read call, while `mint(address,uint256)` was a write transaction.

Check:

- Did you mention state change?
- Did you mention Gas and wallet confirmation for write transactions?

### 7. In my Sepolia ERC20 task, why did `mint(address,uint256)` need confirmation?

My answer:

```text

```

Reference answer:

- `mint(address,uint256)` changed the token balance on-chain.
- It emitted an ERC20 `Transfer` event from the zero address.
- Because it changed contract state, MetaMask asked for manual confirmation and estimated a network fee.

Check:

- Did you explain that mint changes token supply or balance?
- Did you mention wallet confirmation?
- Did you mention that the result can be checked with the transaction hash?

### 8. What should an AI agent never do in this transaction lifecycle?

My answer:

```text

```

Reference answer:

- It should not store or request private keys, mnemonics, or real API keys.
- It should not auto-sign wallet messages.
- It should not auto-send transactions or approve token permissions.
- It should not hide wallet details from the user.

Check:

- Did you mention private key or mnemonic safety?
- Did you mention human-in-the-loop confirmation?

## Real Week 1 Evidence Used

This quiz was reviewed against my own Week 1 Sepolia practice:

- Faucet transaction: `0x905c98746fadaf7748a3ab61e97a9bc1ed860a140c248e20e983f77293ec42e8`
- OKX Wallet to MetaMask transaction: `0xf2d0538039ad29f7a12c152fe6c5044566d801c011a3c6b7fa2cf824394a8cf6`
- ERC20 contract address: `0x95cCA7900A1dbA13814430a6eD4993ABbb4E951D`
- Deploy transaction: `0xec287300f40b20a0df26f1ea54e01a2b3894438f19e02576e8030e839b724810`
- Mint transaction: `0xdf8f064399d2ce71d667cf5c693037c37643a93892c8c6885e5bdff3af7ccc6e`

## What AI Helped With

- AI helped turn the Week 1 Web3 concepts into quiz questions.
- AI helped generate reference answers and checklists.
- AI helped connect the quiz to my real Sepolia transaction and contract interaction records.

## What I Reviewed Or Modified

- I chose the topic based on my own learning path: wallet, signature, Gas, transaction hash, read call, write transaction, and explorer verification.
- I verified the examples against my own Sepolia records.
- I kept private keys, mnemonics, API keys, and wallet secrets out of this file.
- I confirmed that wallet signing and contract writes must remain human-confirmed.

## Limits

- This is a Markdown-based learning artifact, not a real dApp or wallet security tool.
- It does not connect to a live LLM API.
- The reference answers are learning notes, not legal, financial, or security advice.
- Before any mainnet operation, the user should verify details through wallet UI, official docs, and block explorers.

## Reflection

中文：这个小 quiz 帮我把今天的测试网交易和合约部署串成了一条学习流程。我现在能区分 read call 和 write transaction，也知道交易哈希、Gas、区块浏览器和人工确认各自的作用。AI 可以帮我整理题目和解释，但涉及钱包、签名、转账、授权和合约写入时，最终确认必须由人完成。

English: This small quiz helped me connect my testnet transfer and contract deployment into one learning flow. I can now distinguish read calls from write transactions, and I understand the roles of transaction hashes, Gas, block explorers, and manual confirmation. AI can help draft questions and explanations, but wallet signatures, transfers, approvals, and contract writes must remain human-confirmed.
