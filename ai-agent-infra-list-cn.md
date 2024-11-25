全网最全的AI Agent Infra开源项目汇总[持续更新]

# 前言

AI Agent的重要性是行业共识，当前最大的瓶颈在模型能力特别是模型的推理能力。不过随着o1的发布，也许我们可以把一部分目光转到其他的瓶颈上。这是我写这篇文章的初衷。

我在这篇文章中讨论的AI Agent Infra（智能体基础设施），并不包含模型，而主要是除模型之外的其他基础设施，比如记忆、工具、框架、容器等等。

之所以写这篇文章，是因为平时经常会看到一些非常不错的开源项目，但是没有地方记录。有的时候想找一个开源项目，又不好找。所以这篇文章的目的有三个：
- 找个地方记录优秀的、有创意的开源项目
- 帮助AI Agent开发者快速找到合适的基础设施
- 帮助AI Agent开发者快速了解AI Agent基础设施的发展现状

我们暂时只收集开源项目，未来也可能会收集商业产品。

这篇文章我会持续更新，也许会一个月更新一次，每月会更新一些优秀的、有创意的项目。另外，我准备以开源项目的方式来维护这篇文章。我创建了一个github仓库，地址是：[https://github.com/chgaowei/ai-agent-infra-list](https://github.com/chgaowei/ai-agent-infra-list)。

如果你也知道一些优秀的开源项目，或者你对某个项目有不一样的评价，或者你希望推广你的开源项目，欢迎提交PR。

我们也建了一个AI Agent Infra的交流群，欢迎加入一起讨论：

微信：请添加微信号 changshan02 ，备注AI交流入群。

也欢迎加入Discord，和全球技术人一起交流：（https://discord.gg/BNJdvMa5XE）[https://discord.gg/BNJdvMa5XE]

## 本月推荐项目
每月更新的时候，都会推荐一个或多个项目。本月先推荐下我们的开源项目 **AgentConnect**，欢迎关注:
AgentConnect 的愿景是定义智能体的连接方式，并为数十亿智能体构建一个开放、安全和高效的协作网络。AgentConnect提供以下能力：
- 基于W3C DID规范提供了一个去中心化的身份认证方式，可以让智能体掌握自己的身份，并且与其他任意智能体进行跨平台的、安全的、低成本的身份验证。
- 支持基于DID的端到端加密通信，确保智能体之间的通信安全。
- 支持元协议协商，允许智能体之间使用自然语言协商双方能力以及通信协议，并且使用LLM生成代码进行协议通信。这有助于实现自组织自协商的智能体网络。
- 支持应用层协议管理，可以方便的对协议以及协议代码进行加载、更新、卸载，有助于提高智能体之间的通信效率。

github 地址：[https://github.com/chgaowei/AgentConnect](https://github.com/chgaowei/AgentConnect)

技术整体介绍：[https://github.com/chgaowei/AgentNetworkProtocol/blob/main/chinese/00-AgentNetworkProtocol%E6%8A%80%E6%9C%AF%E8%93%9D%E5%9B%BE.md](https://github.com/chgaowei/AgentNetworkProtocol/blob/main/chinese/00-AgentNetworkProtocol%E6%8A%80%E6%9C%AF%E8%93%9D%E5%9B%BE.md)

# 概览

整体的分类结构上，我会按照框架、规划、记忆、工具分为四大类，每个大类下再根据不同的维度细分。分类未必合理，后面可能会做些调整。

- 框架
  - 一站式平台：[dify](https://github.com/langgenius/dify)    [AutoGpt](https://github.com/Significant-Gravitas/AutoGPT)     [FastGPT](https://github.com/labring/FastGPT)     [BISHENG](https://github.com/dataelement/bisheng)

  - 开发框架：[langchain](https://github.com/langchain-ai/langchain)     [llama_index](https://github.com/run-llama/llama_index)     [semantic-kernel](https://github.com/microsoft/semantic-kernel)     [LangGraph](https://github.com/langchain-ai/langgraph)     [phidata](https://github.com/phidatahq/phidata)     [haystack](https://github.com/deepset-ai/haystack)    
  - 多智能体框架：[crewai](https://github.com/crewAIInc/crewAI)     [Autogen](https://github.com/microsoft/autogen)     [Camel](https://github.com/camel-ai/camel)     [Magentic-One](https://github.com/microsoft/autogen/tree/main/python/packages/autogen-magentic-one)     [MetaGPT](https://github.com/geekan/MetaGPT)    

  - 构建工具：[AgentOps](https://github.com/AgentOps-AI/agentops)     [AgentStack](https://github.com/AgentOps-AI/AgentStack)     [dspy](https://github.com/stanfordnlp/dspy)     [phoenix](https://github.com/Arize-ai/phoenix)    

- 规划
  - 工作流编排：[inngest](https://github.com/inngest/inngest)     [prefect](https://github.com/PrefectHQ/prefect)    

- 记忆
  - 记忆引擎：[mem0](https://github.com/mem0ai/mem0)     [DB-GPT](https://github.com/eosphoros-ai/DB-GPT)     [Letta](https://github.com/letta-ai/letta)     [RAGFlow](https://github.com/infiniflow/ragflow)     [Cognee](https://github.com/topoteretes/cognee)     [KnowledgeTable](https://github.com/whyhow-ai/knowledge-table)    

  - GraphRAG技术：[graphrag](https://github.com/microsoft/graphrag)     [fast-graphrag](https://github.com/circlemind-ai/fast-graphrag)     [LightRAG](https://github.com/HKUDS/LightRAG)     [nano-graphrag](https://github.com/gusye1234/nano-graphrag)    

  - 存储：[Milvus](https://github.com/milvus-io/milvus)     [Weaviate](https://github.com/weaviate/weaviate)     [Chroma](https://github.com/chroma-core/chroma)    

- 工具
  - 智能体网络与通信：[AgentConnect](https://github.com/chgaowei/AgentConnect)     [AgentNetworkProtocol](https://github.com/chgaowei/AgentNetworkProtocol)     [Agora Protocol](https://github.com/agora-protocol/paper-demo)     [agent-protocol](https://github.com/AI-Engineer-Foundation/agent-protocol)     [naptha-sdk](https://github.com/NapthaAI/naptha-sdk)    

  - computer use API：[npi](https://github.com/npi-ai/npi)    

  - 身份验证：[AgentConnect](https://github.com/chgaowei/AgentConnect)    

  - 运行时：[E2B](https://github.com/e2b-dev/E2B)    

  - 网页浏览：[Crawlee](https://github.com/apify/crawlee)     [Browserless](https://github.com/browserless/browserless)     [AgentQL](https://github.com/tinyfish-io/agentql)    

# 框架

## 一站式平台

### dify
Dify 是一个开源的 LLM 应用程序开发平台。Dify 的直观界面结合了 AI 工作流程、RAG 管道、代理功能、模型管理、可观测性功能等，让您可以快速从原型到生产。
github 地址：[https://github.com/langgenius/dify](https://github.com/langgenius/dify)

### AutoGpt
AutoGPT 是一个强大的平台，可用于创建、部署和管理持续运行的 AI 智能体，从而实现复杂工作流程的自动化。AutoGpt已经转型，从最早的demo，增加了工作流能力。
github 地址：[https://github.com/Significant-Gravitas/AutoGPT](https://github.com/Significant-Gravitas/AutoGPT)

### fastgpt
FastGPT 是一个基于大型语言模型 (LLMs) 的知识型平台，提供一整套开箱即用的功能，如数据处理、RAG 检索以及可视化的 AI 工作流编排。借助 FastGPT，用户可以轻松开发和部署复杂的问答系统，而无需进行繁琐的设置或配置工作。
github 地址：[https://github.com/labring/FastGPT](https://github.com/labring/FastGPT)

### BISHENG
BISHENG 是一个面向下一代企业 AI 应用的开源 LLM DevOps 平台。其强大且全面的功能包括：生成式 AI 工作流、RAG、智能体、统一模型管理、评估、SFT、数据集管理、企业级系统管理、可观测性等。
github 地址：[https://github.com/dataelement/bisheng](https://github.com/dataelement/bisheng)

## 开发框架

### langchain
LangChain 是一个开发框架，专为构建基于大语言模型的应用程序设计。它提供了一套工具和组件，包括 Models（模型）、Prompts（提示）、Indexes（索引）、Memory（记忆）、Chains（链）和 Agents（代理）等。
github 地址：[https://github.com/langchain-ai/langchain](https://github.com/langchain-ai/langchain)

### llama_index
LlamaIndex（GPT Index）是一个为你的LLM应用构建的数据框架，用于将外部数据与大语言模型（LLM）结合。它支持从各种数据源（如文档、数据库等）创建索引，优化信息检索过程。
github 地址：[https://github.com/run-llama/llama_index](https://github.com/run-llama/llama_index)

### semantic-kernel
Semantic Kernel 是一个 SDK，旨在将大语言模型（LLM）与传统编程语言（如 C#、Python 和 Java）集成，并支持插件的自动协调。它提供了抽象层来管理 AI 服务和记忆存储，支持多种平台和向量数据库，并能自动生成并执行基于 LLM 生成的计划。
github 地址：[https://github.com/microsoft/semantic-kernel](https://github.com/microsoft/semantic-kernel)

### LangGraph
LangGraph是一个用于构建具有状态和多角色应用程序的库，主要用于创建智能体和多智能体工作流。与其他LLM框架相比，它提供了三个核心优势：循环、可控性和持久性。LangGraph允许你定义包含循环的工作流，这是大多数智能体架构所必需的，这使得它与基于DAG（有向无环图）的解决方案有所区别。
github 地址：[https://github.com/langchain-ai/langgraph](https://github.com/langchain-ai/langgraph)

### phidata
Phidata 是一个用于构建智能体系统的框架，允许工程师创建具备记忆、知识、工具和推理能力的智能体。它支持构建能够协同工作的智能体团队，并通过美观的用户界面与智能体进行交互。Phidata 还提供监控、评估和优化智能体的功能，并帮助开发包含 API、数据库和向量数据库的智能体应用。
github 地址：[https://github.com/phidatahq/phidata](https://github.com/phidatahq/phidata)

### haystack
AI 编排框架，用于构建可定制、生产就绪的大语言模型（LLM）应用程序。将组件（模型、向量数据库、文件转换器）连接到可以与数据互动的管道或智能体。通过先进的检索方法，它最适合用于构建 RAG（检索增强生成）、问答、语义搜索或对话智能体聊天机器人。
github 地址：[https://github.com/deepset-ai/haystack](https://github.com/deepset-ai/haystack)

## 多智能体框架

### crewai
CrewAI 是一个多智能体框架，旨在通过协调多个AI智能体协作，完成复杂的任务和工作流。该框架通过任务管理和流程控制，允许用户定义和执行自动化的智能体协作。
github 地址：[https://github.com/crewAIInc/crewAI](https://github.com/crewAIInc/crewAI)

### Autogen
AutoGen 是一个开源框架，用于构建AI智能体系统。它简化了事件驱动、分布式、可扩展和具备韧性的智能体应用程序的创建。AutoGen 允许快速构建系统，在这些系统中，AI智能体能够协作并自主执行任务，或者在人工监督下完成任务。
github 地址：[https://github.com/microsoft/autogen](https://github.com/microsoft/autogen)

### Camel
CAMEL是最早基于大语言模型（LLM）的多智能体框架之一，现已成为一个通用的框架，用于构建和使用基于LLM的智能体解决现实世界中的任务。
github 地址：[https://github.com/camel-ai/camel](https://github.com/camel-ai/camel)

### Magentic-One
Magentic-One 是一个高性能的通用智能体系统，旨在解决复杂任务。它采用多智能体架构，其中主智能体“协调者”（Orchestrator）负责指挥其他四个专门的智能体来完成任务。协调者负责规划、跟踪进展，并在出现错误时重新规划，同时指导这些专门的智能体执行如操作网页浏览器、浏览本地文件或编写和执行Python代码等任务。
github 地址：[https://github.com/microsoft/autogen/tree/main/python/packages/autogen-magentic-one](https://github.com/microsoft/autogen/tree/main/python/packages/autogen-magentic-one)

### MetaGPT
MetaGPT 以一行需求作为输入，输出用户故事/竞争分析/需求/数据结构/API/文档等。MetaGPT 包括产品经理 / 架构师 / 项目经理 / 工程师。它提供了软件公司的整个过程以及精心编排的 SOP。
github 地址：[https://github.com/geekan/MetaGPT](https://github.com/geekan/MetaGPT)

## 构建工具

### AgentOps
用于 AI 代理监控、LLM 成本跟踪、基准测试等的 Python SDK。与大多数 LLM 和代理框架（如 CrewAI、Langchain 和 Autogen）集成。
github 地址：[https://github.com/AgentOps-AI/agentops](https://github.com/AgentOps-AI/agentops)

### AgentStack
AgentStack 开让你从命令行创建 AI 代理项目，它是启动代理项目的绝佳工具，并提供了许多 CLI 实用程序，用于在整个开发过程中轻松生成代码。
github 地址：[https://github.com/AgentOps-AI/AgentStack](https://github.com/AgentOps-AI/AgentStack)

### dspy
DSPy 是由斯坦福大学开发的一个开源框架，旨在优化语言模型（LLM）的使用，它通过将声明式的语言模型调用转换为自我优化的管道来工作。与手动编写每个任务的特定提示不同，DSPy 允许用户定义高级目标和度量，框架会自动优化 LLM 的性能。
github 地址：[https://github.com/stanfordnlp/dspy](https://github.com/stanfordnlp/dspy)

### phoenix
Phoenix 是一个开源的 AI 可观察性平台，主要用于实验、评估和故障排除，支持追踪 LLM 应用程序的运行时、基准测试性能并创建版本化的数据集。它支持跟踪对提示、LLM 和检索方式的改动，并兼容多个框架和 LLM 提供商。
github 地址：[https://github.com/Arize-ai/phoenix](https://github.com/Arize-ai/phoenix)

# 规划

## 工作流编排

### inngest
Inngest 是一个领先的工作流编排平台，可在无服务器架构、服务器或边缘设备上运行有状态的步骤函数和 AI 工作流。
github 地址：[https://github.com/inngest/inngest](https://github.com/inngest/inngest)

### prefect
Prefect 是一个用于构建 Python 数据管道的工作流编排框架。它是将脚本提升为可靠生产工作流的最简单方式。通过 Prefect，用户可以构建具有弹性和动态响应能力的数据管道，能够适应外部变化并从意外情况中恢复。
github 地址：[https://github.com/PrefectHQ/prefect](https://github.com/PrefectHQ/prefect)

# 记忆

## 记忆引擎

### mem0
Mem0 是一个增强 AI 助手和代理的智能内存层，能够实现个性化交互并持续改进，适用于客户支持聊天机器人、AI 助手和自治系统。它通过混合数据库方法管理长期记忆，确保个性化信息存储高效且搜索迅速，提升 AI 代理的响应个性化和相关性。
github 地址：[https://github.com/mem0ai/mem0](https://github.com/mem0ai/mem0)

### DB-GPT
DB-GPT 是一个开源的 AI 原生数据应用开发框架，集成了 AWEL（Agentic Workflow Expression Language）和多智能体技术。其目标是通过开发多项技术能力（如多模型管理 SMMF、Text2SQL 效果优化、RAG 框架优化、多智能体框架协作以及 AWEL 的代理工作流编排等），构建大模型领域的基础设施，从而使数据驱动的大模型应用更加简单和便捷。
github 地址：[https://github.com/eosphoros-ai/DB-GPT](https://github.com/eosphoros-ai/DB-GPT)

### Letta（原MemGPT）
Letta 是一个用于构建有状态 LLM 应用程序的框架，支持个性化聊天机器人、数据驱动代理和自动化 AI 工作流。它允许应用保持长期记忆并连接外部数据源，适用于需要持续交互和动态更新的应用场景。
github 地址：[https://github.com/letta-ai/letta](https://github.com/letta-ai/letta)

### RAGFlow
RAGFlow 是一款基于深度文档理解构建的开源 RAG（Retrieval-Augmented Generation）引擎。RAGFlow 可以为各种规模的企业及个人提供一套精简的 RAG 工作流程，结合大语言模型（LLM）针对用户各类不同的复杂格式数据提供可靠的问答以及有理有据的引用。
github 地址：[https://github.com/infiniflow/ragflow](https://github.com/infiniflow/ragflow)

### Cognee
Cognee 实现了可扩展、模块化的 ECL（Extract, Cognify, Load）流水线，能够帮助用户互联和检索过往对话、文档以及音频转录内容，同时减少幻觉、开发工作量和成本。
github 地址：[https://github.com/topoteretes/cognee](https://github.com/topoteretes/cognee)

### KnowledgeTable
Knowledge Table 是一个开源软件包，旨在简化从非结构化文档中提取和探索结构化数据的过程。
github 地址：[https://github.com/whyhow-ai/knowledge-table](https://github.com/whyhow-ai/knowledge-table)

## GraphRAG技术

### graphrag
GraphRAG 项目是一个数据管道和转换套件，旨在利用 LLM 的强大功能从非结构化文本中提取有意义的结构化数据。
github 地址：[https://github.com/microsoft/graphrag](https://github.com/microsoft/graphrag)

### fast-graphrag
Fast GraphRAG 是一个精简且可提示的框架，旨在为代理驱动的检索工作流提供可解释、高精度的解决方案。它设计用于高效、低成本的操作，支持动态数据生成和增量更新，并能够无缝集成到现有的检索管道中。
github 地址：[https://github.com/circlemind-ai/fast-graphrag](https://github.com/circlemind-ai/fast-graphrag)

### LightRAG
LightRAG 是一个简单快速的 RAG 引擎。
github 地址：[https://github.com/HKUDS/LightRAG](https://github.com/HKUDS/LightRAG)

### nano-graphrag
nano-graphrag 提供了一个更小、更快、更干净的 GraphRAG，同时保留了核心功能。GraphRAG 很好而且功能强大，但官方实现很难阅读或破解。
github 地址：[https://github.com/gusye1234/nano-graphrag](https://github.com/gusye1234/nano-graphrag)


## 存储

### Milvus
Milvus 是一个为大规模设计的高性能向量数据库，AI 应用可使用它进行存储和搜索大量非结构化数据，如文本、图像和多模态信息。
github 地址：[https://github.com/milvus-io/milvus](https://github.com/milvus-io/milvus)

### Weaviate
Weaviate 是一个开源向量数据库，能够同时存储对象和向量，支持将向量搜索与结构化过滤相结合，并具有云原生数据库的容错性和可扩展性。
github 地址：[https://github.com/weaviate/weaviate](https://github.com/weaviate/weaviate)

### Chroma
Chroma 是一个AI 原生开源嵌入数据库。
github 地址：[https://github.com/chroma-core/chroma](https://github.com/chroma-core/chroma)

# 工具

## 智能体网络与通信

### AgentConnect
AgentConnect 的愿景是定义智能体的连接方式，并为数十亿智能体构建一个开放、安全和高效的协作网络。AgentConnect提供以下能力：
- 基于W3C DID规范提供了一个去中心化的身份认证方式，可以让智能体掌握自己的身份，并且与其他任意智能体进行跨平台的、安全的、低成本的身份验证。
- 支持基于DID的端到端加密通信，确保智能体之间的通信安全。
- 支持元协议协商，允许智能体之间使用自然语言协商双方能力以及通信协议，并且使用LLM生成代码进行协议通信。这有助于实现自组织自协商的智能体网络。
- 支持应用层协议管理，可以方便的对协议以及协议代码进行加载、更新、卸载，有助于提高智能体之间的通信效率。

github 地址：[https://github.com/chgaowei/AgentConnect](https://github.com/chgaowei/AgentConnect)

### AgentNetworkProtocol
AgentNetworkProtocol（ANP）是专为智能体网络设计的开放协议框架，旨在建立一个开放、安全、高效、自组织、自协商的智能体协作网络。它总共分为三层，分别是身份与加密通信层、元协议层、应用协议层。AgentConnect是AgentNetworkProtocol的开源实现。
github 地址：[https://github.com/chgaowei/AgentNetworkProtocol](https://github.com/chgaowei/AgentNetworkProtocol)

### Agora Protocol
Agora Protocol Agora 是一个简单的跨平台协议，允许异构 LLM 之间进行高效的通信。它先使用自然语言进行协商通信协议，然后使用通信协议进行通信。
github 地址：[https://github.com/agora-protocol/paper-demo](https://github.com/agora-protocol/paper-demo)

### agent-protocol
agent-protocol 用于与 AI 智能体交互的通用接口。该协议与技术堆栈无关 - 您可以将其与任何框架一起使用来构建代理。它目前构建的是智能体与智能体使用者之间的通信协议。不过现在长时间未更新。
github 地址：[https://github.com/AI-Engineer-Foundation/agent-protocol](https://github.com/AI-Engineer-Foundation/agent-protocol)

### naptha-sdk
Naptha 使用户能够构建去中心化的多代理工作流。去中心化工作流可以在一个或多个节点（而不是一个中央服务器）上运行，具有不同的 LLM 和许多本地数据源。
github 地址：[https://github.com/NapthaAI/naptha-sdk](https://github.com/NapthaAI/naptha-sdk)

## computer use API

### npi
NPINPi 是一个开源平台，提供工具使用 API，使 AI 代理能够在虚拟世界中采取行动, 使 AI 代理能够操作各种软件工具和应用程序并与之交互，允许大型语言模型通过函数调用与现有软件和应用程序生态系统无缝集成。NPi 充当这些模型访问虚拟世界的网关。
github 地址：[https://github.com/npi-ai/npi](https://github.com/npi-ai/npi)

## 身份验证

### AgentConnect
AgentConnect 提供了基于W3C DID规范的智能体身份认证方法，并支持基于DID的端到端加密通信。
github 地址：[https://github.com/chgaowei/AgentConnect](https://github.com/chgaowei/AgentConnect)

## 运行时

### E2B
E2B 是一种开源基础设施，允许您在云中的安全隔离沙箱中运行 AI 生成的代码。
github 地址：[https://github.com/e2b-dev/E2B](https://github.com/e2b-dev/E2B)

## 网页浏览

### Crawlee
Crawlee 是一个用于构建可靠爬虫的 Node.js 网络爬取和浏览器自动化库，支持 JavaScript 和 TypeScript。它可以提取 AI、LLM、RAG 或 GPT 所需的数据，从网站下载 HTML、PDF、JPG、PNG 等文件。
github 地址：[https://github.com/apify/crawlee](https://github.com/apify/crawlee)

### Browserless
Browserless 允许远程客户端连接并执行无头工作，所有操作都在 Docker 环境中进行。它支持标准的、未修改的 Puppeteer 和 Playwright 库，并提供基于 REST 的 API，用于执行常见操作，如数据收集、PDF 生成等。
github 地址：[https://github.com/browserless/browserless](https://github.com/browserless/browserless)

### AgentQL
AgentQL 是一种 AI 驱动的查询语言，用于抓取网站和自动化工作流程。它使用自然语言查询来精确定位任何网页上的数据和元素，包括经过身份验证和动态生成的内容。
github 地址：[https://github.com/tinyfish-io/agentql](https://github.com/tinyfish-io/agentql)




