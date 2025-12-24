# 🛒 Retail Analytics Platform & AI Agent 🤖

A state-of-the-art, "Smart Commerce" platform that blends a high-performance e-commerce engine with advanced AI choreography. This project demonstrates a production-ready architecture using micro-services, secure AI agents, and persistent state management across multiple repositories.

---

## 🌟 Key Features

### 🛍️ Secure Commerce Engine
- **Persistent Cart**: A full-stack shopping cart system that survives sessions and syncs across devices.
- **Wishlist & Favorites**: Smart-save system for users to build their curated collections.
- **User Intelligence**: Personalized profile dashboards featuring order histories and dynamic cart carousels.

### 🤖 AI Orchestration (n8n + Ollama)
- **Safe Tooling**: The AI agent utilizes the backend as a secure "middleware" proxy. It can search, add to cart, and manage favorites without ever touching the database directly.
- **Long-term Memory**: Powered by Postgres Chat Memory, allowing the agent to remember your name, preferences, and previous purchases.
- **Local Inference**: Uses local Ollama (llama3.2) to ensure data privacy and high speed.

### 🏗️ Advanced Infrastructure
- **Multi-Repo Architecture**: Distributed system using Git Submodules for independent scaling of Backend, Frontend, and ETL.
- **Docker Dynamic Orchestration**: A single `.env` file dynamically configures ports, secrets, and internal service URLs across the entire stack.

---

## 🏗️ Project Topology

The system is organized into specialized repositories:

- **🚀 [Backend](https://github.com/jlpbiuma/retail-analytics-demo-backend.git)**: FastAPI orchestrator handling the commerce layer and security proxy.
- **🎨 [Frontend](https://github.com/jlpbiuma/retail-analytics-demo-frontend.git)**: Next.js 14 Web App with a premium glassmorphic UI and sticky assistant bubble.
- **⚙️ [ETL](https://github.com/jlpbiuma/retail-analytics-demo-etl.git)**: Automated data pipeline for schema management and ingestion.
- **🗄️ Database**: PostgreSQL 15 hosting commerce data and persistent AI memory.

---

## 🚀 Quick Start

### 1. Clone & Initialize
```bash
git clone --recursive https://github.com/jlpbiuma/retail-analytics-demo.git
cd retail-analytics-complete
```

### 2. Configure Environment 🔑
The project uses **Docker Interpolation**. One file controls everything:
```bash
cp .env.example .env
# Open .env and adjust your ports or DB credentials
```

### 3. Launch the Stack 🐳
```bash
docker-compose up -d
```

---

## 🛠️ Tech Stack
- **Frontend**: Next.js, Tailwind CSS, Lucide Icons, Sonner.
- **Backend**: FastAPI, SQLAlchemy, Pydantic, HTTPX.
- **AI**: Ollama, n8n (Orchestrator).
- **Database**: PostgreSQL 15.
