# 上游项目与授权说明

## 选型结论

本书采用 [jamwithai/production-agentic-rag-course](https://github.com/jamwithai/production-agentic-rag-course) 作为主底座。选择理由如下：

| 维度 | 观察 |
| --- | --- |
| Star | 约 5.8k stars，属于 RAG 课程类项目中关注度较高的工程项目 |
| License | MIT License，允许复制、修改、再发布，需保留版权和许可声明 |
| 完整度 | 覆盖 FastAPI、PostgreSQL、OpenSearch、Airflow、Ollama、Redis、Langfuse、LangGraph |
| 教学价值 | 按 Week 1-7 组织，天然适合改造成项目式课程 |
| 高中化空间 | 可以把论文助手降维成校园资料助手，保留检索、证据、评价、拒答等关键思想 |

辅助参考：

- [datawhalechina/easy-vecdb](https://github.com/datawhalechina/easy-vecdb)：Apache-2.0，适合作为向量数据库与 ANN 检索概念的中文参考。
- [datawhalechina/llm-universe](https://github.com/datawhalechina/llm-universe)：star 高，但未检测到明确 license，因此本仓库不直接复制其内容，只作为调研参照。

## 本仓库纳入的上游材料

`source-project/production-agentic-rag-course/` 下保留了以下材料：

- `LICENSE`：原项目 MIT License。
- `README.upstream.md`：原项目 README，便于追溯课程全貌。
- `static/`：原项目架构图，供教材讲解系统结构时引用。
- `notebooks/week*-README.md`：原项目每周学习说明，作为高中化改造的工程蓝本。
- `src/services/`：节选关键服务代码，包括文本切分、查询构造与 Agentic RAG 编排。

## 改造原则

1. 保留原项目的工程骨架：数据进入系统、建立索引、检索、生成、监控、扩展。
2. 替换问题情境：从 arXiv 论文助手改为校园资料问答助手。
3. 降低部署门槛：课堂主线用浏览器实验与轻量 Python，社团扩展再进入 Docker / FastAPI。
4. 保留“可信 AI”主线：所有回答必须能追溯资料来源，无法检索到证据时必须拒答。
5. 明确版权边界：直接纳入的上游材料保留 license；教材正文为面向高中场景重新组织和改写。

## 给招聘方看的项目价值

这个仓库展示的不是“会写几页 AI 介绍”，而是把成熟开源 AI 工程课程拆解为高中可实施教材的能力：能读懂真实系统，能选择合适难度，能设计分层实验，也能把项目交付成可在线阅读、可动手、可评价的课程资源。
