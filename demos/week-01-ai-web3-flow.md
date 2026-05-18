# Week 1 AI x Web3 Minimal Flow

Status: draft

```mermaid
flowchart TD
    A["Learner asks AI for help"] --> B["AI drafts explanation, checklist, or interaction plan"]
    B --> C["Human reviews output"]
    C --> D{"Is the action safe and understood?"}
    D -- "No" --> E["Revise prompt, ask questions, or stop"]
    D -- "Yes" --> F["Human opens wallet or Web3 tool"]
    F --> G["Wallet shows message or transaction details"]
    G --> H{"Human confirms?"}
    H -- "No" --> I["Reject transaction and record why"]
    H -- "Yes" --> J["Transaction is signed and broadcast"]
    J --> K["Chain executes or fails"]
    K --> L["Check block explorer"]
    L --> M["Record hash, status, Gas, block height, and lesson in GitHub"]
```

## Human Confirmation Points

- Before using any wallet.
- Before signing any message.
- Before sending any transaction.
- Before approving token permissions.
- Before publishing public proof.

## Failure Points

- AI gives incorrect explanation.
- Wallet is on the wrong network.
- Faucet fails.
- Transaction fails or runs out of Gas.
- Contract address is wrong.
- Explorer link points to the wrong chain.

## Recovery Actions

- Stop and inspect the exact error.
- Check network and address.
- Use block explorer to verify status.
- Ask AI to explain the error, but verify with docs or actual output.
- Record the failure as learning proof.

## Things The Agent Must Not Do

- Store private keys or mnemonics.
- Auto-sign wallet messages.
- Auto-send transactions.
- Auto-approve token allowances.
- Hide transaction details from the human.

