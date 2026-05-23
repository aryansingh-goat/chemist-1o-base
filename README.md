# 🧪 Chemist 1o Base

![License](https://img.shields.io/badge/license-MIT-blue)
![Model format](https://img.shields.io/badge/format-GGUF%20Q4__K__M-orange)
![Model size](https://img.shields.io/badge/size-260%20MB-lightgrey)
![Base model](https://img.shields.io/badge/base-Gemma%203%20270M-green)

**A tiny, offline chemistry assistant – my first AI project.**

## 📘 About

**Chemist 1o Base** is a 4‑bit quantized large language model fine‑tuned to answer chemistry questions. It understands the periodic table, elements, chemical compounds, bonding, and fundamental concepts – all from a single `.gguf` file that runs entirely on your machine with no internet connection.

Built with [Unsloth](https://github.com/unslothai/unsloth) and [QLoRA](https://arxiv.org/abs/2305.14314) on a free Google Colab GPU, this model is a labour of love and a first step into the world of AI.

## ✨ Features

- **🧠 Chemistry knowledge** – 1,448 hand‑crafted Q&A pairs covering elements, compounds, reactions, and definitions.
- **🖥️ Runs offline** – just download the GGUF file and load it with LM Studio, Ollama, or llama.cpp.
- **💾 Tiny footprint** – only ~260 MB, works on CPUs with 4 GB RAM.
- **📚 Educational** – clear, beginner‑friendly answers; perfect for students and curious minds.
- **🔓 Open source** – MIT licensed. Use it, modify it, share it.


---

### Example Questions

## ❓ Example Questions

- *What is the 42nd element in the periodic table?*
- *Explain ionic bonding with an example.*
- *What is the formula of sulfuric acid?*
- *Balance: H₂ + O₂ → H₂O*
- *Who created you?*

The model will answer with the knowledge it learned during fine‑tuning.

## 🔧 Training Details

- **Base model**: [`unsloth/gemma-3-270m-it`](https://huggingface.co/unsloth/gemma-3-270m-it)
- **Fine‑tuning method**: QLoRA (4‑bit quantization) with Unsloth
- **Training data**: `train.jsonl` – 1,448 instruction‑output pairs covering:
  - All 118 elements (symbol, atomic number, mass, electron configuration, shells, etc.)
  - Common chemical compounds
  - Basic concepts (bonding, pH, reactions, etc.)
  - Positional questions (1st element to 118th element)
- **Training steps**: ~200 steps (about 1.1 epochs)
- **Final loss**: 1.34
- **Quantization**: `Q4_K_M` GGUF via llama.cpp

The full dataset (`train.jsonl`) is included in this repository. You can use it to reproduce or improve the model.

## 🙏 Credits

Created by me **Aryan Singh** – a passionate learner building AI from scratch.  
This is my very first AI project, and I'm excited to share it with the world.

## ⭐ Support

I know **Chemist 1o Base** is horrible in quality, but please **star this repository** ⭐ – it means a lot and helps others discover the project! and motivating me for future improvements!

## 📜 License

This project is released under the [MIT License](LICENSE). You are free to use, modify, and distribute it as long as you include the original copyright notice.
