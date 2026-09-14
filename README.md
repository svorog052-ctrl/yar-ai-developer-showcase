# Yar AI Developer — Portfolio Showcase

Curated portfolio repository for **Yar AI Developer**, a Windows desktop project focused on AI-assisted software development.

The full working repository remains private. This showcase contains only public-safe documentation, selected examples and one representative screenshot.

![Yar AI Developer — Synapss Chat](screenshots/yar-ai-developer-synapss-chat.jpg.png)

## What the project explores

- desktop AI-assisted development workflows;
- multiple AI-provider integration;
- local LLM workflows with Ollama;
- REST API / JSON communication;
- project-context loading;
- bounded file operations;
- verification and fail-closed execution;
- Git-oriented development workflows;
- logging and diagnostics;
- browser/UI automation experiments;
- SHA-256 integrity checks.

## High-level architecture

```text
UI
↓
AI Manager
↓
AI Router
↓
AI Providers
↓
Execution Engine
↓
Plugin / Tool Layer
↓
Operating System
```

More detail: [Architecture overview](docs/ARCHITECTURE.md)

## Technology

TypeScript, JavaScript, HTML, CSS, Vite, Tauri, Rust, PowerShell, Git, REST API, JSON, Ollama and AI provider APIs.

## AI-assisted development approach

```text
Task
→ decomposition
→ architecture / constraints
→ AI-assisted implementation
→ run
→ inspect error
→ identify root cause
→ targeted correction
→ test
→ verify real postconditions
→ record the lesson
```

The goal is not to copy the first AI-generated answer. The goal is to get a working, verified result that can be explained and reproduced.

See: [AI-assisted development workflow](docs/AI_ASSISTED_DEVELOPMENT.md)

## Engineering lessons

The project includes public-safe examples of real AI-assisted debugging: browser submission verification, stale file hashes, runtime/build-path mistakes, PowerShell 5.1 compatibility and download automation.

See: [Selected engineering lessons](docs/ENGINEERING_LESSONS.md)

## Project status

Yar AI Developer is an active work in progress. The screenshot above is representative of the current UI, while individual modules and workflows continue to evolve.

## Author

**Yaroslav** — AI-assisted development / AI automation / rapid prototyping
