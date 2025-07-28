# 🧠 PDF Summarizer with Mixtral + Pseudo-Labeling

This project extracts text from a PDF, splits it into manageable token-based chunks, summarizes each chunk using the **Mixtral-8x7B-Instruct** model via the **Together API**, and saves the resulting labeled data in JSONL format for downstream training or analysis.

---

## 📌 Features

- 🔍 Extracts text from PDF using PyMuPDF (`fitz`)
- ✂️ Chunks text into approx. 1024-token blocks using a tokenizer
- 🤖 Summarizes text using the Together API (Mixtral model)
- 💾 Outputs pseudo-labeled JSONL dataset for fine-tuning or training

---

## 📁 File Structure

