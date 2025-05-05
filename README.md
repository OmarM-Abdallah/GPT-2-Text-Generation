# Optimizing and Fine-tuning GPT-2 for Text Generation
This repository contains my implementation of a benchmarking and evaluation task using an open-source language model, specifically **GPT-2**, observe the performance of the model on the given datasets and try to work on improving it.

## Task Objectives

The main goals to achieve in this repo are:

1. Load an open-source language model.
2. Benchmark the model on multiple datasets.
3. Measure and report the **throughput** and **performance metrics** for different types of tasks.

## Task Walkthrough

-  Selected **GPT-2** as the base language model due to its balance between capability and resource requirements.
-  Loaded the model and tokenizer using Hugging Face’s `transformers` library.
-  Benchmarked the model on two datasets:
    - **WikiText** (language modeling): Evaluated using **Perplexity**.
    - **GSM8K** (math reasoning QA): Evaluated using **Exact Match Accuracy**.
-  Computed **throughput metrics**:
    - **Tokens per second**
    - **Samples per second**
-  Compared the performance between:
    - The base GPT-2 model.
    - A quantized fp-16 for performance optimization.
 
##  Evaluation Metrics

- **Perplexity** (WikiText): A measure of the model’s ability to predict the next word in a sequence. Lower values indicate better performance.
- **Accuracy** (GSM8K): Exact match rate of generated answers compared to the ground truth.
- **Throughput**:
  - *Tokens per second*: Measures token-level processing speed.
  - *Samples per second*: Measures how many full input examples are processed per second.

## Technologies Used

- Python
- Hugging Face Transformers
- Datasets (WikiText, GSM8K)
- PyTorch
- BitsAndBytes (for 8-bit model quantization)
- CUDA (for GPU acceleration)

## Observations

- GPT-2 performs well on language modeling tasks, showing reasonable perplexity scores, but can perform better with training or fine-tuning.
- For reasoning tasks like GSM8K, the model struggles, indicating a limitation of base GPT-2 on complex math or logical inference.
- Quantized models significantly reduce memory usage and inference time with minimal performance loss.

More details on each step, including code and comments, can be found in the notebook itself.
