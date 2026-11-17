# 🛡️🔐 AI Security

[![Notebooks CI](https://github.com/jrafa1607/AI_Security/actions/workflows/notebooks.yml/badge.svg)](https://github.com/jrafa1607/AI_Security/actions/workflows/notebooks.yml)

Hands-on Python notebooks on **AI and LLM security**. Each one shows how an AI system fails and which control mitigates the failure, using small, reproducible examples with synthetic data.

![AI Security](assets/ai_security.png)

---

#### 📓 Notebooks

| Notebook | What it covers | OWASP LLM Top 10 | MITRE ATLAS |
| --- | --- | --- | --- |
| [Prompt Injection](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/Prompt_Injection.ipynb) | Direct and indirect injection, detection rate, and containment | LLM01 | AML.T0051 |
| [Guardrails](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/Guardrails.ipynb) | Input, tool, and output controls around an LLM | LLM01, LLM02, LLM05, LLM06, LLM07 | AML.T0051, AML.T0054 |
| [RAG Access Control](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/RAG_Access_Control.ipynb) | Retrieval that respects permissions and sensitivity labels | LLM01, LLM02, LLM08 | AML.T0051 |
| [Privacy and Data Minimization](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/Privacy_And_Data_Minimization.ipynb) | Masking, pseudonymization, and k-anonymity | LLM02 | — |
| [Data Poisoning](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/Data_Poisoning.ipynb) | Corrupted labels, backdoors, and detection | LLM04 | AML.T0020 |
| [Adversarial Attacks](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/Adversarial_Attacks.ipynb) | Evasion with FGSM and adversarial training | — | AML.T0015 |
| [Model Extraction and Inversion](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/Model_Extraction_And_Inversion.ipynb) | Model theft, membership inference, and inversion | LLM02, LLM10 | AML.T0024 |
| [AI Hallucination](https://colab.research.google.com/github/jrafa1607/AI_Security/blob/main/AI_Hallucination.ipynb) | False premises, fictional entities, grounding, and self-consistency | LLM09 | — |

Each link opens the notebook in **Google Colab**; run it with `Runtime > Run all`. To run locally, use `pip install -r requirements.txt`.<br>
Seven notebooks need only NumPy and are executed on every push by the CI. *AI Hallucination* downloads a small model ([Qwen2.5-0.5B-Instruct](https://huggingface.co/Qwen/Qwen2.5-0.5B-Instruct)) and is run manually, since sampled answers vary by design.

---

#### 🔗📚 References

| Reference | Description |
| --- | --- |
| [OWASP Top 10 for LLM Applications 2025](https://genai.owasp.org/llm-top-10/) | The ten most critical security risks in LLM applications |
| [OWASP AI Testing Guide](https://owasp.org/www-project-ai-testing-guide/) | Methodology for security testing of AI systems |
| [MITRE ATLAS](https://atlas.mitre.org/) | Knowledge base of real-world adversary tactics and techniques against AI |
| [NIST AI RMF 1.0](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf) | Framework to govern, map, measure, and manage AI risks |
| [NIST AI 600-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf) | Generative AI profile of the AI RMF |
| [NIST AI 100-2 E2025](https://csrc.nist.gov/pubs/ai/100/2/e2025/final) | Taxonomy and terminology of adversarial machine learning |
| [CSA AI Controls Matrix](https://cloudsecurityalliance.org/blog/2025/07/10/introducing-the-csa-ai-controls-matrix-a-comprehensive-framework-for-trustworthy-ai) | Control framework for trustworthy AI in the cloud |
| [ENISA Multilayer Framework for Good Cybersecurity Practices for AI](https://www.enisa.europa.eu/publications/multilayer-framework-for-good-cybersecurity-practices-for-ai) | European good practices for AI cybersecurity |
| [ISO/IEC 42001:2023](https://www.iso.org/standard/42001) | Management system standard for AI |
| [ISO/IEC 27090:2026](https://www.iso.org/standard/27090) | Guidance on security threats and controls for AI systems |

---

#### ⚠️ Ethical Use

The attack simulations run only against toy models built inside each notebook and exist **for education and defense**. Do not use these techniques against systems you do not own or are not authorized to test.

---

#### 📝 How to Cite

GitHub shows a **Cite this repository** button generated from [`CITATION.cff`](CITATION.cff). APA format:

> Evangelista, J. R. G. (2026). *AI Security: Hands-on Notebooks on AI and LLM Security, Privacy, and Robustness* (Version 1.1.0) [Computer software]. https://github.com/jrafa1607/AI_Security

---

#### ⚖️ Intellectual Property (IP) Notice

All source code, documentation, and research methodologies contained in this repository are the exclusive Intellectual Property of the author. All rights reserved. Use of this content for academic or professional purposes must include proper citation and attribution to the original research (see [How to Cite](#-how-to-cite)).

**Copyright © 2026 [João Rafael](https://www.linkedin.com/in/jrafa1607/).**
