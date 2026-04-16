# HasAIbeenPwned

**[hasaibeenpwned.com](https://hasaibeenpwned.com)** - A community-maintained database tracking jailbreaks, prompt injections, and security vulnerabilities across AI language models.

---

## What is this?

HasAIbeenPwned aggregates real-world security incidents targeting AI models into one structured, searchable database. Each incident is sourced, classified by attack type, scored across multiple dimensions, and enriched with technical context.

The database covers:

- Jailbreaks and safety filter bypasses
- Prompt injection attacks (direct and indirect)
- System prompt extraction
- Training data leakage
- Adversarial inputs (multimodal)
- Tool and agent abuse
- Roleplay and persona-based bypasses
- Multi-turn manipulation
- Context window overflow

---

## Data sources

Incidents are automatically aggregated daily from 9 sources:

| Source | Type |
|---|---|
| [MITRE ATLAS](https://atlas.mitre.org) | Curated incident database |
| [AI Incident Database](https://incidentdatabase.ai) | Curated incident database |
| [arXiv](https://arxiv.org) (cs.CR, cs.AI) | Academic research papers |
| [CVE / NVD](https://nvd.nist.gov) | Official vulnerability database |
| [GitHub Security Advisories](https://github.com/advisories) | Security advisories |
| [HuggingFace Papers](https://huggingface.co/papers) | Research papers |
| [Semantic Scholar](https://semanticscholar.org) | Academic papers |
| [GitHub](https://github.com) | Community repos and PoCs |
| [Hacker News](https://news.ycombinator.com) | Community reports |

All community-sourced incidents go through AI pre-screening followed by manual review before appearing publicly.

---

## Scoring system

Each incident is rated across three dimensions, inspired by Metasploit module scoring:

**Severity** - `Critical` · `High` · `Medium` · `Low`

**Ease of Use** - `Trivial` · `Easy` · `Moderate` · `Complex` · `Expert`

**Effectiveness** - `Excellent` · `Great` · `Good` · `Normal` · `Low`

> Note: AI vulnerabilities are not "patched" like traditional software. Vendors typically release new model versions or add runtime classifiers - original model weights are rarely modified in-place. Open-source models (Llama, Mistral, DeepSeek) cannot be fully mitigated once weights are publicly released.

---

## Models tracked

The database currently covers 44+ AI models including:

| Vendor | Models |
|---|---|
| OpenAI | GPT-5, GPT-4o, GPT-4, GPT-4 Turbo, GPT-3.5 Turbo, o1, o3, o4-mini |
| Anthropic | Claude Sonnet 4.6, Claude Opus 4.6, Claude 3.5 Sonnet, Claude 3 Opus, Claude 2 |
| Google DeepMind | Gemini 2.5 Pro, Gemini 2.5 Flash, Gemini 2.0 Flash, Gemini 1.5 Pro, Bard |
| Meta | Llama 4 Scout, Llama 4 Maverick, Llama 3.3, Llama 3.1, Llama 3, Llama 2 |
| Mistral AI | Mistral Large 3, Mistral Large, Mistral 7B, Mixtral 8x7B |
| xAI | Grok 4.1, Grok 3, Grok 2, Grok 1 |
| Microsoft | Copilot, Phi-4, Phi-3 |
| DeepSeek | DeepSeek R1, DeepSeek V3 |
| And more... | |

---

## Attack taxonomy

10 attack types, mapped to OWASP LLM Top 10 and MITRE ATLAS:

| Type | OWASP | ATLAS |
|---|---|---|
| Jailbreak | LLM01 | AML.T0051 |
| Prompt Injection (Indirect) | LLM01 | AML.T0051.000 |
| System Prompt Extraction | LLM07 | AML.T0056 |
| Model Extraction | LLM10 | AML.T0005 |
| Training Data Leakage | LLM06 | AML.T0024 |
| Adversarial Input | LLM09 | AML.T0031 |
| Roleplay Bypass | LLM01 | AML.T0051 |
| Multi-turn Manipulation | LLM01 | AML.T0051 |
| Tool / Function Call Abuse | LLM08 | AML.T0054 |
| Context Window Overflow | LLM04 | AML.T0051 |

Browse the full Attack Techniques catalog at [hasaibeenpwned.com/attacks](https://hasaibeenpwned.com/attacks).

---

## Incidents vs Techniques

**Incident** - a documented event. Something that happened, with a date, a source, and a specific affected model.

**Technique** - a reusable attack method. How a class of attack works, with example prompts and defense recommendations. One technique can be linked to many incidents.

---

## Submit an incident

Found a vulnerability not in the database? Submit it at **[hasaibeenpwned.com/submit](https://hasaibeenpwned.com/submit)** or open an issue in this repository.

All submissions are manually reviewed before publication.

For critical vulnerabilities with no known mitigations - please notify the vendor first. We support coordinated disclosure and can delay publication on request. See [SECURITY.md](SECURITY.md).

---

## FAQ

**What does "pwned" mean for a model?**
At least one confirmed, publicly documented security incident exists for that model. It does not mean the model is currently exploitable - check the mitigation status on each incident.

**Is this a list of things to do to AI models?**
No. This is a defensive resource. Understanding how attacks work is necessary for building safer AI systems and making informed deployment decisions.

**How is this different from AI safety research?**
AI safety research focuses on long-term alignment risks. This database covers immediate, practical security issues - attacks that can be executed today against production AI deployments.

**What is the difference between an Incident and a Technique?**
An Incident is a documented event with a date, source, and affected model. A Technique is a reusable attack method that may be linked to many incidents.

**How do you verify incidents?**
Incidents from trusted sources (AIID, MITRE ATLAS, arXiv, CVE) are indexed automatically. Community reports go through AI pre-screening followed by manual admin review. Verification status is always shown on every incident.

---

## Links

- Website: [hasaibeenpwned.com](https://hasaibeenpwned.com)
- Submit: [hasaibeenpwned.com/submit](https://hasaibeenpwned.com/submit)
- Rankings: [hasaibeenpwned.com/rankings](https://hasaibeenpwned.com/rankings)
- Attack techniques: [hasaibeenpwned.com/attacks](https://hasaibeenpwned.com/attacks)

---

## Disclaimer

All information published on this site is intended for **educational and research purposes only**. Documented techniques and vulnerabilities are provided to help security researchers, developers, and organizations better understand AI security risks. Any use of this information must comply with applicable laws and the terms of service of the respective AI providers. The authors assume no responsibility for misuse.
