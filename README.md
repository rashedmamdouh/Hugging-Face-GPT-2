# 🤖 GPT-2 Code Generation using Hugging Face Transformers

This project demonstrates how to fine-tune a GPT-2 model for code generation using Hugging Face Transformers. The model is trained on a dataset of Python code snippets to complete code prompts effectively.

---

## 📌 Overview

- **Dataset**: [`codeparrot-ds-train`](https://huggingface.co/datasets/huggingface-course/codeparrot-ds-train)
- **Model**: GPT-2 initialized from `AutoConfig` with custom vocabulary size
- **Goal**: Autocomplete and generate Python code using prompt-based inference
- **Platform**: Google Colab + Google Drive for model storage

---

## 🛠️ Features

- Loads and samples 50k training and 500 validation examples
- Tokenizes Python code using `code-search-net-tokenizer`
- Filters tokenized sequences based on context length (128 tokens)
- Initializes GPT-2 with config adjusted to tokenizer
- Uses `DataCollatorForLanguageModeling` for training
- Trains with Hugging Face `Trainer` and evaluates with perplexity
- Includes GPU-accelerated text generation pipeline with examples

---

## 🧪 Results

- Achieved low perplexity on evaluation set (~best metric to track quality)
- Generates complete Python code snippets from partial inputs
- Outputs show coherent code continuation (e.g., DataFrame operations, plotting)

---

## 💡 Example Prompts

- Creating a scatter plot using NumPy
- Building a DataFrame and calculating mean per group
- Using `RandomForestRegressor` from `scikit-learn`

---

## 📁 File Structure

- `gpt2_code_generation.ipynb` — Main notebook with preprocessing, training, and inference
- `README.md` — Documentation

---

## 📦 Installation

```bash
pip install datasets evaluate transformers[sentencepiece]
apt install git-lfs
