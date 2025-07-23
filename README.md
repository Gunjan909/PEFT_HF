PEFT with LoRA using Hugging Face Transformers

This project demonstrates how to fine-tune a large pretrained model (e.g., DistilBERT) using Parameter-Efficient Fine-Tuning (PEFT) with the LoRA (Low-Rank Adaptation) method from the 🤗 Hugging Face PEFT library.

What is PEFT?

PEFT allows you to fine-tune large language models without updating all their parameters. Instead, it updates a small number of additional parameters—saving memory and speeding up training.

What is LoRA?

LoRA adds small trainable low-rank matrices to certain layers (usually attention layers like query and value). These matrices are trained while keeping the rest of the model frozen, making fine-tuning more efficient.

Dataset

We use the AG News classification dataset, which includes news articles categorized into 4 topics:

    World

    Sports

    Business

    Sci/Tech

How It Works

    Load a pretrained model and tokenizer (e.g., distilbert-base-uncased).

    Apply LoRA using the peft library to inject trainable layers.

    Train the model using Hugging Face's Trainer.

    Save and evaluate the fine-tuned PEFT model.

Requirements

    transformers

    datasets

    peft

    accelerate

    scikit-learn (for evaluation)

Results

This approach achieves competitive accuracy while training far fewer parameters compared to full fine-tuning.
