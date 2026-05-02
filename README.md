# DL-Lab: REALM VLM Fine-Tuning and Evaluation

This repository contains our Design Lab work on **real vs. AI-generated image detection** using **Vision-Language Models (VLMs)**.  
The project follows the REALM-style task format:

`Yes/No/Somewhat, <one sentence identifying the key visual clue>.`

The repo includes:
- an end-to-end lab report,
- notebooks for metric benchmarking and VLM evaluation,
- LoRA fine-tuning pipelines for InternVL and Qwen family models,
- comparison reports before and after fine-tuning.

---

## Project Goal

Given an image, generate a short explanation that decides whether it appears AI-generated and points to a concrete visual clue.

We evaluate model responses with a **G-Eval (LLM-as-judge)** rubric (Gemini-based) that checks:
- verdict agreement (`Yes/No/Somewhat`),
- artifact localization overlap with human reference,
- semantic match quality,
- penalty for hallucinated extra artifacts.

---

## Repository Structure

```text
DL-Lab/
├── DL_Lab.pdf
├── NLP_metric_comparsion.ipynb
├── vlm_inference.ipynb
├── Finetunning Scripts/
│   ├── intervl_finetunning.ipynb
│   └── qwen_finetunning.ipynb
└── Reports/
    ├── internvl_comparison.md
    └── qwen_comparison.md
```

### What each file does

- `DL_Lab.pdf`  
  Full report: problem statement, dataset context, metric selection, model selection, LoRA setup, and results.

- `NLP_metric_comparsion.ipynb`  
  Compares NLP similarity/evaluation metrics and supports selecting G-Eval for this task.

- `vlm_inference.ipynb`  
  Runs VLM inference on REALM-style data, computes per-image G-Eval scores, and aggregates mean/variance.

- `Finetunning Scripts/intervl_finetunning.ipynb`  
  LoRA fine-tuning workflow for `OpenGVLab/InternVL3-14B`.

- `Finetunning Scripts/qwen_finetunning.ipynb`  
  LoRA fine-tuning + evaluation workflow for Qwen3-VL-style setup.

- `Reports/internvl_comparison.md` and `Reports/qwen_comparison.md`  
  Image-wise model-vs-fine-tuned comparison reports with G-Eval reasoning.

---

## Environment and Dependencies

These notebooks were primarily run in Kaggle-like GPU environments (H100 in the report).  
Core libraries used across notebooks include:

- `torch`
- `transformers`
- `accelerate`
- `peft`
- `trl`
- `datasets`
- `pandas`, `numpy`, `Pillow`
- `google-genai` (for Gemini-based judging)
- optional metric tooling: `sentence-transformers`, `evaluate`, `bert_score`, `spacy`, `nltk`, `BLEURT`

> Note: individual notebooks install packages inline. Exact versions differ slightly by notebook.

---

## Setup

1. Create and activate a Python 3.10+ environment.
2. Install core packages:

```bash
pip install torch transformers accelerate peft trl datasets pandas numpy pillow
```

3. Install optional evaluation packages if you plan to run full metric benchmarking:

```bash
pip install sentence-transformers evaluate bert_score spacy nltk google-genai
```

4. Download spaCy model if needed:

```bash
python -m spacy download en_core_web_sm
```

5. Configure required tokens/secrets in your runtime environment:
- Hugging Face token (for gated model access),
- Gemini/Google API key (for G-Eval judging in relevant notebook cells).

---

## Typical Workflow

Recommended order:

1. Read `DL_Lab.pdf` for full methodology and rationale.
2. Run `NLP_metric_comparsion.ipynb` to understand metric choice.
3. Run `vlm_inference.ipynb` for zero-shot and/or adapter inference + G-Eval scoring.
4. Fine-tune with:
   - `Finetunning Scripts/intervl_finetunning.ipynb` (InternVL),
   - `Finetunning Scripts/qwen_finetunning.ipynb` (Qwen).
5. Compare outputs in `Reports/`.

---

## Reported Highlights

From the included report artifacts:
- InternVL3-14B improved from **3.102** to **3.906** average G-Eval after LoRA.
- Qwen3-VL-8B-Thinking improved from **3.483** to **3.734**.
- Fine-tuning generally reduced output variance and improved format consistency.

---

## Notes and Caveats

- Notebook paths and runtime assumptions are Kaggle-oriented in places (`/kaggle/working`, `kaggle_secrets`).
- You may need to adapt file paths and secret-loading logic for local runs.
- Some dependencies (for example flash-attn wheels) are hardware/CUDA-version specific.
- This repo is notebook-first; there is no packaged Python module/CLI yet.

---

## Acknowledgment

This work builds around the REALM framing for multimodal realness assessment and focuses on improving the VLM text description component through parameter-efficient fine-tuning.
