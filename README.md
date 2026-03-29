# 🧬 BioGPT Fine-Tuning for Hallmarks of Cancer (HoC)

## 📖 Project Summary

This project presents the fine-tuning of a  SLM-GPT-based language model on biomedical literature, with a focused objective of understanding and generating insights related to the **Hallmarks of Cancer (HoC)**.

Leveraging domain-specific data from PubMed and a pretrained biomedical tokenizer, the model is adapted to capture complex scientific language patterns and cancer-related knowledge.

---

## 🎯 Objectives

* Adapt a pretrained SLM-GPT-style model to the biomedical domain
* Improve representation of cancer-related scientific concepts

---

## ⚙️ Model Specifications

| Component           | Details               |
| ------------------- | --------------------- |
| Model Type          | GPT-based Transformer |
| Total Parameters    | 27 Million            |
| Vocabulary Size     | 42,380                |
| Total Training Data | 100 Million tokens    |
| Training Iterations | 10,000                |

---

## 🔤 Tokenization Strategy

* Utilized **Byte Pair Encoding (BPE)** from BioGPT
* Reused:

  * Pretrained vocabulary
  * Merge rules optimized for biomedical text

### Why this matters:

* Preserves domain-specific terminology (e.g., gene names, proteins)
* Reduces out-of-vocabulary issues
* Improves semantic consistency during fine-tuning

---

## 📚 Dataset Description

* **Source**: PubMed biomedical abstracts
* **Domain**: Cancer biology (Hallmarks of Cancer)

---

## 🚀 Training Details

* Fine-tuned for **10,000 iterations**
* Training limited by GPU resource constraints

## 📉 Training Performance

Loss curve visualization:

```
C:\Users\hp\Pictures\download.png
```

👉 Replace with:

```md
![Training Loss](images/loss.png)
```

---

## ⚠️ Limitations

* Limited training iterations (10k) may restrict convergence
* Model size (27M) is relatively small compared to SOTA models
* Performance dependent on dataset coverage and quality

---

## 🔮 Future Work

* Scale model size (100M+ parameters)
* Increase training duration and dataset size
* Apply distributed training (DDP/FSDP)
* Integrate additional biomedical corpora
* Evaluate on benchmark biomedical NLP tasks

---

## 🏗️ Suggested Repository Structure

```
├── data/               # Processed PubMed + HoC dataset
├── tokenizer/          # BPE vocab & merges (BioGPT)
├── model/              # Architecture & checkpoints
├── training/           # Training scripts
├── outputs/            # Logs, checkpoints
├── images/             # Loss curves and visuals
└── README.md
```

--
