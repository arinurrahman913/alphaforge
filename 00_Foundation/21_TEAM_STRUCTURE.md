# AlphaForge — Team Structure

> A note before you read further: AlphaForge is built by one human founder
> working alongside multiple AI systems as collaborators. The "roles"
> below describe **how work is delegated by strength**, not legal titles
> or employment. No AI system has authority, accountability, or decision
> rights — Ari Nur Rahman does. Think of this less as an org chart and
> more as a documented workflow: "when I need X, I go to Y."

---

## Founder

**Ari Nur Rahman — Founder & CEO**

Sole human on the team. Owns the vision, the mission, and every final
decision — technical, product, and strategic. Everything below exists to
support that, not replace it.

---

## AI Collaborators

AlphaForge uses different AI systems for different kinds of work, based
on where each one is genuinely strong — not just because "more AI"
sounds impressive. Each entry below explains *why* that system fits that
role, so the mapping stays honest and can be revisited as tools evolve.

### Claude (Anthropic) — Engineering & Architecture

**Why this role:** long-context code review, careful step-by-step
debugging, and a track record in this project specifically of catching
inconsistencies (mismatched scoring logic, unreachable grade thresholds,
crash-prone code paths) rather than just generating code fast.

Typical work:
- Code review, debugging, refactoring
- System architecture and design decisions
- Documentation that needs to stay precise (specs, changelogs, this file)

### ChatGPT (OpenAI) — Research & Content Strategy

**Why this role:** broad general knowledge, strong at brainstorming and
drafting varied content quickly, widely used for research synthesis and
explaining unfamiliar domains.

Typical work:
- Market/industry research drafts
- Content and copywriting (marketing, playbook narrative drafts)
- Brainstorming alternative approaches before committing to one

### Gemini (Google) — Data & Market Analysis

**Why this role:** tight integration with Google's data ecosystem
(Search, Sheets, Finance-adjacent tools), useful where analysis benefits
from broad real-time information retrieval.

Typical work:
- Market data cross-referencing
- Quick fact-checking against current information

### Perplexity — Fact-Checking & Source Verification

**Why this role:** built around cited, sourced answers by default —
useful specifically for claims that end up in playbooks or investment
theses, where an unverifiable claim is a liability, not just an
inconvenience.

Typical work:
- Verifying specific financial/market claims before they enter
  `03_Research/` or `05_Playbooks/`
- Finding primary sources for citations

---

## How This Actually Works Day-to-Day

1. Ari decides what needs doing and picks the tool suited to it (using
   the table above as a starting guide, not a rigid rule).
2. Each AI's output is reviewed by Ari before it's treated as final —
   none of this is autonomous.
3. This document is a **living workflow note**, not a fixed structure.
   If a tool turns out to be a bad fit for its assigned role, or a new
   tool fits better, update this file rather than forcing reality to
   match the doc.

---

## Why Document This At All

AlphaForge's own principle applies here too: *documentation is
development.* Writing down which tool is used for what, and why, makes
the workflow repeatable and reviewable — instead of ad hoc decisions
that live only in Ari's head and get forgotten six months from now.

---

© AlphaForge
