# Week 1 Testnet Transaction Log

Status: done

Date: 2026-05-19

## Network

- Testnet: Sepolia
- Faucet used: Sepolia faucet
- Explorer: Sepolia Etherscan

## Wallet

- Public test wallet address: 0x9b77035cd5f1ffaea61b4cf0989615ec7b6865e3

Do not record mnemonic or private key.

## Transaction

### Transaction 1: Faucet Transfer

- Transaction hash: 0x905c98746fadaf7748a3ab61e97a9bc1ed860a140c248e20e983f77293ec42e8
- Type: Testnet ETH transfer
- Status: Success
- From: 0x42645ce4dd0b766de53ee483cbf54bcea670f9b2
- To: 0x9b77035cd5f1ffaea61b4cf0989615ec7b6865e3
- Value: 0.05 Sepolia ETH
- Gas used: 21000
- Transaction fee: 0.000000389096547 Sepolia ETH
- Block height: 10878942
- Timestamp: 2026-05-19 17:34:24 CST
- Block explorer link: https://sepolia.etherscan.io/tx/0x905c98746fadaf7748a3ab61e97a9bc1ed860a140c248e20e983f77293ec42e8

### Transaction 2: OKX Wallet To MetaMask

- Transaction hash: 0xf2d0538039ad29f7a12c152fe6c5044566d801c011a3c6b7fa2cf824394a8cf6
- Type: Testnet ETH transfer
- Status: Success
- From: 0x9b77035cd5f1ffaea61b4cf0989615ec7b6865e3
- To: 0x8bf8edebfd255c6ace0db31786c90d1f2e2beb06
- Value: 0.02 Sepolia ETH
- Gas used: 21000
- Transaction fee: 0.000002303945364 Sepolia ETH
- Block height: 10879419
- Timestamp: 2026-05-19 19:30:24 CST
- Block explorer link: https://sepolia.etherscan.io/tx/0xf2d0538039ad29f7a12c152fe6c5044566d801c011a3c6b7fa2cf824394a8cf6

## What I Did

- I used a test wallet on Sepolia.
- I received testnet ETH from a faucet.
- I transferred 0.02 Sepolia ETH from OKX Wallet to a MetaMask wallet address.
- I opened the transaction link in Sepolia Etherscan.
- I used the transaction hash to verify the transaction status, sender, receiver, value, Gas, block height, and time.

## What The Wallet Asked Me To Confirm

- The action was on the Sepolia testnet.
- The transaction was a testnet ETH transfer.
- The transaction involved testnet funds only.
- Signing or sending a transaction must be confirmed manually by the wallet owner.

## What The Block Explorer Proved

- The transaction status was successful.
- Transaction 1 was included in block 10878942.
- Transaction 1 transferred 0.05 Sepolia ETH to 0x9b77035cd5f1ffaea61b4cf0989615ec7b6865e3.
- Transaction 2 was included in block 10879419.
- Transaction 2 transferred 0.02 Sepolia ETH from OKX Wallet address 0x9b77035cd5f1ffaea61b4cf0989615ec7b6865e3 to MetaMask address 0x8bf8edebfd255c6ace0db31786c90d1f2e2beb06.
- Both transactions used 21000 Gas, which matches basic ETH transfers.
- Both transaction inputs were empty, so these were not smart contract calls.

## Problems And Recovery

- Etherscan page loading was slow from the local environment.
- I used the public transaction hash and Sepolia RPC data to verify the transaction details.
- No private key, mnemonic, or sensitive wallet data was needed for verification.

## My Understanding

- 中文：这两笔交易让我看到了测试网转账的完整链路：水龙头或钱包发起交易，钱包人工确认，交易广播到 Sepolia，链上执行后生成交易哈希，最后用区块浏览器验证状态、Gas、区块高度和时间。第二笔交易也让我练习了从 OKX 钱包转到 MetaMask 钱包的跨钱包测试网转账。
- English: These two transactions helped me understand the full testnet transfer flow: a faucet or wallet initiates the transaction, the wallet owner manually confirms it, the transaction is broadcast to Sepolia, the chain executes it and produces a transaction hash, and the block explorer verifies its status, Gas, block height, and time. The second transaction also let me practice a cross-wallet testnet transfer from OKX Wallet to MetaMask.

## AI x Web3 Safety Boundary

- AI can help read public transaction data and organize the learning record.
- AI must not receive mnemonic phrases or private keys.
- AI must not automatically confirm signatures, transfers, approvals, or contract writes.

## Privacy Check

- [x] No mnemonic included.
- [x] No private key included.
- [x] No real funds used.
- [x] Screenshot reviewed before sharing.
