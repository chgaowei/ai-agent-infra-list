全网最全的AI Agent Infra开源项目汇总[持续更新]

# 前言

AI Agent 的重要性是行业共识。到 2026 年，瓶颈已不只是模型能力：还包括智能体如何**互认身份**、**调用工具**、**委派任务**、**与用户交互**以及**安全运行**。本清单覆盖这一分层栈，不包含模型本身。

这篇文章的目的有三个：

- 找个地方记录优秀的、有创意的开源项目
- 帮助 AI Agent 开发者快速找到合适的基础设施
- 帮助 AI Agent 开发者快速了解 AI Agent 基础设施的发展现状

我们暂时只收集开源项目，未来也可能会收集商业产品。

这篇文章我会持续更新。我以开源项目的方式维护它：[https://github.com/chgaowei/ai-agent-infra-list](https://github.com/chgaowei/ai-agent-infra-list)。

如果你也知道一些优秀的开源项目，或者你对某个项目有不一样的评价，或者你希望推广你的开源项目，欢迎提交 PR。

我们也建了一个 AI Agent Infra 的交流群，欢迎加入一起讨论：

微信：请添加微信号 changshan02 ，备注 AI 交流入群。

也欢迎加入 Discord，和全球技术人一起交流：[https://discord.gg/BNJdvMa5XE](https://discord.gg/BNJdvMa5XE)

## 本次更新（2026-09）

**推荐：** 把协议看成**分层栈**，而不是互相替代的竞品。

- **身份 / 开放互联网：** [ANP 1.1](https://github.com/agent-network-protocol/AgentNetworkProtocol)（`did:wba`），孵化于 [W3C AI Agent Protocol Community Group](https://www.w3.org/community/agentprotocol/)
- **智能体之间的任务：** [A2A](https://github.com/a2aproject/A2A)
- **工具与上下文：** [MCP](https://modelcontextprotocol.io)

ANP 是开放互联网上的身份与发现层；A2A 是任务/运行时协作层；MCP 是工具层。三者一起用。

命名陷阱：**IBM ACP**（Agent Communication Protocol）已于 **2025 年 8 月并入 A2A**，不再作为独立标准。**Zed ACP**（Agent Client Protocol）以及 **OpenAI/Stripe 的 Agentic Commerce Protocol** 也缩写为 “ACP”，三者互不相关。

### 协议对照（分层，而非对立）

| 协议 | 层级 | 标准化内容 | 说明 |
| --- | --- | --- | --- |
| **ANP / did:wba** | 身份与开放互联网 | 去中心化身份、发现、能力描述、加密协作 | 与 A2A/MCP 是对等层，不是替代。规范：[AgentNetworkProtocol](https://github.com/agent-network-protocol/AgentNetworkProtocol)。SDK：[AgentConnect](https://github.com/agent-network-protocol/anp)（仓库现名 `anp`）。站点：[agent-network-protocol.com](https://agent-network-protocol.com/) |
| **A2A** | 智能体间任务 | Agent Card、任务生命周期、不透明智能体协作 | Linux Foundation。IBM ACP 于 2025 年 8 月并入。[a2a-protocol.org](https://a2a-protocol.org) |
| **MCP** | 智能体到工具 | 工具、资源、提示词 | [modelcontextprotocol.io](https://modelcontextprotocol.io) |
| **AG-UI / A2UI** | 智能体到用户界面 | 前端事件流（AG-UI）；声明式原生 UI（A2UI） | 互补，不是竞品 |
| **Zed ACP** | 智能体到编辑器 / IDE | 任意编辑器连接任意编码智能体 | **不是** IBM ACP，也 **不是** A2A |

# 概览

2026 年的分类快照。项目可能横跨多个类别；正文一般只详写一次（ANP / A2A / MCP 会有交叉引用）。

- 标准组织与工作组：[W3C AI Agent Protocol CG](https://www.w3.org/community/agentprotocol/) · [AAIF](https://aaif.io) · [A2A](https://github.com/a2aproject/A2A) · [AGNTCY](https://agntcy.org) · [AP2](https://github.com/google-agentic-commerce/AP2)
- 身份与信任：[ANP](https://github.com/agent-network-protocol/AgentNetworkProtocol) · [did:wba](https://github.com/agent-network-protocol/AgentNetworkProtocol) · [AgentConnect](https://github.com/agent-network-protocol/anp) · [W3C DID](https://www.w3.org/TR/did/)
- 智能体间协议：[ANP](https://github.com/agent-network-protocol/AgentNetworkProtocol) · [A2A](https://github.com/a2aproject/A2A)
- 智能体到工具 / MCP：[MCP spec](https://github.com/modelcontextprotocol/modelcontextprotocol) · [servers](https://github.com/modelcontextprotocol/servers) · [registry](https://registry.modelcontextprotocol.io) · [goose](https://github.com/block/goose) · [AGENTS.md](https://github.com/agentsmd/agents.md) · [agentgateway](https://github.com/agentgateway/agentgateway)
- 智能体到用户 / UI：[AG-UI](https://github.com/ag-ui-protocol/ag-ui) · [A2UI](https://a2ui.org)
- 智能体到客户端 / IDE：[Zed ACP](https://github.com/zed-industries/agent-client-protocol)
- 商务与支付：[AP2](https://github.com/google-agentic-commerce/AP2) · [Agentic Commerce Protocol](https://github.com/agentic-commerce-protocol/agentic-commerce-protocol)
- 框架与编排：[OpenAI Agents SDK](https://github.com/openai/openai-agents-python) · [Google ADK](https://github.com/google/adk-python) · [Claude Agent SDK](https://github.com/anthropics/claude-agent-sdk-python) · [Microsoft Agent Framework](https://github.com/microsoft/agent-framework) · [LangGraph](https://github.com/langchain-ai/langgraph) · [LangChain](https://github.com/langchain-ai/langchain) · [LlamaIndex](https://github.com/run-llama/llama_index) · [Agno](https://github.com/agno-agi/agno) · [Pydantic AI](https://github.com/pydantic/pydantic-ai) · [Mastra](https://github.com/mastra-ai/mastra) · [Qwen-Agent](https://github.com/QwenLM/Qwen-Agent) · [Strands](https://github.com/strands-agents/sdk-python) · [Haystack](https://github.com/deepset-ai/haystack) · [DSPy](https://github.com/stanfordnlp/dspy) · [Inngest](https://github.com/inngest/inngest) · [Prefect](https://github.com/PrefectHQ/prefect) · [TEN-Agent](https://github.com/TEN-framework/ten-framework) · [AgentStack](https://github.com/agentstack-ai/AgentStack)
- 多智能体：[CrewAI](https://github.com/crewAIInc/crewAI) · [CAMEL](https://github.com/camel-ai/camel) · [MetaGPT](https://github.com/FoundationAgents/MetaGPT)（另见 LangGraph / Microsoft Agent Framework）
- 记忆与 RAG：[mem0](https://github.com/mem0ai/mem0) · [Graphiti](https://github.com/getzep/graphiti) · [Letta](https://github.com/letta-ai/letta) · [RAGFlow](https://github.com/infiniflow/ragflow) · [Cognee](https://github.com/topoteretes/cognee) · [DB-GPT](https://github.com/eosphoros-ai/DB-GPT) · [GraphRAG](https://github.com/microsoft/graphrag) · [fast-graphrag](https://github.com/circlemind-ai/fast-graphrag) · [LightRAG](https://github.com/HKUDS/LightRAG) · [nano-graphrag](https://github.com/gusye1234/nano-graphrag) · [Milvus](https://github.com/milvus-io/milvus) · [Weaviate](https://github.com/weaviate/weaviate) · [Chroma](https://github.com/chroma-core/chroma)
- 浏览器与计算机使用：[Scrapeless](https://github.com/scrapeless-ai) · [browser-use](https://github.com/browser-use/browser-use) · [Skyvern](https://github.com/Skyvern-AI/skyvern) · [Open-AutoGLM](https://github.com/zai-org/Open-AutoGLM) · [Crawlee](https://github.com/apify/crawlee) · [Browserless](https://github.com/browserless/browserless) · [AgentQL](https://github.com/tinyfish-io/agentql)
- 运行时、沙箱与网关：[Daytona](https://github.com/daytonaio/daytona) · [E2B](https://github.com/e2b-dev/E2B) · [SandBase Harness](https://github.com/sandbaseai/sandbase-harness) · [goose](https://github.com/block/goose) · [agentgateway](https://github.com/agentgateway/agentgateway)
- 可观测性与评测：[Langfuse](https://github.com/langfuse/langfuse) · [Phoenix](https://github.com/Arize-ai/phoenix) · [AgentOps](https://github.com/AgentOps-AI/agentops) · [OpenTelemetry GenAI conventions](https://github.com/open-telemetry/semantic-conventions-genai)
- 可视化 / 低代码平台：[n8n](https://github.com/n8n-io/n8n) · [Coze Studio](https://github.com/coze-dev/coze-studio) · [Dify](https://github.com/langgenius/dify) · [FastGPT](https://github.com/labring/FastGPT) · [BISHENG](https://github.com/dataelement/bisheng)
- 历史 / 归档 / 维护模式：[AutoGPT](https://github.com/Significant-Gravitas/AutoGPT) · [AutoGen](https://github.com/microsoft/autogen) · [Semantic Kernel](https://github.com/microsoft/semantic-kernel) · [Magentic-One](https://github.com/microsoft/autogen/tree/main/python/packages/autogen-magentic-one) · [npi](https://github.com/sheet0/npi) · [agent-protocol](https://github.com/agi-inc/agent-protocol) · [Agora Protocol](https://github.com/agora-protocol/paper-demo) · [naptha-sdk](https://github.com/NapthaAI/naptha-sdk)


# 1. 标准组织与工作组

### W3C AI Agent Protocol Community Group

W3C 社区组，制定开放、可互操作的协议，使智能体能够在 Web 上发现、识别并协作。ANP / `did:wba` 在此孵化。

站点：[https://www.w3.org/community/agentprotocol/](https://www.w3.org/community/agentprotocol/)

草案：[https://w3c-cg.github.io/ai-agent-protocol/](https://w3c-cg.github.io/ai-agent-protocol/)

### AAIF（Agentic AI Foundation）

位于 [aaif.io](https://aaif.io) 的产业基金会，推动智能体 AI 的工程化（身份与信任、可观测性、商务、安全、工作流）。协调若干开源项目，包括 goose。

站点：[https://aaif.io](https://aaif.io)

### A2A（Agent2Agent Protocol）

面向不透明智能体应用之间通信的开放协议（Agent Card、任务生命周期）。现为 Linux Foundation 项目。IBM 的 Agent Communication Protocol（ACP）已于 2025 年 8 月并入 A2A。

github 地址：[https://github.com/a2aproject/A2A](https://github.com/a2aproject/A2A)

站点：[https://a2a-protocol.org](https://a2a-protocol.org)

### AGNTCY

Linux Foundation 项目，构建「智能体互联网」基础设施：跨厂商、跨框架的发现、身份、消息（SLIM）与可观测性。

站点：[https://agntcy.org](https://agntcy.org)

github 地址：[https://github.com/agntcy](https://github.com/agntcy)

### AP2（Agent Payments Protocol）

Google 提出的开放协议，用于智能体与商户之间安全、可互操作的支付与授权（mandate）。补充 A2A / MCP，它不是智能体间任务协议。

github 地址：[https://github.com/google-agentic-commerce/AP2](https://github.com/google-agentic-commerce/AP2)

# 2. 身份与信任

这是开放互联网层：智能体如何证明「我是谁」、被发现，以及**跨平台**安全通信，而不依赖中心化 IdP。**ANP / `did:wba` / AgentConnect** 属于这一层，而不是放在 A2A 下面。

### Agent Network Protocol（ANP）

面向开放互联网的智能体身份、命名、发现、协商与协作协议套件。1.1 规范覆盖 `did:wba`、WNS 句柄、智能体描述、发现、端到端消息以及支付。与 W3C AI Agent Protocol CG 共同孵化。补充 A2A（任务）和 MCP（工具），并不替代它们。

github 地址：[https://github.com/agent-network-protocol/AgentNetworkProtocol](https://github.com/agent-network-protocol/AgentNetworkProtocol)

站点：[https://agent-network-protocol.com/](https://agent-network-protocol.com/)

W3C CG：[https://www.w3.org/community/agentprotocol/](https://www.w3.org/community/agentprotocol/)

### did:wba

ANP 使用的基于 Web 的 DID 方法，用于跨平台智能体身份与认证（兼容 W3C DID，面向现有 HTTPS 基础设施）。定义在 ANP 1.1 套件中。

github 地址：[https://github.com/agent-network-protocol/AgentNetworkProtocol](https://github.com/agent-network-protocol/AgentNetworkProtocol)

### AgentConnect

ANP 的多语言 SDK 与参考实现：`did:wba` 身份、智能体描述、发现、RPC、可验证证明以及端到端加密通信。GitHub 仓库现发布为 `anp`；历史路径 `chgaowei/AgentConnect` 与 `agent-network-protocol/AgentConnect` 会重定向到该仓库。

github 地址：[https://github.com/agent-network-protocol/anp](https://github.com/agent-network-protocol/anp)

主页：[https://agent-network-protocol.com/](https://agent-network-protocol.com/)

### W3C Decentralized Identifiers（DID）

W3C 去中心化标识符标准。ANP 的 `did:wba` 是一种 DID method；许多智能体身份方案复用 DID / VC，而不是另起一套 ID。

规范：[https://www.w3.org/TR/did/](https://www.w3.org/TR/did/)

github 地址：[https://github.com/w3c/did](https://github.com/w3c/did)

# 3. 智能体间协议

ANP 与 A2A 是**分层**，不是竞品：ANP 覆盖开放互联网上的身份与发现；A2A 覆盖不透明智能体之间的结构化任务交换（通常在平台内，或在身份已经建立之后）。

### Agent Network Protocol（ANP）

见[身份与信任](#2-身份与信任)。在应用层，ANP 定义智能体描述与发现，使异构智能体可以找到并调用彼此。

github 地址：[https://github.com/agent-network-protocol/AgentNetworkProtocol](https://github.com/agent-network-protocol/AgentNetworkProtocol)

### A2A

见[标准组织](#1-标准组织与工作组)。当你需要共享的任务模型（提交 / 执行 / 完成）以及现有运行时之间的 Agent Card 时使用 A2A。

github 地址：[https://github.com/a2aproject/A2A](https://github.com/a2aproject/A2A)

站点：[https://a2a-protocol.org](https://a2a-protocol.org)

# 4. 智能体到工具 / MCP

### Model Context Protocol（MCP）

连接 LLM 应用与外部工具、数据和提示词的开放协议。2026 年事实上的工具层；与 ANP（身份）和 A2A（任务）互补。

站点：[https://modelcontextprotocol.io](https://modelcontextprotocol.io)

规范仓库：[https://github.com/modelcontextprotocol/modelcontextprotocol](https://github.com/modelcontextprotocol/modelcontextprotocol)

官方 servers：[https://github.com/modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers)

github 组织：[https://github.com/modelcontextprotocol](https://github.com/modelcontextprotocol)

### MCP servers

参考与社区 MCP server 实现（文件系统、git、浏览器、SaaS 连接器等）。

github 地址：[https://github.com/modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers)

### MCP Registry

公开 MCP server 的官方元数据注册表（预览）。供客户端和市场发现服务。

注册表：[https://registry.modelcontextprotocol.io](https://registry.modelcontextprotocol.io)

### goose

Block 出品、现托管于 AAIF 的开源可扩展智能体，可安装、执行、编辑并用任意 LLM 做测试。偏 MCP 原生的本机/编码智能体。

github 地址：[https://github.com/block/goose](https://github.com/block/goose)（当前仓库：[https://github.com/aaif-goose/goose](https://github.com/aaif-goose/goose)）

### AGENTS.md

简单开放的 Markdown 格式，用于在仓库内指导编码智能体（约定、命令、注意事项）。与 MCP 互补：它是项目本地说明，不是工具协议。

github 地址：[https://github.com/agentsmd/agents.md](https://github.com/agentsmd/agents.md)

站点：[https://agents.md](https://agents.md)

### agentgateway

面向 AI 智能体和 MCP server 的开源代理/网关（路由、策略、工具前的连接）。

github 地址：[https://github.com/agentgateway/agentgateway](https://github.com/agentgateway/agentgateway)

# 5. 智能体到用户 / UI

### AG-UI

Agent-User Interaction Protocol：轻量事件协议，把智能体后端接到面向用户的应用（流式文本、工具调用、共享状态、人在环）。补充 MCP（工具）和 A2A（智能体协作）。

github 地址：[https://github.com/ag-ui-protocol/ag-ui](https://github.com/ag-ui-protocol/ag-ui)

### A2UI

Agent-to-User Interface 协议（Google，与 CopilotKit 等合作）：智能体发送声明式 UI 描述，客户端用原生组件渲染，而不是下发可执行 UI 代码。常承载于 AG-UI 或 A2A 流中。

站点：[https://a2ui.org](https://a2ui.org)

# 6. 智能体到客户端 / IDE

**不是 A2A。不是 IBM ACP。** Zed 的 Agent Client Protocol（同样缩写 ACP）是编辑器与编码智能体之间的协议。

### Agent Client Protocol（Zed ACP）

用于将任意编辑器/IDE 连接到任意编码智能体。起源于 Zed；规范仓库现位于 `agentclientprotocol` 组织。不要与已并入 A2A 的 IBM ACP，或 OpenAI/Stripe 的 Agentic Commerce Protocol 混淆。

github 地址：[https://github.com/zed-industries/agent-client-protocol](https://github.com/zed-industries/agent-client-protocol)（当前仓库：[https://github.com/agentclientprotocol/agent-client-protocol](https://github.com/agentclientprotocol/agent-client-protocol)）

# 7. 商务与支付

短节：智能体如何支付与结账。这不是身份层，也不是 A2A。

### AP2（Agent Payments Protocol）

见[标准组织](#1-标准组织与工作组)。面向智能体购买的授权/支付层。

github 地址：[https://github.com/google-agentic-commerce/AP2](https://github.com/google-agentic-commerce/AP2)

### Agentic Commerce Protocol（OpenAI / Stripe）

开放标准（同样缩写 **ACP**），连接买家、其智能体与商家完成购买。由 OpenAI 与 Stripe 维护。与 IBM ACP、Zed ACP 无关。

github 地址：[https://github.com/agentic-commerce-protocol/agentic-commerce-protocol](https://github.com/agentic-commerce-protocol/agentic-commerce-protocol)


# 8. 框架与编排

LangChain 仍被广泛使用；该家族中的**智能体运行时是 LangGraph**。微软现在的默认选择是 **Microsoft Agent Framework**（AutoGen 与 Semantic Kernel 见历史分类）。Phidata 已更名为 **Agno**。

### OpenAI Agents SDK

轻量 Python SDK，用于在 OpenAI 模型上构建智能体与多智能体工作流（handoff、工具、tracing）。

github 地址：[https://github.com/openai/openai-agents-python](https://github.com/openai/openai-agents-python)

### Google ADK（Agent Development Kit）

代码优先的 Python 工具包，用于构建、评估与部署智能体，并与 Gemini、A2A、MCP、Vertex 深度集成。

github 地址：[https://github.com/google/adk-python](https://github.com/google/adk-python)

### Claude Agent SDK

Anthropic 的 Python SDK，用于基于 Claude 构建智能体（工具、会话、类似 Claude Code 的 harness 模式）。

github 地址：[https://github.com/anthropics/claude-agent-sdk-python](https://github.com/anthropics/claude-agent-sdk-python)

### Microsoft Agent Framework

微软用于构建、编排和部署智能体及多智能体工作流的生产级框架（Python 与 .NET）。AutoGen 与 Semantic Kernel 的后续路径。

github 地址：[https://github.com/microsoft/agent-framework](https://github.com/microsoft/agent-framework)

### LangGraph

用于有状态、含循环的智能体与多智能体应用的库（循环、可控性、持久化）。这是 LangChain 家族的智能体运行时；做智能体时优先用它而不是原始 chain。

github 地址：[https://github.com/langchain-ai/langgraph](https://github.com/langchain-ai/langgraph)

### LangChain

通用 LLM 应用框架（模型、提示、检索、工具）。仍是许多栈的集成面；智能体场景请用 LangGraph。

github 地址：[https://github.com/langchain-ai/langchain](https://github.com/langchain-ai/langchain)

### LlamaIndex

把 LLM 接到私有数据的数据框架（索引、检索、智能体式 RAG 工作流）。

github 地址：[https://github.com/run-llama/llama_index](https://github.com/run-llama/llama_index)

### Agno（原 phidata）

用于构建多模态智能体与智能体团队的 Python 框架，带记忆、知识与工具。Phidata 于 2025 年更名为 Agno；旧仓库 `phidatahq/phidata` 会重定向到这里。

github 地址：[https://github.com/agno-agi/agno](https://github.com/agno-agi/agno)

### Pydantic AI

Pydantic 团队的带类型 Python 智能体框架：智能体、工具、以及基于 Pydantic 模型的结构化输出。

github 地址：[https://github.com/pydantic/pydantic-ai](https://github.com/pydantic/pydantic-ai)

### Mastra

面向 AI 应用与智能体的 TypeScript 框架（工作流、工具、评测与可观测性）。

github 地址：[https://github.com/mastra-ai/mastra](https://github.com/mastra-ai/mastra)

### Qwen-Agent

基于 Qwen（>=3.0）的智能体框架与应用：函数调用、MCP、代码解释器、RAG、Chrome 扩展。

github 地址：[https://github.com/QwenLM/Qwen-Agent](https://github.com/QwenLM/Qwen-Agent)

### Strands

用于生产智能体的开源 SDK（Python 与 TypeScript），模型与云无关。`sdk-python` 仓库现重定向到 `harness-sdk`。

github 地址：[https://github.com/strands-agents/sdk-python](https://github.com/strands-agents/sdk-python)

### Haystack

生产级 LLM 应用的管道/智能体编排：把模型、转换器、向量库连成 RAG、问答与智能体。

github 地址：[https://github.com/deepset-ai/haystack](https://github.com/deepset-ai/haystack)

### DSPy

斯坦福框架，把声明式语言模型程序变成可自优化的管道，而不是手写提示词。

github 地址：[https://github.com/stanfordnlp/dspy](https://github.com/stanfordnlp/dspy)

### Inngest

工作流编排平台，可在无服务器、服务器或边缘上运行有状态步骤函数和 AI 工作流。

github 地址：[https://github.com/inngest/inngest](https://github.com/inngest/inngest)

### Prefect

Python 工作流编排：把脚本变成可重试、可适应的生产管道。

github 地址：[https://github.com/PrefectHQ/prefect](https://github.com/PrefectHQ/prefect)

### TEN-Agent

开源实时多模态/语音智能体框架（RTC + 低延迟对话）。GitHub 仓库已更名为 `ten-framework`；`TEN-Agent` 路径会重定向。

github 地址：[https://github.com/TEN-framework/ten-framework](https://github.com/TEN-framework/ten-framework)  
（历史路径 `TEN-Agent` 会重定向到此仓库；产品名仍称 TEN-Agent）

### AgentStack

从命令行启动 AI 智能体项目并生成样板代码的 CLI。活跃度低于最初收录时。GitHub 组织现为 `agentstack-ai`。

github 地址：[https://github.com/agentstack-ai/AgentStack](https://github.com/agentstack-ai/AgentStack)

# 9. 多智能体

简写：新工作大多发生在 **LangGraph**、**Microsoft Agent Framework** 或 **CrewAI** 中。下面是仍值得了解的专用多智能体项目。

### CrewAI

基于角色的多智能体框架：定义智能体、任务与流程，让多个智能体协作完成工作流。

github 地址：[https://github.com/crewAIInc/crewAI](https://github.com/crewAIInc/crewAI)

### CAMEL

早期基于 LLM 的多智能体框架，已发展为构建与研究通信智能体的通用工具包。

github 地址：[https://github.com/camel-ai/camel](https://github.com/camel-ai/camel)

### MetaGPT

多智能体「软件公司」模式：一行需求输入，产出 PM / 架构师 / 工程师等角色与 SOP。仓库已从 `geekan/MetaGPT` 迁至 FoundationAgents/MetaGPT。

github 地址：[https://github.com/FoundationAgents/MetaGPT](https://github.com/FoundationAgents/MetaGPT)

另见：[LangGraph](#langgraph)、[Microsoft Agent Framework](#microsoft-agent-framework)、[Agno](#agno原-phidata)。

# 10. 记忆与 RAG

### mem0

助手与智能体的记忆层：存储并检索长期个性化事实，使跨会话回复保持相关。

github 地址：[https://github.com/mem0ai/mem0](https://github.com/mem0ai/mem0)

### Graphiti

面向 AI 智能体的实时知识图谱（来自持续活动的时序图记忆，而不是只做批处理 GraphRAG）。

github 地址：[https://github.com/getzep/graphiti](https://github.com/getzep/graphiti)

### Letta（原 MemGPT）

用于有状态 LLM 智能体的框架：长期记忆、自管理上下文，以及连接外部数据。

github 地址：[https://github.com/letta-ai/letta](https://github.com/letta-ai/letta)

### RAGFlow

基于深度文档理解的开源 RAG 引擎，能为复杂企业文件提供带引用的问答。

github 地址：[https://github.com/infiniflow/ragflow](https://github.com/infiniflow/ragflow)

### Cognee

ECL（Extract, Cognify, Load）流水线，把对话、文档和转写变成可检索的记忆图。

github 地址：[https://github.com/topoteretes/cognee](https://github.com/topoteretes/cognee)

### DB-GPT

AI 原生数据应用框架：Text2SQL、RAG、多模型管理，以及面向数据库的 AWEL 智能体工作流编排。

github 地址：[https://github.com/eosphoros-ai/DB-GPT](https://github.com/eosphoros-ai/DB-GPT)

### GraphRAG

微软数据管道，用 LLM 从非结构化文本抽取知识图谱以供检索。

github 地址：[https://github.com/microsoft/graphrag](https://github.com/microsoft/graphrag)

### fast-graphrag

精简、可增量更新的 GraphRAG 风格检索，面向智能体工作流（可解释、更低成本更新）。

github 地址：[https://github.com/circlemind-ai/fast-graphrag](https://github.com/circlemind-ai/fast-graphrag)

### LightRAG

简单、快速的图增强 RAG 引擎。

github 地址：[https://github.com/HKUDS/LightRAG](https://github.com/HKUDS/LightRAG)

### nano-graphrag

更小、更好改的 GraphRAG 实现，保留核心思路、去掉官方仓库的重量。

github 地址：[https://github.com/gusye1234/nano-graphrag](https://github.com/gusye1234/nano-graphrag)

### Milvus

面向大规模的高性能开源向量数据库，用于存储和检索 embedding。

github 地址：[https://github.com/milvus-io/milvus](https://github.com/milvus-io/milvus)

### Weaviate

开源向量数据库：同时存储对象与向量，支持向量检索加结构化过滤，云原生运维。

github 地址：[https://github.com/weaviate/weaviate](https://github.com/weaviate/weaviate)

### Chroma

AI 原生开源 embedding 数据库，常作为 RAG 的本地/开发向量库。

github 地址：[https://github.com/chroma-core/chroma](https://github.com/chroma-core/chroma)


# 11. 浏览器与计算机使用

### Scrapeless

社区 PR：面向智能体的网页数据采集相关开源组织，提供 SDK 与配套仓库。

github 地址：[https://github.com/scrapeless-ai](https://github.com/scrapeless-ai)

### browser-use

把 LLM 智能体接到网页上的流行开源项目。

github 地址：[https://github.com/browser-use/browser-use](https://github.com/browser-use/browser-use)

### Skyvern

用 LLM 驱动网站工作流的开源项目。

github 地址：[https://github.com/Skyvern-AI/skyvern](https://github.com/Skyvern-AI/skyvern)

### Open-AutoGLM

智谱（Z.ai）开源的手机智能体模型与框架。

github 地址：[https://github.com/zai-org/Open-AutoGLM](https://github.com/zai-org/Open-AutoGLM)

### Crawlee

用于构建可靠网页采集器的 Node.js 库（JS/TS），可向 RAG / LLM 管道提供数据。

github 地址：[https://github.com/apify/crawlee](https://github.com/apify/crawlee)

### Browserless

基于 Docker 的 Chrome 服务，提供截图、PDF 与页面提取等 REST API。

github 地址：[https://github.com/browserless/browserless](https://github.com/browserless/browserless)

### AgentQL

用自然语言查询定位页面上的数据与元素，包括需登录和动态生成的内容。

github 地址：[https://github.com/tinyfish-io/agentql](https://github.com/tinyfish-io/agentql)

# 12. 运行时、沙箱与网关

### Daytona

用于在隔离环境中运行 AI 生成代码的安全、弹性基础设施。

github 地址：[https://github.com/daytonaio/daytona](https://github.com/daytonaio/daytona)

### E2B

开源基础设施，可在云中的隔离沙箱里运行 AI 生成的代码。

github 地址：[https://github.com/e2b-dev/E2B](https://github.com/e2b-dev/E2B)

### SandBase Harness

本地优先的 TypeScript AI Agent Runtime：持久化会话、沙箱工具执行、MCP、记忆、凭据隔离、审计日志与执行回放。支持本地、Docker、Kubernetes 以及自托管部署。

github 地址：[https://github.com/sandbaseai/sandbase-harness](https://github.com/sandbaseai/sandbase-harness)

# 13. 可观测性与评测

LangSmith 是 LangChain 的**商业**产品（追踪、数据集、评测），此处不作为开源项目列出。开源栈优先考虑 Langfuse / Phoenix / OTel。

### Langfuse

开源 LLM 工程平台：追踪、指标、评测、提示管理、Playground、数据集。可与 LangChain、LlamaIndex、OpenAI SDK 等集成。

github 地址：[https://github.com/langfuse/langfuse](https://github.com/langfuse/langfuse)

### Phoenix

Arize 的开源 AI 可观测性平台：追踪、评测、数据集，以及 LLM/智能体应用排障。

github 地址：[https://github.com/Arize-ai/phoenix](https://github.com/Arize-ai/phoenix)

### AgentOps

用于智能体监控、LLM 成本跟踪和基准测试的 Python SDK；可与 CrewAI、LangChain、AutoGen 等集成。

github 地址：[https://github.com/AgentOps-AI/agentops](https://github.com/AgentOps-AI/agentops)

### OpenTelemetry GenAI semantic conventions

生成式 AI / 智能体工作负载的语义约定，使追踪可跨厂商互操作。

github 地址：[https://github.com/open-telemetry/semantic-conventions-genai](https://github.com/open-telemetry/semantic-conventions-genai)

# 14. 可视化 / 低代码平台

### n8n

Fair-code 工作流自动化，带原生 AI 节点：可视化搭建加上自定义代码，可自托管或上云。

github 地址：[https://github.com/n8n-io/n8n](https://github.com/n8n-io/n8n)

### Coze Studio

扣子团队开源的可视化 AI 智能体开发平台（创建、调试、部署）。

github 地址：[https://github.com/coze-dev/coze-studio](https://github.com/coze-dev/coze-studio)

### Dify

开源 LLM 应用开发平台：可视化 AI 工作流、RAG、智能体、模型管理与可观测性，从原型到生产。

github 地址：[https://github.com/langgenius/dify](https://github.com/langgenius/dify)

### FastGPT

基于 LLM 的知识库平台：数据处理、RAG 检索以及可视化 AI 工作流编排，便于部署问答系统。

github 地址：[https://github.com/labring/FastGPT](https://github.com/labring/FastGPT)

### BISHENG

面向企业 AI 应用的开源 LLM DevOps 平台：工作流、RAG、智能体、统一模型管理、评估、SFT 与可观测性。

github 地址：[https://github.com/dataelement/bisheng](https://github.com/dataelement/bisheng)

# 15. 历史 / 归档 / 维护模式

保留以便旧书签仍能找到。新项目请优先使用上文 2026 年的替代方案。

### AutoGPT

早期自主智能体平台，后来增加了工作流。有历史意义；新的智能体工作大多已转到上文框架。

github 地址：[https://github.com/Significant-Gravitas/AutoGPT](https://github.com/Significant-Gravitas/AutoGPT)

### AutoGen

微软多智能体框架。新开发请使用 **Microsoft Agent Framework**；仅存量应用继续用 AutoGen。迁移指南见 MAF 文档。

github 地址：[https://github.com/microsoft/autogen](https://github.com/microsoft/autogen)

### Semantic Kernel

微软用于把 LLM 与 C# / Python / Java 插件结合的 SDK。后续路径是 **Microsoft Agent Framework**；SK 处于维护支持。

github 地址：[https://github.com/microsoft/semantic-kernel](https://github.com/microsoft/semantic-kernel)

### Magentic-One

通用多智能体系统（协调者 + 专长智能体），以 AutoGen 包形式发布。原 `autogen-magentic-one` 目录现为**弃用占位**；Magentic 风格编排现位于 AutoGen AgentChat，新项目请用 Microsoft Agent Framework。此处归入 AutoGen/历史，不再作为在列框架。

github 地址：[https://github.com/microsoft/autogen/tree/main/python/packages/autogen-magentic-one](https://github.com/microsoft/autogen/tree/main/python/packages/autogen-magentic-one)

### npi

早期的工具网关 API，让智能体可以操作各类软件。原 `npi-ai/npi` 现重定向到 `sheet0/npi`；2025 年后鲜有更新。更推荐 MCP 与现代运行时。

github 地址：[https://github.com/sheet0/npi](https://github.com/sheet0/npi)

### agent-protocol（AI Engineer Foundation）

早期与智能体交互的 HTTP 通用接口，与技术栈无关。长期未更新；仓库现重定向到 `agi-inc/agent-protocol`。实践中已被 A2A / MCP / AG-UI 取代。

github 地址：[https://github.com/agi-inc/agent-protocol](https://github.com/agi-inc/agent-protocol)

### Agora Protocol

论文演示协议：先用自然语言协商通信方案，再切换到约定协议。研究产物，不是生产标准。

github 地址：[https://github.com/agora-protocol/paper-demo](https://github.com/agora-protocol/paper-demo)

### naptha-sdk

用于在异构节点与模型上构建去中心化多智能体工作流的 SDK。2025 年后公开活动很少，仅作参考保留。

github 地址：[https://github.com/NapthaAI/naptha-sdk](https://github.com/NapthaAI/naptha-sdk)

### phidata（已更名）

Phidata 于 2025 年更名为 **Agno**。请不要在旧名称下开始新工作。

github 地址：[https://github.com/phidatahq/phidata](https://github.com/phidatahq/phidata) -> [https://github.com/agno-agi/agno](https://github.com/agno-agi/agno)

### KnowledgeTable（已失效）

曾用于从非结构化文档提取结构化表格。原仓库 `whyhow-ai/knowledge-table` 现已 **404**，从在列清单中移除。

原 github 地址：[https://github.com/whyhow-ai/knowledge-table](https://github.com/whyhow-ai/knowledge-table)（404）
