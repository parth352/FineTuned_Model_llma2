# 🦙 TinyLLaMA Fine-Tuning with LoRA (PEFT) on Pseudo-Labeled Data

This repository contains code for fine-tuning the [TinyLLaMA](https://huggingface.co/cognitivecomputations/TinyLlama-1.1B-Chat-v1.0) model using **pseudo-labeled data** and **LoRA-based parameter-efficient fine-tuning (PEFT)**.

The pseudo-labeled dataset is assumed to have been generated using an external LLM (like Mixtral) and saved in JSONL format with the keys: `instruction`, `input`, and `output`.

---

## 📁 Project Structure

