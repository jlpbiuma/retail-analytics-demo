# Retail Analytics Platform & AI Agent 🛍️🤖

A comprehensive full-stack retail platform featuring a persistent shopping cart, favorites system, and an AI agent powered by n8n and Ollama.

## 🏗️ Project Architecture

The project is structured as a main orchestrator with submodules:

- **[Backend](https://github.com/REPLACE_WITH_YOUR_BACKEND_URL)**: FastAPI service handling commerce logic, products, and agent proxy.
- **[Frontend](https://github.com/REPLACE_WITH_YOUR_FRONTEND_URL)**: Next.js application with a modern UI and sticky agent bubble.
- **[ETL](https://github.com/REPLACE_WITH_YOUR_ETL_URL)**: Python scripts for data synchronization and database schema management.
- **Database**: PostgreSQL 15.

---

## 🚀 Getting Started

### 1. Clone the project with submodules
```bash
git clone --recursive <MAIN_REPO_URL>
cd retail-analytics-complete
```

### 2. Set up Environment Variables
Copy the template and adjust values:
```bash
cp .env.example .env
```

### 3. Start the Infrastructure
```bash
docker-compose up -d
```

### 4. Initialize Data
Run the ETL scripts to populate the database:
```bash
cd etl
uv run python sync_sequences.py
# (Run other ETL scripts as needed)
```

---

## 🤖 AI Agent Integration (n8n)

The AI agent is orchestrated by **n8n** to provide secure, tool-enabled interactions.

- **Orchestrator**: n8n Webhook -> AI Agent Node -> Ollama LLM.
- **Tools**: The agent can search products, manage carts, and check favorites via backend proxy.
- **Memory**: Persistent Postgres Chat Memory stores conversation history by `user_id`.

### n8n Setup
1. Access n8n at `http://localhost:5678`.
2. Import the agent workflow.
3. Toggle the workflow to **Active** to enable the production webhook.

---

## 🛠️ Tech Stack
- **Frontend**: Next.js, Tailwind CSS, Lucide Icons, Sonner.
- **Backend**: FastAPI, SQLAlchemy, Pydantic, HTTPX.
- **AI**: Ollama (llama3.2), n8n.
- **Database**: PostgreSQL.
