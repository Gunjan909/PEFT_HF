#  PEFT with LoRA using Hugging Face Transformers

This project demonstrates how to fine-tune a large pretrained model (e.g., `DistilBERT`) using **Parameter-Efficient Fine-Tuning (PEFT)** with the **LoRA** (Low-Rank Adaptation) method from the [🤗 Hugging Face PEFT library](https://github.com/huggingface/peft).

---

## What is PEFT?

**PEFT** allows you to fine-tune large language models without updating all their parameters. Instead, it updates a small number of additional parameters—saving memory and speeding up training.

---

## What is LoRA?

**LoRA** adds small **trainable low-rank matrices** to certain layers (usually attention layers like `query`, `key`,  and `value`). These matrices are trained while keeping the rest of the model frozen, making fine-tuning more efficient.

---

## Dataset

We use the **AG News** classification dataset, which includes news articles categorized into 4 topics:

- World
- Sports
- Business
- Sci/Tech

---

## How It Works

1. Load a pretrained model and tokenizer (e.g., `distilbert-base-uncased`).
2. Apply LoRA using the `peft` library to inject trainable layers.
3. Train the model using Hugging Face's `Trainer`.
4. Save and evaluate the fine-tuned PEFT model.

---

## Requirements

Make sure to install the following Python packages:

```bash
pip install transformers datasets peft accelerate scikit-learn
