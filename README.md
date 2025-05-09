# 🧠 Explainable AI with SHAP for LLaMA-3 on e-SNLI

This project investigates **explainable NLP** by leveraging SHAP (SHapley Additive exPlanations) to guide the `llama-3-8b` model in generating better justifications for natural language inference tasks using the **e-SNLI** dataset. We assess both baseline and SHAP-informed explanation strategies and compare them using an LLM-based judge.

---

## 📁 Repository Structure

| File | Description |
|------|-------------|
| `STEP1-llama3_esnli_shap.ipynb` | Prepares the e-SNLI dataset and computes SHAP values using LLaMA-3. |
| `STEP2-llama3_8B_esnli_baseline_explainations.ipynb` | Generates baseline explanations from LLaMA-3-8B. |
| `STEP3-llama3_esnli_shap_explainations.ipynb` | Constructs SHAP-informed prompts and generates improved explanations. |
| `STEP4-claude_llm_judge.ipynb` | Uses Claude (or similar) LLM to evaluate explanation quality. |

---

## 🧪 Project Overview

- **Dataset**: [e-SNLI](https://nlp.cs.washington.edu/e-sNLI/) – SNLI with human-annotated justifications.
- **Model**: `llama-3-8b` accessed via Together AI.
- **Strategies Compared**:
  - 🧱 **Baseline** – Direct LLaMA-3 predictions with vanilla prompts.
  - 🔍 **SHAP-Informed** – Explanations guided by SHAP feature importance.
- **Evaluation**:
  - LLM-based judge (Claude/OpenAI) compares outputs to gold-standard human explanations on criteria like helpfulness, coherence, and relevance.

---

## 📊 Results Summary

- SHAP-informed prompts produced richer, more detailed explanations but sometimes at the cost of brevity and precision.
- LLM judge results across 180 samples:

| Model            | Win Rate (SHAP over Baseline) |
|------------------|-------------------------------|
| `llama-2-7b`     | **22.35%**                    |
| `llama-3-8b`     | **31.84%**                    |

---

## ⚙️ Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/ArnaVin/NLP-Final-Project.git
   cd NLP-Final-Project
# NLP-Final-Project
