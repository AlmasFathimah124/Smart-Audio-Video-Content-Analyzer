# 🔐 Smart Audio/Video Content Analyzer (Whisper Edition)

This desktop application transcribes audio or video content, classifies sensitive topics using large language models, detects toxicity, redacts unsafe content, and provides justifications — all through an intuitive GUI built with Tkinter.

## 🎯 Purpose

This tool helps protect private, sensitive, or inappropriate speech content in recordings — whether from interviews, meetings, or live conversations — by offering smart classification and explainability.

---

## 🧠 Key Features

- 🎙️ **Speech Recognition**: Transcribe audio/video to text using OpenAI’s Whisper
- 📌 **Sensitive Topic Classification**: Label sentences by user-defined topics using FLAN-T5
- ⚠️ **Toxicity Detection**: Identify toxic content using `unitary/toxic-bert`
- 🔍 **Semantic Explainability**: Justify every alert with concise reasoning
- 🕶️ **Redaction Engine**: Replace unsafe sentences with `[REDACTED]`
- 💾 **Save Output**: Export flagged results to JSON
- 🖥️ **GUI**: Easy-to-use interface built with Tkinter

---

## 💻 Installation

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/audio-content-analyzer.git
cd audio-content-analyzer
