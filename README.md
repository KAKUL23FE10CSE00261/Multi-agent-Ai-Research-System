# 🔬 ResearchMind – Multi-Agent AI Research System

ResearchMind is an AI-powered research assistant that automates the complete research workflow using multiple specialized AI components.

Instead of relying on a single LLM prompt, the system divides the task into dedicated stages—searching, web reading, report writing, and report evaluation—to generate well-structured and reliable research reports.

The project is built using **LangChain**, **Mistral AI**, **LCEL (LangChain Expression Language)**, **Tavily Search**, **BeautifulSoup**, and **Streamlit**.

---

## 🚀 Live Demo

**Live Application**

https://multi-agent-ai-research-system-nssxqvahqkv62kn99v4fba.streamlit.app/

---

## ✨ Features

- 🔎 AI-powered web search using Tavily Search API
- 🌐 Automatic webpage scraping using BeautifulSoup
- 🤖 Tool-enabled Search and Reader agents
- 📝 AI-generated structured research reports
- 📊 Automatic report evaluation with quality scoring
- ⚡ LCEL (Runnable Pipeline) implementation
- 🎨 Modern Streamlit UI
- 📚 Source-aware research generation
- 🔄 End-to-end automated research workflow

---

# 🏗️ System Architecture

```
                 User Query
                      │
                      ▼
              Search Agent
          (Tavily Search Tool)
                      │
                      ▼
              Reader Agent
        (BeautifulSoup Scraper)
                      │
                      ▼
              Writer Chain (LCEL)
                      │
                      ▼
              Critic Chain (LCEL)
                      │
                      ▼
              Final Research Report
```

---

# ⚙️ Tech Stack

### AI Framework

- LangChain
- LangChain Core
- LCEL (Runnable Pipeline)

### LLM

- Mistral AI (`mistral-small-latest`)

### Search

- Tavily Search API

### Web Scraping

- BeautifulSoup4
- Requests

### Frontend

- Streamlit

### Utilities

- Python
- dotenv
- Rich

---

# 📂 Project Structure

```
Multi-agent-Ai-Research-System
│
├── app.py              # Streamlit frontend
├── pipeline.py         # Complete research workflow
├── agents.py           # Search Agent, Reader Agent, Writer Chain & Critic Chain
├── tools.py            # Tavily Search + Web Scraper
├── requirements.txt
├── README.md
└── LICENSE
```

---

# 🔄 Research Pipeline

The workflow consists of four sequential stages.

## 1️⃣ Search Agent

Uses the Tavily Search API to search the web for recent and reliable information related to the user query.

Output:

- Relevant URLs
- Article titles
- Search snippets

---

## 2️⃣ Reader Agent

Selects the most relevant webpage and extracts clean textual content using BeautifulSoup.

This stage removes:

- Scripts
- Navigation bars
- Footer content
- HTML tags

to obtain readable research material.

---

## 3️⃣ Writer Chain

The Writer Chain combines:

- Search results
- Scraped webpage content

and generates a structured research report consisting of:

- Introduction
- Key Findings
- Conclusion
- Sources

---

## 4️⃣ Critic Chain

The Critic reviews the generated report and provides:

- Overall quality score
- Strengths
- Weaknesses
- Suggestions for improvement
- Final verdict

---

# 🛠️ Tools Used

## Tavily Search Tool

Responsible for searching recent web information.

Returns:

- Title
- URL
- Snippet

---

## BeautifulSoup Scraper

Responsible for extracting meaningful content from webpages while removing unnecessary HTML elements.

---

# 🔑 Environment Variables

Create a `.env` file in the project root.

```env
MISTRAL_API_KEY=your_mistral_api_key
TAVILY_API_KEY=your_tavily_api_key
```

---

# 📦 Installation

Clone the repository

```bash
git clone https://github.com/your-username/Multi-agent-Ai-Research-System.git
```

Move into the project

```bash
cd Multi-agent-Ai-Research-System
```

Install dependencies

```bash
pip install -r requirements.txt
```

Run the application

```bash
streamlit run app.py
```

---

# 💡 Example Query

```
Recent developments in Quantum Computing

Latest AI regulations in Europe

Impact of Generative AI on Healthcare

Future of Electric Vehicles
```

---

# 🎯 Future Improvements

- LangGraph workflow orchestration
- Multi-source webpage scraping
- PDF export
- Citation generation
- Research memory
- Multi-agent planning
- Follow-up question support
- Vector database integration
- RAG support
- Async execution

---

# 📚 Learning Outcomes

This project demonstrates:

- Multi-Agent AI Systems
- Tool Calling
- AI Workflow Orchestration
- Prompt Engineering
- LCEL (Runnable Pipelines)
- Web Search Integration
- Web Scraping
- Streamlit Deployment
- Mistral AI Integration
- LangChain Development

---

# 👨‍💻 Author

**Kakul Barsaiya**

B.Tech Computer Science Engineering

Manipal University Jaipur

---

# ⭐ If you found this project useful

Please consider giving this repository a ⭐ on GitHub.
