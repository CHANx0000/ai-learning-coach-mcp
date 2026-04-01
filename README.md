# 🎓 AI Learning Coach MCP — Personalized Learning Digest Server

[![](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=darkgreen)](https://www.python.org)
[![](https://img.shields.io/badge/FastMCP-000000?style=for-the-badge&logoColor=white)](https://github.com/jlowin/fastmcp)
[![](https://img.shields.io/badge/Supabase-3FCF8E?style=for-the-badge&logo=supabase&logoColor=white)](https://supabase.com/)
[![](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)](https://openai.com/)
[![](https://img.shields.io/badge/HuggingFace-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/)
[![](https://img.shields.io/badge/pgvector-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)](https://github.com/pgvector/pgvector)
[![](https://img.shields.io/badge/RAG-1C3C3C?style=for-the-badge&logoColor=white)](https://en.wikipedia.org/wiki/Retrieval-augmented_generation)
[![](https://img.shields.io/badge/Claude_Desktop-191919?style=for-the-badge&logo=anthropic&logoColor=white)](https://claude.ai/)

---

> 🚧 **Status: In Development** — This project is currently being built. README describes the planned scope and architecture.

## 📌 Problem

Learning new topics requires sifting through dozens of sources daily — blogs, X posts, Reddit threads, documentation. The process of finding relevant content matched to your current skill level is manual and inconsistent. Most learners either drown in beginner content they've outgrown or jump into advanced material they're not ready for.

## 🎯 What AI Learning Coach Will Do

An MCP (Model Context Protocol) server that acts as a personal AI Learning Coach. It tracks your learning progress, fetches relevant content from trusted sources using RAG, and generates daily personalized learning digests — all accessible through Claude Desktop as a natural conversation.

## 🔧 Planned Features

* **Content Management** — Store learning content from trusted sources (blogs, X, Reddit). Track current week, topics, and learning goals.
* **Daily Learning Digest** — Generate 5–7 personalized learning insights each day using RAG. Adapt difficulty based on current progress week.
* **MCP Tool Calls** — `generate_daily_digest`, `add_content_source`, `update_progress`, `search_insights` — all callable from Claude Desktop.
* **Semantic Search** — Vector embeddings to match content to current learning topics. Relevance scoring using RAGAS evaluation.

## 🏗 Planned Architecture

```
learning-coach-mcp/
├── src/
│   ├── server.py              # Main MCP server with tools
│   ├── rag/
│   │   └── digest_generator.py # RAG pipeline
│   ├── ingestion/
│   │   └── content_fetcher.py  # RSS feed / content scraper
│   └── utils/
│       ├── database.py         # Supabase client
│       └── openai_client.py    # OpenAI client
├── .env
└── requirements.txt
```

## 🛠 Planned Tech Stack

| Category | Tools |
|----------|-------|
| **MCP Server** | FastMCP |
| **Database** | Supabase (PostgreSQL + pgvector) |
| **Embeddings** | OpenAI text-embedding-3-small, HuggingFace models |
| **LLM** | OpenAI GPT for insight generation |
| **Client** | Claude Desktop |
| **Evaluation** | RAGAS for relevance scoring |
| **Language** | Python |

## 🗺 How It Will Work

1. **Setup** — User adds trusted learning sources through Claude Desktop
2. **Background** — System periodically scrapes and embeds new content
3. **Daily** — User asks Claude to generate a digest; MCP server uses RAG to create relevant insights matched to the user's current level
4. **Progress** — User updates their week/topics; future digests adapt accordingly

---

## 📬 Contact

- **GitHub:** [CHANx0000](https://github.com/CHANx0000)
