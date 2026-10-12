# 🧠 OmniQuiz-AI 2.0
### *(Rework of the original 1.0)*

> **Drop a file. Get a quiz.**
> Upload any study document and let AI generate a complete exam paper — multiple choice, short answer, and long essay questions — instantly in your browser.

[![Live Demo](https://img.shields.io/badge/demo-online-brightgreen.svg)](https://s250038-hub.github.io/OmniQuiz-AI-2/)
[![Android APK](https://img.shields.io/badge/Android-APK%20Download-3DDC84?logo=android)](https://github.com/s250038-hub/OmniQuiz-AI-2/raw/main/download/android/app.apk)
[![iOS App](https://img.shields.io/badge/iOS-Simulator%20Build-000000?logo=apple)](https://github.com/s250038-hub/OmniQuiz-AI-2/raw/main/download/ios/app.app.zip)
![GitHub Pages](https://img.shields.io/badge/Hosted%20on-GitHub%20Pages-blue)
![AI Engine](https://img.shields.io/badge/AI-NVIDIA%20NIM-76b900)
![Security](https://img.shields.io/badge/Proxy-Cloudflare%20Workers-orange)
![CI/CD](https://img.shields.io/badge/CI%2FCD-GitHub%20Actions-2088FF)
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
| 📱 **Mobile apps** | Auto-built Android APK + iOS app on every push |
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

---
┌──────────────────────────────────────────────────────────┐
│ USER'S BROWSER / APP │
│ │
│ ┌──────────┐ ┌──────────────┐ ┌──────────────────┐ │
│ │ Upload │──▶│ Parse File │──▶│ Build Prompt │ │
│ │ PDF/DOCX/ │ │ (pdf.js / │ │ (no API key) │ │
│ │ PPTX/TXT │ │ mammoth.js) │ └────────┬─────────┘ │
│ └──────────┘ └──────────────┘ │ │
└──────────────────────────────────────────────┼───────────┘
│
▼
┌──────────────────────────────┐
│ CLOUDFLARE WORKER │
│ (Serverless Proxy) │
│ │
│ • Injects hidden API key │
│ • Forwards to NVIDIA NIM │
│ • Returns JSON + retry on │
│ placeholder detection │
└──────────────┬───────────────┘
│
▼
┌──────────────────────────────┐
│ NVIDIA NIM API │
│ Model: Nemotron Lightning │
│ → Generates quiz JSON │
└──────────────┬───────────────┘
│
▼
┌──────────────────────────────┐
│ RENDER & EXPORT │
│ │
│ • Interactive question paper│
│ • Auto-grading + stamp │
│ • PDF / Markdown export │
│ • Mobile APK/IPA builds │
└──────────────────────────────┘

---

## 🚀 Live Demo

👉 **[https://s250038-hub.github.io/OmniQuiz-AI-2/](https://s250038-hub.github.io/OmniQuiz-AI-2/)**

---

## 📱 Mobile Apps

Every push to `main` automatically rebuilds both mobile apps via GitHub Actions:

| Platform | Download Link | Notes |
|---|---|---|
| 🤖 **Android** | [`download/android/app.apk`](https://github.com/s250038-hub/OmniQuiz-AI-2/raw/main/download/android/app.apk) | Installable on any Android device |
| 🍎 **iOS** | [`download/ios/app.app.zip`](https://github.com/s250038-hub/OmniQuiz-AI-2/raw/main/download/ios/app.app.zip) | Simulator build (Apple Developer account required for real devices) |

> Both apps wrap the live web version via Capacitor, so they stay auto-updated.

---

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
| AI Engine | NVIDIA NIM — `nvidia/nemotron-3.5-lightning-30b-a3b` |
| Mobile Wrapper | [Capacitor](https://capacitorjs.com/) |
| CI/CD | GitHub Actions (auto-builds APK + iOS on push) |
| Hosting | GitHub Pages (free) |
