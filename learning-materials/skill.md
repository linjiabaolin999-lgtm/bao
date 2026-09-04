# 概念学习资料：Skill（技能包）

## 1. 个人解释
Skill（技能包）是对特定业务场景或任务流程的标准化封装。它将 Prompt 指令、结构化约束、工作流程（SOP）和可调用工具整合为一个可复用的知识与能力模块。

## 2. 核心机制与组成
- **元数据定义（YAML Metadata）**：声明 Skill 的名称、适用场景与触发条件。
- **流程与规范（Workflow Rules）**：定义输入格式、处理步骤、质量检查项（Self-Check）。
- **示例与模版（Templates）**：提供标准化的输出结构，确保生成结果的一致性。

## 3. 典型应用场景
- **标准化代码评审 Skill**：封装安全审查、性能优化与代码规范核查流程，AI 载入该 Skill 后可自动按固定格式输出高质量审查报告。

## 4. 易混淆点与使用边界
- **与 Prompt 的区别**：Prompt 往往是一次性的自然语言提示；Skill 是模块化、工程化且具备明确自检能力的完整任务包。
- **与 Hardcoded API 的区别**：Skill 依赖大模型的语义理解能力去执行规范，具备很强的泛化能力，但对硬性确定性业务逻辑仍需配合代码逻辑进行硬约束。

## 5. 可核查参考来源
- [WorkBuddy Skill Specification Docs](https://github.com/workbuddy)
- [Semantic Kernel Plugins & Skills Concepts](https://learn.microsoft.com/en-us/semantic-kernel/concepts/plugins/)
