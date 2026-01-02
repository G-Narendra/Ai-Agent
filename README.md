
# 🤖 Ai-Agent: Browser Web UI
### Autonomous Web Automation Interface for AI Agents

<p align="center">
<img src="https://img.shields.io/badge/Python-3.11+-blue?style=for-the-badge&logo=python">
<img src="https://img.shields.io/badge/Framework-Gradio-orange?style=for-the-badge">
<img src="https://img.shields.io/badge/Library-Playwright-2EAD33?style=for-the-badge&logo=playwright">
<img src="https://img.shields.io/badge/LLM-Multi--Model%20Support-8E44AD?style=for-the-badge">
<img src="https://img.shields.io/badge/Docker-Supported-2496ED?style=for-the-badge&logo=docker">
</p>

---

## 🚀 Project Overview

**Ai-Agent Web UI** is a user-friendly graphical interface built on Gradio, designed to make web automation accessible for AI agents. Built upon the foundation of `browser-use`, this tool allows AI to interact with websites as a human would—searching, clicking, and extracting data autonomously.

<p align="center">
<img src="./assets/web-ui.png" alt="Browser Use Web UI" width="100%"/>
</p>

### Key Capabilities:
- **User-Friendly WebUI:** Easily interact with browser agents without writing code.
- **Expanded LLM Support:** Integrated with OpenAI, Google Gemini, Anthropic, DeepSeek, Azure, and Ollama.
- **Custom Browser Support:** Use your existing Chrome profile to bypass logins and 2FA.
- **Persistent Sessions:** Keep the browser open between tasks to maintain state and history.
- **Visual Monitoring:** High-definition screen recording and real-time VNC viewing.

---

## 🧠 Tech Stack

| Category | Tools |
| :--- | :--- |
| **Frontend UI** | Gradio |
| **Automation** | Playwright, Browser-Use |
| **Environment** | Python 3.11+, UV / Docker |
| **LLMs** | GPT-4, Claude 3.5, Gemini Pro, DeepSeek-R1 |
| **Visualization** | noVNC (Docker Mode) |

---

## ⚙️ Installation Guide

### Option 1: Local Installation (Recommended)

#### 1️⃣ Clone the Repository
```bash
git clone [https://github.com/G-Narendra/Ai-Agent.git](https://github.com/G-Narendra/Ai-Agent.git)
cd Ai-Agent

```

#### 2️⃣ Set Up Python Environment

Using `uv` for high-speed dependency management:

```bash
uv venv --python 3.11
# Activate (Windows)
.venv\Scripts\activate
# Activate (Mac/Linux)
source .venv/bin/activate

```

#### 3️⃣ Install Dependencies

```bash
uv pip install -r requirements.txt
playwright install --with-deps chromium

```

#### 4️⃣ Configure Environment

Copy `.env.example` to `.env` and add your API keys:

```bash
cp .env.example .env

```

---

### Option 2: Docker Installation

For a consistent environment with VNC support:

```bash
# Build and start
docker compose up --build

# Run with persistent session (browser stays open)
CHROME_PERSISTENT_SESSION=true docker compose up --build

```

* **Web Interface:** `http://localhost:7788`
* **VNC Viewer:** `http://localhost:6080/vnc.html` (Password: `youvncpassword`)

---

## ▶️ Usage

### Local Setup

Launch the WebUI with custom parameters:

```bash
python webui.py --ip 127.0.0.1 --port 7788 --theme Ocean --dark-mode

```

**Theme Options:** `Ocean` (Default), `Soft`, `Monochrome`, `Glass`, `Origin`, `Citrus`.

### Using Your Own Browser

To use your local Chrome profile (avoiding re-logins):

1. Set `CHROME_PATH` in `.env` (e.g., `C:\Program Files\Google\Chrome\Application\chrome.exe`).
2. Close all existing Chrome windows.
3. Enable "Use Own Browser" in the UI settings.

---

## 📈 Changelog & Milestones

* ✅ **2025/01/26:** Integration with **DeepSeek-R1** for complex "deep thinking" reasoning.
* ✅ **2025/01/10:** Added **Docker Setup** and persistent browser session support.
* ✅ **2025/01/06:** Released the new, well-designed **Gradio WebUI**.

---

## 👨‍💻 Author

**Narendra (G‑Narendra)** AI | ML | Python | Full Stack | GenAI Enthusiast

GitHub: [https://github.com/G-Narendra](https://github.com/G-Narendra)

Portfolio: [View Live Portfolio](https://g-narendra-portfolio.lovable.app/)

---

<p align="center">⭐ If you find this agent useful, please give the repository a star! 🚀</p>

