
# Node & Playwright Setup

This project uses **LangChain's Playwright Browser Toolkit**, which relies on **Playwright**.

## 1) Install Node.js
- Download and install Node.js (LTS) from the official website.

## 2) Install Playwright Python package and browsers
```bash
pip install playwright
playwright install
# If you want only chromium:
# playwright install chromium
```

## 3) Windows Notebook Heads‑Up
If you face `NotImplementedError` from Playwright inside a Jupyter notebook on Windows, see the workaround included in the notebook:
- Patch `kernelapp.py` around the Windows event loop policy (comment out the `WindowsSelectorEventLoopPolicy()` switch)
- Or prefer running from a **Python module** (Day 5 approach) instead of a notebook.
