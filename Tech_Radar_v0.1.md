# AI Tech Radar v0.1 (SDLC-focused, 1k+ Developers)

Purpose
A living radar to guide enterprise selection and rollout of AI tools that impact the SDLC or are SDLC-adjacent. Emphasis on security, governance, integration at 1k+ developer scale, and measurable ROI.

Scope Categories
1) IDE Copilots & Agents
2) Code Intelligence & Search
3) Test Generation & QA
4) CI/CD & Release Automation
5) Architecture & Design Assistants
6) Code Security & Secret Scanning
7) Dependency & SCA with AI
8) Incident Management with AI
9) Documentation & Knowledge Assistants
10) Platform Engineering AI (Backstage, golden paths)
11) Model & Platform Governance (gateways, evals, observability, policy)

Ring Definitions
- Adopt: Proven at 1k+ developer scale. Meets enterprise controls (zero-retention or approved retention policy, no training on private code by default), SSO/RBAC, audit logging, enterprise support, stable roadmap, strong ROI and integration depth.
- Trial: Meets core enterprise controls and shows strong promise; requires controlled pilot to validate scale, integration, and change management.
- Assess: Promising capability but missing one or more enterprise criteria (scale, controls, support) or unclear ROI; evaluate in labs or small PoCs.
- Hold: Avoid or restrict due to material risks (security, privacy, governance, reliability) or poor fit today. Reassess only if conditions materially change.

Initial Placements (from current research)
Note: This is v0.1; re-evaluate quarterly.

1) IDE Copilots & Agents
- Adopt: GitHub Copilot (Business/Enterprise)
- Trial: Claude Code (terminal-native assistant)
- Trial: Copilot Workspace (agentic workflows via Actions) in constrained scenarios
- Assess: Sourcegraph Amp (agentic features) as an IDE-adjacent agent complement
- Assess: Cline (open-source IDE agent with MCP)
- Assess: Roo Code (open-source, multi-modal agents, BYOK)
- Assess: Kilo Code (hybrid, newer ecosystem)
- Hold: Trae (ByteDance VS Code fork) — significant telemetry/privacy concerns for enterprise

2) Code Intelligence & Search
- Adopt: Sourcegraph code intelligence/search (Cody for assist as appropriate)
- Trial: Sourcegraph Amp agentic features (advanced automation) behind security gates
- Assess: Open-source embedding + repo RAG patterns with gateway enforcement and org policy
- Assess: IDE-native code search combos (JetBrains/VS Code plugins) for small teams

3) Test Generation & QA
- Trial: Copilot test generation features (language/framework champions)
- Assess: Dedicated AI test-generation platforms (evaluate mutation testing, flaky detection, CI integration)
- Assess: Model-in-the-loop fuzzing and property testing pilots
- Hold: Autonomous test approval without human gates

4) CI/CD & Release Automation
- Trial: Copilot + GitHub Actions authoring and remediation suggestions
- Assess: AI-assisted pipeline policy generation (OPA/Rego co-piloting, guarded)
- Assess: Release note generation with audit trails
- Hold: Autonomous production deployment decisions by agents

5) Architecture & Design Assistants
- Trial: Claude Code for CLI-first ADR drafting and sequence diagrams
- Assess: Copilot/Workspace for architecture scaffolding under review gates
- Assess: Spec-to-skeleton generators (OpenAPI/AsyncAPI, IaC) with human validation

6) Code Security & Secret Scanning
- Adopt: Enterprise-grade scanners (e.g., GitHub Advanced Security, Snyk, Semgrep) with AI explain/fix
- Trial: Sourcegraph Amp secret redaction and security governance features
- Assess: LLM-assisted fix PRs under policy review

7) Dependency & SCA with AI
- Adopt/Trial: SCA platforms with AI remediation guidance (Snyk/Whitesource/GHAS Dependabot+) based on current stack
- Assess: LLM-generated upgrade PRs with build/coverage gates

8) Incident Management with AI
- Trial: AIOps assistants (incident summarization, RCA draft, runbook retrieval) integrated with existing observability
- Assess: On-call copilots that propose queries and actions; human-in-the-loop mandatory

9) Documentation & Knowledge Assistants
- Adopt: Copilot documentation generation; guarded content filters
- Trial: Repo and ticket RAG with enterprise gateway/policy, internal KB integration
- Assess: Auto-sync from ADRs, code comments, and PRs to internal docs

10) Platform Engineering AI
- Trial: Backstage AI plugins (golden path generation, template assistants)
- Assess: Paved road authoring/refactoring copilots with policy checks
- Hold: Autonomous platform changes without approvals

11) Model & Platform Governance
- Adopt: Enterprise model gateways with zero-retention endpoints, SSO/RBAC, PII redaction, audit (Azure OpenAI, AWS Bedrock, Anthropic Enterprise/Console with enterprise terms, or approved gateway)
- Trial: LLM observability/evals (Langfuse/Log10 + internal eval harnesses)
- Assess: Policy-as-code for prompts/PII/PHI handling and output guardrails

Pilot Wave 1 (90 days) — recommended for scale validation
- Tracks:
  A) IDE Copilot: GitHub Copilot Business/Enterprise across top 3 languages and 6+ product teams
  B) Code Intelligence: Sourcegraph search + Cody assist for 3 repos with different sizes
  C) CLI Assistant: Claude Code for platform/SRE and services teams

- Guardrails:
  - Zero data retention on private code; no training on your code
  - SSO/RBAC; audit logging enabled; org policy docs signed
  - AI-generated code must pass normal review, tests, and security scans

- Success metrics (per team, baseline vs. pilot):
  - Suggestion acceptance rate; time to PR; code review cycle time
  - Test coverage delta; defect escape rate; security finding rate
  - Mean time to understanding (new joiners) and to first PR
  - Developer satisfaction (quarterly survey), opt-in/active usage
  - Cost per active user and ROI vs. baseline

Build vs Buy Guidance (summary)
- Buy for: Copilot, Sourcegraph code intelligence, enterprise gateways/governance
- Trial/Assess build: repo RAG, policy adapters, eval harnesses, Backstage plugins
- Hold build: full autonomous agents that perform CI/CD without human gates

Change Management and Governance
- Mandatory training on secure AI-assisted dev
- Policy: acceptable use, IP/PII protection, review and testing requirements
- Monthly telemetry to executive dashboard; quarterly ring updates

Review Cadence
- Rings updated quarterly; category owners propose movement with metrics
- Executive readout bi-annually with ROI and risk posture

Appendix A: Evidence Sources
- Internal whitepapers in repo (Copilot, Sourcegraph Amp, IDE agents)
- External vendor docs and security posture references (tracked in rubric file)