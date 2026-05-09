# 1. 从生产级 RAG 课程拆出高中项目

本章先读一个真实工程，而不是直接写玩具 Demo。上游项目 `production-agentic-rag-course` 的主线是“arXiv Paper Curator”：系统自动获取论文、解析 PDF、建立检索索引，再用大模型回答研究问题。这个项目对高中课程来说过重，但它的结构很清楚，适合被改造成课堂项目。

## 原项目的 7 周路线

| 原项目阶段 | 工程问题 | 高中化改造 |
| --- | --- | --- |
| Week 1 Infrastructure | FastAPI、数据库、OpenSearch、Airflow | 用一张系统图认识“前端、资料库、检索器、大模型” |
| Week 2 Data Ingestion | 自动抓取 arXiv 与解析 PDF | 改为整理校园公开资料、社团章程、活动说明 |
| Week 3 Keyword Search | BM25 与 OpenSearch | 用关键词命中解释“为什么 AI 要先找资料” |
| Week 4 Hybrid Search | Chunking、Embedding、RRF | 用小型文本卡片比较关键词检索和语义检索 |
| Week 5 Complete RAG | 检索结果进入 LLM 生成回答 | 设计“回答必须带引用”的提示词模板 |
| Week 6 Monitoring & Cache | Langfuse、Redis、性能优化 | 用日志表记录问题、证据、回答质量 |
| Week 7 Agentic RAG | LangGraph、查询改写、守门节点 | 作为社团挑战：让系统判断要不要改写问题 |

## 课堂项目为什么不能直接照搬原项目

原项目是面向 AI 工程学习者的完整生产系统，技术栈较重。高中课堂如果直接要求 Docker、OpenSearch、Airflow、LangGraph 全部跑起来，注意力会被环境配置占满，反而看不见 RAG 的核心思想。

因此本书做两层改造：

- **课堂主线**：只保留“资料、检索、引用、拒答、评价”五个核心环节，使用浏览器实验和轻量脚本完成。
- **社团扩展**：把上游项目中的 FastAPI、OpenSearch、Agentic RAG 代码作为进阶阅读和二次开发素材。

## 本章动手任务

打开 [`source-project/production-agentic-rag-course/README.upstream.md`](../source-project/production-agentic-rag-course/README.upstream.md)，完成三件事：

1. 找出系统中负责“存资料”的模块。
2. 找出系统中负责“找资料”的模块。
3. 找出系统中负责“生成回答”的模块。

然后把它们画成一张四格图：

```text
资料来源 -> 检索器 -> 大模型 -> 带证据的回答
```

这张图会贯穿整本书。后面的每个实验都要回到这条线索上：AI 的回答从哪里来，证据在哪里，什么时候不能回答。
