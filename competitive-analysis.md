 竞品分析

现有中文法律 RAG 问答系统调研：

项目	链接	技术栈	核心功能	缺陷
law-assistant	https://github.com/silence4allen/law-assistant	LlamaIndex + ChromaDB + GLM-4 + Streamlit	劳动法RAG检索 + 法条溯源 + 思维链可视化	仅做问答，无降级兜底，意图识别只有关键词硬匹配
legal-qa-system	https://github.com/NEO-7-hash/legal-qa-system	RAG + Qwen + FAISS + Docker	CLI/Web/API三端 + 法条溯源	无兜底策略，无意图分流
legal_AI_assistant	https://github.com/Jaron-U/legal_AI_assistant	RAG + Qwen + ElasticSearch	意图识别99% + 查询重写命中率98%	无降级兜底，分类粒度粗
RAGknowledge	https://github.com/l1iquan/RAGknowledge	FAISS + m3e-base + GPT	RAG评估模块 + BLEU/ROUGE评测	侧重评测，非产品设计
ChatLaw	https://github.com/PKU-YuanGroup/ChatLaw	自研MoE + 知识图谱	法考超越GPT-4	研究型项目，无工程兜底

结论：现有项目均聚焦"如何回答"，未覆盖"回答不了怎么办"以及"如何从咨询过渡到律师对接"。本项目差异点：双LLM解耦（咨询+路由）、四层降级兜底、HITL人工确认机制、用户→Agent→真人律师的完整链路。
