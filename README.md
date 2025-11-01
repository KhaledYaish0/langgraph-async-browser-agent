
# LangGraph Async Browser Agent

An **asynchronous LangGraph** agent that can **browse the web** using LangChain's **Playwright Browser Toolkit**, send **Pushover** notifications, chat via **Gradio**, and keep **stateful memory** with `MemorySaver`.

This repo packages your *Week 4, Day 4* notebook into a clean project you can push to GitHub.

## Features
- ⚙️ **Async-first** graph: uses `ainvoke` and async tools
- 🌐 **Web browsing tools** via Playwright (navigate pages, extract text, etc.)
- 🔔 **Pushover** tool for push notifications
- 💬 **Gradio** chat UI
- 🧠 **Memory** using `langgraph.checkpoint.memory.MemorySaver`
- 🧵 Typed state with `TypedDict` + `add_messages` reducer

## Project Structure
```
langgraph-async-browser-agent/
├─ notebooks/
│  └─ langgraph_async_day4.ipynb
├─ setup/
│  └─ SETUP-node.md
├─ .env.example
├─ .gitignore
├─ LICENSE
├─ README.md
└─ requirements.txt
```

## Quickstart

### 1) Create and activate a virtual environment
```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate
```

### 2) Install dependencies
```bash
pip install -r requirements.txt
```

### 3) Playwright setup (required for browser tools)
See **setup/SETUP-node.md** then run:
```bash
pip install playwright
playwright install
```

### 4) Configure environment
Copy `.env.example` to `.env` and set values:
- `OPENAI_API_KEY` (required)
- (optional) `PUSHOVER_TOKEN`, `PUSHOVER_USER`

```bash
cp .env.example .env
# edit .env
```

### 5) Run the notebook
Open:
```
notebooks/langgraph_async_day4.ipynb
```
Run all cells. Gradio launches a local UI. The agent can **navigate** and **extract** page text via Playwright tools.

> **Windows Jupyter note**: if you hit an `NotImplementedError` from Playwright, check the workaround embedded in the notebook comments, or run the logic from a Python module instead.

## Environment Variables
```
OPENAI_API_KEY=sk-...
# Optional push notifications
PUSHOVER_TOKEN=...
PUSHOVER_USER=...
```

## GitHub Upload
```bash
git init
git add .
git commit -m "Init: LangGraph async browser agent"
git branch -M main
git remote add origin https://github.com/<YOUR_USERNAME>/langgraph-async-browser-agent.git
git push -u origin main
```

## License
MIT — see `LICENSE`.
