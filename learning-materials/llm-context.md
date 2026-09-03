# 概念学习：大模型的上下文（LLM Context）
## 个人解释
上下文是传递给大模型的所有背景信息，相当于大模型的实时工作记忆。
## 核心机制
System Prompt、对话历史、RAG 检索内容、Token 窗口上限。
## 应用场景
智能客服：每次生成回答前实时插入最新的产品手册。
## 易混淆点与边界
模型本身无长期记忆，每次回答依赖当次传入的全部 Context。
## 资料来源
- https://platform.openai.com/docs/guides/text-generation
