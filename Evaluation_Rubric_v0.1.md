# Enterprise Evaluation Rubric v0.1 (SDLC AI Tools, 1k+ Developers)

Purpose
A consistent, auditable rubric to evaluate SDLC and SDLC-adjacent AI tools for a 1k+ developer enterprise. Use this for market scans, shortlists, and pilot exit criteria. Scoring supports ring placement in the Tech Radar.

How to Use
- Score each criterion 0-5. Multiply by weight to get weighted score.
- Sum weighted scores to obtain Total Score (0-100).
- Ring guidance:
  - Adopt: ≥80 and no Critical Red flags
  - Trial: 60–79 and no Critical Red flags
  - Assess: 40–59 or has 1 Critical mitigated; requires constraints
  - Hold: <40 or any unmitigated Critical Red flag

Scoring Scale
0 = Not present / unacceptable
1 = Minimal / proof-of-concept only
2 = Partial; gaps require compensating controls
3 = Adequate; meets baseline enterprise needs
4 = Strong; well-integrated and reliable
5 = Excellent; industry-leading

Weights and Criteria (Total 100)
1) Security & Compliance (Critical) — 18
  a) Certifications & attestations (SOC2, ISO27001, PCI, HIPAA options): 0-5 (5)
  b) Secure SDLC & vulnerability posture (SAST/DAST/SBOM, patch cadence): 0-5 (6)
  c) Incident response, logging, forensics, breach comms: 0-5 (7)

2) Data Handling & Retention (Critical) — 12
  a) Zero retention or configurable retention with proofs; data locality: 0-5 (6)
  b) No training on private code by default; contractual guarantees: 0-5 (6)

3) Identity, Access & Admin — 8
  a) SSO/SAML/OIDC, SCIM/JIT, RBAC/ABAC granularity: 0-5 (5)
  b) Org-wide policy controls, auditability, exportable logs: 0-5 (3)

4) Integration & Interop — 12
  a) IDEs (VS Code/JetBrains/Visual Studio) and VCS/PR systems: 0-5 (6)
  b) CI/CD, security tools, issue tracking, API/SDK/webhooks: 0-5 (6)

5) Scalability & Reliability — 10
  a) Proven scale (1k+ devs), performance SLOs, regional coverage: 0-5 (5)
  b) Availability, rate limits, capacity planning, multi-tenant isolation: 0-5 (5)

6) Developer UX & Adoption — 8
  a) Time-to-value, learning curve, docs/support, accessibility: 0-5 (5)
  b) Enterprise features for change management and enablement: 0-5 (3)

7) Observability, Evals & Safety — 8
  a) Tracing, prompt/result logging, redaction, PHI/PII guards: 0-5 (5)
  b) Offline/evals integration (Langfuse/Log10/custom harness): 0-5 (3)

8) Cost, TCO & ROI — 10
  a) Pricing transparency, predictability, unit economics: 0-5 (5)
  b) Expected ROI at scale; procurement/commercial terms: 0-5 (5)

9) Vendor Viability & Roadmap — 8
  a) Financial health, support SLAs, customer references: 0-5 (5)
  b) Roadmap alignment, cadence, openness to enterprise asks: 0-5 (3)

10) Lock-in, Exit & Governance Fit — 6
  a) Data export, portability, standards (MCP/OCI/open APIs): 0-5 (3)
  b) Policy-as-code fit, legal/IP terms, indemnification: 0-5 (3)

Critical Red Flags (automatic Hold unless mitigated with executive sign-off)
- Unchangeable retention of customer code, or training on private code by default
- Lack of SSO/RBAC and inadequate audit trails for regulated teams
- Persistent undisclosed telemetry or opaque data sharing to unapproved regions
- Absence of incident response commitments or breach notifications
- Known security vulnerabilities with slow or absent remediation
- Prohibited jurisdictions or supply chain risks per company policy

Assessment Template (copy per tool)
- Tool/Version:
- Category:
- Deployment Model:
- Regions/Data Residency:
- Models/Providers used:
- Summary:
- Ring Recommendation (initial):
- Risk Register (key risks, owners, target mitigations, dates):

Scorecard
1) Security & Compliance [18]:
  a) Certs/Attestations: [0-5] ×5 = 
  b) Secure SDLC/Vuln Posture: [0-5] ×6 = 
  c) IR/Logging/Forensics: [0-5] ×7 = 
2) Data Handling & Retention [12]:
  a) Retention/Locality: [0-5] ×6 = 
  b) Training on private code: [0-5] ×6 = 
3) Identity & Admin [8]:
  a) SSO/RBAC/SCIM: [0-5] ×5 = 
  b) Policies/Audit: [0-5] ×3 = 
4) Integration & Interop [12]:
  a) IDE/VCS: [0-5] ×6 = 
  b) CI/CD/APIs: [0-5] ×6 = 
5) Scale & Reliability [10]:
  a) Scale/SLOs: [0-5] ×5 = 
  b) Availability/Isolation: [0-5] ×5 = 
6) UX & Adoption [8]:
  a) TTV/Docs/Support: [0-5] ×5 = 
  b) Enablement: [0-5] ×3 = 
7) Observability & Evals [8]:
  a) Tracing/Redaction/PII: [0-5] ×5 = 
  b) Evals Integration: [0-5] ×3 = 
8) Cost, TCO & ROI [10]:
  a) Pricing/Unit economics: [0-5] ×5 = 
  b) ROI/Terms: [0-5] ×5 = 
9) Vendor & Roadmap [8]:
  a) Viability/SLAs/Refs: [0-5] ×5 = 
  b) Roadmap/Alignment: [0-5] ×3 = 
10) Lock-in & Governance [6]:
  a) Portability/Standards: [0-5] ×3 = 
  b) Policy/IP/Indemnity: [0-5] ×3 = 

Total (0–100):

Pilot Playbook Addendum (v0.1)
Pilot Design (30-60-90)
- 0–30 days: Baseline metrics; enable SSO, policies, audit; initial training; small cohort (≤100 devs)
- 31–60 days: Expand to 300–500 devs; enable advanced features; integrate CI/CD and security scans; weekly metrics
- 61–90 days: Stabilize; optimize prompts/workflows; formal exit review with ROI and risk outcomes

Pilot Metrics (collect per team weekly)
- Productivity: suggestion acceptance rate; time-to-PR; review cycle time; story throughput
- Quality: test coverage delta; defect escape rate; static analysis/security findings per KLOC
- Reliability: outage/latency incidents impacting devs; error rates
- Adoption/Satisfaction: DAU/WAU; usage depth; survey score (1–10)
- Financials: license/utilization; model spend; cost per active user; ROI trend

Success Criteria & Exit
- Move to Adopt ring if Total Score ≥80, KPIs meet targets, and no Critical Red flags
- Move to Trial ring if Total Score 60–79 with clear plan to close gaps in 1–2 quarters
- Defer/Hold if material risks persist or ROI is negative after remediation attempts

Category-Specific Notes (v0.1 excerpts)
- IDE Copilots & Agents: Emphasize zero-retention, SSO/audit, code review gates; restrict autonomous file edits in CI
- Code Intelligence & Search: Validate indexing boundaries, secret redaction, and access control inheritance
- Test Gen & QA: Require mutation testing or equivalent signal; block auto-merge without reviewer approval
- CI/CD & Release: Disallow autonomous prod changes; require policy-as-code and approval workflows
- Gov/Model Platform: Prefer enterprise gateways (Azure OpenAI, Bedrock, Anthropic Enterprise/Console) with auditable policies

Initial Example Ring Mappings (traceable to Tech_Radar_v0.1)
- GitHub Copilot (Business/Enterprise): Expect Adopt (≥80) given security, scale, ROI
- Sourcegraph code intelligence/search: Adopt for code search; Amp agentic features Trial pending security validation
- Claude Code: Trial for CLI-first use; validate IR/audit integration and data handling
- Cline/Roo/Kilo: Assess due to scale/support; strong for niche/open-source needs with MCP; ensure BYOK and policy
- Trae: Hold due to telemetry/privacy risks at enterprise

Governance & Cadence
- Quarterly re-scoring and ring proposals by category owners
- Bi-annual executive review with ROI and risk heatmaps
- Central registry of assessments and decisions; change logs for audit

Appendix
- Evidence links: maintain per-tool references and internal test results
- Definitions: Critical = could trigger legal, compliance, or material IP risk without mitigation
- Versioning: v0.1 seeded from internal whitepapers and current market data; iterate monthly on hot categories