# Awesome Software Design Patterns — AGI Era Edition

> 设计模式是软件工程的通用语言。在 AGI 时代，AI 负责写代码，你负责做决策。
> 这个仓库帮助你理解：哪些模式是永恒的核心，哪些正在被 AI 抽象掉，以及 AGI 时代涌现的新模式。

![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)

---

## 理解本仓库的分类

本仓库将设计模式分为四个价值层级：

| 图标 | 层级 | 含义 |
|------|------|------|
| 🧱 | **永恒核心** | 计算机科学的通用语言，无论是否 AI 时代都必须理解 |
| 🛠 | **仍很重要** | 概念和决策逻辑仍关键，但 AI 正逐步接管实现细节 |
| 📖 | **值得了解** | 特定场景有价值，不需要深入掌握 |
| 🔄 | **正在被重构** | AI/现代语言大幅降低了其必要性，了解即可 |

---

## AGI 时代设计模式学习路线图

以下直接回答一个问题：**在 AI 编程时代，哪些模式还值得花时间学？**

### 🟢 无论何时都必须学（永恒核心）

> 这些是软件工程的"通用语言"，AI 辅助不改变其价值。你负责决策，AI 负责实现。

| 类别 | 核心模式 | 为什么必须学 |
|------|---------|------------|
| **GoF 核心** | Strategy, Factory, Observer, Composite, Adapter, Facade, Command, State, Template Method | AI 工具底层架构（Agent、MCP、Workflow）直接复用这些模式 |
| **SOLID** | 全部 5 条原则 | 你审查 AI 代码质量的标准，架构决策的依据 |
| **系统架构** | 分层、六边形、CQRS、事件溯源 | 高层的系统划分 AI 不会替你拍板 |
| **分布式** | 断路器、隔板、重试退避、Saga、共识 | 分布式系统是物理约束，AI 做不了取舍决策 |
| **企业集成** | 消息队列、发布订阅、事件驱动通道 | Agent 间通信、工具编排的底层模型 |
| **数据模式** | 规范化、索引策略、物化视图、CQRS | 数据模型设计是业务核心，AI 优化不了 |

### 🟡 未来 3-5 年仍然必须学（但 AI 正逐步接管实现层）

> 概念和决策逻辑仍重要，但具体实现细节可以越来越依赖 AI。

| 类别 | 重点 | 为什么还学 | 什么正在被 AI 替代 |
|------|------|-----------|------------------|
| **云架构** | 多租户、弹性伸缩、成本优化 | 架构决策和账单还得你负责 | Infra-as-Code + AI 自动化运维 |
| **微服务** | API 网关、Strangler Fig、Saga | 系统拆分的粒度决策 | 服务间通信代码生成 |
| **容器/K8s** | Sidecar、Ambassador、Adapter | 可观测性和运维设计 | YAML/manifest AI 生成 |
| **安全** | 认证授权、加密、OWASP | 安全决策永远要人负责 | 漏洞检测和修复辅助 |
| **前端** | 状态管理、组件组合 | 用户体验架构 | UI 组件代码生成 |

### 🔴 不怎么需要学了（价值大幅降低）

> 这些是原仓库中的内容。AI 和现代语言已经大幅降低了它们的学习必要性。

| 原分类 | 原因 |
|--------|------|
| **语言特定实现**（Java 23 种设计模式、C# 模式、Python 模式等） | AI 在任何语言间翻译模式，理解概念即可，无需记忆具体代码实现 |
| **解决语言缺陷的模式**（Java 版 Builder、笨重 Singleton、大量 Boilerplate） | 现代语言特性（kotlin data class、records、named params）+ AI 生成消除了手写需求 |
| **纯代码级微观模式** | AI 在函数级别已经生成质量很高 |
| **CSS 命名约定**（BEM、OOCSS、SMACSS） | Tailwind/CSS-in-JS + AI 生成让这些成为历史 |
| **过时 UI 架构**（MVC/MVP 移动端细分变体） | 现代框架（React/Vue/Flutter）已范式化 |
| **手写设计模式类图** | AI 可以直接生成并解释，你只需要识别和选择 |

### 🔄 AGI 时代真正需要的新模式

这些是传统模式书籍里没有、但你在未来必须掌握的全新模式（详见下文章节）：

- Agent 编排（ReAct、Plan-Execute、Multi-Agent）
- MCP 工具集成设计
- Skill/Workflow 编排（Composition、Fan-out、Checkpoint）
- 人机协作模式（Progressive Autonomy、Trust Calibration）
- RAG 知识管理（Chunking、Hybrid Search、Contextual Retrieval）
- 代码生成验证（Generate-Test Loop、Self-Consistency Check）

---

## 目录

- [🧱 永恒核心模式](#-永恒核心模式)
  - [GoF 经典设计模式](#gof-经典设计模式)
  - [SOLID 与设计原则](#solid-与设计原则)
  - [架构模式](#架构模式)
  - [分布式系统模式](#分布式系统模式)
  - [企业集成模式](#企业集成模式)
  - [数据库模式](#数据库模式)
- [🛠 仍很重要的模式](#-仍很重要的模式)
  - [云架构模式](#云架构模式)
  - [微服务模式](#微服务模式)
  - [容器与 K8s 模式](#容器与-k8s-模式)
  - [安全模式](#安全模式)
  - [前端架构模式](#前端架构模式)
- [🔄 AGI 时代的全新模式](#-agi-时代的全新模式)
  - [Agent 编排模式](#agent-编排模式)
  - [MCP / 工具集成模式](#mcp--工具集成模式)
  - [Skill / Workflow 编排模式](#skill--workflow-编排模式)
  - [人机协作模式](#人机协作模式)
  - [RAG 与知识管理模式](#rag-与知识管理模式)
  - [代码生成与验证模式](#代码生成与验证模式)
- [📖 特定领域模式](#-特定领域模式)
- [📚 推荐阅读](#-推荐阅读)

---

## 🧱 永恒核心模式

> 这些是软件设计的"基础词汇"。AI 可以帮助实现它们，但**何时、为何、如何组合**这些模式需要你来决策。

### GoF 经典设计模式

- [Refactoring Guru — Design Patterns](https://refactoring.guru/design-patterns) — 带图解的最清晰设计模式参考。
- [SourceMaking — Design Patterns & Anti-Patterns](https://sourcemaking.com/design_patterns) — 模式与反模式对照。
- [oodesign.com](https://www.oodesign.com/) — 带 UML 的模式目录。

**关键模式清单（按使用频度排序）：**

| 模式 | 适用场景 | AGI 时代价值 |
|------|----------|-------------|
| **Strategy** | 算法族互换、LLM Provider 切换 | 🧱 AI 工具的选择器逻辑就是 Strategy |
| **Factory / Abstract Factory** | 对象创建逻辑封装 | 🧱 Agent 创建、工具实例化 |
| **Observer / Event Emitter** | 事件驱动、状态变更通知 | 🧱 MCP 事件流、Agent 间通信 |
| **Composite** | 树形结构、递归组合 | 🧱 Workflow/Skill 的层级组合 |
| **Adapter** | 接口兼容、第三方集成 | 🧱 MCP 工具适配不同 API |
| **Decorator** | 职责动态叠加 | 🧱 Agent 中间件、Prompt 装饰链 |
| **Facade** | 简化复杂子系统 | 🧱 Agent 对多工具的封装暴露 |
| **Command** | 请求封装、事务、撤销 | 🧱 Agent 动作序列化与回滚 |
| **Chain of Responsibility** | 请求链式处理 | 🧱 Agent 工具调用链、审核流水线 |
| **State** | 状态驱动的行为切换 | 🧱 Agent 状态机、工作流编排 |
| **Template Method** | 算法骨架固定，步骤可变 | 🧱 Skill 模板、Prompt 模板 |
| **Visitor** | 在不修改类的前提下增加操作 | 🧱 AST/CST 操作、代码生成后处理 |

### SOLID 与设计原则

- [SOLID 原则详解](https://www.digitalocean.com/community/conceptual-articles/s-o-l-i-d-the-first-five-principles-of-object-oriented-design)
- [Martin Fowler — Patterns of Enterprise Application Architecture](https://martinfowler.com/eaaCatalog)

| 原则 | 核心思想 | AGI 应用 |
|------|---------|---------|
| **SRP** | 一个类/模块只有一个变更理由 | Agent 技能拆解、工具职责单一 |
| **OCP** | 对扩展开放，对修改关闭 | MCP 工具可插拔设计 |
| **LSP** | 子类型可替换父类型 | Agent 工具接口契约 |
| **ISP** | 接口应小而专 | Skill 粒度设计、上下文窗口优化 |
| **DIP** | 依赖抽象而非具体实现 | Agent 通过 MCP 协议而非具体 API |

### 架构模式

- [10 Common Software Architectural Patterns](https://towardsdatascience.com/10-common-software-architectural-patterns-in-a-nutshell-a0b47a1e9013)
- [Reactive Design Patterns](https://www.reactivedesignpatterns.com/categories.html)
- [System Design Primer](https://github.com/donnemartin/system-design-primer)
- [Martin Fowler — GUI Architectures](https://martinfowler.com/eaaDev/uiArchs.html)

### 分布式系统模式

- [Martin Fowler — Patterns of Distributed Systems](https://martinfowler.com/articles/patterns-of-distributed-systems/)
- [Scalable System Design Patterns](https://dzone.com/articles/scalable-system-design)
- [Enterprise Integration Patterns](http://www.enterpriseintegrationpatterns.com/patterns/messaging/toc.html)

### 数据库模式

- [SQL Table Design Patterns](http://database-programmer.blogspot.com/2008/01/table-design-patterns.html)
- [SQLCheck — Anti-patterns in SQL](https://github.com/jarulraj/sqlcheck)
- [MongoDB Design Patterns](https://www.mongodb.com/blog/post/building-with-patterns-a-summary)
- [DynamoDB Design Patterns](https://amazon-dynamodb-labs.com/design-patterns.html)
- [Redis Applied Design Patterns](https://redislabs.com/redis-best-practices/introduction/)
- [ETL/ELT Design Patterns for Lake House](https://aws.amazon.com/blogs/big-data/etl-and-elt-design-patterns-for-lake-house-architecture-using-amazon-redshift-part-1/)
- [Industry-specific SQL Data Models](http://www.databaseanswers.org/data_models)

---

## 🛠 仍很重要的模式

> AI 正在逐步接管这些模式的实现和运维细节，但架构决策和取舍仍需人来掌握。

### 云架构模式

- [AWS Cloud Design Patterns](http://en.clouddesignpattern.org/index.php/Main_Page)
- [Azure Cloud Design Patterns](https://docs.microsoft.com/en-us/azure/architecture/patterns)
- [Cloud Computing Patterns](http://www.cloudcomputingpatterns.org)
- [Google Cloud Solutions](https://gcp.solutions)
- [SaaS Tenant Isolation Strategies](https://d1.awsstatic.com/whitepapers/saas-tenant-isolation-strategies.pdf)
- [Multi-Tenancy Design Patterns on AWS](https://www.nagarro.com/en/blog/architectural-design-patterns-aws-multi-tenancy)
- [Cloud Cost Hacking](https://hackernoon.com/cloud-cost-hacking-fc35fd19985d)

### 微服务模式

- [Microservices.io — Pattern Language](http://microservices.io/patterns)
- [12 Factor App](https://12factor.net)
- [Microservices Antipatterns](https://www.oreilly.com/ideas/microservices-antipatterns-and-pitfalls)
- [Microservices: Sync vs Async](https://dzone.com/articles/patterns-for-microservices-sync-vs-async)
- [Message Queue Architectures](http://tech.forter.com/comparing-message-queue-architectures-on-aws)

### 容器与 K8s 模式

- [Containers Patterns](https://l0rd.github.io/containerspatterns)
- [Kubernetes Patterns](https://k8spatterns.io/)
- [Kubernetes Production Patterns](https://github.com/gravitational/workshop/blob/master/k8sprod.md)
- [Container Design Patterns for Pods](https://vitalflux.com/container-design-patterns-kubernetes-pods-design)

### 安全模式

- [OWASP Security by Design Principles](https://owasp.org/www-community/Security_by_Design_Principles)
- [Open Security Architecture — Pattern Landscape](http://www.opensecurityarchitecture.org/cms/library/patternlandscape)
- [Martin Fowler — Web Security Basics](https://www.martinfowler.com/articles/web-security-basics.html)
- [Cloud Security Architecture](https://www.infoq.com/articles/cloud-security-architecture-intro)

### 前端架构模式

- [React Patterns](https://reactpatterns.com)
- [Vue Patterns](https://learn-vuejs.github.io/vue-patterns/)
- [UI Patterns](http://ui-patterns.com)
- [Responsive Design Patterns](https://bradfrost.github.io/this-is-responsive/patterns.html)
- [CSS Protips](https://github.com/AllThingsSmitty/css-protips)

---

## 🔄 AGI 时代的全新模式

> 这些是传统设计模式书籍中不存在、但在 AI 编程时代至关重要的新模式。

### Agent 编排模式

- [Anthropic — Building Effective Agents](https://docs.anthropic.com/en/docs/build-with-claude/agentic) — Agent 架构模式官方指南。
- [OpenAI — Agent Patterns](https://platform.openai.com/docs/guides/agents) — OpenAI Agent 架构最佳实践。
- [LangGraph — Agent Architecture Patterns](https://langchain-ai.github.io/langgraph/)
- [Patterns for Agentic Systems](https://www.deeplearning.ai/the-batch/how-agents-can-improve-llm-performance/) — Andrew Ng 关于 Agent Workflow 的经典文章。

| 模式 | 描述 |
|------|------|
| **Chain of Thought** | 逐步推理，中间结果可观察 |
| **ReAct (Reason + Act)** | 推理与工具调用交替进行 |
| **Plan-Execute** | 先规划再执行，长任务分解 |
| **Multi-Agent Debate** | 多 Agent 交叉验证提高正确性 |
| **Reflection** | Agent 自我审查与修正 |
| **Tool-use Loop** | 循环调用工具直到任务完成 |
| **Human-in-the-Loop** | 关键节点人工确认 |
| **Orchestrator-Workers** | 中央编排 + 子任务 Worker |

### MCP / 工具集成模式

- [Model Context Protocol — Specification](https://modelcontextprotocol.io/)
- [MCP Servers Directory](https://github.com/modelcontextprotocol/servers)
- [OpenAI Function Calling Docs](https://platform.openai.com/docs/guides/function-calling)

| 模式 | 描述 |
|------|------|
| **Resource as Tool** | 将数据资源暴露为 Agent 可用的工具 |
| **Prompt Template Injection** | 通过 MCP 注入特定技能的 Prompt |
| **Context Window Management** | 管理工具的上下文窗口占用 |
| **Tool Permission Scoping** | 工具的最小权限原则 |
| **Fallback Tool Chain** | 主工具失败时的降级策略 |
| **Tool Composition** | 多个工具组合为复合能力 |

### Skill / Workflow 编排模式

- [OpenCode Skills](https://opencode.ai/docs/guides/skills)
- [OpenCode Workflows](https://opencode.ai/docs/guides/workflows)
- [Cline — Custom Instructions & MCP](https://github.com/cline/cline)

| 模式 | 描述 |
|------|------|
| **Skill Composition** | 多个 Skill 按需组合为复杂能力 |
| **Workflow as Pipeline** | 将工作流建模为数据管道 |
| **Checkpoint & Resume** | 工作流中断后的断点续传 |
| **Parallel Fan-out** | 并行执行多个独立子任务 |
| **Conditional Branching** | 基于中间结果的工作流分支 |
| **Retry with Escalation** | 失败后自动重试 + 升级处理 |
| **Approval Gate** | 关键操作前的人工审批节点 |
| **Observability Hook** | 在工作流中嵌入监控和日志点 |

### 人机协作模式

| 模式 | 描述 |
|------|------|
| **Progressive Autonomy** | 从完全监督逐步过渡到自主执行 |
| **Trust Calibration** | 基于历史准确性动态调整信任等级 |
| **Review Boundary** | 明确定义哪些输出需要人工审查 |
| **Suggestion Mode** | Agent 只建议不执行，由人决策 |
| **Diff Review** | 只审查变更部分而非完整输出 |
| **Structured Handoff** | 明确的上下文交接协议 |

### RAG 与知识管理模式

- [LangChain — RAG Patterns](https://python.langchain.com/docs/use_cases/question_answering/)
- [LlamaIndex — RAG Best Practices](https://docs.llamaindex.ai/en/stable/)
- [Anthropic — Contextual Retrieval](https://www.anthropic.com/news/contextual-retrieval)

| 模式 | 描述 |
|------|------|
| **Chunking Strategy** | 文档分块策略（固定/语义/递归） |
| **Multi-stage Retrieval** | 先粗筛再精排的检索流程 |
| **Hybrid Search** | 关键词 + 向量混合搜索 |
| **Query Rewriting** | 将用户问题改写为更好的检索 query |
| **Contextual Retrieval** | 带上下文的检索增强 |
| **Cache-as-Tool** | 将缓存封装为 Agent 可用工具 |

### 代码生成与验证模式

| 模式 | 描述 |
|------|------|
| **Generate-Test Loop** | 生成代码 → 运行测试 → 修复 |
| **Progressive Refinement** | 分步生成，逐步精化 |
| **Self-Consistency Check** | 多种方式验证结果一致性 |
| **Test-as-Specification** | 测试用例作为需求的精确描述 |
| **Diff-only Apply** | 只应用生成代码的变更部分 |
| **Vulnerability Scanning Gate** | 生成代码自动安全扫描 |

---

## 📖 特定领域模式

> 这些是特定技术领域的模式，按需查阅即可。

### 物联网
- [IoT Communication Patterns](https://dzone.com/articles/strengths-and-weaknesses-of-iot-communication-patterns)
- [Design Patterns for IoT](https://community.arm.com/iot/b/blog/posts/design-patterns-for-an-internet-of-things)

### 大数据
- [MapReduce Patterns](https://highlyscalable.wordpress.com/2012/02/01/mapreduce-patterns)
- [Stream Processing Patterns](https://iwringer.wordpress.com/2015/08/03/patterns-for-streaming-realtime-analytics)

### 机器学习
- [Distributed ML Patterns](https://github.com/terrytangyuan/distributed-ml-patterns)

### 移动端
- [iOS Architecture Patterns](https://medium.com/ios-os-x-development/ios-architecture-patterns-ecba4c38de52)
- [Common Design Patterns for Android](https://www.raywenderlich.com/109843/common-design-patterns-for-android)

---

## 如何在这个 AGI 时代学习设计模式

1. **先学核心概念（🧱 层）** — Strategy、Factory、Observer、Composite、Adapter 是所有 AI 工具架构的底层。理解了这些，你就理解了为什么 MCP 长这样。
2. **理解 SOLID（🧱 层）** — 这是你审查 AI 生成代码质量的标准。
3. **掌握分布式基础（🧱 层）** — Agent 分布式协作的底层逻辑。
4. **了解传统模式在哪里被 AI 推翻（🛠 → 🔄）** — 比如 Builder 模式在 AI 生成代码时代已不需要手写。
5. **学习 AGI 新模式（🔄 层）** — Agent 编排、Skill 组合、MCP 工具设计、人机协作是你在 AGI 时代的核心技能。

---

## 本仓库的演变（原始内容 → AGI 版本对比）

这个仓库最初（2018 年）是一个传统的 Awesome List，汇总了前 AGI 时代的各类设计模式资源。
以下是原始内容的去向：

### 保留并升级

| 原始章节 | 新位置 | 变更 |
|---------|--------|------|
| General Architecture | 🧱 架构模式 / 分布式系统模式 | 保留，补充 AGI 时代解读 |
| Micro services & Distributed Systems | 🧱 分布式系统模式 / 🛠 微服务模式 | 保留核心，精简实现细节 |
| Cloud Architecture | 🛠 云架构模式 | 保留，标注 AI 接管趋势 |
| Databases & Storage | 🧱 数据库模式 | 保留核心，删去过时的具体产品链接 |
| DevOps & Containers | 🛠 容器与 K8s 模式 | 保留，精简 |
| Security | 🛠 安全模式 | 保留核心 |
| Front End Development | 🛠 前端架构模式 | 保留，删去 BEM/OOCSS 等过时内容 |
| GoF / SOLID | 🧱 GoF 经典设计模式 / SOLID | 大幅加强，逐个模式标注 AGI 应用场景 |
| Books | 📚 推荐阅读 | 保留经典，新增 AGI 必读 |

### 删除或精简

| 原始章节 | 处理 | 原因 |
|---------|------|------|
| Programming Language Design Patterns | ❌ **删除** | AI 可在任何语言间翻译模式，按语言列实现已无意义。保留 Refactoring Guru 作为语言无关参考。 |
| Serverless Architecture | 🔀 合并到 🛠 云架构 | 无服务器已不是独立领域，而是云架构的子集 |
| Internet of Things | 📖 精简为 2 个链接 | 领域过窄 |
| Big Data | 📖 精简为 2 个链接 | MapReduce 已不是主流关注点 |
| Machine Learning | 📖 精简为 1 个链接 | ML 模式发展迅速，原链接已过时 |
| Mobile | 📖 精简 | 移动端架构已稳定，框架化 |
| UML | ❌ **删除** | 类图生成 AI 已内置，无需单独资源 |
| AngularJS | ❌ **删除** | AngularJS 已 EOL |

### 新增

新章节全部是原仓库没有的内容：

- 🔄 **AGI 时代的全新模式**（整个章节）— Agent 编排、MCP、Skill/Workflow、人机协作、RAG、代码验证
- 🟢🟡🔴 **AGI 时代学习路线图** — 明确告诉你哪些值得学、哪些不用学
- 🧱🛠🔄📖 **分层体系** — 每个模式的价值层级一目了然

---

## 📚 推荐阅读

### 经典必读
- [Design Patterns: Elements of Reusable Object-Oriented Software](https://www.amazon.com/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612/) — GoF 四人帮，永恒经典
- [Head First Design Patterns](https://www.amazon.com/Head-First-Design-Patterns-Brain-Friendly/dp/0596007124/) — 最容易入门的模式书
- [Effective Java (3rd Edition)](https://www.amazon.com/Effective-Java-3rd-Joshua-Bloch/dp/0134685997/) — Java 最佳实践的模式化总结，超越语言
- [Game Programming Patterns](https://github.com/munificent/game-programming-patterns) — 模式在实际游戏引擎中的应用

### 架构与分布式
- [Designing Microservices](https://www.manning.com/books/designing-microservices)
- [Node.js Design Patterns](https://www.packtpub.com/web-development/nodejs-design-patterns-second-edition)
- [Object Design Style Guide](https://www.manning.com/books/object-design-style-guide)

### AGI / Agent 模式必读
- [Anthropic — Building Effective Agents](https://docs.anthropic.com/en/docs/build-with-claude/agentic)
- [OpenAI — Agent Patterns Guide](https://platform.openai.com/docs/guides/agents)
- [Model Context Protocol](https://modelcontextprotocol.io/)
- [LangGraph Documentation](https://langchain-ai.github.io/langgraph/)

---

## 贡献

欢迎贡献！请先阅读 [contributing guidelines](contributing.md)。

本仓库特别欢迎：
- AGI 时代的新模式资源
- 经典模式的 AGI 时代新解读
- 模式在 AI 编程中的实际案例
- 反模式 — 在 AI 时代常见的设计错误

---

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0)

To the extent possible under law, this work has been adapted from [Dov Amir's original](https://github.com/DovAmir/awesome-design-patterns).
