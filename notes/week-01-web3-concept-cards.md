# Week 1 Web3 Concept Cards

Status: draft

## Account

An account is an entity on-chain that can hold assets and interact with contracts. In Ethereum-like systems, common account types include EOAs and smart contract accounts.

Risk:

- Control of an account depends on private keys or contract permissions.

## Address

An address is the public identifier used to receive assets and interact on-chain.

Risk:

- Addresses are public and traceable. They are not the same as true anonymity.

## Wallet

A wallet is the user-facing tool for managing keys, viewing assets, signing messages, and sending transactions.

Risk:

- A wallet is not just a login app. It is the control surface for on-chain assets and permissions.

## Mnemonic

A mnemonic, or seed phrase, can recover wallet keys.

Risk:

- Never upload, screenshot, paste, or commit a mnemonic.

## Private Key

A private key controls signing for an account.

Risk:

- Whoever has the private key can control the account.
- AI Agents should never receive private keys.

## Signature

A signature proves that the account owner approved a specific message or action.

Risk:

- Signing is not harmless. A signature may authorize login, orders, approvals, or other actions depending on the message.

## Transaction

A transaction is a signed on-chain action, such as sending ETH, deploying a contract, or calling a contract write function.

Risk:

- Transactions cost Gas and can fail.
- Once confirmed, they are usually irreversible.

## Gas

Gas is the cost mechanism for chain execution. It prices computation, storage, and transaction inclusion.

Risk:

- Failed transactions can still consume Gas.

## Smart Contract

A smart contract is code deployed on-chain. It has public state and executes according to chain rules.

Risk:

- Contract logic is public.
- Upgrade permissions and admin roles matter.
- Some contracts cannot be changed after deployment.

## Testnet

A testnet is a practice network for learning and experimentation.

Risk:

- Testnet assets have no real value, but the habits learned there affect real mainnet safety.

## Block Explorer

A block explorer lets users inspect transactions, addresses, contracts, Gas, status, and block height.

Risk:

- Explorer data should be used for verification, not just decoration in notes.

## My Current Operation Chain

Wallet creates or imports account -> user confirms action -> wallet signs -> transaction is broadcast -> chain executes -> block explorer verifies -> learning repo records proof.

