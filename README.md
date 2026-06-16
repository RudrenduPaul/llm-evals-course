# Statistical Testing for LLM Evaluations

### Design Experiments to Measure Gen AI Features at Scale

Companion notebooks for the O'Reilly live course **Statistical Testing for LLM Evaluations**, taught by **Rudrendu Paul** and **Lorenzo Toni**.

Your LLM eval says the new version is better. Should you trust it? Most LLM evaluations are underpowered, run the wrong statistical test, or measure a metric that does not survive production. These four notebooks give you the statistical toolkit to catch those failures before you ship. Every notebook runs on synthetic data, so there are no API keys, no accounts, and no setup beyond `pip install`.

---

## Notebooks

| # | Notebook | What it shows | Open in Colab |
|---|----------|---------------|---------------|
| 01 | [Power analysis for LLM evals](notebooks/01-power-analysis-llm-evals.ipynb) | Why 50 examples is statistical vapor. Detecting a 5-point faithfulness gain on a noisy 0-100 judge score needs 847 examples per arm, not 50. Sizing for binary, ordinal, and judge-based metrics. | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RudrenduPaul/llm-evals-course/blob/main/notebooks/01-power-analysis-llm-evals.ipynb) |
| 02 | [Hypothesis testing for LLM metrics](notebooks/02-hypothesis-testing-llm-metrics.ipynb) | The same paired data where a t-test says "no difference" (p=0.10) but Wilcoxon catches the real improvement (p=0.0078). Mann-Whitney, bootstrap CIs, and the multiple-comparisons trap. | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RudrenduPaul/llm-evals-course/blob/main/notebooks/02-hypothesis-testing-llm-metrics.ipynb) |
| 03 | [RAG evaluation case study](notebooks/03-rag-evaluation-case-study.ipynb) | A 14-point retrieval-recall collapse (0.82 to 0.68) hiding behind a steady end-to-end score, and the component-level design that surfaces it. | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RudrenduPaul/llm-evals-course/blob/main/notebooks/03-rag-evaluation-case-study.ipynb) |
| 04 | [Agent evaluation mini-case](notebooks/04-agent-evaluation-mini-case.ipynb) *(bonus)* | Agent A wins the benchmark (0.845) but collapses under production constraints (0.705) while Agent B holds steady (0.795) and overtakes it. Multi-level and production-constraint evaluation. | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RudrenduPaul/llm-evals-course/blob/main/notebooks/04-agent-evaluation-mini-case.ipynb) |

> **Notebook 04 is a bonus.** The live course covers power analysis, hypothesis testing, and the RAG case in 60 minutes. The agent mini-case is an optional deep-dive to explore on your own.

> **Open in Colab:** click any badge to launch the notebook in Google Colab (no local setup). You can also download the `.ipynb` and upload it to Colab, or run it locally.

All notebooks ship with their outputs saved, so you can read the charts and tables without running a single cell.

---

## Run locally

```bash
git clone https://github.com/RudrenduPaul/llm-evals-course.git
cd llm-evals-course
python -m venv .venv && source .venv/bin/activate   # optional
pip install -r requirements.txt
jupyter lab
```

Python 3.10+ is recommended. No API keys are required. All data is synthetic and generated inside each notebook.

---

## The 5-question LLM eval checklist

Before you act on any eval result, run it through five questions. The one-page version is in [`5-question-llm-eval-checklist.md`](5-question-llm-eval-checklist.md).

1. Was the comparison randomized, or are you reading a confound?
2. Does the metric measure what actually matters in production?
3. Was the sample large enough to detect the effect you care about?
4. Is the LLM-as-judge biased by position, length, or model family?
5. Will the offline result survive production latency, traffic, and drift?

---

## Companion book

These notebooks preview a slice of *Statistical Evaluation Methods for AI Systems* by Rudrendu Paul and Lorenzo Toni (O'Reilly, forthcoming): power analysis, hypothesis testing, RAG and agent evaluation, plus Bayesian decisions, CUPED variance reduction, causal methods for constrained rollouts, LLM-as-judge debiasing, and CI/CD regression testing.

---

## Further reading (all O'Reilly)

- *Practical Statistics for Data Scientists*, Peter Bruce, Andrew Bruce, and Peter Gedeck (O'Reilly)
- *Evals for AI Engineers*, Shreya Shankar and Hamel Husain (O'Reilly, 2026)
- *AI Engineering: Building Applications with Foundation Models*, Chip Huyen (O'Reilly, 2025)

---

## Connect

- LinkedIn: [linkedin.com/in/rudrendupaul](https://www.linkedin.com/in/rudrendupaul)
- ORCID: [0009-0008-0141-4690](https://orcid.org/0009-0008-0141-4690)
- Medium: [medium.com/@rudrendupaul](https://medium.com/@rudrendupaul)

Licensed under the MIT License. See [LICENSE](LICENSE).
