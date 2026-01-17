# Contributing Guide  
## Project Aether — Enterprise AI Governance Gateway

Thank you for your interest in contributing to **Project Aether**.

Aether is a **research-driven, design-focused project** that demonstrates patterns for **AI governance, safety enforcement, and red-teaming infrastructure**.  
While contributions are welcome, the primary goal of this repository is to serve as a **reference implementation and architectural exemplar**, not a general-purpose open-source product.

---

## 1. Contribution Philosophy

Project Aether prioritizes:

- **Clarity over feature volume**
- **Deterministic safety guarantees over flexibility**
- **Design correctness over rapid iteration**

As such, not all contributions will be accepted.

Changes that weaken safety guarantees, reduce auditability, or introduce ambiguous behavior will be rejected.

---

## 2. What Contributions Are Welcome

We welcome contributions in the following areas:

### 2.1 Documentation Improvements
- Clarifying architecture or threat model explanations
- Improving readability without changing meaning
- Adding diagrams or annotations that do **not** leak sensitive implementation details

### 2.2 Red-Teaming & Evaluation
- New adversarial test cases
- Additional threat categories
- Improvements to red-team documentation methodology

### 2.3 Safety Research
- References to relevant papers or industry practices
- Alternative approaches to toxicity detection or PII handling (design-level only)

### 2.4 Bug Fixes (Scoped)
- Deterministic bugs in detection logic
- Logging, observability, or audit trail issues
- Clearly bounded correctness fixes

---

## 3. What Contributions Are NOT Accepted

The following will generally not be accepted:

- Feature requests that expand scope beyond governance and safety
- Prompt engineering changes intended to “fix” unsafe behavior
- Model fine-tuning or alignment experiments
- UI/UX redesigns unrelated to safety or auditability
- Changes that reduce blocking strictness or fail-open behavior
- Requests to expose internal prompts, thresholds, or secrets

Aether is intentionally conservative by design.

---

## 4. Design Constraints (Non-Negotiable)

All contributions must respect the following constraints:

- **Fail-closed by default**
- **Safety enforced outside the LLM**
- **Blocking over rewriting**
- **Auditability over convenience**
- **Defense-in-depth over single-layer detection**

If a change violates any of the above, it will not be merged.

---

## 5. Submitting Changes

### 5.1 Pull Requests
- Keep pull requests small and focused
- One logical change per PR
- Include clear motivation and impact analysis

### 5.2 Documentation Changes
- Use precise, technical language
- Avoid marketing-style claims
- Prefer explicit guarantees over aspirational statements

### 5.3 Code Contributions (When Opened)
- Follow existing structure and patterns
- Include docstrings and comments (Google-style where applicable)
- Avoid introducing non-deterministic behavior

---

## 6. Security Disclosure

If you discover a **security vulnerability** or a **safety bypass**, **do not open a public issue**.

Instead:
- Document the issue clearly
- Provide reproduction steps
- Label it as a security concern if private channels are provided

Responsible disclosure is expected.

>At present, no public vulnerability intake is provided; this guidance exists to set expectations for responsible disclosure should private reporting channels be added in the future.

---

## 7. Code of Conduct

This project follows standard professional conduct expectations:

- Be respectful and constructive
- Assume good intent
- Focus discussions on technical merit

Harassment, abuse, or adversarial behavior toward contributors will not be tolerated.

---

## 8. Final Note

Project Aether is maintained as a reference architecture to demonstrate that AI safety can be managed as a deterministic infrastructure requirement.\
Contributions that reinforce the rigor, auditability, and fail-closed nature of this gateway are highly valued.

Thank you for helping maintain the technical integrity of this governance framework.
