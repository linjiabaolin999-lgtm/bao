# 概念学习资料：LLM Context（大模型上下文）

## 1. 个人解释
LLM Context（上下文）是大模型在进行单次推理决策时所能“看到”和“记住”的全部信息范围。它相当于模型工作时的“桌面工作记忆”，决定了当前交互的背景与边界。

## 2. 核心机制与组成
- **Context Window（上下文窗口）**：大模型所能处理的最大 Token 数量上限（如 128k Tokens）。
- **Attention 机制**：模型在生成下一个 Token 时，通过注意力机制对上下文中的关键信息进行加权计算。
- **Prompt 组成**：包含 System Prompt（系统指令）、Few-shot 示例、历史对话记录以及注入的外部知识。

## 3. 典型应用场景
- **长文档/代码库问答（RAG 系统）**：将检索到的文档片段注入到 Context 中，使大模型能够在不重新训练的前提下准确回答特定领域问题。

## 4. 易混淆点与使用边界
- **与长期记忆（Long-term Memory）的区别**：Context 是单次请求中的“短期无状态记忆”，会随着会话结束或窗口超限而被截断；长期记忆则需要依赖向量数据库等外部存储。
- **“大海捞针”与 Middle Lost 局限**：即使 Context 窗口极大（如 1M Tokens），模型对长文本中间位置信息的检索能力（Needle in a Haystack）仍可能下降。

## 5. 可核查参考来源
- [OpenAI API Reference - Context Window](https://platform.openai.com/docs/models)
- [Anthropic Claude Context Window Guide](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview)
