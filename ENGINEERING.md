# How I Work

Defense in Depth: strong preventive architecture, backed by response that actually runs.

## Selected work

### Detection, response and Zero Trust
- Evaluate detection tooling with a scoring framework weighted on coverage, response automation and integration needs.
- Route alerts into a single incident queue with severity-based routing, SLAs and escalation paths.
- Pair FIDO2 hardware security keys with device-posture conditional access, including for remote and third-party access.

**Trade-offs I weigh**
- **Security and user experience:** phase in strong authentication alongside device management to limit friction and lockouts.
- **Build and buy:** a managed detection service gives round-the-clock cover and frees engineers for architecture, automation and oversight, at the cost of some hands-on alert handling.
- **Coverage and perfection:** protect high-value endpoints first rather than waiting for every edge case.

Related: [Here-IAM](https://github.com/sebeaguele/Here-IAM) · [30-days-Detection-Engineering](https://github.com/sebeaguele/30-days-Detection-Engineering) · [incident-response-tool](https://github.com/sebeaguele/incident-response-tool)

### Vulnerability management engineers can trust
- Normalise findings from endpoint, cloud and container scanners so one flaw does not become several tickets.
- Prioritise on exploitability (EPSS, CISA KEV) and asset criticality, not CVSS alone.
- Automate ticketing, ownership, SLAs and escalation.
- Where patching is unsafe, apply compensating controls and a time-bound risk acceptance with a named owner.
- Report coverage, SLA adherence, ageing and residual risk in terms leaders can act on.

The hard part is data modelling and identity resolution: a vulnerable library, the image that contains it and the workload running it can look like three unrelated problems.

Related: [Threat modelling in 5 steps](https://github.com/sebeaguele/5-Step-threat-modelin-process-to-improve-resiliency-identity-close-gaps-)

## Playbook: LLM-jacking through a developer's session

*A generalised response pattern for an emerging threat.*

**Signal:** AI coding assistant usage spikes well outside normal development, with no leaked static API key to explain it.

1. **Investigate live.** Correlate processes, parent-child trees and network connections on the endpoint.
2. **Trace the source.** Follow execution back to the code responsible, such as an unvetted repository, and read its scripts and configuration.
3. **Check the blast radius.** Review environment variables, shell history, persistence points and access to other credentials.
4. **Contain.** Revoke OAuth tokens and sessions, remove the code and verify nothing persists.
5. **Prevent.** Vet third-party repositories and AI extensions, tighten token lifetimes and conditional access, and alert on unusual AI consumption.

Related: [claude-code-security](https://github.com/sebeaguele/claude-code-security)

## Writing: choosing a skill that pays you back

Popularity is not employability. Score a skill on three things:

| Test | Question |
|---|---|
| Time to income | Can you earn from it within 6–12 months? |
| Market demand | Is it driven by compliance, audits, cloud cost pressure or AI governance? |
| Defensibility | Does it need judgement, sit between tech and business, and scale with AI? |

| Skill | Technical level | Why it pays |
|---|---|---|
| AI risk and governance | Low to medium | Regulation and risk mitigation |
| Cybersecurity GRC | Low | Mandatory spend |
| Cloud security posture | Medium | Breach prevention |
| AI operations and oversight | Low | AI needs human accountability |

Learn a concept, explain it in plain English, find the confusion and refine. If you can explain to a CEO why an AI system is risky, you are employable.

Related: [Cybersecurity-Beginner-Roadmap](https://github.com/sebeaguele/Cybersecurity-Beginner-Roadmap)

## Talks and workshops

**Beyond CVSS: risk-based vulnerability management engineering teams trust.** Covered in remediation workshops and leadership briefings: multi-source findings, exploit-led priority, automated ownership, risk acceptance and honest reporting.

## Why I enjoy working with teams in cybersecurity

I am happiest in a room with infrastructure and product engineers, walking through why a vulnerability matters, showing the exposure path and clearing whatever blocks the fix. A compliance argument turns into shared problem-solving, and people leave with a short, defensible priority list.

I have little patience for security theatre. I care about:
- **Responsibility:** every accepted risk has an owner, a control and a review date.
- **Urgency with empathy:** reduce exposure immediately, and give teams room to plan a safe fix without breaking production.
- **Candour:** surface uncomfortable realities early and ground decisions in evidence.
- **Plain language:** technical depth matters most when others can act on it.
