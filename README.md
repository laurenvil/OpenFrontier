# 🦙 OpenFrontier — Build Your Own AI Lab

> **Turn your laptop into a micro-version of what happens inside OpenAI and Anthropic.**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![llama.cpp](https://img.shields.io/badge/powered%20by-llama.cpp-orange)](https://github.com/ggerganov/llama.cpp)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-green.svg)](https://www.python.org/)

---

## What Is This?

Have you ever wondered how companies like **OpenAI** (ChatGPT) or **Anthropic** (Claude) actually serve their AI models to millions of people? They use massive data centers with thousands of GPUs, but the *core mechanics* of what they do can be replicated on your own computer.

In this curriculum, you will use [`llama.cpp`](https://github.com/ggerganov/llama.cpp) and its built-in `llama-server` to turn your machine into a **frontier AI lab**. You'll compile C++ from source, host an OpenAI-compatible API, prompt a model with your own data, and build a real AI agent — all running locally, offline, and for free.

> [!NOTE]
> **No cloud account or API key required.** Everything runs on your hardware.

---

## 🎯 Learning Objectives

By the end of this curriculum you will be able to:

| # | Skill | What You'll Do |
|---|-------|----------------|
| 1 | **Compile from source** | Clone a C++ repository and build a binary with `cmake` / `make` |
| 2 | **Understand model formats** | Load a GGUF model into memory and explain quantization |
| 3 | **Host an OpenAI-compatible API** | Run `llama-server` and call it with the same Python code used for ChatGPT |
| 4 | **Prompt engineering** | Craft system prompts, control temperature, and feed unstructured data to an LLM |
| 5 | **Build an AI agent** | Create a local Study Buddy that reads your notes, answers questions, and generates flashcards |
| 6 | **Ship a full-stack product** | Build a web app with Flask, ChromaDB, and HTMX — a real Demo Day project |

---

## 📚 Modules

| Module | Title | Description |
|--------|-------|-------------|
| **[Module 1](./modules/01-setup-and-hardware/)** | Setup & Hardware | Clone `llama.cpp`, compile the server, and download a GGUF model |
| **[Module 2](./modules/02-openai-api-wrapper/)** | The OpenAI API Wrapper | Start `llama-server` and connect to it with the Python `openai` library |
| **[Module 3](./modules/03-prompting-and-inference/)** | Prompting & Inference | Context windows, temperature, and asking questions about documents |
| **[Module 4](./modules/04-practical-application/)** | Practical Application | Build a local AI Study Buddy Agent with slash-command features |
| **[Module 5](./modules/05-demo-day/)** | 🎓 Demo Day | Full-stack capstone: web app + AI pipeline + entrepreneurship |

---

## 🗂️ Repository Structure

```
OpenFrontier/
├── README.md                          ← You are here
├── LICENSE
├── docs/
│   ├── llamaFrontier.md               ← Deep-dive: llama-server vs. frontier labs
│   └── hardware-recommendations.md    ← Suggested hardware for students
├── modules/
│   ├── 01-setup-and-hardware/
│   │   └── README.md
│   ├── 02-openai-api-wrapper/
│   │   ├── README.md
│   │   └── code/
│   │       ├── test_api.py
│   │       └── requirements.txt
│   ├── 03-prompting-and-inference/
│   │   ├── README.md
│   │   └── code/
│   │       ├── ask_notes.py
│   │       └── biology_notes.txt
│   ├── 04-practical-application/
│   │   ├── README.md
│   │   └── code/
│   │       ├── study_buddy_agent.py
│   │       ├── history_notes.txt
│   │       └── requirements.txt
│   └── 05-demo-day/                   ← 🎓 Capstone: full-stack web app
│       ├── README.md
│       └── code/
│           ├── app.py                 ← Flask web server
│           ├── ai_engine.py           ← llama-server AI client
│           ├── vector_store.py        ← ChromaDB semantic search
│           ├── database.py            ← SQLite storage
│           └── templates/             ← Jinja2 + HTMX + DaisyUI
└── assets/
    └── architecture-diagram.md        ← Mermaid diagram of the full pipeline
```

---

## 🚀 Quick Start

```bash
# 1. Clone this curriculum
git clone https://github.com/your-org/OpenFrontier.git
cd OpenFrontier

# 2. Start with Module 1
cd modules/01-setup-and-hardware
# Follow the README.md instructions
```

---

## Prerequisites

| Requirement | Details |
|-------------|---------|
| **Computer** | Windows 10/11, macOS (Intel or Apple Silicon), or Linux |
| **RAM** | 8 GB minimum (16 GB recommended for larger models) |
| **Disk** | ~5 GB free for llama.cpp + model files |
| **Software** | Git, Python 3.10+, a C++ compiler (see Module 1), VS Code |
| **Experience** | Basic comfort with a terminal; beginner Python is fine |

---

## 🧠 The Big Idea

`llama-server` is like a **high-performance engine in a single car**. Frontier labs like OpenAI are like a **massive logistics fleet** with thousands of those engines coordinated by a global dispatch system.

One teaches you how the *combustion* (inference) works. The other is about *traffic management* (scaling).

This curriculum focuses on the **combustion** — the part you can touch, run, and experiment with right now.

> Read the full comparison in [`docs/llamaFrontier.md`](./docs/llamaFrontier.md).

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 🤝 Contributing

Found a typo? Have an idea for a new module? Open an issue or submit a pull request!
