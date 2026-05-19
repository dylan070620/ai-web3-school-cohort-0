# Week 1 AI Concept Cards

Status: draft

## LLM

My understanding / 我的理解:

- 中文：LLM 是一个根据上下文来预测和生成合理回答的“文字超级函数”。它可以和人对话、聊天，也可以处理很多读写类文字需求。
- English: An LLM is like a “super text function” that predicts and generates a reasonable response based on the context it can see. It can chat with people and handle many reading and writing tasks.

When to use / 适合用来做什么:

- 中文：适合生成文章、报告、学习笔记，也适合修改和优化稿件。
- English: It is useful for writing articles, reports, and study notes, and for revising or improving drafts.

Risk / 风险:

- 中文：LLM 只能生成看似合理的答案，可能出现幻觉，甚至凭空说一些不存在的内容。所以重要内容需要严谨验证，也需要用提示词限制它的输出。在法律、医疗、金融分析等领域要特别谨慎。
- English: An LLM can generate answers that only look reasonable. It may hallucinate and invent things that do not exist. Important outputs need careful verification, and prompts should set clear limits. It should be used with extra caution in legal, medical, and financial analysis contexts.

## Prompt

My understanding / 我的理解:

- 中文：Prompt 就是提示词，是用户给 LLM 输入的任务。LLM 会根据这个任务进行推理和回答。
- English: A prompt is the task instruction that a user gives to an LLM. The LLM uses it to reason and generate a response.

What a good prompt should include / 好的 Prompt 应该包含什么:

- 中文：好的 Prompt 需要有明确的限制、角色设定和回答方式。例如让模型扮演一个数学老师，学生提问时不要直接给答案，而是先理清思维，再一步步引导学生解答。
- English: A good prompt should include clear constraints, role setting, and the expected response style. For example, I can ask the model to act as a math teacher and guide a student step by step instead of directly giving the final answer.

Risk / 风险:

- 中文：Prompt 也有局限。模型可能出现逻辑错误，在复杂或高风险问题里也可能带来安全风险，比如投资建议这类内容不能只靠模型回答，需要额外验证和人工判断。
- English: Prompts have limits. The model can still make logical mistakes, and complex or high-risk tasks can create safety issues. For example, investment advice should not rely only on an LLM answer; it needs extra verification and human judgment.

## Workflow

My understanding / 我的理解:

- 中文：Workflow 是给 AI 明确一套流水线任务，让它按照固定的执行步骤完成工作。
- English: A workflow gives AI a clear pipeline of tasks and asks it to follow fixed execution steps.

Difference from a prompt / 和单个 Prompt 的区别:

- 中文：单个 Prompt 主要是让回答方向更明确，确定一个边界；Workflow 更像是严谨地要求 AI 按步骤行事。例如客服场景中，用户输入订单号，系统调用 API 获取数据，再整理结果返回给用户。
- English: A single prompt mainly clarifies the direction and boundaries of one response. A workflow is stricter and makes AI follow a sequence of steps. For example, in customer service, the user enters an order number, the system calls an API to get data, and then returns a structured answer.

When to use / 适合用来做什么:

- 中文：Workflow 适合自主判断少、不确定因素少的固定流程任务，比如学习资料整理、日报生成、客服查询、固定格式的记录整理。
- English: Workflows are suitable for fixed processes with little need for autonomous judgment and fewer uncertain factors, such as organizing study materials, generating daily reports, customer service lookup, and structured logging.

Risk / 风险:

- 中文：如果目标很模糊，或者中间结果会强烈影响下一步，Workflow 可能变得不可控，也可能放大幻觉或错误执行。
- English: If the goal is vague or intermediate results strongly affect the next step, a workflow can become hard to control and may amplify hallucinations or execution errors.

## Agent

My understanding / 我的理解:

- 中文：Agent 可以理解成一个“全副武装的 LLM”：它不只是回答问题，还能自主规划任务、拆分步骤、使用工具、保存记忆，并对过程进行一定的审查。
- English: An Agent can be understood as a “fully equipped LLM.” It does not only answer questions; it can plan tasks, break them into steps, use tools, keep memory, and review parts of the process.

Difference from a workflow / 和 Workflow 的区别:

- 中文：Agent 和 Workflow 最大的区别是，Agent 有更强的自主性。它可以自己拆任务、规划任务路径，并根据中间结果决定下一步；Workflow 更偏固定步骤。
- English: The biggest difference is autonomy. An Agent can decompose tasks, plan the path, and decide the next step based on intermediate results, while a workflow usually follows fixed steps.

AI x Web3 safety boundary / AI x Web3 安全边界:

- 中文：在 AI x Web3 中，智能合约逻辑安全、转账、签名、授权和合约写入都必须人工核查。因为 Web3 是直接接触钱和权限的环境，任何不严谨的小错误都可能导致资产损失，甚至项目上线后财产归零。
- English: In AI x Web3, smart contract logic safety, transfers, signatures, approvals, and contract write actions must be manually reviewed. Web3 directly touches money and permissions, so even a small careless mistake can lead to asset loss or a project becoming financially unsafe after launch.

Risk / 风险:

- 中文：Agent 越自主，越需要日志、权限边界、人工确认、失败恢复和验证材料。
- English: The more autonomous an Agent is, the more it needs logs, permission boundaries, human confirmation, failure recovery, and verification evidence.

## Tool Use

My understanding / 我的理解:

- 中文：如果把 LLM 理解成 CPU，那么 Tool 就像它的传感器和马达。Tool Use 就是让 AI 不只是在文字里回答，而是可以调用外部工具、API、文件、终端或其他系统来完成动作。
- English: If an LLM is like a CPU, tools are like its sensors and motors. Tool Use means AI does not only answer in text; it can call external tools, APIs, files, terminals, or other systems to take actions.

Why it matters / 为什么重要:

- 中文：只会聊天的 AI 只能给建议或输出文字；能调用工具的 AI 可以真正执行任务，比如查天气 API、debug、发邮件、更新 GitHub、甚至触发转账或链上交互。
- English: A chat-only AI can only give advice or produce text. An AI with tool use can actually execute tasks, such as checking a weather API, debugging, sending emails, updating GitHub, or even triggering transfers and on-chain interactions.

Risk / 风险:

- 中文：风险在于执行高危操作时可能造成真实后果，比如转账、删除文件、Git commit / push、链上交易或合约写入。因为 LLM 本身有不稳定因素，这类动作必须人工确认。
- English: The risk is that high-impact actions can create real consequences, such as transfers, deleting files, Git commit / push, on-chain transactions, or contract writes. Because LLM behavior can be unstable, these actions must require human confirmation.

## AI Coding

My understanding / 我的理解:

- 中文：AI Coding 工具可以理解成专注 coding 的 Agent。它能拆项目任务，和用户沟通需求，独立完成代码开发、测试、debug，并把结果反馈给用户。
- English: AI Coding tools can be understood as coding-focused Agents. They can break down project tasks, communicate with the user about requirements, write code, run tests, debug problems, and report the result back to the user.

When to use / 适合用来做什么:

- 中文：适合用来读代码、解释陌生项目、生成原型、写样板代码、修复 syntax error、跑测试和整理学习仓库。
- English: They are useful for reading code, explaining unfamiliar projects, creating prototypes, writing boilerplate, fixing syntax errors, running tests, and maintaining a learning repo.

Risk / 风险:

- 中文：不能完全相信 AI 写的代码。它可能能解决 syntax error，但 Web3 里很多黑客事件来自逻辑错误，而不是语法错误。甚至通过审计的项目也可能有漏洞。所以在人类设计项目时，必须把安全意识贯穿整个开发过程，尤其是权限、资金流、合约升级和边界条件。
- English: I cannot fully trust AI-generated code. It may fix syntax errors, but many Web3 hacks come from logic errors rather than syntax errors. Even audited projects can still have vulnerabilities. Human developers must keep security throughout the whole development process, especially around permissions, fund flows, contract upgrades, and edge cases.

## My Current Understanding

- Prompt is best for asking.
- Workflow is best for fixed processes.
- Agent is best when the path depends on tool results.
- The closer AI gets to execution, the more I need logs, verification, permissions, and human confirmation.
