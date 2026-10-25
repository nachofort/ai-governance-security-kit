# AI Governance & Security Kit for SMEs

A practical toolkit to **assess, govern and test** the use of generative and agentic AI in a small/medium-sized company — combining a governance layer (inventory, risk classification, policies) with a technical layer (a prompt-injection testing harness for LLM pipelines).

> **Status:** 🚧 Work in progress — built incrementally alongside my studies in *AI Cybersecurity & Governance* (Columbia Engineering).
> The case study uses a **fictional company**. No real corporate data is included.

---

## Why this project

AI adoption in SMEs usually happens bottom-up: employees use chatbots, copilots and AI features embedded in SaaS tools before any policy exists (*Shadow AI*). Meanwhile, the **EU AI Act**, **GDPR** and, depending on the sector, **NIS2 / DORA / ENS** raise the bar on what companies must document and control.

This kit answers three questions a management team would ask:

1. **What AI are we actually using?** → AI inventory / AI-BOM
2. **How risky is it, and what does the regulation require?** → risk & regulatory classification
3. **Would our AI-powered processes resist a real attack?** → prompt-injection test harness with measurable results

---

## Repository structure

```
.
├── governance/
│   ├── ai-bom/                # AI Bill of Materials template + filled example
│   ├── risk-classification/   # EU AI Act risk tiering + GDPR touchpoints
│   ├── policies/              # Shadow AI / acceptable-use policy
│   └── hitl-checklist/        # Human-in-the-loop controls per use case
├── redteam/
│   ├── attacks/               # Prompt-injection payloads (YAML)
│   ├── src/                   # Test harness (Python)
│   ├── results/               # Metrics & reports per run
│   └── README.md
├── case-study/                # Fictional SME: context, AI use cases, findings
├── docs/                      # Methodology, framework mapping, decisions log
├── .env.example
├── requirements.txt
└── README.md
```

---

## Frameworks & regulation referenced

| Area | References |
|---|---|
| AI management systems | ISO/IEC 42001 |
| Risk management | NIST AI RMF |
| Secure AI design | Google SAIF, AIUC-1 |
| Threat taxonomy | OWASP Top 10 for LLM Applications, MITRE ATLAS |
| EU / Spain regulation | EU AI Act (Reg. 2024/1689, as amended by Reg. 2026/1744), GDPR, NIS2, DORA, ENS |

---

## Roadmap

- [ ] Fictional SME case study and AI use-case inventory
- [ ] AI-BOM template + filled example
- [ ] EU AI Act risk classification of each use case
- [ ] Shadow AI / acceptable-use policy
- [ ] Prompt-injection harness: direct & indirect injection, baseline vs. guardrails
- [ ] Results dashboard (attack success rate per defense)
- [ ] Human-in-the-loop checklist for agentic workflows
- [ ] Executive summary: findings, residual risk and cost of controls

---

## Getting started

```bash
git clone https://github.com/<your-user>/ai-governance-security-kit.git
cd ai-governance-security-kit
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
cp .env.example .env   # add your own API keys — never commit .env
```

---

## Author

**Ignacio Fort Sanz** — Data Analyst | Business, finance & data engineering
[LinkedIn](#) · Madrid, Spain

## License

Code: MIT · Documentation: CC BY 4.0
