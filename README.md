# AI Evidence Quest：基于生产级 RAG 项目的高中 AI 项目教材

> 本教材从高 star 开源项目 [jamwithai/production-agentic-rag-course](https://github.com/jamwithai/production-agentic-rag-course) 改造而来。原项目以 arXiv 论文助手为主线，覆盖数据摄取、BM25、混合检索、RAG、监控、缓存与 Agentic RAG。本仓库把这条工程路线压缩、重排并转译为适合高中人工智能课程与科创社团的项目式教材。

## 这本书的主线

本书只围绕一个问题展开：**如何让 AI 回答问题时给出可追溯证据，并知道什么时候应该拒答**。

学习者最终会完成一个“校园资料问答助手”：输入关于校规、活动安排、课程介绍的提问，系统先检索资料，再生成回答，并展示引用来源、置信度与拒答理由。课程不把“会调用大模型”当作终点，而把检索、证据、评价与安全边界作为核心。

## 上游底座

本仓库不是从零搭空架子，而是把一个完整生产级 RAG 课程拆解成高中课堂可承载的层级。

| 来源 | 许可 | 在本书中的作用 |
| --- | --- | --- |
| [production-agentic-rag-course](https://github.com/jamwithai/production-agentic-rag-course) | MIT | 主底座：RAG 工程路线、检索架构、Notebook 周计划、关键服务代码 |
| [datawhalechina/easy-vecdb](https://github.com/datawhalechina/easy-vecdb) | Apache-2.0 | 参考：向量数据库与 ANN 检索的中文解释框架 |

已纳入本仓库的上游材料位于 [`source-project/production-agentic-rag-course`](source-project/production-agentic-rag-course/README.upstream.md)，包括原项目 README、许可、架构图、周学习 README 与若干关键服务代码。教材正文会明确标注“来自上游工程的概念”与“高中化改造后的任务”。

## 教材结构

| 编 | 内容 | 产出 |
| --- | --- | --- |
| 第一编：读懂一个真实 RAG 系统 | 从上游项目的 7 周路线读懂检索增强生成 | 一张系统结构图与术语卡片 |
| 第二编：把生产系统降维到校园资料 | 把论文助手改造成校园资料问答助手 | 校园资料集、分块方案、检索日志 |
| 第三编：检索先于生成 | BM25、向量相似、混合检索与重排 | 可解释的检索排序实验 |
| 第四编：可信回答 | 引用、拒答、反幻觉、评价表 | 可演示的可信问答 Demo |
| 第五编：科创扩展 | 监控、缓存、Agentic RAG 的可选挑战 | 社团展示版项目报告 |

## 互动实验

- [证据检索 Playground](https://sherkevin.github.io/ai-evidence-quest/labs/playground.html)：浏览器内运行的小型检索实验，用于观察关键词命中、语义相似、证据引用与拒答边界。
- [`source-project/production-agentic-rag-course/src/services`](source-project/production-agentic-rag-course/src/services/)：来自上游项目的文本切分、OpenSearch 查询与 Agentic RAG 代码，用于教师备课和进阶讲解。

## 适用场景

- 高中人工智能校本课程
- 信息科技拓展课
- 科创社团项目
- “大模型应用与可信 AI”主题讲座

## 阅读方式

在线阅读：[https://sherkevin.github.io/ai-evidence-quest/](https://sherkevin.github.io/ai-evidence-quest/)

本仓库采用 Docsify / GitBook 兼容目录组织。`SUMMARY.md` 可供 GitBook 类工具读取，`sidebar.md` 供在线站点使用。
