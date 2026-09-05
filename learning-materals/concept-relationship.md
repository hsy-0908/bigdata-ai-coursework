# Agent、LLM‑Context、Skill 三者概念关系
## Skill
Skill 是Agent的能力单元，封装具体任务逻辑，提供可被调用的执行能力，定义Agent可以完成哪些工作。

## LLM‑Context
大模型上下文环境，存储对话历史、提示词、输入输出，是大模型推理的记忆载体，维护完整会话状态。

## Agent
智能运行主体，接收用户请求，依靠LLM‑Context保存会话信息，调度Skill完成用户交给的任务。

### 相互关系
Agent是运行主体；LLM‑Context提供会话记忆环境；Skill提供执行能力。
Agent接收用户指令后，依靠LLM‑Context理解上下文，调用对应Skill执行任务，三者协同实现智能代理。