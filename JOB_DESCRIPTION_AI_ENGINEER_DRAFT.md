# Job Description (Draft) — Senior Engineer, AI & Automation Platform

> Draft grounded in two internal systems: a quarterly investment-reporting pipeline and a due-diligence
> memo generation platform (plus a newer effort to generalize the latter into a framework-learner +
> generator pair). Posting to be issued under **Vectera** (wholly owned by Townsend) — do not use
> "Townsend" in the external posting.

## About the role

We're looking for an engineer to build and own the automation that turns firm and client documents —
spreadsheets, PDFs, decks, committee logs, due-diligence materials — into audit-ready institutional
deliverables: quarterly client reports and investment-committee memos among them. Every number has to
foot, every factual claim has to trace to a source, and a person signs off before anything reaches a
client or committee.

You'll draw the line between deterministic code and model judgment, keep the model's output honest once
it's in the loop (multi-pass generation, critique, citation audit, full-source verification), and take
systems from a local prototype to something running unattended on a server, reproducibly.

## What you'll do

**AI-assisted document automation**
- Build ingestion pipelines across heterogeneous sources (multi-sheet workbooks, PDFs, decks with chart
  data trapped in raster images) into structured, verified output.
- Keep computation, ranking/selection, reconciliation, and compliance checks deterministic; use a model
  only where judgment is genuinely required, with its output grounded and verified, not trusted.
- Design conservative, traceable entity resolution — not silent fuzzy-matching.
- Handle missing, malformed, or irrelevant inputs gracefully: fail loud and safe, and distinguish "flag
  and continue" from "stop for human review."

**Multi-pass generation & knowledge systems**
- Build generate → critique → revise → audit → verify pipelines, not single-shot prompts.
- Verify absence-claims against the full source corpus, not just retrieved context.
- Keep domain/analytical knowledge in structured, human-editable data files, not hardcoded logic — the
  engine stays generic; a different knowledge pack should change the output, not the code.
- Design prompt systems as maintainable, composable scopes rather than one large fragile template.
- *(Stretch)* Contribute to systems that learn that structure from example documents rather than
  having it hand-authored.

**Human-in-the-loop & traceability**
- Design the draft/approve boundary and how sign-off gets recorded.
- Make every material figure and factual claim resolve to a machine-readable source.

**Platform engineering**
- Own reproducibility and adaptability: same inputs → same output; next period's inputs should work via
  configuration, not a rewrite.
- Take systems from local scripts to server-deployed production — environment parity, secrets,
  scheduling, monitoring for unattended runs.
- Cache expensive third-party extraction calls; re-run only when sources actually change.
- Keep components isolated, with a single auditable handoff between them.
- Build a lightweight operator interface (kick off a run, review the output), and bring real testing,
  dependency management, and LLM-call observability.

**Cross-functional**
- Translate reporting and analytical rules from investment teams into code and verification logic.

## What we're looking for

- **The ability to cleanly separate probabilistic AI behavior from deterministic business logic and
  validation** — knowing what must never be delegated to a model, and building the guardrails that keep
  it that way.
- Strong engineering fundamentals; production data pipelines shipped, not just prototypes.
- Real experience building LLM-integrated systems with grounding/verification, and a clear sense of
  where models fail and how to design around it.
- Experience with multi-pass/self-critique LLM workflows, and the judgment to know when that's worth it.
- Experience extracting data from unstructured/semi-structured documents, including chart data that
  only exists as pixels.
- Demonstrated testing/verification judgment — how you know output is correct, how you'd catch a
  regression.
- Comfort taking a system from a laptop to unattended production (secrets, scheduling, monitoring).
- Clear, honest technical communication about what a system does and doesn't do.

## Nice to have

- Asset management, real estate, or other regulated financial services experience.
- Vision-capable/multimodal model experience for image/scanned-document extraction.
- Third-party document-parsing/OCR API experience and cost-aware caching.
- Lightweight internal tool/UI building for non-engineering stakeholders.
- Data governance/audit/compliance exposure.
- Information-extraction or taxonomy-induction experience (clustering/normalizing inconsistent content).
- We run primarily on Azure — useful (not required) familiarity with any of: Azure OpenAI, Azure AI
  Search, Azure AI Document Intelligence, Azure Blob Storage, Azure Functions or Container Apps, Service
  Bus, Azure SQL or PostgreSQL, Key Vault, Microsoft Entra ID, Application Insights. Not expected to have
  used every service.

## How we hire for this

A practical take-home exercise plus a live technical round, focused on engineering judgment rather than
trivia — the differentiator is whether you understand what you built well enough to defend and adapt it
live.

## Working style

Vectera operates with the pace, ownership, and responsiveness of a small, high-output engineering team.
Best suited to someone who moves quickly, works through ambiguity, and owns things from design through
production operation. Important releases and business-critical deliverables may periodically require
flexibility outside standard working hours, and the team interacts multiple times throughout the day.
This is not a 9-to-5 role, and it is not a lifestyle-friendly remote arrangement.
