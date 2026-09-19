The Most Comprehensive Collection of AI Agent Infrastructure Open Source Projects [Continuously Updated]

# Introduction

The importance of AI Agents is an industry consensus. By 2026 the bottleneck is no longer only model quality: it is how agents **identify one another**, **call tools**, **delegate tasks**, **talk to users**, and **run safely**. This list covers that layered stack — not the models themselves.

This article has three purposes:

- To have a place to record excellent and creative open source projects
- To help AI Agent developers quickly find suitable infrastructure
- To help AI Agent developers quickly understand the current state of AI Agent infrastructure development

For now, we only collect open source projects, though we may include commercial products in the future.

I will continuously update this article. I maintain it as an open source project: [https://github.com/chgaowei/ai-agent-infra-list](https://github.com/chgaowei/ai-agent-infra-list).

If you know of any excellent open source projects, have different opinions about certain projects, or wish to promote your open source project, feel free to submit a PR.

We have also created an AI Agent Infra discussion group. Welcome to join:

WeChat: Please add WeChat ID changshan02, with note "AI discussion group".

Also welcome to join Discord to discuss with global tech professionals: [https://discord.gg/BNJdvMa5XE](https://discord.gg/BNJdvMa5XE)

## This update (2026-09)

**Recommendation:** treat protocols as a **layered stack**, not as rivals.

- **Identity / open internet:** [ANP 1.1](https://github.com/agent-network-protocol/AgentNetworkProtocol) (`did:wba`) in the [W3C AI Agent Protocol Community Group](https://www.w3.org/community/agentprotocol/)
- **Tasks between agents:** [A2A](https://github.com/a2aproject/A2A)
- **Tools and context:** [MCP](https://modelcontextprotocol.io)

ANP is the identity and discovery layer for agents on the open internet. A2A is the task/runtime collab layer. MCP is the tool layer. Use them together.

Naming trap: **IBM ACP** (Agent Communication Protocol) **merged into A2A in August 2025** and is no longer a separate standard. **Zed ACP** (Agent Client Protocol) and **OpenAI/Stripe Agentic Commerce Protocol** also use the letters "ACP" — they are unrelated.

### Protocol comparison (layers, not rivals)

| Protocol | Layer | What it standardizes | Notes |
| --- | --- | --- | --- |
| **ANP / did:wba** | Identity and open internet | Decentralized agent identity, discovery, descriptions, encrypted collab | Peer of A2A/MCP, not a replacement. Specs: [AgentNetworkProtocol](https://github.com/agent-network-protocol/AgentNetworkProtocol). SDK: [AgentConnect](https://github.com/agent-network-protocol/anp) (repo now `anp`). Site: [agent-network-protocol.com](https://agent-network-protocol.com/) |
| **A2A** | Agent-to-agent tasks | Agent Cards, task lifecycle, collab between opaque agents | Linux Foundation. IBM ACP merged here (Aug 2025). [a2a-protocol.org](https://a2a-protocol.org) |
| **MCP** | Agent-to-tool | Tools, resources, and prompts for LLM apps | [modelcontextprotocol.io](https://modelcontextprotocol.io) |
| **AG-UI / A2UI** | Agent-to-user UI | Event stream to the frontend (AG-UI); declarative native UI (A2UI) | Complementary, not competitors |
| **Zed ACP** | Agent-to-editor / IDE | Connect any editor to any coding agent | **Not** IBM ACP and **not** A2A |

# Overview

Classification is a snapshot of 2026. Projects may fit more than one bucket; we list each once in the detailed sections (with a few cross-links for ANP / A2A / MCP).

- Standards bodies & working groups: [W3C AI Agent Protocol CG](https://www.w3.org/community/agentprotocol/) · [AAIF](https://aaif.io) · [A2A](https://github.com/a2aproject/A2A) · [AGNTCY](https://agntcy.org) · [AP2](https://github.com/google-agentic-commerce/AP2)
- Identity & trust: [ANP](https://github.com/agent-network-protocol/AgentNetworkProtocol) · [did:wba](https://github.com/agent-network-protocol/AgentNetworkProtocol) · [AgentConnect](https://github.com/agent-network-protocol/anp) · [W3C DID](https://www.w3.org/TR/did/)
- Agent-to-agent protocols: [ANP](https://github.com/agent-network-protocol/AgentNetworkProtocol) · [A2A](https://github.com/a2aproject/A2A)
- Agent-to-tool / MCP: [MCP spec](https://github.com/modelcontextprotocol/modelcontextprotocol) · [servers](https://github.com/modelcontextprotocol/servers) · [registry](https://registry.modelcontextprotocol.io) · [goose](https://github.com/block/goose) · [AGENTS.md](https://github.com/agentsmd/agents.md) · [agentgateway](https://github.com/agentgateway/agentgateway)
- Agent-to-user / UI: [AG-UI](https://github.com/ag-ui-protocol/ag-ui) · [A2UI](https://a2ui.org)
- Agent-to-client / IDE: [Zed ACP](https://github.com/zed-industries/agent-client-protocol)
- Commerce & payments: [AP2](https://github.com/google-agentic-commerce/AP2) · [Agentic Commerce Protocol](https://github.com/agentic-commerce-protocol/agentic-commerce-protocol) · [x402](https://github.com/x402-foundation/x402)
- Frameworks & orchestration: [OpenAI Agents SDK](https://github.com/openai/openai-agents-python) · [Google ADK](https://github.com/google/adk-python) · [Claude Agent SDK](https://github.com/anthropics/claude-agent-sdk-python) · [Microsoft Agent Framework](https://github.com/microsoft/agent-framework) · [LangGraph](https://github.com/langchain-ai/langgraph) · [LangChain](https://github.com/langchain-ai/langchain) · [LlamaIndex](https://github.com/run-llama/llama_index) · [Agno](https://github.com/agno-agi/agno) · [Pydantic AI](https://github.com/pydantic/pydantic-ai) · [Mastra](https://github.com/mastra-ai/mastra) · [Qwen-Agent](https://github.com/QwenLM/Qwen-Agent) · [Strands](https://github.com/strands-agents/sdk-python) · [Haystack](https://github.com/deepset-ai/haystack) · [DSPy](https://github.com/stanfordnlp/dspy) · [Inngest](https://github.com/inngest/inngest) · [Prefect](https://github.com/PrefectHQ/prefect) · [TEN-Agent](https://github.com/TEN-framework/ten-framework) · [AgentStack](https://github.com/agentstack-ai/AgentStack)
- Multi-agent: [CrewAI](https://github.com/crewAIInc/crewAI) · [CAMEL](https://github.com/camel-ai/camel) · [MetaGPT](https://github.com/FoundationAgents/MetaGPT) (also LangGraph / Microsoft Agent Framework)
- Memory & RAG: [mem0](https://github.com/mem0ai/mem0) · [Graphiti](https://github.com/getzep/graphiti) · [Letta](https://github.com/letta-ai/letta) · [RAGFlow](https://github.com/infiniflow/ragflow) · [Cognee](https://github.com/topoteretes/cognee) · [DB-GPT](https://github.com/eosphoros-ai/DB-GPT) · [GraphRAG](https://github.com/microsoft/graphrag) · [fast-graphrag](https://github.com/circlemind-ai/fast-graphrag) · [LightRAG](https://github.com/HKUDS/LightRAG) · [nano-graphrag](https://github.com/gusye1234/nano-graphrag) · [Milvus](https://github.com/milvus-io/milvus) · [Weaviate](https://github.com/weaviate/weaviate) · [Chroma](https://github.com/chroma-core/chroma)
- Browser & computer use: [Scrapeless](https://github.com/scrapeless-ai) · [browser-use](https://github.com/browser-use/browser-use) · [Skyvern](https://github.com/Skyvern-AI/skyvern) · [Open-AutoGLM](https://github.com/zai-org/Open-AutoGLM) · [Crawlee](https://github.com/apify/crawlee) · [Browserless](https://github.com/browserless/browserless) · [AgentQL](https://github.com/tinyfish-io/agentql)
- Runtimes, sandboxes & gateways: [Daytona](https://github.com/daytonaio/daytona) · [E2B](https://github.com/e2b-dev/E2B) · [SandBase Harness](https://github.com/sandbaseai/sandbase-harness) · [Bifrost](https://github.com/maximhq/bifrost) · [YYLO](https://github.com/yylo-dev/yylo) · [goose](https://github.com/block/goose) · [agentgateway](https://github.com/agentgateway/agentgateway)
- Observability & evals: [Langfuse](https://github.com/langfuse/langfuse) · [Phoenix](https://github.com/Arize-ai/phoenix) · [AgentOps](https://github.com/AgentOps-AI/agentops) · [OpenTelemetry GenAI conventions](https://github.com/open-telemetry/semantic-conventions-genai)
- Visual / low-code platforms: [n8n](https://github.com/n8n-io/n8n) · [Coze Studio](https://github.com/coze-dev/coze-studio) · [Dify](https://github.com/langgenius/dify) · [FastGPT](https://github.com/labring/FastGPT) · [BISHENG](https://github.com/dataelement/bisheng)
- Historical / archived / maintenance-mode: [AutoGPT](https://github.com/Significant-Gravitas/AutoGPT) · [AutoGen](https://github.com/microsoft/autogen) · [Semantic Kernel](https://github.com/microsoft/semantic-kernel) · [Magentic-One](https://github.com/microsoft/autogen/tree/main/python/packages/autogen-magentic-one) · [npi](https://github.com/sheet0/npi) · [agent-protocol](https://github.com/agi-inc/agent-protocol) · [Agora Protocol](https://github.com/agora-protocol/paper-demo) · [naptha-sdk](https://github.com/NapthaAI/naptha-sdk)


# 1. Standards bodies & working groups

### W3C AI Agent Protocol Community Group

W3C Community Group developing open, interoperable protocols so agents can discover, identify, and collaborate on the Web. ANP / `did:wba` work is incubated here.

Site: [https://www.w3.org/community/agentprotocol/](https://www.w3.org/community/agentprotocol/)

Drafts: [https://w3c-cg.github.io/ai-agent-protocol/](https://w3c-cg.github.io/ai-agent-protocol/)

### AAIF (Agentic AI Foundation)

Industry foundation at [aaif.io](https://aaif.io) working on operationalizing agentic AI (identity and trust, observability, commerce, security, workflows). Hosts and coordinates several agentic open-source efforts, including goose.

Site: [https://aaif.io](https://aaif.io)

### A2A (Agent2Agent Protocol)

Open protocol for communication between opaque agentic applications (Agent Cards, task lifecycle). Now a Linux Foundation project. IBM's Agent Communication Protocol (ACP) merged into A2A in August 2025.

GitHub repository: [https://github.com/a2aproject/A2A](https://github.com/a2aproject/A2A)

Site: [https://a2a-protocol.org](https://a2a-protocol.org)

### AGNTCY

Linux Foundation project building "Internet of Agents" infrastructure: discovery, identity, messaging (SLIM), and observability across vendors and frameworks.

Site: [https://agntcy.org](https://agntcy.org)

GitHub repository: [https://github.com/agntcy](https://github.com/agntcy)

### AP2 (Agent Payments Protocol)

Google's open protocol for secure, interoperable AI-driven payments and authorization (mandates) between agents and merchants. Complements A2A / MCP; it is not an agent-to-agent task protocol.

GitHub repository: [https://github.com/google-agentic-commerce/AP2](https://github.com/google-agentic-commerce/AP2)

# 2. Identity & trust

This is the open-internet layer: how an agent proves who it is, is discovered, and talks securely **across platforms**, without a central IdP. **ANP / `did:wba` / AgentConnect** belong here — not under A2A.

### Agent Network Protocol (ANP)

Open protocol suite for agent identity, naming, discovery, negotiation, and collaboration on the open internet. The 1.1 spec line covers `did:wba`, WNS handles, agent description, agent discovery, end-to-end messaging, and agent payments. Incubated with the W3C AI Agent Protocol CG. Complements A2A (tasks) and MCP (tools); it does not replace them.

GitHub repository: [https://github.com/agent-network-protocol/AgentNetworkProtocol](https://github.com/agent-network-protocol/AgentNetworkProtocol)

Site: [https://agent-network-protocol.com/](https://agent-network-protocol.com/)

W3C CG: [https://www.w3.org/community/agentprotocol/](https://www.w3.org/community/agentprotocol/)

### did:wba

Web-based DID method used by ANP for cross-platform agent identity and authentication (W3C DID compatible, designed for agents on existing HTTPS infrastructure). Specified in the ANP 1.1 suite.

GitHub repository: [https://github.com/agent-network-protocol/AgentNetworkProtocol](https://github.com/agent-network-protocol/AgentNetworkProtocol)

### AgentConnect

Multi-language SDK and reference implementation of ANP: `did:wba` identity, agent description, discovery, RPC, verifiable proofs, and end-to-end encrypted communication. The GitHub repo is now published as `anp`; historical `chgaowei/AgentConnect` and `agent-network-protocol/AgentConnect` redirect there.

GitHub repository: [https://github.com/agent-network-protocol/anp](https://github.com/agent-network-protocol/anp)

Homepage: [https://agent-network-protocol.com/](https://agent-network-protocol.com/)

### W3C Decentralized Identifiers (DID)

W3C standard for decentralized identifiers. ANP's `did:wba` is a DID method; many agent identity designs reuse DID / VC rather than inventing a new ID scheme.

Specification: [https://www.w3.org/TR/did/](https://www.w3.org/TR/did/)

GitHub repository: [https://github.com/w3c/did](https://github.com/w3c/did)

# 3. Agent-to-agent protocols

ANP and A2A are **layers**, not rivals: ANP covers identity/discovery on the open internet; A2A covers structured task exchange between opaque agents (often inside a platform or after identity is established).

### Agent Network Protocol (ANP)

See [Identity & trust](#2-identity--trust). At the application layer ANP defines agent description and discovery so heterogeneous agents can find and invoke each other.

GitHub repository: [https://github.com/agent-network-protocol/AgentNetworkProtocol](https://github.com/agent-network-protocol/AgentNetworkProtocol)

### A2A

See [Standards](#1-standards-bodies--working-groups). Use A2A when you need a shared task model (submit / work / complete) and Agent Cards between existing agent runtimes.

GitHub repository: [https://github.com/a2aproject/A2A](https://github.com/a2aproject/A2A)

Site: [https://a2a-protocol.org](https://a2a-protocol.org)

# 4. Agent-to-tool / MCP

### Model Context Protocol (MCP)

Open protocol for connecting LLM applications to external tools, data, and prompts. De-facto tool layer for agents in 2026; complementary to ANP (identity) and A2A (tasks).

Site: [https://modelcontextprotocol.io](https://modelcontextprotocol.io)

Specification: [https://github.com/modelcontextprotocol/modelcontextprotocol](https://github.com/modelcontextprotocol/modelcontextprotocol)

Official servers: [https://github.com/modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers)

GitHub organization: [https://github.com/modelcontextprotocol](https://github.com/modelcontextprotocol)

### MCP servers

Reference and community MCP server implementations (filesystem, git, browsers, SaaS connectors, and more).

GitHub repository: [https://github.com/modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers)

### MCP Registry

Official metadata registry for publicly listed MCP servers (preview). Used by clients and marketplaces to discover servers.

Registry: [https://registry.modelcontextprotocol.io](https://registry.modelcontextprotocol.io)

### goose

Open-source, extensible agent from Block (now under AAIF) that can install, execute, edit, and test with any LLM. A practical MCP-native coding/on-machine agent.

GitHub repository: [https://github.com/block/goose](https://github.com/block/goose) (canonical: [https://github.com/aaif-goose/goose](https://github.com/aaif-goose/goose))

### AGENTS.md

A simple, open markdown format for guiding coding agents about a repo (conventions, commands, pitfalls). Complementary to MCP: it is project-local instruction, not a tool protocol.

GitHub repository: [https://github.com/agentsmd/agents.md](https://github.com/agentsmd/agents.md)

Site: [https://agents.md](https://agents.md)

### agentgateway

Open-source agentic proxy / gateway for AI agents and MCP servers (routing, policy, and connectivity in front of tools).

GitHub repository: [https://github.com/agentgateway/agentgateway](https://github.com/agentgateway/agentgateway)

# 5. Agent-to-user / UI

### AG-UI

Agent-User Interaction Protocol: a lightweight event-based standard for connecting agent backends to user-facing apps (streaming text, tool calls, shared state, human-in-the-loop). Complements MCP (tools) and A2A (agent collab).

GitHub repository: [https://github.com/ag-ui-protocol/ag-ui](https://github.com/ag-ui-protocol/ag-ui)

### A2UI

Agent-to-User Interface protocol (Google, with CopilotKit and others): agents send declarative UI descriptions that clients render with native widgets, instead of shipping executable UI code. Often carried inside AG-UI or A2A streams.

Site: [https://a2ui.org](https://a2ui.org)

# 6. Agent-to-client / IDE

**Not A2A. Not IBM ACP.** Zed's Agent Client Protocol (also abbreviated ACP) is an editor-to-agent wire protocol.

### Agent Client Protocol (Zed ACP)

Protocol for connecting any editor/IDE to any coding agent. Originated at Zed; the spec repo now lives under the `agentclientprotocol` org. Do not confuse with IBM ACP (merged into A2A) or the OpenAI/Stripe Agentic Commerce Protocol.

GitHub repository: [https://github.com/zed-industries/agent-client-protocol](https://github.com/zed-industries/agent-client-protocol) (canonical: [https://github.com/agentclientprotocol/agent-client-protocol](https://github.com/agentclientprotocol/agent-client-protocol))

# 7. Commerce & payments

Short section: how agents pay and check out. This is not identity and not A2A.

### AP2 (Agent Payments Protocol)

See [Standards](#1-standards-bodies--working-groups). Authorization / payments layer for agent-driven purchases.

GitHub repository: [https://github.com/google-agentic-commerce/AP2](https://github.com/google-agentic-commerce/AP2)

### Agentic Commerce Protocol (OpenAI / Stripe)

Open standard (also abbreviated **ACP**) for connecting buyers, their agents, and businesses to complete purchases. Maintained by OpenAI and Stripe. Unrelated to IBM ACP and Zed ACP.

GitHub repository: [https://github.com/agentic-commerce-protocol/agentic-commerce-protocol](https://github.com/agentic-commerce-protocol/agentic-commerce-protocol)

### x402 (settlement rail for agent payments)

The agent-payment settlement protocol: a merchant returns HTTP 402 Payment Required with a `PAYMENT-REQUIRED` header declaring the asset, amount and payee; the agent pays and retries. Settlement-rail agnostic — any asset the counterparty accepts. A feeless, instant self-custodied rail that works with x402 is **Nano (XNO)**, a peer-to-peer layer-1 with no issuer that cannot freeze funds, via the exact scheme on `nano:mainnet`.

Spec: [https://github.com/x402-foundation/x402](https://github.com/x402-foundation/x402)
GitHub repository: [https://github.com/PANDeveloper001/openai-agents-nano-x402](https://github.com/PANDeveloper001/openai-agents-nano-x402) (OpenAI Agents SDK payer for x402)

# 8. Frameworks & orchestration

LangChain remains widely used; **LangGraph is the agent runtime** in that family. Microsoft's new default is **Microsoft Agent Framework** (AutoGen and Semantic Kernel are in Historical). Phidata was renamed **Agno**.

### OpenAI Agents SDK

Lightweight Python SDK for building agent and multi-agent workflows on OpenAI models (handoffs, tools, tracing).

GitHub repository: [https://github.com/openai/openai-agents-python](https://github.com/openai/openai-agents-python)

### Google ADK (Agent Development Kit)

Code-first Python toolkit for building, evaluating, and deploying agents, with first-class ties to Gemini, A2A, MCP, and Vertex.

GitHub repository: [https://github.com/google/adk-python](https://github.com/google/adk-python)

### Claude Agent SDK

Anthropic's Python SDK for building agents with Claude (tools, sessions, Claude Code-style harness patterns).

GitHub repository: [https://github.com/anthropics/claude-agent-sdk-python](https://github.com/anthropics/claude-agent-sdk-python)

### Microsoft Agent Framework

Microsoft's production framework for building, orchestrating, and deploying agents and multi-agent workflows in Python and .NET. Successor path for AutoGen and Semantic Kernel.

GitHub repository: [https://github.com/microsoft/agent-framework](https://github.com/microsoft/agent-framework)

### LangGraph

Library for stateful, cyclic agent and multi-agent applications (loops, control, persistence). This is LangChain's agent runtime; prefer it over raw chains for agents.

GitHub repository: [https://github.com/langchain-ai/langgraph](https://github.com/langchain-ai/langgraph)

### LangChain

General LLM application framework (models, prompts, retrieval, tools). Still the integration surface for many stacks; for agents, use LangGraph.

GitHub repository: [https://github.com/langchain-ai/langchain](https://github.com/langchain-ai/langchain)

### LlamaIndex

Data framework for connecting LLMs to private data (indexes, retrieval, agentic RAG workflows).

GitHub repository: [https://github.com/run-llama/llama_index](https://github.com/run-llama/llama_index)

### Agno (formerly phidata)

Python framework for building multimodal agents and agent teams with memory, knowledge, and tools. Phidata was renamed Agno in 2025; the old `phidatahq/phidata` repo redirects here.

GitHub repository: [https://github.com/agno-agi/agno](https://github.com/agno-agi/agno)

### Pydantic AI

Typed Python agent framework from the Pydantic team: agents, tools, and structured output with Pydantic models.

GitHub repository: [https://github.com/pydantic/pydantic-ai](https://github.com/pydantic/pydantic-ai)

### Mastra

TypeScript framework for AI applications and agents (workflows, tools, evals, and observability in JS/TS).

GitHub repository: [https://github.com/mastra-ai/mastra](https://github.com/mastra-ai/mastra)

### Qwen-Agent

Agent framework and applications on Qwen (>=3.0): function calling, MCP, code interpreter, RAG, and a Chrome extension.

GitHub repository: [https://github.com/QwenLM/Qwen-Agent](https://github.com/QwenLM/Qwen-Agent)

### Strands

Open-source SDK for production agents in Python (and TypeScript), model- and cloud-agnostic. The `sdk-python` repo now redirects to `harness-sdk`.

GitHub repository: [https://github.com/strands-agents/sdk-python](https://github.com/strands-agents/sdk-python)

### Haystack

Pipeline/agent orchestration for production LLM apps: connect models, converters, and vector stores into RAG, QA, and agents.

GitHub repository: [https://github.com/deepset-ai/haystack](https://github.com/deepset-ai/haystack)

### DSPy

Stanford framework that turns declarative LM programs into self-optimizing pipelines, instead of hand-written prompts.

GitHub repository: [https://github.com/stanfordnlp/dspy](https://github.com/stanfordnlp/dspy)

### Inngest

Workflow orchestration for stateful step functions and AI workflows on serverless, servers, or the edge.

GitHub repository: [https://github.com/inngest/inngest](https://github.com/inngest/inngest)

### Prefect

Python workflow orchestration: turn scripts into durable production pipelines that retry and adapt.

GitHub repository: [https://github.com/PrefectHQ/prefect](https://github.com/PrefectHQ/prefect)

### TEN-Agent

Open-source realtime multimodal / voice agent framework (RTC + low-latency conversation). The GitHub repo was renamed to `ten-framework`; the `TEN-Agent` path redirects.

GitHub repository: [https://github.com/TEN-framework/ten-framework](https://github.com/TEN-framework/ten-framework)  
(historical `TEN-Agent` path redirects here; keep TEN-Agent as the product name)

### AgentStack

CLI for bootstrapping AI agent projects and generating boilerplate. Less active than at first listing. The GitHub org is now `agentstack-ai`.

GitHub repository: [https://github.com/agentstack-ai/AgentStack](https://github.com/agentstack-ai/AgentStack)

# 9. Multi-agent

Short: most new work happens inside **LangGraph**, **Microsoft Agent Framework**, or **CrewAI**. The entries below are dedicated multi-agent projects still worth knowing.

### CrewAI

Multi-agent framework for role-based crews: define agents, tasks, and processes so several agents collaborate on a workflow.

GitHub repository: [https://github.com/crewAIInc/crewAI](https://github.com/crewAIInc/crewAI)

### CAMEL

Early LLM multi-agent framework that grew into a general toolkit for building and studying communicating agents.

GitHub repository: [https://github.com/camel-ai/camel](https://github.com/camel-ai/camel)

### MetaGPT

Multi-agent "software company" pattern: one-line requirement in, roles (PM / architect / engineer) and SOPs out. Repository moved from `geekan/MetaGPT` to FoundationAgents/MetaGPT.

GitHub repository: [https://github.com/FoundationAgents/MetaGPT](https://github.com/FoundationAgents/MetaGPT)

Also see: [LangGraph](#langgraph), [Microsoft Agent Framework](#microsoft-agent-framework), [Agno](#agno-formerly-phidata).

# 10. Memory & RAG

### mem0

Memory layer for assistants and agents: store and retrieve long-term personalized facts so responses stay relevant across sessions.

GitHub repository: [https://github.com/mem0ai/mem0](https://github.com/mem0ai/mem0)

### Graphiti

Real-time knowledge graphs for AI agents (temporally-aware graph memory from ongoing activity, not batch-only GraphRAG).

GitHub repository: [https://github.com/getzep/graphiti](https://github.com/getzep/graphiti)

### Letta (formerly MemGPT)

Framework for stateful LLM agents with long-term memory, self-managed context, and connections to external data.

GitHub repository: [https://github.com/letta-ai/letta](https://github.com/letta-ai/letta)

### RAGFlow

Open-source RAG engine built on deep document understanding, with citations for complex enterprise files.

GitHub repository: [https://github.com/infiniflow/ragflow](https://github.com/infiniflow/ragflow)

### Cognee

ECL (Extract, Cognify, Load) pipelines that turn conversations, documents, and transcripts into a retrievable memory graph.

GitHub repository: [https://github.com/topoteretes/cognee](https://github.com/topoteretes/cognee)

### DB-GPT

AI-native data-app framework: Text2SQL, RAG, multi-model management, and AWEL agent workflow orchestration over databases.

GitHub repository: [https://github.com/eosphoros-ai/DB-GPT](https://github.com/eosphoros-ai/DB-GPT)

### GraphRAG

Microsoft data pipeline that uses LLMs to extract a knowledge graph from unstructured text for retrieval.

GitHub repository: [https://github.com/microsoft/graphrag](https://github.com/microsoft/graphrag)

### fast-graphrag

Lean, incremental GraphRAG-style retrieval aimed at agent workflows (interpretable, lower-cost updates).

GitHub repository: [https://github.com/circlemind-ai/fast-graphrag](https://github.com/circlemind-ai/fast-graphrag)

### LightRAG

Simple, fast graph-enhanced RAG engine.

GitHub repository: [https://github.com/HKUDS/LightRAG](https://github.com/HKUDS/LightRAG)

### nano-graphrag

Smaller, hackable GraphRAG implementation that keeps the core idea without the official repo's weight.

GitHub repository: [https://github.com/gusye1234/nano-graphrag](https://github.com/gusye1234/nano-graphrag)

### Milvus

High-performance open-source vector database for storing and searching embeddings at scale.

GitHub repository: [https://github.com/milvus-io/milvus](https://github.com/milvus-io/milvus)

### Weaviate

Open-source vector database: objects + vectors, hybrid search with filters, cloud-native operations.

GitHub repository: [https://github.com/weaviate/weaviate](https://github.com/weaviate/weaviate)

### Chroma

AI-native open-source embedding database, commonly used as a local/dev vector store for RAG.

GitHub repository: [https://github.com/chroma-core/chroma](https://github.com/chroma-core/chroma)


# 11. Browser & computer use

### Scrapeless

Open-source org for agent-oriented web data collection (community PR). See their GitHub org for SDKs and related repos.

GitHub repository: [https://github.com/scrapeless-ai](https://github.com/scrapeless-ai)

### browser-use

Popular open-source project that connects LLM agents to the web.

GitHub repository: [https://github.com/browser-use/browser-use](https://github.com/browser-use/browser-use)

### Skyvern

Open-source project for LLM-driven website workflows.

GitHub repository: [https://github.com/Skyvern-AI/skyvern](https://github.com/Skyvern-AI/skyvern)

### Open-AutoGLM

Open phone-agent model and framework from Zhipu (Z.ai).

GitHub repository: [https://github.com/zai-org/Open-AutoGLM](https://github.com/zai-org/Open-AutoGLM)

### Crawlee

Node.js library (JS/TS) for building reliable web collectors that feed RAG / LLM pipelines.

GitHub repository: [https://github.com/apify/crawlee](https://github.com/apify/crawlee)

### Browserless

Docker-based Chrome service with REST APIs for screenshots, PDFs, and page extraction.

GitHub repository: [https://github.com/browserless/browserless](https://github.com/browserless/browserless)

### AgentQL

Query language for locating data and elements on pages, including authenticated and dynamic content.

GitHub repository: [https://github.com/tinyfish-io/agentql](https://github.com/tinyfish-io/agentql)

# 12. Runtimes, sandboxes & gateways

### Daytona

Secure, elastic infrastructure for running AI-generated code in isolated environments.

GitHub repository: [https://github.com/daytonaio/daytona](https://github.com/daytonaio/daytona)

### E2B

Open-source infra for running AI-generated code in isolated cloud sandboxes.

GitHub repository: [https://github.com/e2b-dev/E2B](https://github.com/e2b-dev/E2B)

### SandBase Harness

Local-first TypeScript AI agent runtime: persistent sessions, sandboxed tools, MCP, memory, credential isolation, audit logs, and execution replay. Supports local, Docker, Kubernetes, and self-hosted deploys.

GitHub repository: [https://github.com/sandbaseai/sandbase-harness](https://github.com/sandbaseai/sandbase-harness)

### Bifrost

Go-native, OpenAI-compatible AI gateway for routing requests across multiple model providers with load balancing, automatic failover, guardrails, MCP gateway support, and built-in logs, metrics, and tracing.

GitHub repository: [https://github.com/maximhq/bifrost](https://github.com/maximhq/bifrost)

### YYLO

YYLO is a command-line orchestrator for coding agents: typed task lifecycle with per-task branch/worktree isolation, validation and preflight gates, and a risk-based merge queue with sequential review, keeping repository changes receipt-backed under human merge authority. Published on npm as @yylo/cli.

GitHub repository: [https://github.com/yylo-dev/yylo](https://github.com/yylo-dev/yylo)

# 13. Observability & evals

LangSmith is a **commercial** LangChain product (tracing, datasets, evals), not listed here as OSS. Prefer Langfuse / Phoenix / OTel for open stacks.

### Langfuse

Open-source LLM engineering platform: traces, metrics, evals, prompt management, playground, datasets. Integrates with LangChain, LlamaIndex, OpenAI SDK, and others.

GitHub repository: [https://github.com/langfuse/langfuse](https://github.com/langfuse/langfuse)

### Phoenix

Open-source AI observability from Arize: tracing, evals, datasets, and troubleshooting for LLM/agent apps.

GitHub repository: [https://github.com/Arize-ai/phoenix](https://github.com/Arize-ai/phoenix)

### AgentOps

Python SDK for agent monitoring, LLM cost tracking, and benchmarking; integrates with CrewAI, LangChain, AutoGen, and others.

GitHub repository: [https://github.com/AgentOps-AI/agentops](https://github.com/AgentOps-AI/agentops)

### OpenTelemetry GenAI semantic conventions

Semantic conventions for tracing generative AI / agent workloads so traces are interoperable across vendors.

GitHub repository: [https://github.com/open-telemetry/semantic-conventions-genai](https://github.com/open-telemetry/semantic-conventions-genai)

# 14. Visual / low-code platforms

### n8n

Fair-code workflow automation with native AI nodes: visual building plus custom code, self-host or cloud.

GitHub repository: [https://github.com/n8n-io/n8n](https://github.com/n8n-io/n8n)

### Coze Studio

Open-source visual AI agent development platform (create, debug, deploy) from the Coze team.

GitHub repository: [https://github.com/coze-dev/coze-studio](https://github.com/coze-dev/coze-studio)

### Dify

Open-source LLM app platform: visual AI workflows, RAG, agents, model management, and observability, prototype to production.

GitHub repository: [https://github.com/langgenius/dify](https://github.com/langgenius/dify)

### FastGPT

Knowledge-base platform on LLMs: data processing, RAG, and visual AI workflow orchestration for Q&A systems.

GitHub repository: [https://github.com/labring/FastGPT](https://github.com/labring/FastGPT)

### BISHENG

Open-source LLM DevOps platform for enterprise apps: workflows, RAG, agents, model management, eval, SFT, and observability.

GitHub repository: [https://github.com/dataelement/bisheng](https://github.com/dataelement/bisheng)

# 15. Historical / archived / maintenance-mode

Kept so older bookmarks still resolve. Prefer the 2026 replacements noted below.

### AutoGPT

Early autonomous-agent platform that later added workflows. Historically important; most new agent work has moved to the frameworks above.

GitHub repository: [https://github.com/Significant-Gravitas/AutoGPT](https://github.com/Significant-Gravitas/AutoGPT)

### AutoGen

Microsoft's multi-agent framework. New development is **Microsoft Agent Framework**; use AutoGen only for existing apps. Migration guide is in the MAF docs.

GitHub repository: [https://github.com/microsoft/autogen](https://github.com/microsoft/autogen)

### Semantic Kernel

Microsoft SDK for mixing LLMs with C# / Python / Java plugins. Folded into **Microsoft Agent Framework** as the successor; SK remains supported in maintenance.

GitHub repository: [https://github.com/microsoft/semantic-kernel](https://github.com/microsoft/semantic-kernel)

### Magentic-One

Generalist multi-agent system (Orchestrator + specialist agents) shipped as an AutoGen package. The original `autogen-magentic-one` tree is a **deprecation stub**; Magentic-style orchestration now lives in AutoGen AgentChat and, for new work, in Microsoft Agent Framework. Folded here under AutoGen rather than listed as a live framework.

GitHub repository: [https://github.com/microsoft/autogen/tree/main/python/packages/autogen-magentic-one](https://github.com/microsoft/autogen/tree/main/python/packages/autogen-magentic-one)

### npi

Early tool-gateway API so agents could act in software apps. Historical; the live repo is `sheet0/npi` (old `npi-ai/npi` redirects). Prefer MCP plus modern runtimes.

GitHub repository: [https://github.com/sheet0/npi](https://github.com/sheet0/npi)

### agent-protocol (AI Engineer Foundation)

Early HTTP interface for interacting with agents, stack-agnostic. Long stale. Live URL: `agi-inc/agent-protocol` (old AI-Engineer-Foundation path redirects). Unrelated to ANP, A2A, Zed ACP, or IBM ACP. Superseded in practice by A2A / MCP / AG-UI.

GitHub repository: [https://github.com/agi-inc/agent-protocol](https://github.com/agi-inc/agent-protocol)

### Agora Protocol

Paper-demo protocol: negotiate a communication scheme in natural language, then switch to the agreed protocol. Research artifact, not a production standard.

GitHub repository: [https://github.com/agora-protocol/paper-demo](https://github.com/agora-protocol/paper-demo)

### naptha-sdk

SDK for decentralized multi-agent workflows across heterogeneous nodes and models. Little public activity since 2025; kept for reference.

GitHub repository: [https://github.com/NapthaAI/naptha-sdk](https://github.com/NapthaAI/naptha-sdk)

### phidata (renamed)

Phidata was renamed **Agno** in 2025. Do not start new work under the old name.

GitHub repository: [https://github.com/phidatahq/phidata](https://github.com/phidatahq/phidata) -> [https://github.com/agno-agi/agno](https://github.com/agno-agi/agno)

### KnowledgeTable (gone)

Open-source package for extracting structured tables from unstructured documents. The owner-original repo `whyhow-ai/knowledge-table` now returns **404** and is dropped from the live list.

Former GitHub repository: [https://github.com/whyhow-ai/knowledge-table](https://github.com/whyhow-ai/knowledge-table) (404)
