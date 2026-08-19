# 🤖 Agentic AI using LangChain

A hands-on learning repository for exploring **LangChain** and building **Agentic AI applications** using Large Language Models (LLMs), tools, APIs, agents, and external services.

This repository contains experiments, mini-projects, and implementations created while learning LangChain and modern Generative AI application development.

---

## 🚀 What This Repository Covers

The repository focuses on the following concepts:

* 🦜 LangChain fundamentals
* 🤖 LLM integration
* 🔧 Tool integration
* 🧠 AI Agents
* 🔌 API integration
* 🛠️ Custom tools
* 📡 External API calling
* 💬 Prompt engineering
* 🔗 Chains and workflows
* 🧩 Agent-based workflows
* 🌐 Generative AI applications
* 🔐 Environment variables and API keys
* 🐍 Python-based AI application development

---

## 🏗️ Tech Stack

| Technology    | Purpose                         |
| ------------- | ------------------------------- |
| Python        | Primary programming language    |
| LangChain     | LLM application framework       |
| Google Gemini | Large Language Model            |
| LangGraph     | Agent/workflow concepts         |
| APIs          | External data and services      |
| dotenv        | Environment variable management |
| Git & GitHub  | Version control                 |

---

## 📂 Repository Structure

```text
Agentic-AI-using-Langchain/
│
├── .venv/                  # Virtual environment
├── notebooks/              # Experiments and learning notebooks
├── tools/                  # Custom LangChain tools
├── agents/                 # Agent implementations
├── projects/               # Mini projects
├── api/                    # API integration examples
│
├── .env                    # Environment variables (not committed)
├── .gitignore
├── requirements.txt
└── README.md
```

> The structure may evolve as new LangChain concepts and projects are added.

---

## 🧠 Learning Roadmap

### 1. LangChain Fundamentals

* Understanding LangChain
* LLMs and Chat Models
* Prompts
* Prompt Templates
* Messages
* Output Parsers
* Chains
* Runnables

### 2. Model Integration

Learning how to connect different LLM providers with LangChain.

Example:

```python
from langchain.agents import create_agent

agent = create_agent(
    model="gemini-2.5-flash",
    tools=[],
    system_prompt="You are a helpful AI assistant."
)
```

---

### 3. Tool Integration

One of the main focuses of this repository is learning how AI agents can use external tools.

Example:

```python
def get_weather(city: str) -> str:
    """Get the weather for a city."""
    return f"The weather in {city} is sunny."
```

The function can then be provided to an agent as a tool:

```python
agent = create_agent(
    model="gemini-2.5-flash",
    tools=[get_weather],
    system_prompt="You are a helpful assistant."
)
```

This allows the agent to decide when a tool should be used.

---

## 🔌 API Integration

The repository also explores integrating external APIs with LangChain tools.

Typical workflow:

```text
User
 │
 ▼
AI Agent
 │
 ├── Understands the request
 │
 ├── Selects a tool
 │
 ▼
Custom Tool
 │
 ▼
External API
 │
 ▼
API Response
 │
 ▼
AI Agent
 │
 ▼
Final Answer
```

Examples of APIs that can be integrated:

* Weather APIs
* Search APIs
* Database APIs
* Financial APIs
* REST APIs
* Custom backend APIs

---

## 🤖 Agents

The repository explores how agents can:

1. Understand a user's request
2. Decide whether a tool is required
3. Select the appropriate tool
4. Execute the tool
5. Process the result
6. Generate the final response

Conceptually:

```text
                ┌──────────────┐
                │    User      │
                └──────┬───────┘
                       │
                       ▼
                ┌──────────────┐
                │  AI Agent    │
                └──────┬───────┘
                       │
              ┌────────┴────────┐
              │                 │
              ▼                 ▼
        Direct Answer       Use Tool
                                │
                                ▼
                         External API
                                │
                                ▼
                         Tool Response
                                │
                                ▼
                           AI Agent
                                │
                                ▼
                          Final Answer
```

---

## 🧪 Mini Projects

### 📚 AI Study Assistant

A Generative AI study assistant built while learning LangChain.

Features include:

* Ask questions
* Summarize text
* Generate quizzes
* LLM-powered responses
* Tool-based functionality

---

### 🌦️ AI Weather Assistant

An agent that uses a weather tool/API to retrieve weather information.

Example:

```text
User:
What's the weather in Kolkata?

       ↓

AI Agent

       ↓

Weather Tool

       ↓

Weather API

       ↓

Weather Data

       ↓

AI Agent

       ↓

The weather in Kolkata is ...
```

---

## 🔐 Environment Variables

API keys should **never be hardcoded** in the source code.

Create a `.env` file:

```env
GOOGLE_API_KEY=your_api_key_here
```

Load the environment variables using:

```python
from dotenv import load_dotenv

load_dotenv()
```

Make sure `.env` is included in `.gitignore`:

```gitignore
.env
.venv/
__pycache__/
```

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/arnab-003/Agentic-AI-using-Langchain.git
```

### 2. Navigate to the project

```bash
cd Agentic-AI-using-Langchain
```

### 3. Create a virtual environment

Using Python:

```bash
python -m venv .venv
```

Activate it on Windows:

```powershell
.venv\Scripts\activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

### 5. Configure environment variables

Create a `.env` file and add the required API keys.

```env
GOOGLE_API_KEY=your_api_key_here
```

### 6. Run the project

Run the relevant Python file or notebook from the repository.

---

## 📌 Goals of This Repository

The main goal is to move from understanding **LLM fundamentals** to building practical **Agentic AI applications**.

The learning progression is:

```text
Python
   ↓
Machine Learning
   ↓
Deep Learning
   ↓
NLP
   ↓
Transformers
   ↓
LLMs
   ↓
Generative AI
   ↓
LangChain
   ↓
Tools
   ↓
APIs
   ↓
Agents
   ↓
Agentic AI Applications
```

---

## 🛣️ Future Plans

Planned topics and projects include:

* [ ] Advanced LangChain
* [ ] LangGraph
* [ ] RAG applications
* [ ] Vector databases
* [ ] Embeddings
* [ ] Retrieval systems
* [ ] Multi-tool agents
* [ ] Agentic RAG
* [ ] Memory systems
* [ ] Structured output
* [ ] MCP
* [ ] Evaluation of LLM applications
* [ ] Production-ready AI applications
* [ ] Deployment
* [ ] MLOps for GenAI

---

## 📈 Progress

This repository is continuously updated as new concepts and projects are learned and implemented.

> **Learn → Build → Experiment → Improve**

---

## 👨‍💻 Author

**Arnab Deb**

B.Tech in Artificial Intelligence & Machine Learning

Interested in:

* 🤖 Artificial Intelligence
* 🧠 Machine Learning
* 🧬 Deep Learning
* 💬 NLP
* ✨ Generative AI
* 🦜 LangChain
* 🤝 Agentic AI
* ⚙️ MLOps

---

## ⭐ Support

If you find this repository useful, consider giving it a ⭐ on GitHub.

---

## 📄 License

This repository is intended primarily for learning and experimentation.
