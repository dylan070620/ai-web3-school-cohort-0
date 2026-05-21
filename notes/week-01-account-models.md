# Week 1｜EOA、智能账户和多签账户权限对比

Status: done

这份笔记是我用自己的话整理的账户模型对比。重点不是背定义，而是搞清楚：**谁能控制账户，谁能批准交易，哪里必须让人停下来确认。**

## 快速对比

| 维度 | EOA 普通账户 | 智能账户 | 多签账户 |
| --- | --- | --- | --- |
| 控制权 | 一个私钥 / 助记词控制 | 智能合约规则控制 | 多个 signer 共同控制 |
| 发起交易 | 私钥持有人 | 被规则允许的人、模块或 agent | signer 可以发起提案 |
| 批准方式 | 一个签名就够 | 按合约规则判断 | 达到阈值才执行，例如 2/3、3/5 |
| 多人确认 | 默认没有 | 可以写进合约规则 | 天生支持 |
| 恢复 / 限额 | 默认没有 | 可以设计恢复、每日限额、可交互地址 | 可以通过 signer 和阈值调整 |
| 自动化 | 不适合直接交给 agent | 比较适合受限自动化 | 可以自动提案，但执行通常要多人确认 |
| 适合场景 | 个人钱包、测试网学习、小额交互 | AI-native wallet、受限 agent、自动化账户 | DAO、公司、团队金库、大项目资金 |
| 主要风险 | 私钥泄露、助记词丢失、乱签名 | 合约漏洞、权限规则写错、agent 被攻击 | signer 串通、私钥丢失、流程慢 |

## EOA：一个人拿一把钥匙

EOA，也就是外部账户，可以理解成由单一私钥或助记词控制的钱包。谁有私钥，谁就能控制这个钱包地址，发起交易、签名、转账，或者和合约交互。它跟我平时理解的普通钱包地址基本一样，适合个人小额钱包、学习测试、测试网交互和普通项目体验。

它最大的风险也很直接：控制权太集中。私钥或助记词丢了，我可能就永远拿不回这个账户；如果泄露了，别人就可以直接控制钱包，资产可能瞬间归零。还有一种更现实的风险是，我在恶意合约或钓鱼网站里没看清就签名、授权，也可能把权限交出去。

**English:** An EOA is a wallet controlled by one private key or seed phrase. Whoever has the key controls the address and can sign, transfer, or interact with contracts. It is simple and useful for personal wallets, testnet learning, and small interactions, but the risk is concentrated: if the key is lost or leaked, the account and assets may be lost. Malicious signatures and approvals are also a major risk.

## 智能账户：一个带规则的钱包

智能账户可以理解成由智能合约控制的钱包。虽然合约本身也是一个链上地址，但它不是只靠一个私钥直接控制，而是由程序逻辑来管理。所以它可以写规则，比如每日限额、限制可交互地址、限制可调用函数、设置恢复方式，甚至把账户做成多签钱包或 agent 代理钱包。

我觉得它和 AI agent 的关系很重要。因为 agent 可以根据 ABI 准备调用，但智能账户可以用访问限制、限额和权限规则控制它能做什么、不能做什么。这样比“把私钥交给 AI”安全很多。但智能账户也不是魔法安全，合约代码有漏洞、权限设计写错、agent 被恶意提示词攻击，都可能出问题。

**English:** A smart account is a wallet controlled by smart contract logic. It can include rules like daily limits, allowed addresses, allowed functions, recovery methods, or agent-based permissions. This makes it useful for AI agents and automation, because the agent can operate inside clear boundaries instead of holding the private key. The risk is that contract bugs, bad permission design, or prompt attacks can still make the account unsafe.

## 多签账户：团队保险柜

多签账户可以理解成由多个独立 signer 共同管理的钱包。它不是把一个私钥简单切成几份，而是每个 signer 都有自己的私钥，再由智能合约组织交易和批准流程。比如 2/3 多签，就是 3 个 signer 里至少 2 个人授权后，交易才会执行。

它适合公司、DAO、组织或大项目管理资金和重要权限。比如团队金库转账、合约升级、协议参数修改，都不应该一个人说了算。多签能降低单点风险，但也不是万能的。如果几个 signer 串通好，还是可以一起把钱转走；如果 signer 私钥丢太多，也可能导致账户卡住；如果大家只是机械点确认，多签也只是形式安全。

**English:** A multi-sig account is controlled by multiple independent signers. It is not one private key split into pieces; each signer has their own key, and the contract executes only after enough approvals, such as 2-of-3 or 3-of-5. It is useful for DAOs, companies, treasuries, and important contract permissions. The risks are signer collusion, lost keys, slow execution, and careless approvals.

## 我对 AI Agent 权限边界的理解

我一开始会觉得“涉及链上就全部人工确认”，但现在感觉要分层看。

如果以后真的有链上交易机器人或 AI agent，不可能每一笔低风险操作都手工确认，否则自动化就没有意义。更合理的是：人先设置清楚边界，比如最大交易额度、每日限额、止损规则、可交互合约、可调用函数和允许资产范围。agent 可以在这些边界内执行低风险操作。

但有些操作必须人工确认，因为它们不是普通执行，而是在改权限边界本身：

- 授权 token
- 合约升级
- 提高限额
- 更改交易策略
- 添加或删除 signer / owner
- 给 agent 新权限

我现在更倾向的安全模型是：**普通执行可以被限制后自动化，权限边界的修改必须人工确认。**

**English:** My current view is that not every low-risk on-chain action must be manually confirmed, otherwise automation loses its value. A better model is to let humans define the boundaries first: trade size, daily limits, stop-loss rules, allowed contracts, allowed functions, and allowed assets. The agent can operate inside those limits. But approvals, upgrades, limit changes, strategy changes, signer/owner changes, and new agent permissions must be manually confirmed because they change the permission boundary itself.

## 安全检查

- [x] 没有记录私钥、助记词或 API Key
- [x] 没有上传 `.env`
- [x] 不需要真实创建这些账户
- [x] 包含 EOA、智能账户、多签账户三类对比
- [x] 包含适用场景、风险点和人工确认边界
