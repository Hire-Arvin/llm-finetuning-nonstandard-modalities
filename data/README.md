# Data

Place dataset files here before running the notebook.

## Required datasets

- **Mini ImageNet** (Part 1 — CNN/ResNet): Loaded automatically from HuggingFace via `load_dataset("timm/mini-imagenet")`. No manual download needed.
- **TinyStories** (Part 1 — Transformer): Loaded automatically from HuggingFace. No manual download needed.
- **DNA sequences** (Part 2 — DNABERT): `chimpanzee_train.txt`, `dog_train.txt`, `human_train.txt` — download from the CS 189 course repository.
- **UrbanSound8K** (Part 2 — ConvNeXt): Download `fold1` audio clips from [Kaggle](https://www.kaggle.com/datasets/chrisfilo/urbansound8k) and place the `.wav` files in `data/fold1_train/`.

## Note on large files

CSV and zip files in this directory are excluded from git. If sharing this project, reference the download links above.
