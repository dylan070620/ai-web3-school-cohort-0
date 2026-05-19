# Week 1 Web3 Concept Cards

Status: draft

## Account

My understanding / 我的理解:

- 中文：Account 可以理解成链上的账户，用户平时看到的是 public address / 地址，背后由私钥控制。它不像普通互联网账号那样依赖平台登录，而是通过钱包和签名来证明控制权。
- English: An account is an on-chain account. What users usually see is the public address, and control comes from the private key behind it. Unlike a normal internet account, it does not rely on platform login; control is proven through a wallet and signatures.

Privacy / 隐私特点:

- 中文：Account 有匿名感，但不是完全隐私。地址本身不直接写真实姓名，可是链上交互记录是透明的，谁都可以查到这个地址做过什么交易和合约交互。
- English: An account can feel anonymous, but it is not fully private. The address does not directly show a real name, but on-chain activity is transparent, and anyone can inspect its transactions and contract interactions.

Risk / 风险:

- 中文：Account 的安全重点是私钥、助记词和钱包权限。只要私钥泄露，别人就可能控制这个账户。
- English: The key security points are the private key, mnemonic, and wallet permissions. If the private key is leaked, someone else may control the account.

## Address

My understanding / 我的理解:

- 中文：Address 是链上的公开地址，可以理解成由私钥推导出来的一串公开标识。更准确地说，私钥可以推导出公钥，再由公钥生成地址，但不能从地址反推出私钥。
- English: An address is a public on-chain identifier. It can be understood as something derived from the private key. More precisely, a private key can derive a public key, and the public key can generate an address, but the address cannot be used to recover the private key.

Relationship with wallet / 和钱包的关系:

- 中文：钱包是管理和使用地址的工具。用户通过钱包查看地址、发起交易和签名，但真正控制地址的是背后的私钥。
- English: A wallet is the tool used to manage and use addresses. Users view addresses, send transactions, and sign actions through the wallet, but real control comes from the private key behind the address.

Privacy / 隐私特点:

- 中文：因为区块链的特性，链上操作都是透明的。地址是公开可查的，别人可以看到它的交易和合约交互，所以地址不等于真正匿名。
- English: Because of how blockchains work, on-chain actions are transparent. An address is publicly inspectable, and others can see its transactions and contract interactions, so an address is not the same as true anonymity.

## Wallet

My understanding / 我的理解:

- 中文：Wallet 是一个管理工具，用来管理私钥，并提供用户接口来发起交易、签名、授权和查看资产。
- English: A wallet is a management tool. It manages private keys and gives users an interface to send transactions, sign messages, approve permissions, and view assets.

Difference from normal login / 和普通登录的区别:

- 中文：普通 App 登录通常只是进入一个平台账号；Web3 钱包连接后，可能会涉及资产、权限和链上行为。它不是单纯的登录工具。
- English: Normal app login usually just gives access to a platform account. A Web3 wallet connection may involve assets, permissions, and on-chain actions. It is not just a login tool.

Risk / 风险:

- 中文：钱包是链上资产和权限的操作入口。签名、授权、转账、合约写入这些动作都可能有真实后果，必须看清楚钱包提示并人工确认。
- English: A wallet is the control surface for on-chain assets and permissions. Signing, approvals, transfers, and contract writes can all have real consequences, so wallet prompts must be checked carefully and confirmed manually.

## Mnemonic

My understanding / 我的理解:

- 中文：Mnemonic 助记词和私钥很接近，可以理解成恢复钱包的一组种子词。通过对应的加密和推导规则，它可以生成或恢复钱包里的私钥和地址。
- English: A mnemonic, or seed phrase, is closely related to private keys. It can be understood as a set of seed words used to recover a wallet. Through cryptographic derivation rules, it can generate or recover the wallet's private keys and addresses.

Recovery / 恢复作用:

- 中文：如果手机或钱包 App 丢了，助记词可以用来恢复钱包账户。所以它不是普通密码，而是资产控制权的根。
- English: If a phone or wallet app is lost, the mnemonic can recover the wallet accounts. It is not a normal password; it is the root of asset control.

Risk / 风险:

- 中文：助记词一定不能泄漏，泄漏等于交出控制权。不能截图、上传、发给 AI、复制到聊天窗口，也不能 commit 到 GitHub。
- English: A mnemonic must never be leaked. Leaking it is the same as handing over control. It should never be screenshotted, uploaded, sent to AI, pasted into chats, or committed to GitHub.

## Private Key

My understanding / 我的理解:

- 中文：Private Key 私钥是控制账户的核心。谁掌握私钥，谁就能控制这个账户。
- English: A private key is the core of account control. Whoever has the private key can control the account.

Relationship with address and signature / 和地址、签名的关系:

- 中文：地址是公开给别人看的标识，私钥是不能公开的控制权。私钥可以用来生成签名，证明某个链上动作是账户控制者授权的。
- English: The address is the public identifier, while the private key is the hidden control authority. The private key can generate signatures to prove that an action was authorized by the account controller.

Risk:

- 中文：私钥泄漏等于资产归零。AI Agent、脚本、网页、聊天窗口都不应该拿到真实私钥，因为一旦被记录、上传或误用，就可能直接造成资产损失。
- English: Leaking a private key can mean losing everything in the account. AI Agents, scripts, websites, and chat windows should never receive a real private key, because if it is logged, uploaded, or misused, it can directly cause asset loss.

## Signature

My understanding / 我的理解:

- 中文：Signature 签名可以分成普通签名和交易签名。普通签名主要是为了证明“我是这个地址的主人，我拥有对应私钥”，例如登录网站或证明地址控制权。交易签名则是授权一笔链上动作，例如转账、授权代币、部署合约或调用合约写入函数。
- English: A signature can be divided into message signatures and transaction signatures. A message signature is mainly used to prove “I control this address and have the corresponding private key,” such as logging into a website or proving address ownership. A transaction signature authorizes an on-chain action, such as transferring assets, approving tokens, deploying a contract, or calling a contract write function.

Relationship with transaction / 和交易的关系:

- 中文：不是所有签名都会立刻转账。普通签名通常不直接上链，也不一定消耗 Gas；交易签名会被广播到链上执行，通常需要 Gas，并且执行后会留下交易记录。
- English: Not every signature directly transfers assets. A message signature usually does not go on-chain and may not cost Gas. A transaction signature is broadcast to the chain for execution, usually costs Gas, and leaves an on-chain transaction record.

Risk:

- 中文：签名不能随便点确认。普通签名虽然不一定转账，但可能被用来登录、绑定身份、确认订单或授权某种操作；交易签名更可能直接影响资产和权限。确认前必须看清签名内容、网站来源、授权对象和钱包提示。
- English: Signing should not be confirmed casually. A message signature may not transfer assets directly, but it can be used for login, identity binding, order confirmation, or other authorization. A transaction signature can directly affect assets and permissions. Before confirming, I must check the message content, website source, approval target, and wallet prompt.

## Transaction

My understanding / 我的理解:

- 中文：Transaction 交易是一笔经过账户签名后发送到链上的动作。它不是普通 App 里的按钮点击，而是会被网络验证、执行并记录在区块链上的操作。
- English: A transaction is an action signed by an account and sent to the blockchain. It is not just a normal app button click; it is verified, executed, and recorded on-chain.

What it can do / 可以包含哪些动作:

- 中文：交易可以是转账，也可以是部署智能合约、调用合约写入函数、授权代币、修改链上状态等。
- English: A transaction can transfer assets, deploy a smart contract, call a contract write function, approve tokens, or change on-chain state.

Risk / 风险:

- 中文：交易需要消耗 Gas，而且可能失败。交易一旦确认，通常不能像普通互联网操作一样撤回，所以签名前必须检查收款地址、合约地址、交互内容、金额和钱包提示。
- English: Transactions cost Gas and can fail. Once confirmed, they usually cannot be reversed like normal internet actions, so I must check the recipient address, contract address, interaction content, amount, and wallet prompt before signing.

## Gas

My understanding / 我的理解:

- 中文：Gas 是链上执行的成本机制。可以理解成用户为区块链网络执行计算、存储数据和打包交易支付的费用。
- English: Gas is the cost mechanism for on-chain execution. It is the fee users pay for the blockchain network to run computation, store data, and include transactions.

Why it exists / 为什么需要 Gas:

- 中文：Gas 不是单纯的手续费，它也限制了链上计算资源，防止有人无限占用网络。操作越复杂、写入状态越多，通常 Gas 成本越高。
- English: Gas is not just a simple fee. It also limits on-chain computing resources and prevents unlimited network usage. More complex operations and more state changes usually cost more Gas.

Risk / 风险:

- 中文：失败的交易也可能消耗 Gas，因为网络已经尝试执行过。测试网练习时也要养成看 Gas、看失败原因、看交易回执的习惯。
- English: Failed transactions can still consume Gas because the network has already attempted execution. Even on testnets, I should build the habit of checking Gas, failure reasons, and transaction receipts.

## Smart Contract

My understanding / 我的理解:

- 中文：Smart Contract 智能合约是部署在链上的代码。它按照链上的规则执行，状态和交互记录通常是公开可查的。
- English: A smart contract is code deployed on-chain. It executes according to blockchain rules, and its state and interaction history are usually publicly inspectable.

Difference from normal backend / 和普通后端的区别:

- 中文：普通后端代码通常由公司服务器控制，可以隐藏、修改或回滚；智能合约一旦部署，代码和状态更公开，很多逻辑不能随便改，升级权限和管理员权限也需要被检查。
- English: Normal backend code is usually controlled by company servers and can be hidden, modified, or rolled back. A smart contract is more public after deployment, many parts cannot be changed casually, and upgrade permissions or admin roles must be checked.

Risk / 风险:

- 中文：智能合约风险主要来自逻辑错误、权限设计、资金流、升级权限和边界条件。能编译通过不代表安全，测试通过也不代表没有漏洞。
- English: Smart contract risks often come from logic errors, permission design, fund flows, upgrade permissions, and edge cases. Compiling successfully does not mean it is safe, and passing tests does not mean there are no vulnerabilities.

## Testnet

My understanding / 我的理解:

- 中文：Testnet 测试网是用来学习、实验和测试链上操作的网络。测试币没有真实价值，适合先练习钱包、交易、部署合约和查看区块浏览器。
- English: A testnet is a network for learning, experiments, and testing on-chain operations. Testnet tokens have no real value, so it is suitable for practicing wallet usage, transactions, contract deployment, and block explorer verification.

Why it matters / 为什么重要:

- 中文：在主网操作前，应该先在测试网跑通流程。测试网可以帮助我理解钱包确认、Gas、失败交易、合约地址、交易哈希和验证材料。
- English: Before operating on mainnet, I should first run the process on a testnet. A testnet helps me understand wallet confirmation, Gas, failed transactions, contract addresses, transaction hashes, and verification evidence.

Risk / 风险:

- 中文：测试网资产没有真实价值，但测试网养成的习惯会影响主网安全。不能因为是测试网就随便暴露助记词、私钥或乱点授权。
- English: Testnet assets have no real value, but habits learned on testnets affect mainnet safety. I should not expose mnemonics, private keys, or approve things carelessly just because it is a testnet.

## Block Explorer

My understanding / 我的理解:

- 中文：Block Explorer 区块浏览器是查看链上记录的工具。可以用它查询地址、交易哈希、合约地址、Gas、状态、区块高度和合约交互记录。
- English: A block explorer is a tool for viewing on-chain records. It can be used to inspect addresses, transaction hashes, contract addresses, Gas, status, block height, and contract interactions.

How I use it / 我怎么用:

- 中文：做完测试网交易或合约交互后，我应该用区块浏览器验证交易是否成功、花了多少 Gas、在哪个区块、调用了哪个合约，并把链接记录到学习仓库。
- English: After a testnet transaction or contract interaction, I should use a block explorer to verify whether it succeeded, how much Gas it used, which block it was included in, which contract it called, and then record the link in my learning repo.

Risk / 风险:

- 中文：区块浏览器链接不是装饰，而是 proof-of-work 的验证材料。记录时不能包含私钥、助记词或敏感截图。
- English: A block explorer link is not decoration; it is verification evidence for proof-of-work. Records must not include private keys, mnemonics, or sensitive screenshots.

## My Current Operation Chain

My current operation chain / 我的当前链上操作流程:

- 中文：钱包创建或导入账户 -> 用户检查操作内容 -> 钱包发起签名或交易 -> 人工确认 -> 交易广播到链上 -> 区块链执行 -> 区块浏览器验证 -> 学习仓库记录证明。
- English: Wallet creates or imports an account -> user checks the action content -> wallet initiates a signature or transaction -> human confirms -> transaction is broadcast on-chain -> blockchain executes it -> block explorer verifies it -> learning repo records the proof.

AI x Web3 boundary / AI x Web3 边界:

- 中文：AI 可以帮我解释概念、生成步骤、检查记录和整理 proof-of-work，但不能直接接触助记词、私钥，也不能替我自动确认签名、转账、授权或合约写入。
- English: AI can help me explain concepts, generate steps, check records, and organize proof-of-work, but it must not directly access mnemonics or private keys, and it must not automatically confirm signatures, transfers, approvals, or contract writes for me.
