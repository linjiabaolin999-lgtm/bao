# 概念学习资料：Agent（智能体）

## 1. 个人解释
Agent（智能体）是具备自主感知、思考、决策和工具调用能力的 AI 系统。它不仅能回答问题，还能像一个“数字员工”一样，根据既定目标自主规划步骤并执行复杂任务。

## 2. 核心机制与组成
- **感知（Perception）**：接收并解析来自用户或环境的输入信息。
- **规划（Planning）**：将复杂目标拆解为可执行的子任务序列。
- **记忆（Memory）**：结合短期上下文与长期记忆检索历史信息。
- **工具调用（Tool Use）**：通过 API 调用外部工具（如搜索引擎、代码解释器、数据库）完成操作。

## 3. 典型应用场景
- **自动化代码助手**：如 GitHub Copilot Workspace，能够根据 Issue 自动分析代码库、定位 Bug、编写修复代码并提交 Pull Request。

## 4. 易混淆点与使用边界
- **与普通 Prompt 对话的区别**：普通 Prompt 是单轮或多轮的“问答”，而 Agent 具有“目标导向”和“自主循环（Action Loop）”，能自动根据工具返回结果修正下一步行动。
- **局限性与边界**：Agent 在多步骤规划中可能出现死循环或幻觉；对环境输入的理解受限于底层大模型的推理能力。

## 5. 可核查参考来源
- [LangChain Agents Documentation](https://python.langchain.com/docs/modules/agents/)
- [OpenAI Function Calling & Agents Guide](https://platform.openai.com/docs/guides/function-calling)
