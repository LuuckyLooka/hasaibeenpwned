# HasAIbeenPwned

**[hasaibeenpwned.com](https://hasaibeenpwned.com)** - A community-maintained database tracking jailbreaks, prompt injections, and security vulnerabilities across AI language models.

---

## What is this?

HasAIbeenPwned aggregates real-world security incidents targeting AI models into one structured, searchable database. Each incident is sourced, classified by attack type, scored across multiple dimensions, and enriched with technical context.

The database covers:

- Jailbreaks and safety filter bypasses
- Prompt injection attacks
- System prompt extraction
- Training data leakage
- Adversarial inputs
- Tool and agent abuse
- Roleplay and persona-based bypasses
- Multi-turn manipulation

---

## Scoring system

Each incident is rated across four dimensions:

**Severity** - Critical / High / Medium / Low

**Ease of Use** - Trivial / Easy / Moderate / Complex / Expert

**Effectiveness** - Excellent / Great / Good / Normal / Low

**Mitigation Status** - Active / Partial / Mitigated / Unknown

Note: AI vulnerabilities are not "patched" like traditional software. Vendors typically release new model versions or add runtime classifiers - original model weights are rarely modified in-place. Open-source models (Llama, Mistral) cannot be fully mitigated once weights are publicly released.

---

## Models tracked

The database currently covers 40+ AI models including:

| Vendor | Models |
|---|---|
| OpenAI | GPT-4o, GPT-4, GPT-4 Turbo, GPT-3.5 Turbo, o1, o3 |
| Anthropic | Claude 3.5 Sonnet, Claude 3 Opus, Claude 3 Haiku, Claude 2 |
| Google DeepMind | Gemini 1.5 Pro, Gemini 1.5 Flash, Gemini 2.0, Bard |
| Meta | Llama 3.3, Llama 3.1, Llama 3, Llama 2 |
| Mistral AI | Mistral Large, Mistral Medium, Mistral Small |
| xAI | Grok-2, Grok-1 |
| Microsoft | Copilot, Phi-3 |
| And more... | Falcon, Cohere Command, DeepSeek, etc. |

---

## Attack techniques

Beyond individual incidents, the database includes an Attack Techniques catalog - reusable attack methods with example prompts, severity ratings, and defense recommendations. Browse at [hasaibeenpwned.com/attacks](https://hasaibeenpwned.com/attacks).

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

---

## Links

- Website: [hasaibeenpwned.com](https://hasaibeenpwned.com)
- Submit: [hasaibeenpwned.com/submit](https://hasaibeenpwned.com/submit)
- Rankings: [hasaibeenpwned.com/rankings](https://hasaibeenpwned.com/rankings)
- Attack types: [hasaibeenpwned.com/attack-types](https://hasaibeenpwned.com/attack-types)
