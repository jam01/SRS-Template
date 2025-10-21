# Software Requirements Specification (SRS) Template

A modern, practical SRS template aligned with IEEE 830 and ISO/IEC/IEEE 29148:2011/2017. It emphasizes verifiable requirements, traceability, quality attributes, and clear separation of “what” (requirements) from “how” (design).

This SRS template builds on IEEE 830 and ISO/IEC/IEEE 29148, with the non-functional requirement organization and language based on van Lamsweerde’s Requirements Engineering taxonomy of non-functional requirements. It incorporates modern software component requirements—continuous delivery, observability, and AI/ML.

Designed to be:
- Readable, developer‑friendly, and AI‑usable
- Visually clear, comment‑rich, and easy to fill out
- Comprehensive without being overkill—focused on what most projects need, with clear section goals, sensible defaults, and extensibility points so sections can be filled, skipped, or removed
- Compatible with interactive AI use (models may help fill it conversationally)

## Highlights

- Standards-aligned: IEEE 830, ISO/IEC/IEEE 29148
- Comprehensive structure with clear, testable requirement patterns
- Dedicated sections for Quality of Service, Compliance, and AI/ML
- Built-in guidance, tips, and checklists for each section
- Traceability-ready requirement ID schema and verification matrix
- Suitable for regulated and enterprise contexts

## Who Should Use This

- Product managers and business analysts defining scope and outcomes
- Architects and engineers designing solutions from stable requirements
- QA and SRE teams planning verification and SLAs/SLOs
- Security, compliance, and data governance teams
- AI/ML practitioners needing lifecycle and guardrail requirements

## Template Structure (Overview)

- 1. Introduction: Purpose, scope, glossary, references, and document conventions
- 2. Product Overview: Context, functions, constraints, users, assumptions, allocation
- 3. Requirements:
    - External Interfaces (UI, hardware, software)
    - Functional Requirements (testable “shall” statements)
    - Quality of Service (performance, security, reliability, availability, observability, data quality)
    - Compliance (regulatory/contractual obligations)
    - Design & Implementation constraints (installation, build/delivery, distribution, maintainability, reusability, portability, cost, deadlines, POCs, change management)
    - AI/ML (model specs, data management, guardrails, ethics, human-in-the-loop, lifecycle)
- 4. Verification: Methods, environments, artifacts, and traceability
- 5. Appendixes: Supporting, non-normative materials

## Requirement ID and Traceability

- Format: REQ-[AREA]-[NNN]-[VER] (e.g., REQ-SEC-003-1)
- Areas: FUNC, INT, PERF, SEC, REL, AVAIL, OBS, DATA, COMP, BUILD, DIST, MAINT, REUSE, PORT, COST, DEAD, POC, CM, ML
- Keep IDs immutable; increment version suffix for changes
- Link verification artifacts (tests/analysis/inspection/demo) to IDs

## Getting Started

1. Copy the template file into your repository (e.g., docs/srs.md).
2. Fill metadata (version, author, organization, date).
3. Complete Section 1 to establish context, glossary, references, and conventions.
4. Draft Section 2 with product context and constraints before writing detailed requirements.
5. Capture testable requirements in Section 3 with unique IDs and acceptance criteria.
6. Define verification in Section 4 and maintain the traceability matrix.
7. Keep revision history updated and align with your VCS releases.

## Best Practices

- Write verifiable requirements (avoid vague terms; include metrics/thresholds).
- Separate normative requirements from informative guidance.
- Keep interface definitions declarative and versioned (e.g., OpenAPI/AsyncAPI/JSON Schema).
- Centralize security and compliance requirements for auditability.
- For AI/ML, specify datasets, metrics, guardrails, drift thresholds, and human oversight.
- Maintain change logs and release notes aligned with requirement changes.

## Related Templates

- Software Design Description (SDD) [template](https://github.com/jam01/SDD-Template) (for the “how”): use alongside this SRS to capture architecture and design decisions.
- Markdown Architecture Decision Records (MADR) [templates](https://adr.github.io/madr/) — lightweight ADRs to document significant decisions with context, alternatives, and consequences.

## License

This template is provided as-is. Adapt and extend to meet your organization’s standards and regulatory needs.