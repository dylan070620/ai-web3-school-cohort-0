# Week 1 Minimal Smart Contract Interaction

Status: done

Date: 2026-05-20

## Tool

- Remix

## Network

- Testnet: Sepolia

## Contract

- Contract name: Mytoken
- Token name: BoWei Token
- Token symbol: BVB
- Source file: `/Users/dylanz/Desktop/Web3-develop-AI-Finance-Research/02_coding/2025-5-6/MyToken.sol`
- Contract address: 0x95cCA7900A1dbA13814430a6eD4993ABbb4E951D
- Deploy transaction hash: 0xec287300f40b20a0df26f1ea54e01a2b3894438f19e02576e8030e839b724810
- Deploy status: Success
- Deploy block: 10884097
- Deploy gas used: 1169942
- Block explorer link: https://sepolia.etherscan.io/address/0x95cCA7900A1dbA13814430a6eD4993ABbb4E951D
- Deploy transaction link: https://sepolia.etherscan.io/tx/0xec287300f40b20a0df26f1ea54e01a2b3894438f19e02576e8030e839b724810

## Deploy Events

- `OwnershipTransferred`: owner set to 0x8BF8EdebfD255c6acE0DB31786c90d1F2e2BeB06
- `Transfer`: initial mint from 0x0000000000000000000000000000000000000000 to 0x8BF8EdebfD255c6acE0DB31786c90d1F2e2BeB06
- Initial minted amount: 1000000000000000000000000 raw units
- Human-readable initial amount: 1,000,000 BVB with 18 decimals

## Read Interaction

- Function: `_getbalance()`
- Caller / `msg.sender`: 0x8BF8EdebfD255c6acE0DB31786c90d1F2e2BeB06
- Contract: 0x95cCA7900A1dbA13814430a6eD4993ABbb4E951D
- Raw result: 1000000000000000000000000
- Human-readable result: 1,000,000 BVB
- Explanation: `_getbalance()` calls `balanceOf(msg.sender)`, so it returned the token balance of the wallet that called the function.

## Write Interaction

- Function: `mint(address to, uint256 amount)`
- To: 0x8BF8EdebfD255c6acE0DB31786c90d1F2e2BeB06
- Amount: 1000000000000000000 raw units
- Human-readable amount: 1 BVB
- Transaction hash: 0xdf8f064399d2ce71d667cf5c693037c37643a93892c8c6885e5bdff3af7ccc6e
- Status: Success
- Block: 10884124
- Gas used: 37075
- Block explorer link: https://sepolia.etherscan.io/tx/0xdf8f064399d2ce71d667cf5c693037c37643a93892c8c6885e5bdff3af7ccc6e
- Event emitted: `Transfer`
- Transfer event:
  - From: 0x0000000000000000000000000000000000000000
  - To: 0x8BF8EdebfD255c6acE0DB31786c90d1F2e2BeB06
  - Amount: 1000000000000000000 raw units

## What I Verified

- The contract deployment transaction was successful.
- The deployed contract address was created on Sepolia.
- The constructor emitted an `OwnershipTransferred` event.
- The constructor minted 1,000,000 BVB to the deployer address.
- The read call `_getbalance()` returned the deployer wallet's current BVB balance.
- The write transaction `mint(address,uint256)` successfully minted 1 BVB to the deployer wallet.
- The mint transaction emitted a standard ERC20 `Transfer` event from the zero address.
- Etherscan verification was skipped because no Etherscan API key was configured in Remix.
- Blockscout verification succeeded according to Remix output.

## Problems And Recovery

- Etherscan verification was skipped due to missing API key.
- This is not blocking for the Week 1 task because the deployment transaction, contract address, and logs are enough for basic proof.
- The contract write interaction required a wallet confirmation because it changed on-chain state.

## What The Wallet Asked Me To Confirm

- Network: Sepolia
- Request origin: remix.ethereum.org
- Action type: contract deployment
- Estimated network fee: about 0.0008 Sepolia ETH
- This was manually confirmed by the wallet owner.
- For the mint transaction:
  - Network: Sepolia
  - Request origin: remix.ethereum.org
  - Interacting contract: 0x95cCA7900A1dbA13814430a6eD4993ABbb4E951D
  - Action type: contract write call
  - Expected result: mint 1 BVB to 0x8BF8EdebfD255c6acE0DB31786c90d1F2e2BeB06
  - Estimated network fee: about 0.0001 Sepolia ETH
  - This was manually confirmed by the wallet owner.

## My Understanding

- 中文：这次我用 Remix 在 Sepolia 上部署了一个 ERC20 合约。部署交易会创建合约地址，并在 constructor 里把初始 1,000,000 BVB mint 给部署者。`_getbalance()` 是 read call，不需要消耗 Gas，也不会改变链上状态；`mint(address,uint256)` 是 write transaction，会改变代币余额，所以必须通过钱包人工确认并支付测试网 Gas。
- English: In this task, I used Remix to deploy an ERC20 contract on Sepolia. The deployment transaction created a contract address and minted the initial 1,000,000 BVB to the deployer in the constructor. `_getbalance()` was a read call, so it did not cost Gas or change on-chain state. `mint(address,uint256)` was a write transaction that changed token balances, so it required manual wallet confirmation and testnet Gas.

## Privacy Check

- [x] No private key included.
- [x] No mnemonic included.
- [x] Contract address is safe to publish.
- [x] Transaction hash is safe to publish.
