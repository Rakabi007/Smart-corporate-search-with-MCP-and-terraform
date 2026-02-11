# The Smart Corporate Search 🤖

An intelligent internal RAG (Retrieval Augmented Generation) application that allows you to query your internal systems using natural language. Ask questions like "Who is our biggest customer by total revenue?" and get instant answers with detailed analysis, interactive charts, and actionable business insights powered by AI agents and your corporate data.

## ✨ Key Features

- **Natural Language Queries**: Ask complex business questions in plain English
- **Intelligent Analysis**: AI agents provide detailed insights and contextual analysis
- **Interactive Charts**: Automatic visualization generation for trends, comparisons, and distributions
- **Sequential Agent Architecture**: Specialized agents for data retrieval and presentation
- **Real-time Chat Interface**: Streamlit-powered frontend with persistent chat history
- **SQL Tool Integration**: MCP toolbox with comprehensive database operations

## 🏗️ Architecture

This project consists of four main components:

- **Frontend (Port 8501)**: Streamlit-based chat interface with interactive chart rendering
- **AI Agent (Port 8080)**: FastAPI + Google ADK featuring sequential agent architecture (retriever + presenter)
- **MCP Toolbox (Port 8081)**: Model Context Protocol server with 8 SQL tools
- **PostgreSQL (Port 5432)**: Database with sample e-commerce dataset

## 🚀 Quick Start

### Prerequisites

- Docker and Docker Compose
- Google AI API Key (Gemini)

### Setup

1. **Clone the repository**

   ```bash
   git clone <your-repo-url>
   cd the-smart-corporate-search-v2
   ```

2. **Configure your Google AI API Key**

   ```bash
   cp ai-agent/corporate_agent/.env.example ai-agent/corporate_agent/.env
   ```
   
   Edit `ai-agent/corporate_agent/.env`:

   ```env
   GOOGLE_API_KEY=your_google_ai_api_key_here
   GOOGLE_GENAI_USE_VERTEXAI=0
   ```

3. **Start all services**

   ```bash
   docker-compose up --watch
   ```

4. **Access the application**
   - Frontend: [http://localhost:8501](http://localhost:8501)
   - AI Agent API: [http://localhost:8080](http://localhost:8080)
   - MCP Toolbox: [http://localhost:8081](http://localhost:8081)

## 📝 Usage Examples

- **"Who is our biggest customer by total revenue?"** — Text analysis with revenue figures
- **"What was the revenue per month for January to July 2024?"** — Interactive bar charts
- **"Give me the top 2 customers who made the most purchases in 2024"** — Comparative visualizations

## 📄 License

MIT
