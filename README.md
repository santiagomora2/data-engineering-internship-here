# Data Engineering Internship - HERE Technologies

**Role:** Data Engineering Intern  
**Organization:** HERE Technologies (Governance & Validation Business Unit)  
**Location:** Guadalajara, Mexico  
**Period:** Oct 2025 - Dec 2025  

This repository is a **high-level technical description** of the work I completed during my data engineering internship at HERE Technologies.

⚠️ **Note:**  
No proprietary code, internal data, screenshots, schemas, credentials, or system identifiers are included.  
This repository exists purely as a **personal technical reference and portfolio explanation**.

---

## Background & Context

During my internship, I worked on improving how **Technical Notification Memorandums (TNMs)** were integrated into an internal **data governance and monitoring platform**.

TNMs are structured documents used to communicate significant product changes, launches, or discontinuations. These documents originate from issue-tracking systems and contain a mix of structured fields and free-text descriptions, making them challenging to analyze and visualize at scale.

The platform consuming this data is designed to:
- Centralize governance signals
- Improve data quality oversight
- Enable decision-making across multiple teams

---

## Problem Statement

Before this work:
- TNM information existed in fragmented, semi-structured formats
- Extracting actionable insights required manual inspection
- Data was not optimized for analytics or frontend visualization

The core challenge was to:
> **Transform semi-structured issue-tracking data into clean, reproducible, and readable datasets suitable for governance workflows.**

---

## My Responsibilities

I was responsible for designing and implementing a **data pipeline** that:

- Extracted TNM-related data from an issue-tracking system
- Normalized and validated heterogeneous fields
- Persisted structured records in a scalable NoSQL store
- Exposed read-optimized data for frontend consumption

I worked independently on some tasks while collaborating closely with data engineers and frontend developers to ensure alignment with existing systems.

---

## Technical Overview (High-Level)

The solution followed a modular architecture:

1. **Data Extraction**
   - Serverless functions authenticate and retrieve TNM-related records via REST APIs
   - Linked entities and metadata are resolved during ingestion

2. **Data Transformation**
   - Nested JSON structures are flattened
   - Custom fields are mapped to readable, consistent attributes
   - Dates, enums, and identifiers are type-cast and validated

3. **Persistence Layer**
   - Cleaned records are stored in a NoSQL database
   - Idempotent writes prevent duplication
   - Schema design prioritizes read efficiency

4. **Access Layer**
   - API endpoints expose structured data
   - Responses are formatted for frontend rendering and filtering
   - Errors and edge cases are handled explicitly

---

## Key Data Engineering Challenges

Some of the main challenges I addressed:

- **Schema variability:**  
  Input records contained optional and evolving fields

- **Nested data structures:**  
  Required careful flattening without losing semantic meaning

- **Reproducibility:**  
  Ensuring repeated ingestion runs produced consistent results

- **Data quality:**  
  Validating required attributes and handling incomplete records

- **Performance:**  
  Designing for fast reads and scalable access patterns

---

## Design Decisions

A few principles guided the implementation:

- Favor **read-optimized data models** over raw ingestion
- Normalize early to reduce downstream complexity
- Keep transformations deterministic and testable
- Separate ingestion logic from formatting logic
- Treat monitoring and logging as first-class concerns

---

## Outcomes & Impact

The resulting pipeline:

- Improved readability and accessibility of TNM data
- Reduced manual lookup and cross-team friction
- Enabled consistent frontend visualization
- Provided a scalable pattern for future integrations

The solution was successfully integrated into internal workflows and used by governance stakeholders.

---

## Collaboration & Professional Growth

Beyond the technical work, the internship strengthened my experience in:

- Communicating technical trade-offs clearly
- Working across backend and frontend boundaries
- Taking initiative and ownership over ambiguous tasks
- Designing systems with long-term maintainability in mind

---

## Professional Feedback

> *“Santiago consistently impressed us with his proactive approach, taking initiative without waiting for instructions. His strong technical aptitude, collaborative mindset, and leadership potential made a meaningful impact on our team.”*  
> — **Asrafi A’sat**, Sr. Database Engineer Manager  
> HERE Governance & Validation Business Unit

📄 Extended feedback available in [`TESTIMONIAL.md`](TESTIMONIAL.md)

---

## Final Notes

This repository intentionally avoids implementation details.  
It is meant to capture **what I worked on, how I approached it, and what I learned**, rather than serve as a deployable project.

For questions or discussion, feel free to reach out.
