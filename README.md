# 🧠 OmniQuiz-AI 2.0
### (1.0 deleted and this is it's rework version)
> **Drop a file. Get a quiz.**  
> Upload any study document and let AI generate a complete exam paper — multiple choice + short answer — instantly in your browser.
[![Least version](https://img.shields.io/badge/demo-online-brightgreen.svg)](https://s250038-hub.github.io/OmniQuiz-AI-2/)
![GitHub Pages](https://img.shields.io/badge/Hosted%20on-GitHub%20Pages-blue)
![AI Engine](https://img.shields.io/badge/AI-NVIDIA%20NIM-76b900)
![Security](https://img.shields.io/badge/Proxy-Cloudflare%20Workers-orange)
![License](https://img.shields.io/badge/License-MIT-green)

---

## ✨ Features

| Feature | Description |
|---|---|
| 📄 **Multi-format parsing** | Upload PDF, DOCX, PPTX, TXT, or Markdown files |
| 🧩 **MC + Short Answer** | Generates multiple-choice AND short-answer questions |
| 🎚️ **Difficulty control** | Easy, Medium, or Hard question generation |
| 🌐 **Auto language** | Detects document language or lets you specify one |
| 🎯 **Topic focus** | Optionally emphasize a specific topic |
| ✅ **Auto-grading** | Click answers and get instant scoring with a stamp |
| 🔑 **Answer key** | Toggle to reveal all correct answers + explanations |
| 📋 **Export** | Copy as Markdown, download `.md`, or print as PDF |
| 🔒 **100% private** | Files are parsed in-browser. No API key needed|

---

## 🏗️ Architecture
## 🚀 Live Demo

👉 **[https://s250038-hub.github.io/OmniQuiz-AI-2/](https://s250038-hub.github.io/OmniQuiz-AI-2/)**

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Vanilla HTML / CSS / JavaScript (single file) |
| PDF Parsing | [pdf.js](https://mozilla.github.io/pdf.js/) |
| DOCX Parsing | [Mammoth.js](https://github.com/mwilliamson/mammoth.js) |
| PPTX Parsing | [JSZip](https://stuk.github.io/jszip/) |
| UI Fonts | Fraunces, Space Grotesk, Space Mono (Google Fonts) |
| API Proxy | Cloudflare Workers (free tier) |
| AI Engine | NVIDIA NIM — `nvidia/nemotron-3.5-lightning-30b-a3b` |
| Hosting | GitHub Pages (free) |

---

## 📁 Project Structure
OmniQuiz-AI-2/
├── index.html ← Complete app (single file, no build step)
└── README.md ← This file
