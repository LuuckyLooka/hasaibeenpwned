# HasAIbeenPwned

> Has your AI model been compromised?

**[hasaibeenpwned.com](https://hasaibeenpwned.com)** — A community-maintained database tracking jailbreaks, prompt injections, and security vulnerabilities across major AI models.

---

## What is this?

Inspired by [HaveIBeenPwned](https://haveibeenpwned.com), this project tracks known security incidents affecting AI language models — including:

- **Jailbreaks** — prompts that bypass safety guardrails
- **Prompt Injection** — indirect attacks via external content
- **System Prompt Extraction** — leaking confidential instructions
- **Training Data Leakage** — extracting memorized private data
- **Model Extraction** — reconstructing model behavior/weights
- **Adversarial Inputs** — inputs causing unexpected model behavior

Each incident is scored using a **Metasploit-style rating**:
- **Severity** — Critical / High / Medium / Low
- **Ease of Use** — Trivial / Easy / Moderate / Complex / Expert
- **Effectiveness** — Excellent / Great / Good / Normal / Low
- **Patch Status** — Active / Partial / Patched / Unknown

---

## Models Tracked

| Vendor | Models |
|--------|--------|
| OpenAI | GPT-4o, GPT-4, GPT-3.5 |
| Anthropic | Claude 3.5 Sonnet, Claude 3 Opus, Claude 3 Haiku |
| Google DeepMind | Gemini 1.5 Pro, Gemini 1.5 Flash |
| xAI | Grok-2, Grok-1 |
| Mistral AI | Mistral Large, Mistral Medium |
| Meta | Llama 3.3, Llama 3.1 |

---

## Submit an Incident

Found a vulnerability not listed here? Submit it at **[hasaibeenpwned.com/submit](https://hasaibeenpwned.com/submit)** or [open an issue](../../issues/new?template=incident_report.md) in this repository.

All submissions are manually reviewed before publication.

**Please follow responsible disclosure** — see [SECURITY.md](SECURITY.md).

---

## Report a Bug / Request a Feature

- [Bug report](../../issues/new?template=bug_report.md)
- [Feature request](../../issues/new?template=feature_request.md)
- [General discussion](../../discussions)

---

## Data Sources

Incidents are sourced from:
- Security research papers (arXiv, USENIX, IEEE)
- Community reports (Reddit, HackerNews, Twitter/X)
- Vendor security advisories
- [MITRE ATLAS](https://atlas.mitre.org)
- [AVID — AI Vulnerability Database](https://avidml.org)
- Community submissions

---

## Methodology

All incidents must meet the following criteria before publication:

1. **Reproducible** — the attack must be demonstrable
2. **Sourced** — must have a credible source or reporter
3. **Relevant** — must affect a tracked model's safety/security
4. **Responsible** — we do not publish prompts that could cause direct harm without context

---

## License

Data in this repository is available under [CC BY 4.0](LICENSE).

---

*HasAIbeenPwned is an independent security research project. We are not affiliated with any AI vendor.*
