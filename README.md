# main


🔥 Agentic Web Scraping Assistant (MCP + LangGraph + Firecrawl)

This project implements an Agentic AI assistant that can search, scrape, crawl, and extract data from websites using **Firecrawl tools** via the **Model Context Protocol (MCP).
The agent is powered by a ReAct-style reasoning loop** built with LangGraph and an LLM accessed through **OpenRouter**.

---

🚀 What This Project Does

* Connects to a Firecrawl MCP server using stdio
* Dynamically loads scraping and crawling tools
* Uses a ReAct agent to reason and decide when to call tools
* Allows users to interactively query websites from the terminal
* Returns structured, LLM-generated insights from live web data

---

🧠 Tech Stack

* Python
* LangGraph – ReAct agent framework
* LangChain MCP Adapters – Tool loading via MCP
* Firecrawl MCP – Web scraping & crawling
* OpenRouter – LLM API gateway
* AsyncIO – Asynchronous execution

---

⚙️ How It Works (High-Level)

1. LLM Setup
   Uses `ChatOpenAI` with an OpenRouter-hosted model.

2. MCP Server Connection
   Starts the Firecrawl MCP server using `npx firecrawl-mcp`.

3. Tool Discovery
   Dynamically loads Firecrawl tools (search, scrape, crawl).

4. Agent Creation
   Builds a ReAct agent using LangGraph that can reason + act.

5. Interactive Chat Loop

   * User enters a query
   * Agent decides which tools to use
   * Scraped data is processed and summarized by the LLM

---

📦 Installation & Setup

1️⃣ Install Dependencies

```bash
pip install langchain langgraph langchain-openai langchain-mcp-adapters mcp python-dotenv
```

2️⃣ Install Firecrawl MCP

```bash
npm install -g firecrawl-mcp
```

3️⃣ Environment Variables

Create a `.env` file:

```env
OPENROUTER_API_KEY=your_openrouter_api_key
FIRECRAWL_API_KEY=your_firecrawl_api_key
```

---

## ▶️ Run the Agent

```bash
python main.py

Type your queries in the terminal:

```text
You: Scrape the pricing page of openai.com


Exit anytime:

```text
You: quit



🧩 Example Use Cases

* Tool & SaaS research
* Competitive analysis
* Pricing & feature extraction
* Developer documentation scraping
* Autonomous web data gathering agents

---

🌟 Why This Project Matters

This project demonstrates:

* Agentic AI design
* Tool-using LLMs
* MCP-based integrations
* Production-style async workflows

It’s a strong example of "real-world autonomous AI systems", not just basic chatbots.


📌 Future Improvements

* Structured outputs with Pydantic
* Persistent memory (vector DB)
* Multi-agent workflows
* Web UI (Streamlit / Next.js)
