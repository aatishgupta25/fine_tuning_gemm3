## Image-to-LaTeX with Fine-Tuned Gemma 3 - 4B (QLoRA)

This project fine-tunes [`unsloth/gemma-3-4b-it`](https://huggingface.co/unsloth/gemma-3-4b-it) on the [`linxy/LaTeX_OCR`](https://huggingface.co/datasets/linxy/LaTeX_OCR) dataset to improve image-to-LaTeX generation using parameter-efficient QLoRA training.

---

### 1. Features

* Fine-tuning on \~76K OCR-aligned LaTeX samples
* 4-bit quantization with `bitsandbytes` for low-resource training
* Runs on free Google Colab (Tesla T4 GPU)
* BLEU score improvement from \~68.2 → \~89.3

---

### 2. Dependencies

* `transformers`
* `unsloth`
* `bitsandbytes`
* `datasets`
* `peft`
* `accelerate`

---

### 3. How to Run

```bash
# Clone repo and install deps
git clone https://github.com/<your_github_username>/image-to-latex-gemma.git
cd image-to-latex-gemma
pip install -r requirements.txt
```
---

### 4. Results

* **Model**: `unsloth/gemma-3-4b-it`
* **Dataset**: `linxy/LaTeX_OCR`
* **Metric**: BLEU
* **Pre-fine-tune**: 68.2
* **Post-fine-tune**: 89.3

