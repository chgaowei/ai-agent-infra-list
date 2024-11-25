
The Most Comprehensive Collection of AI Agent Infrastructure Open Source Projects [Continuously Updated]

# Introduction

The importance of AI Agents is an industry consensus, with the current biggest bottleneck being model capabilities, especially model reasoning abilities. However, with the release of o1, perhaps we can shift some attention to other bottlenecks. This is the original intention behind writing this article.

The AI Agent Infrastructure discussed in this article does not include models, but rather focuses on other infrastructure components besides models, such as memory, tools, frameworks, containers, etc.

The reason for writing this article is that I often come across excellent open source projects but have no place to record them. Sometimes when looking for an open source project, it's difficult to find. Therefore, this article has three purposes:

- To have a place to record excellent and creative open source projects

- To help AI Agent developers quickly find suitable infrastructure

- To help AI Agent developers quickly understand the current state of AI Agent infrastructure development


For now, we only collect open source projects, though we may include commercial products in the future.

I will continuously update this article, perhaps once a month, adding excellent and creative projects each time. Additionally, I plan to maintain this article as an open source project. I have created a GitHub repository at: [https://github.com/chgaowei/ai-agent-infra-list](https://github.com/chgaowei/ai-agent-infra-list).

If you know of any excellent open source projects, have different opinions about certain projects, or wish to promote your open source project, feel free to submit a PR.

We have also created an AI Agent Infra discussion group. Welcome to join:

WeChat: Please add WeChat ID changshan02, with note "AI discussion group".

Also welcome to join Discord to discuss with global tech professionals: [https://discord.gg/BNJdvMa5XE](https://discord.gg/BNJdvMa5XE)


## This Month's Recommended Projects

Each monthly update will recommend one or more projects. This month, we'd like to recommend our open source project **AgentConnect**:

AgentConnect's vision is to define how agents connect and build an open, secure, and efficient collaboration network for billions of agents. AgentConnect provides the following capabilities:

- Provides a decentralized authentication method based on W3C DID specification, allowing agents to control their own identity and perform cross-platform, secure, low-cost identity verification with any other agent.

- Supports DID-based end-to-end encrypted communication, ensuring secure communication between agents.

- Supports meta-protocol negotiation, allowing agents to negotiate capabilities and communication protocols using natural language, and use LLM to generate code for protocol communication. This helps achieve self-organizing and self-negotiating agent networks.

- Supports application layer protocol management, enabling convenient loading, updating, and unloading of protocols and protocol code, helping improve communication efficiency between agents.


GitHub repository: [https://github.com/chgaowei/AgentConnect](https://github.com/chgaowei/AgentConnect)

Technical overview: [https://github.com/chgaowei/AgentNetworkProtocol/blob/main/chinese/00-AgentNetworkProtocol%E6%8A%80%E6%9C%AF%E8%93%9D%E5%9B%BE.md](https://github.com/chgaowei/AgentNetworkProtocol/blob/main/chinese/00-AgentNetworkProtocol%E6%8A%80%E6%9C%AF%E8%93%9D%E5%9B%BE.md)


# Overview

For the overall classification structure, I will divide it into four main categories: frameworks, planning, memory, and tools, with each category further subdivided based on different dimensions. The classification may not be perfect and might be adjusted later.
- Frameworks
  - One-Stop Platforms: [dify](https://github.com/langgenius/dify)    [AutoGpt](https://github.com/Significant-Gravitas/AutoGPT)     [FastGPT](https://github.com/labring/FastGPT)     [BISHENG](https://github.com/dataelement/bisheng)
  - Development Frameworks: [langchain](https://github.com/langchain-ai/langchain)     [llama_index](https://github.com/run-llama/llama_index)     [semantic-kernel](https://github.com/microsoft/semantic-kernel)     [LangGraph](https://github.com/langchain-ai/langgraph)     [phidata](https://github.com/phidatahq/phidata)     [haystack](https://github.com/deepset-ai/haystack)
  - Multi-Agent Frameworks: [crewai](https://github.com/crewAIInc/crewAI)     [Autogen](https://github.com/microsoft/autogen)     [Camel](https://github.com/camel-ai/camel)     [Magentic-One](https://github.com/microsoft/autogen/tree/main/python/packages/autogen-magentic-one)     [MetaGPT](https://github.com/geekan/MetaGPT)
  - Build Tools: [AgentOps](https://github.com/AgentOps-AI/agentops)     [AgentStack](https://github.com/AgentOps-AI/AgentStack)     [dspy](https://github.com/stanfordnlp/dspy)     [phoenix](https://github.com/Arize-ai/phoenix)
- Planning
  - Workflow Orchestration: [inngest](https://github.com/inngest/inngest)     [prefect](https://github.com/PrefectHQ/prefect)
- Memory
  - Memory Engines: [mem0](https://github.com/mem0ai/mem0)     [DB-GPT](https://github.com/eosphoros-ai/DB-GPT)     [Letta](https://github.com/letta-ai/letta)     [RAGFlow](https://github.com/infiniflow/ragflow)     [Cognee](https://github.com/topoteretes/cognee)     [KnowledgeTable](https://github.com/whyhow-ai/knowledge-table)
  - GraphRAG Technology: [graphrag](https://github.com/microsoft/graphrag)     [fast-graphrag](https://github.com/circlemind-ai/fast-graphrag)     [LightRAG](https://github.com/HKUDS/LightRAG)     [nano-graphrag](https://github.com/gusye1234/nano-graphrag)
  - Storage: [Milvus](https://github.com/milvus-io/milvus)     [Weaviate](https://github.com/weaviate/weaviate)     [Chroma](https://github.com/chroma-core/chroma)
- Tools
  - Networking and Communication: [AgentConnect](https://github.com/chgaowei/AgentConnect)     [AgentNetworkProtocol](https://github.com/chgaowei/AgentNetworkProtocol)     [Agora Protocol](https://github.com/agora-protocol/paper-demo)     [agent-protocol](https://github.com/AI-Engineer-Foundation/agent-protocol)     [naptha-sdk](https://github.com/NapthaAI/naptha-sdk)
  - Computer Use API: [npi](https://github.com/npi-ai/npi)
  - Authentication: [AgentConnect](https://github.com/chgaowei/AgentConnect)
  - Runtime: [E2B](https://github.com/e2b-dev/E2B)
  - Web Browsing: [Crawlee](https://github.com/apify/crawlee)     [Browserless](https://github.com/browserless/browserless)     [AgentQL](https://github.com/tinyfish-io/agentql)

  
# Frameworks


## One-Stop Platforms


### dify

Dify is an open-source LLM application development platform. Its intuitive interface combines AI workflows, RAG pipelines, agent capabilities, model management, and observability features, enabling rapid progression from prototype to production.

GitHub repository: [https://github.com/langgenius/dify](https://github.com/langgenius/dify)


### AutoGpt

AutoGPT is a powerful platform for creating, deploying, and managing continuously running AI agents to automate complex workflows. AutoGPT has evolved from its early demo stage to include workflow capabilities.

GitHub repository: [https://github.com/Significant-Gravitas/AutoGPT](https://github.com/Significant-Gravitas/AutoGPT)


### fastgpt

FastGPT is a knowledge-based platform built on Large Language Models (LLMs), offering a comprehensive set of out-of-the-box features including data processing, RAG retrieval, and visual AI workflow orchestration. With FastGPT, users can easily develop and deploy sophisticated Q&A systems without complex setup or configuration.

GitHub repository: [https://github.com/labring/FastGPT](https://github.com/labring/FastGPT)


### BISHENG

BISHENG is an open-source LLM DevOps platform designed for next-generation enterprise AI applications. Its powerful and comprehensive features include: generative AI workflows, RAG, agents, unified model management, evaluation, SFT, dataset management, enterprise-grade system management, and observability.

GitHub repository: [https://github.com/dataelement/bisheng](https://github.com/dataelement/bisheng)


## Development Frameworks


### langchain

LangChain is a development framework designed for building applications powered by large language models. It provides a suite of tools and components including Models, Prompts, Indexes, Memory, Chains, and Agents.

GitHub repository: [https://github.com/langchain-ai/langchain](https://github.com/langchain-ai/langchain)


### llama_index

LlamaIndex (GPT Index) is a data framework for LLM applications that combines external data with large language models (LLMs). It supports creating indexes from various data sources (such as documents, databases, etc.) and optimizes information retrieval processes.

GitHub repository: [https://github.com/run-llama/llama_index](https://github.com/run-llama/llama_index)


### semantic-kernel

Semantic Kernel is an SDK designed to integrate large language models (LLMs) with traditional programming languages like C#, Python, and Java, supporting automatic coordination of plugins. It provides abstraction layers for managing AI services and memory storage, supports multiple platforms and vector databases, and can automatically generate and execute LLM-generated plans.

GitHub repository: [https://github.com/microsoft/semantic-kernel](https://github.com/microsoft/semantic-kernel)


### LangGraph

LangGraph is a library for building stateful, multi-agent applications. It provides three core advantages over other LLM frameworks: loops, controllability, and persistence. LangGraph allows you to define workflows that include loops, which are essential for most agent architectures, distinguishing it from DAG-based solutions.

GitHub repository: [https://github.com/langchain-ai/langgraph](https://github.com/langchain-ai/langgraph)


### phidata

Phidata is a framework for building agent systems that allows engineers to create agents with memory, knowledge, tools, and reasoning capabilities. It supports building teams of agents that can work together and interact with agents through a beautiful user interface. Phidata also provides functionality for monitoring, evaluating, and optimizing agents, and helps develop agent applications with APIs, databases, and vector databases.

GitHub repository: [https://github.com/phidatahq/phidata](https://github.com/phidatahq/phidata)


### haystack

An AI orchestration framework for building customizable, production-ready Large Language Model (LLM) applications. Connect components (models, vector databases, file converters) into pipelines or agents that can interact with data. With advanced retrieval methods, it's ideal for building RAG (Retrieval Augmented Generation), question-answering, semantic search, or conversational agent chatbots.

GitHub repository: [https://github.com/deepset-ai/haystack](https://github.com/deepset-ai/haystack)


## Multi-Agent Frameworks


### crewai

CrewAI is a multi-agent framework designed to coordinate multiple AI agents working together to complete complex tasks and workflows. The framework enables users to define and execute automated agent collaborations through task management and process control.

GitHub repository: [https://github.com/crewAIInc/crewAI](https://github.com/crewAIInc/crewAI)


### Autogen

AutoGen is an open-source framework for building AI agent systems. It simplifies the creation of event-driven, distributed, scalable, and resilient agent applications. AutoGen enables rapid system construction where AI agents can collaborate and execute tasks autonomously or under human supervision.

GitHub repository: [https://github.com/microsoft/autogen](https://github.com/microsoft/autogen)


### Camel

CAMEL is one of the earliest multi-agent frameworks based on Large Language Models (LLMs) and has evolved into a general framework for building and utilizing LLM-based agents to solve real-world tasks.

GitHub repository: [https://github.com/camel-ai/camel](https://github.com/camel-ai/camel)


### Magentic-One

Magentic-One is a high-performance general-purpose agent system designed to solve complex tasks. It employs a multi-agent architecture where a main agent "Orchestrator" directs four specialized agents to complete tasks. The Orchestrator is responsible for planning, tracking progress, and replanning when errors occur, while guiding these specialized agents to perform tasks such as operating web browsers, browsing local files, or writing and executing Python code.

GitHub repository: [https://github.com/microsoft/autogen/tree/main/python/packages/autogen-magentic-one](https://github.com/microsoft/autogen/tree/main/python/packages/autogen-magentic-one)


### MetaGPT

MetaGPT takes a one-line requirement as input and outputs user stories, competitive analysis, requirements, data structures, APIs, and documentation. MetaGPT includes roles such as Product Manager, Architect, Project Manager, and Engineer. It provides the entire process of a software company with carefully orchestrated SOPs.

GitHub repository: [https://github.com/geekan/MetaGPT](https://github.com/geekan/MetaGPT)


## Building Tools


### AgentOps

A Python SDK for AI agent monitoring, LLM cost tracking, benchmarking, and more. Integrates with most LLM and agent frameworks such as CrewAI, Langchain, and Autogen.

GitHub repository: [https://github.com/AgentOps-AI/agentops](https://github.com/AgentOps-AI/agentops)


### AgentStack

AgentStack enables you to create AI agent projects from the command line. It's an excellent tool for bootstrapping agent projects and provides numerous CLI utilities for easy code generation throughout the development process.

GitHub repository: [https://github.com/AgentOps-AI/AgentStack](https://github.com/AgentOps-AI/AgentStack)


### dspy

DSPy is an open-source framework developed by Stanford University aimed at optimizing the use of Language Models (LLMs). It works by transforming declarative language model calls into self-optimizing pipelines. Instead of manually writing specific prompts for each task, DSPy allows users to define high-level objectives and metrics, and the framework automatically optimizes LLM performance.

GitHub repository: [https://github.com/stanfordnlp/dspy](https://github.com/stanfordnlp/dspy)


### phoenix

Phoenix is an open-source AI observability platform primarily used for experimentation, evaluation, and troubleshooting. It supports tracking LLM application runtime, benchmarking performance, and creating versioned datasets. It enables tracking changes to prompts, LLMs, and retrieval methods, and is compatible with multiple frameworks and LLM providers.

GitHub repository: [https://github.com/Arize-ai/phoenix](https://github.com/Arize-ai/phoenix)


# Planning


## Workflow Orchestration


### inngest

Inngest is a leading workflow orchestration platform that runs stateful step functions and AI workflows on serverless architectures, servers, or at the edge.

GitHub repository: [https://github.com/inngest/inngest](https://github.com/inngest/inngest)


### prefect

Prefect is a workflow orchestration framework for building Python data pipelines. It's the simplest way to transform scripts into reliable production workflows. With Prefect, users can build resilient and dynamically responsive data pipelines that can adapt to external changes and recover from unexpected situations.

GitHub repository: [https://github.com/PrefectHQ/prefect](https://github.com/PrefectHQ/prefect)


# Memory


## Memory Engines


### mem0

Mem0 is an intelligent memory layer that enhances AI assistants and agents, enabling personalized interactions and continuous improvement, suitable for customer support chatbots, AI assistants, and autonomous systems. It manages long-term memory through a hybrid database approach, ensuring efficient storage of personalized information and quick retrieval, enhancing the personalization and relevance of AI agent responses.

GitHub repository: [https://github.com/mem0ai/mem0](https://github.com/mem0ai/mem0)


### DB-GPT

DB-GPT is an open-source AI-native data application development framework that integrates AWEL (Agentic Workflow Expression Language) and multi-agent technology. Its goal is to build infrastructure in the large model domain by developing multiple technical capabilities (such as multi-model management SMMF, Text2SQL optimization, RAG framework optimization, multi-agent framework collaboration, and AWEL agent workflow orchestration), making data-driven large model applications simpler and more convenient.

GitHub repository: [https://github.com/eosphoros-ai/DB-GPT](https://github.com/eosphoros-ai/DB-GPT)


### Letta (formerly MemGPT)

Letta is a framework for building stateful LLM applications, supporting personalized chatbots, data-driven agents, and automated AI workflows. It allows applications to maintain long-term memory and connect to external data sources, suitable for applications requiring continuous interaction and dynamic updates.

GitHub repository: [https://github.com/letta-ai/letta](https://github.com/letta-ai/letta)


### RAGFlow

RAGFlow is an open-source RAG (Retrieval-Augmented Generation) engine built on deep document understanding. RAGFlow provides enterprises and individuals of all sizes with a streamlined RAG workflow, combining large language models (LLMs) to provide reliable question-answering and well-referenced citations for various complex data formats.

GitHub repository: [https://github.com/infiniflow/ragflow](https://github.com/infiniflow/ragflow)


### Cognee

Cognee implements scalable, modular ECL (Extract, Cognify, Load) pipelines that help users interconnect and retrieve past conversations, documents, and audio transcriptions while reducing hallucinations, development effort, and costs.

GitHub repository: [https://github.com/topoteretes/cognee](https://github.com/topoteretes/cognee)


### KnowledgeTable

Knowledge Table is an open-source package designed to simplify the process of extracting and exploring structured data from unstructured documents.

GitHub repository: [https://github.com/whyhow-ai/knowledge-table](https://github.com/whyhow-ai/knowledge-table)


## GraphRAG Technology


### graphrag

The GraphRAG project is a data pipeline and transformation suite designed to leverage the power of LLMs to extract meaningful structured data from unstructured text.

GitHub repository: [https://github.com/microsoft/graphrag](https://github.com/microsoft/graphrag)


### fast-graphrag

Fast GraphRAG is a lean and promptable framework designed to provide interpretable, high-precision solutions for agent-driven retrieval workflows. It is designed for efficient, low-cost operations, supports dynamic data generation and incremental updates, and can seamlessly integrate into existing retrieval pipelines.

GitHub repository: [https://github.com/circlemind-ai/fast-graphrag](https://github.com/circlemind-ai/fast-graphrag)


### LightRAG

LightRAG is a simple and fast RAG engine.

GitHub repository: [https://github.com/HKUDS/LightRAG](https://github.com/HKUDS/LightRAG)


### nano-graphrag

nano-graphrag provides a smaller, faster, and cleaner GraphRAG while maintaining core functionality. While GraphRAG is good and powerful, the official implementation is difficult to read or hack.

GitHub repository: [https://github.com/gusye1234/nano-graphrag](https://github.com/gusye1234/nano-graphrag)


## Storage


### Milvus

Milvus is a high-performance vector database designed for scale, which AI applications can use to store and search large amounts of unstructured data such as text, images, and multimodal information.

GitHub repository: [https://github.com/milvus-io/milvus](https://github.com/milvus-io/milvus)


### Weaviate

Weaviate is an open-source vector database that can store both objects and vectors, supporting vector search combined with structured filtering, and offering the fault tolerance and scalability of a cloud-native database.

GitHub repository: [https://github.com/weaviate/weaviate](https://github.com/weaviate/weaviate)


### Chroma

Chroma is an AI-native open-source embedding database.

GitHub repository: [https://github.com/chroma-core/chroma](https://github.com/chroma-core/chroma)


# Tools


## Network and Communication


### AgentConnect

AgentConnect's vision is to define how agents connect and build an open, secure, and efficient collaboration network for billions of agents. AgentConnect provides the following capabilities:

- Provides a decentralized authentication method based on W3C DID specification, allowing agents to control their own identity and perform cross-platform, secure, low-cost identity verification with any other agent.

- Supports end-to-end encrypted communication based on DID to ensure secure communication between agents.

- Supports meta-protocol negotiation, allowing agents to negotiate capabilities and communication protocols using natural language, and use LLM to generate code for protocol communication. This helps achieve self-organizing and self-negotiating agent networks.

- Supports application layer protocol management, enabling convenient loading, updating, and unloading of protocols and protocol code, helping improve communication efficiency between agents.


GitHub repository: [https://github.com/chgaowei/AgentConnect](https://github.com/chgaowei/AgentConnect)


### AgentNetworkProtocol

AgentNetworkProtocol (ANP) is an open protocol framework designed specifically for agent networks, aiming to establish an open, secure, efficient, self-organizing, and self-negotiating agent collaboration network. It consists of three layers: Identity and Encrypted Communication Layer, Meta Protocol Layer, and Application Protocol Layer. AgentConnect is the open-source implementation of AgentNetworkProtocol.

GitHub repository: [https://github.com/chgaowei/AgentNetworkProtocol](https://github.com/chgaowei/AgentNetworkProtocol)


### Agora Protocol

Agora Protocol is a simple cross-platform protocol that enables efficient communication between heterogeneous LLMs. It first negotiates communication protocols using natural language and then communicates using the agreed protocol.

GitHub repository: [https://github.com/agora-protocol/paper-demo](https://github.com/agora-protocol/paper-demo)


### agent-protocol

agent-protocol is a universal interface for interacting with AI agents. The protocol is technology stack agnostic - you can use it with any framework to build agents. It currently builds communication protocols between agents and agent users. However, it hasn't been updated for a long time.

GitHub repository: [https://github.com/AI-Engineer-Foundation/agent-protocol](https://github.com/AI-Engineer-Foundation/agent-protocol)


### naptha-sdk

Naptha enables users to build decentralized multi-agent workflows. Decentralized workflows can run on one or more nodes (rather than a central server) with different LLMs and numerous local data sources.

GitHub repository: [https://github.com/NapthaAI/naptha-sdk](https://github.com/NapthaAI/naptha-sdk)


## Computer Use API


### npi

NPI is an open-source platform providing tool usage APIs that enable AI agents to take actions in the virtual world. It allows AI agents to operate and interact with various software tools and applications, enabling large language models to seamlessly integrate with existing software and application ecosystems through function calls. NPI acts as a gateway for these models to access the virtual world.

GitHub repository: [https://github.com/npi-ai/npi](https://github.com/npi-ai/npi)


## Authentication


### AgentConnect

AgentConnect provides agent authentication methods based on the W3C DID specification and supports end-to-end encrypted communication based on DID.

GitHub repository: [https://github.com/chgaowei/AgentConnect](https://github.com/chgaowei/AgentConnect)


## Runtime


### E2B

E2B is an open-source infrastructure that allows you to run AI-generated code in secure isolated sandboxes in the cloud.

GitHub repository: [https://github.com/e2b-dev/E2B](https://github.com/e2b-dev/E2B)


## Web Browsing


### Crawlee

Crawlee is a Node.js web scraping and browser automation library for building reliable crawlers, supporting JavaScript and TypeScript. It can extract data needed for AI, LLM, RAG, or GPT, downloading HTML, PDF, JPG, PNG, and other files from websites.

GitHub repository: [https://github.com/apify/crawlee](https://github.com/apify/crawlee)


### Browserless

Browserless allows remote clients to connect and perform headless work, all within a Docker environment. It supports standard, unmodified Puppeteer and Playwright libraries and provides a REST-based API for performing common operations like data collection, PDF generation, and more.

GitHub repository: [https://github.com/browserless/browserless](https://github.com/browserless/browserless)


### AgentQL

AgentQL is an AI-powered query language for scraping websites and automating workflows. It uses natural language queries to precisely target data and elements on any webpage, including authenticated and dynamically generated content.

GitHub repository: [https://github.com/tinyfish-io/agentql](https://github.com/tinyfish-io/agentql)
