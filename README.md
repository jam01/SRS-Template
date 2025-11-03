# Markdown Software Requirements Specification (MSRS)

A modern, practical markdown **Software Requirements Specification (SRS)** template aligned with **IEEE 830** and **ISO/IEC/IEEE 29148:2011/2017**. It emphasizes verifiable requirements, traceability, quality attributes, and clear separation of “what” (requirements) from “how” (design)—leaving that to complementary artifacts such as [Markdown Software Design Description (MSDD)](https://github.com/jam01/SDD-Template).

This SRS template **builds on formal standards**, with the non-functional requirement organization and language based on van Lamsweerde’s Requirements Engineering taxonomy of non-functional requirements, and **incorporates modern software component requirements**—continuous delivery, observability, and AI/ML.

Designed to be:
- Readable, developer‑friendly, and AI‑interpretable
- Comprehensive with intuitive structuring—focused on essential project needs, with clear section goals, sensible defaults, and extensibility points so sections can be filled, skipped, or removed

## Highlights

- **Standards-aligned:** IEEE 830, ISO/IEC/IEEE 29148
- **Comprehensive structure** with clear, testable requirement patterns
- Dedicated sections for Quality of Service, Compliance, and AI/ML
- **Built-in guidance, tips, and checklists** for each section
- **Traceability-ready** requirement ID schema and verification matrix
- Suitable for regulated and enterprise contexts

## Who Should Use This

- **Product managers and business analysts** defining scope and outcomes
- **Architects and engineers** designing solutions from stable requirements
- **QA and SRE teams** planning verification and SLAs/SLOs
- **Security, compliance, and data governance teams**

## Quick Start

1. Copy the template file into your repository (e.g., `docs/srs.md`).
2. Fill metadata (version, author, organization, date).
3. Complete Section 1 to establish context, glossary, references, and conventions.
4. Draft Section 2 with product context and constraints before writing detailed requirements.
5. Capture testable requirements in Section 3 with unique IDs and acceptance criteria.
6. Define verification in Section 4 and maintain the traceability matrix.
7. Keep revision history updated and align with your VCS releases.

## Template Structure (Overview)

1. Introduction: Purpose, scope, glossary, references, and document conventions
2. Product Overview: Context, functions, constraints, users, assumptions, allocation
3. Requirements:
    - External Interfaces (UI, hardware, software)
    - Functional Requirements (externally observable behaviors)
    - Quality of Service (performance, security, reliability, availability, observability)
    - Compliance (regulatory/contractual obligations)
    - Design & Implementation constraints (installation, build/delivery, distribution, maintainability, reusability, portability, cost, deadlines, POCs, change management)
    - AI/ML (model specs, data management, guardrails, ethics, human-in-the-loop, lifecycle)
4. Verification: Methods, environments, artifacts, and traceability
5. Appendixes: Supporting, non-normative materials

## Workflows

* [srs-template.md](srs-template.md) — Guided SRS with explanations and tips.
* [srs-template-bare.md](srs-template-bare.md) — Minimal SRS scaffold.
* [req-template.md](req-template.md) — Guided requirement template with prompts and tips for non-monolithic SRS.
* [req-template-bare.md](req-template-bare.md) — Minimal requirement template for non-monolithic SRS.

#### One-shot document

  * Fill `srs-template.md`.
  * Export to PDF/HTML (e.g., pandoc) and share.

#### Long-lived SRS in VCS
  * Keep `srs-template.md` as `docs/srs.md`.
  * Incrementally add/modify requirements.
  * Export on releases for stakeholders. 
  * Treat `docs/srs.md` as the source of truth.
  * Keep templates available in-repo to standardize language and structure.
  * Provide the guided SRS and requirement templates to an LLM as context.

#### Breakout files (MADR-inspired)

  * Maintain an SRS plus separate requirement files under `docs/requirements/`.
  * Use `req-template.md` or `req-template-bare.md` for each requirement (one file per REQ). 
  * Link each requirement from the SRS (Section 3 index). 
  * Track verification links in SRS Section 4. 

#### Requirements-only (MADR-style)

  * Manage `docs/requirements/*.md` without a monolithic SRS.
  * Generate a simple index or roll-up SRS as needed.

## On Requirements Engineering

#### Overlaps Between Functional and Non-Functional Requirements

In practice, the line between functional and non-functional requirements is rarely clear-cut. Many requirements naturally span both domains. For example, a safety injection signal in a nuclear power system is both functional—it defines when the signal must activate—and non-functional, as it enforces a safety constraint. The same applies to features like call screening or firewall management, which provide specific functionality while also ensuring privacy and security. Categories often overlap; an availability requirement, for instance, contributes to both system reliability and security.

#### Why Requirement Taxonomies Still Matter

Even with these overlaps, maintaining a taxonomy of requirements adds structure and clarity to the requirements engineering (RE) process. Categorization helps teams articulate not only what a system must do, but also how well and under what constraints it must operate. Functional requirements typically describe concrete system behaviors, while non-functional ones define qualities that cut across features—like usability, performance, or confidentiality. This distinction also supports systematic analysis: it makes it easier to spot missing requirements (e.g., is there any explainability requirement on X?), detect potential conflicts (e.g., between usability and security), and prioritize trade-offs during design and validation.

For developers, QA engineers, and architects, a requirements taxonomy acts as a mental model for navigating complexity. It provides a shared vocabulary for reasoning about behavior, quality, and constraints throughout the software lifecycle—guiding not just how systems are built, but how they are tested, evaluated, and evolved.

## Related Projects

* [Markdown Software Design Description (MSDD)](https://github.com/jam01/SDD-Template)
* [Markdown Architecture Decision Records (MADR)](https://adr.github.io/madr/)

## License

This template is dedicated to the public domain under the [Creative Commons Zero v1.0 Universal (CC0 1.0)](https://creativecommons.org/publicdomain/zero/1.0/) license.

You can copy, modify, distribute, and use the work, even for commercial purposes, without asking for permission.
