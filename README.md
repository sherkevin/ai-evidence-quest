# AI Evidence Quest：智能体与可信问答项目课

这是一套以智能体课程为主体的高中 AI 项目教材。仓库主路径保留完整 lesson、notebook、代码示例和图示资源，课堂展示只在首页、目录与导读层做必要整理，避免把厚课程压缩成几页说明。

课程主线是：**工具调用、Agentic RAG、多智能体协作、可信智能体、安全与生产部署**。学习者最终完成一个“校园资料智能体”：它能调用检索工具、检查资料来源、生成带证据回答，并在证据不足或问题越界时拒答。

## 课程主体

| 单元 | 主题 | 主要材料 |
| --- | --- | --- |
| 00 | 课程环境 | `00-course-setup/` |
| 01 | AI Agents 入门 | `01-intro-to-ai-agents/` |
| 02 | 智能体框架 | `02-explore-agentic-frameworks/` |
| 03 | Agentic Design Patterns | `03-agentic-design-patterns/` |
| 04 | Tool Use | `04-tool-use/` |
| 05 | Agentic RAG | `05-agentic-rag/` |
| 06 | Trustworthy Agents | `06-building-trustworthy-agents/` |
| 07 | Planning Design | `07-planning-design/` |
| 08 | Multi-Agent | `08-multi-agent/` |
| 09 | Metacognition | `09-metacognition/` |
| 10 | Production Agents | `10-ai-agents-production/` |
| 11 | MCP / A2A Protocols | `11-agentic-protocols/` |
| 12 | Context Engineering | `12-context-engineering/` |
| 13 | Agent Memory | `13-agent-memory/` |
| 14 | Microsoft Agent Framework | `14-microsoft-agent-framework/` |
| 15 | Browser Use | `15-browser-use/` |
| 18 | Securing AI Agents | `18-securing-ai-agents/` |

## 高中课堂路径

这套课不要求高中阶段完整跑通所有云服务。课堂建议采用“三层路径”：

| 层级 | 学习目标 | 推荐单元 |
| --- | --- | --- |
| 入门课 | 认识智能体、工具调用、证据回答 | 01、03、04、05 |
| 项目课 | 做一个校园资料智能体 | 05、06、07、08、12 |
| 科创社团 | 多智能体、MCP、浏览器代理、安全 | 08、10、11、14、15、18 |

## 互动实验室

[证据检索实验室](https://sherkevin.github.io/ai-evidence-quest/labs/playground.html) 是本仓库的轻量课堂前端，用来快速演示资料卡片、混合检索、拒答阈值和引用记录。正式项目代码和 Notebook 以各 lesson 目录为准。

## 原始课程与许可

本仓库主体材料来自 Microsoft 官方课程 [AI Agents for Beginners](https://github.com/microsoft/ai-agents-for-beginners)（MIT License，约 61k stars），并保留其 lesson 结构、notebook 与代码示例。生成式 AI、RAG 和向量数据库补充材料见 `source-project/microsoft-generative-ai-for-beginners/`。许可与来源见 [开源许可与课程资源](LICENSES.md)。

## 阅读方式

在线阅读：[https://sherkevin.github.io/ai-evidence-quest/](https://sherkevin.github.io/ai-evidence-quest/)

本仓库采用 Docsify / GitBook 兼容目录组织。`SUMMARY.md` 可供 GitBook 类工具读取，`sidebar.md` 供在线站点使用。
