# LLM Fine-Tuning & Deep Learning on Non-Standard Modalities

A single question — *how far can one architectural idea travel?* — carried from convolutional and transformer networks built from scratch in PyTorch, to fine-tuning pretrained models on data they were never designed for: raw DNA sequences, urban audio, and multiple-choice reasoning. The final arc fine-tunes a small language model (Qwen2.5-0.5B) three ways and, through a rigorous held-out evaluation, finds that **in-context learning beats supervised fine-tuning** on the target task.

**[View Report →](https://hire-arvin.github.io/llm-finetuning-nonstandard-modalities/)**

## What's Inside

- **From-scratch deep learning** — CNN, ResNet-18 with residual connections, and a full encoder–decoder Transformer (attention, multi-head, positional encoding) implemented and trained in PyTorch.
- **Genomics transfer learning** — Fine-tuning DNABERT on k-mer-tokenized sequences to classify DNA by species (human, chimpanzee, dog).
- **Audio as vision** — Converting waveforms to mel spectrograms and fine-tuning a pretrained ConvNeXt across 10 urban-sound classes, comparing frozen-backbone vs. full fine-tuning.
- **LLM fine-tuning & catastrophic-forgetting study** — Adapting Qwen2.5-0.5B with LoRA and partial-layer fine-tuning; likelihood-based multiple-choice evaluation; a held-out design that measures general-knowledge retention; and a 169-question hidden-test comparison against in-context learning.

## Key Finding

On a 169-question hidden test, placing **four worked examples in the prompt (0.42) outperformed every fine-tuned model — including supervised fine-tuning (0.34) — with no weight updates at all.** Accuracy peaked at 4 shots and *declined* by 8, and neither fine-tuning method caused catastrophic forgetting. A 25-question local gauge pointed the opposite way, underscoring that a properly sized, truly held-out evaluation is what separates a real result from a misleading one.

## Tech Stack

Python · PyTorch · HuggingFace Transformers · trl (SFTTrainer) · PEFT (LoRA) · torchaudio · torchvision · NumPy · Pandas · Matplotlib

## Files

| File | Description |
|------|-------------|
| `deep_learning_nonstandard_modalities_2026-09-11.qmd` | Quarto source — full write-up with embedded code |
| `index.html` | Self-contained rendered report (open in browser) |
| `images/` | Result figures embedded in the report |
| `data/README.md` | Dataset download instructions (data files not committed) |
