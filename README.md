### 🛡️🔐 AI Security

This repository is a centralized collection of Python notebooks dedicated to **Artificial Intelligence Security, Privacy Preservation, and Model Robustness**. The objective is to show, in small and reproducible examples, how AI and Large Language Model (LLM) systems fail and how to mitigate those failures with practical controls. Every notebook runs on **Google Colab** with one click.

| Notebook | What you will learn | Related risks | Open |
| --- | --- | --- | --- |
| **[Adversarial Attacks](Adversarial_Attacks.ipynb)** | FGSM evasion on a fraud-like classifier, robustness curves, and adversarial training | MITRE ATLAS · NIST AI 100-2 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/Adversarial_Attacks.ipynb) |
| **[AI Hallucination](AI_Hallucination.ipynb)** | Factual inconsistencies in small language models | OWASP LLM09 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/AI_Hallucination.ipynb) |
| **[Prompt Injection](Prompt_Injection.ipynb)** | Direct and indirect prompt injection, and why allowlists enforce what prompts cannot | OWASP LLM01 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/Prompt_Injection.ipynb) |
| **[Guardrails](Guardrails.ipynb)** | Input normalization, PII redaction (CPF, cards, e-mail), tool allowlists by role, output schema validation, and canary tokens | OWASP LLM01, LLM02, LLM05, LLM06, LLM07 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/Guardrails.ipynb) |
| **[RAG Access Control](RAG_Access_Control.ipynb)** | Permission-aware retrieval, pre-filtering vs. post-filtering, sensitivity labels, and audit logs | OWASP LLM02, LLM08 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/RAG_Access_Control.ipynb) |
| **[Privacy & Data Minimization](Privacy_And_Data_Minimization.ipynb)** | Minimization, masking, and pseudonymization of personal data | OWASP LLM02 · LGPD | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/Privacy_And_Data_Minimization.ipynb) |
| **[Data Poisoning](Data_Poisoning.ipynb)** | Label corruption, backdoors, and data quality checks before training | OWASP LLM04 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/Data_Poisoning.ipynb) |
| **[Model Extraction & Inversion](Model_Extraction_And_Inversion.ipynb)** | Stealing a model through its API, membership inference, model inversion, and their defenses | OWASP LLM02, LLM10 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/Model_Extraction_And_Inversion.ipynb) |

#### ▶️ How to use

1. Click **Open in Colab** on the notebook you want.
2. Run the cells from top to bottom (`Runtime > Run all`).
3. Most notebooks use only the Python standard library and NumPy. *AI Hallucination* downloads a small model from Hugging Face.

All examples use **synthetic data and fictional secrets** (for example, `DEMO-ONLY-123`, `example.invalid`).

---

#### 🔗📚 Important Resources for AI Security and Compliance

* **[AI Risk Management Framework (AI-RMF 1.0)](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf)**
* **[CSA AI Controls Matrix](https://cloudsecurityalliance.org/blog/2025/07/10/introducing-the-csa-ai-controls-matrix-a-comprehensive-framework-for-trustworthy-ai)**
* **[ENISA The Framework for AI Cybersecurity Practices (FAICP)](https://www.faicp-framework.com/)**
* **[ISO/IEC 42001:2023](https://www.iso.org/standard/42001)**
* **[ISO/IEC 27090](https://www.iso.org/standard/27090)**
* **[MITRE ATLAS SAFE-AI](https://atlas.mitre.org/pdf-files/SAFEAI_Full_Report.pdf)**
* **[OWASP AI Testing Guide](https://owasp.org/www-project-ai-testing-guide/)**
* **[OWASP Top 10 for LLMs](https://owasp.org/www-project-top-10-for-large-language-model-applications/)**

---

#### ⚠️ Ethical Use

The attack simulations in this repository are simplified, run only against toy models built inside each notebook, and exist **for education and defense**. Do not use these techniques against systems you do not own or are not authorized to test.

---

#### ⚖️ Intellectual Property (IP) Notice

All source code, documentation, and research methodologies contained in this repository are the exclusive Intellectual Property of the author. All rights reserved. Use of this content for academic or professional purposes must include proper citation and attribution to the original research.

**Copyright © 2026 João Rafael.**
