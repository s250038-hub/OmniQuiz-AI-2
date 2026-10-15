# 🧠 OmniQuiz-AI 2.0
### *(Rework of the original 1.0)*

> **Drop a file. Get a quiz.**
> Upload any study document and let AI generate a complete exam paper — multiple choice, short answer, and long essay questions — instantly in your browser.

[![Live Demo](https://img.shields.io/badge/demo-online-brightgreen.svg)](https://s250038-hub.github.io/OmniQuiz-AI-2/)
![GitHub Pages](https://img.shields.io/badge/Hosted%20on-GitHub%20Pages-blue)
![AI Engine](https://img.shields.io/badge/AI-NVIDIA%20NIM-76b900)
![Security](https://img.shields.io/badge/Proxy-Cloudflare%20Workers-orange)
![License](https://img.shields.io/badge/License-MIT-green)

---

## ✨ Features

| Feature | Description |
|---|---|
| 📄 **Multi-format parsing** | Upload PDF, DOCX, PPTX, TXT, or Markdown files |
| 🧩 **Three question types** | Multiple choice, short answer, AND long/essay questions |
| 🎚️ **Difficulty control** | Easy, Medium, or Hard question generation |
| 🌐 **Auto language** | Detects document language or lets you specify one |
| 🎯 **Topic focus** | Optionally emphasize a specific topic |
| ✅ **Auto-grading** | Click answers and get instant scoring with a stamp |
| 🔑 **Answer key** | Toggle to reveal all correct answers + explanations |
| 📋 **PDF export** | Download printable PDF with question paper + answer key |
| ⧉ **Markdown export** | Copy or download as `.md` |
| 🔄 **Smart top-up** | Auto-retries and fills in any missing questions |
| 🔒 **100% private** | Files parsed in-browser. API key hidden via proxy |

### 🎓 Sample Output
Here's what the AI generates from a single PDF upload:

> **Q:** How many beats are there in each bar for music written in duple metre?
> - A. 2 beats  **✓**
> - B. 3 beats
> - C. 4 beats
> - D. 1 beat
>
> *Answer: A — Duple metre means 2 beats in each bar.*

## 🚀 Live Demo

👉 **[https://s250038-hub.github.io/OmniQuiz-AI-2/](https://s250038-hub.github.io/OmniQuiz-AI-2/)**

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Vanilla HTML / CSS / JavaScript (single file) |
| PDF Parsing | [pdf.js](https://mozilla.github.io/pdf.js/) |
| DOCX Parsing | [Mammoth.js](https://github.com/mwilliamson/mammoth.js) |
| PPTX Parsing | [JSZip](https://stuk.github.io/jszip/) |
| PDF Export | [jsPDF](https://github.com/parallax/jsPDF) |
| UI Fonts | Fraunces, Space Grotesk, Space Mono (Google Fonts) |
| API Proxy | Cloudflare Workers (free tier) |
| AI Engine | NVIDIA NIM — `nvidia/nemotron-3-nano-omni-30b-a3b-reasoning` |
| Mobile Wrapper | [Capacitor](https://capacitorjs.com/) |
| Hosting | GitHub Pages (free) |
## hahaha
