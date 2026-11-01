### 🛡️🔐 AI Security

[![OWASP Top 10 for LLMs 2025](https://img.shields.io/badge/OWASP-Top%2010%20for%20LLMs%202025-000000?logo=owasp)](https://genai.owasp.org/llm-top-10/)
[![MITRE ATLAS](https://img.shields.io/badge/MITRE-ATLAS-0B3D91)](https://atlas.mitre.org/)
[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Notebooks CI](https://github.com/jrafa1607/AI_Security/actions/workflows/notebooks.yml/badge.svg)](https://github.com/jrafa1607/AI_Security/actions/workflows/notebooks.yml)

Hands-on Python notebooks on **Artificial Intelligence Security, Privacy Preservation, and Model Robustness**. Each notebook shows, in a small and reproducible example, **how an AI or LLM system fails** and **which control mitigates the failure**, with results you can measure.

All examples use **synthetic data and fictional secrets** (for example, `DEMO-ONLY-123`, `example.invalid`).

---

#### 📓 Notebooks

| # | Notebook | What you will see | Controls demonstrated | Risk mapping | Open |
| ---: | --- | --- | --- | --- | :---: |
| 1 | [Prompt Injection](Prompt_Injection.ipynb) | 20 direct and indirect injection patterns against a naive assistant | Action allowlist, spotlighting of untrusted content, encoded-secret leakage check | LLM01, LLM07 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/Prompt_Injection.ipynb) |
| 2 | [Guardrails](Guardrails.ipynb) | A layered input → tool → output pipeline around a deliberately unsafe fake model | PII detection with CPF and Luhn validation, Unicode normalization, least-privilege tools, canary tokens, schema validation, audit log | LLM01, LLM02, LLM05, LLM06, LLM07 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/Guardrails.ipynb) |
| 3 | [RAG Access Control](RAG_Access_Control.ipynb) | A retriever that leaks HR and incident documents to an intern | Pre-filtering by ACL, sensitivity labels, PII redaction, injection flags, citations, audit log | LLM02, LLM08, LLM01 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/RAG_Access_Control.ipynb) |
| 4 | [Privacy and Data Minimization](Privacy_And_Data_Minimization.ipynb) | Personal data flowing into analytics and AI pipelines | Minimization, masking, HMAC pseudonymization, generalization, k-anonymity, small-count suppression | LLM02 · LGPD · GDPR | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/Privacy_And_Data_Minimization.ipynb) |
| 5 | [Data Poisoning](Data_Poisoning.ipynb) | Mislabeled records and a backdoor trigger changing predictions | Provenance, schema and duplicate checks, label-consistency check, trigger-token detection | LLM04 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/Data_Poisoning.ipynb) |
| 6 | [Adversarial Attacks](Adversarial_Attacks.ipynb) | FGSM evasion of a fraud-like classifier vs. random noise of the same size | Robustness curve, adversarial training | MITRE ATLAS · NIST AI 100-2 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/Adversarial_Attacks.ipynb) |
| 7 | [Model Extraction and Inversion](Model_Extraction_And_Inversion.ipynb) | Stealing a model through its API, membership inference, class reconstruction | Label-only outputs, query monitoring, L2 regularization as a privacy test | LLM02, LLM10 · MITRE ATLAS | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/Model_Extraction_And_Inversion.ipynb) |
| 8 | [AI Hallucination](AI_Hallucination.ipynb) | A small language model answering false premises and fictional entities | Grounding with abstention, self-consistency check | LLM09 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/AI_Hallucination.ipynb) |

---

#### 📊 Key results (reproducible, fixed seeds)

| Notebook | Measurement | Result |
| --- | --- | --- |
| Adversarial Attacks | Accuracy at perturbation ε = 0.6: random noise vs. FGSM | **0.64 vs. 0.25** — crafted attacks are far stronger than noise |
| Adversarial Attacks | Accuracy under FGSM at ε = 0.6: standard vs. adversarially trained model | **0.25 → 0.77** (clean accuracy 0.995 → 0.885) |
| Model Extraction | Surrogate fidelity after 10 queries: probability API vs. label-only API | **1.00 vs. 0.86** — never expose raw scores you do not need |
| Model Extraction | Membership-inference accuracy: overfitted vs. regularized model | **0.69 → 0.50** (back to guessing) |
| Model Inversion | Cosine similarity between reconstructed input and the hidden class profile | **0.998** |
| RAG Access Control | Intern asking for salary bands: naive RAG vs. pre-filtered RAG | Restricted HR document leaked → **only permitted documents returned** |

---

#### ▶️ How to use

1. Click **Open in Colab** in the table above, then run `Runtime > Run all`.
2. To run locally:

   ```bash
   python -m venv .venv && source .venv/bin/activate   # Windows: .venv\Scripts\activate
   pip install -r requirements.txt
   jupyter lab
   ```

3. Seven notebooks need only the Python standard library and NumPy. **AI Hallucination** downloads a small model (`distilgpt2`, ~350 MB) from Hugging Face on the first run.

---

#### 🔗📚 Frameworks and references

* **[NIST AI Risk Management Framework (AI RMF 1.0)](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf)** and **[NIST AI 100-2 — Adversarial Machine Learning](https://csrc.nist.gov/pubs/ai/100/2/e2025/final)**
* **[OWASP Top 10 for LLM Applications 2025](https://genai.owasp.org/llm-top-10/)** and **[OWASP AI Testing Guide](https://owasp.org/www-project-ai-testing-guide/)**
* **[MITRE ATLAS](https://atlas.mitre.org/)** and **[MITRE SAFE-AI](https://atlas.mitre.org/pdf-files/SAFEAI_Full_Report.pdf)**
* **[CSA AI Controls Matrix](https://cloudsecurityalliance.org/blog/2025/07/10/introducing-the-csa-ai-controls-matrix-a-comprehensive-framework-for-trustworthy-ai)**
* **[ENISA Framework for AI Cybersecurity Practices (FAICP)](https://www.faicp-framework.com/)**
* **[ISO/IEC 42001:2023](https://www.iso.org/standard/42001)** and **[ISO/IEC 27090:2026](https://www.iso.org/standard/27090)**

---

#### ⚠️ Ethical use

The attack simulations are simplified, run only against toy models built inside each notebook, and exist **for education and defense**. Do not use these techniques against systems you do not own or are not authorized to test.

---

#### 👤 Author

**João Rafael, Ph.D.** — Cloud, Data & AI Security Architect · DataSecOps
[LinkedIn](https://www.linkedin.com/in/jrafa1607/) · [GitHub](https://github.com/jrafa1607)

If this repository helps your work or research, please cite it (see [`CITATION.cff`](CITATION.cff) or the **Cite this repository** button on GitHub).

---

#### ⚖️ Intellectual Property (IP) Notice

All source code, documentation, and research methodologies contained in this repository are the exclusive Intellectual Property of the author. All rights reserved. Use of this content for academic or professional purposes must include proper citation and attribution to the original research.

**Copyright © 2026 João Rafael.**
