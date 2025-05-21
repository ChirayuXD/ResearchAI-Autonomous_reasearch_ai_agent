````markdown
# 🧠 Research Crew

A modular and extensible AI agent workflow for conducting deep research and generating professional reports using CrewAI.

---

## 📚 Project Overview

This project uses [CrewAI](https://docs.crewai.com/) to orchestrate autonomous agents that:
1. **Research** a given topic using a web search tool.
2. **Analyze** the findings and generate a well-structured markdown report.

---

## 🛠️ Features

- 🤖 Multi-agent setup (Researcher + Analyst)
- 🔎 Web search integration via Serper.dev
- 📂 Outputs markdown reports to `output/report.md`
- 🔁 Modular configuration via YAML files
- ✅ Works with open LLMs (LLaMA, Gemma, etc.)

---

## 🚀 Quick Start

### 1. Clone the Repo

```bash
git clone https://github.com/your-username/research-crew.git
cd research-crew
````

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Set Up API Keys

Make sure you have access to Groq-compatible models and Serper.dev.

```bash
export SERPER_API_KEY=your_serper_api_key
export GROQ_API_KEY=your_groq_api_key
```

> If you're using `.env`, add those keys there.

---

## 🧪 Run the Crew

```bash
python src/research_crew/main.py
```

This will:

* Ask the Researcher agent to conduct research
* Send results to the Analyst agent
* Save the final report to: `output/report.md`

---

## 🧩 Project Structure

```
research-crew/
├── src/
│   └── research_crew/
│       ├── crew.py            # Defines agents, tasks, and crew workflow
│       ├── main.py            # Entrypoint for running the crew
│       └── config/
│           ├── agents.yaml    # Agent roles, goals, backstories, LLMs
│           └── tasks.yaml     # Task prompts and assignments
├── output/
│   └── report.md              # Generated markdown report
├── requirements.txt
└── README.md
```

---

## ⚙️ Configuration

### `config/agents.yaml`

Define your agents' behavior, personality, and model.

### `config/tasks.yaml`

Define what tasks the crew should perform and how they relate to one another.

---

## 🧠 Example Use Case

Research topic: **Artificial Intelligence in Healthcare**

Generates a report with:

* Executive summary
* History, trends, and key developments
* Future outlook and recommendations

---

## 📌 Notes

* Avoid using moderation-only models like `llama-guard`; they return static responses like `"safe"`.
* Use lightweight generation models like `llama-3-8b-instruct`, `gemma-7b-it`, or `llama2-7b-chat`.

---
