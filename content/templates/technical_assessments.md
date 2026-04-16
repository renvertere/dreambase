---
title: "<% tp.file.title %>"
type: solution-assessment
tags:
  - solution
  - assessment
  - architecture
  - strategy
created: <% tp.date.now("YYYY-MM-DD") %>
status:
owner:
stakeholders:
---

# 🧭 Solution Assessment — <% tp.file.title %>

> Structured evaluation of a proposed solution to address a defined business or technical problem.

---

# 0. Executive Summary

## Recommendation

> State the decision clearly:
>
> * Approve / Reject / Conditional Approval

## Why This Solution

* Key reason 1
* Key reason 2
* Key reason 3

## Expected Outcome

* Business impact
* Operational impact

## Cost Summary

* Estimated cost (high-level)
* Key cost drivers

## Key Risks

* Risk 1 + mitigation
* Risk 2 + mitigation

## Decision Required

> What action is needed and by whom

---

# 1. Problem Statement

Define the **problem or opportunity** being addressed.

Include:

* Business context
* Technical context (if relevant)
* Current limitations
* Why action is required

Questions this section should answer:

* What is broken or missing?
* Who is impacted?
* What happens if the problem remains unsolved?

---

# 2. Desired Outcome

Describe the **target state** the solution should achieve.

Include:

* Operational improvements
* Business impact
* Risk reduction
* Performance improvements

---

# 3. Proposed Solution

Provide a **clear narrative description** of the proposed solution.

Focus on:

* What the solution does
* How it addresses the problem
* Why this approach was chosen

Avoid vendor or tool bias in this section.

---

# 4. Solution Components

Describe the **logical components of the solution**, not just technologies.

| Component   | Role     | Responsibility | Notes              |
| ----------- | -------- | -------------- | ------------------ |
| Component A | Function | What it does   | Key considerations |
| Component B | Function | What it does   | Dependencies       |

Components may include:

* Processes
* Platforms
* Tools
* Governance mechanisms
* Operational procedures

---

# 5. Operational Model

Describe how the solution will be **operated and maintained**.

Include:

* Ownership model
* Operational responsibilities
* Support model
* Monitoring and maintenance approach

Example questions:

* Who owns the system?
* Who responds to failures?
* How are updates deployed?

---

# 6. Cost Assessment

## 6.1 Infrastructure / Platform Cost

| Category   | Description | Estimated Cost |
| ---------- | ----------- | -------------- |
| Compute    |             |                |
| Storage    |             |                |
| Licensing  |             |                |
| Networking |             |                |

## 6.2 Operational Cost

| Category         | Description           | Estimated Cost |
| ---------------- | --------------------- | -------------- |
| Engineering Time | Implementation effort |                |
| Operations       | Maintenance effort    |                |
| Training         | Knowledge development |                |

## 6.3 Long-Term Cost Drivers

Discuss:

* Scaling impact
* Data growth
* Operational overhead
* Vendor lock-in risks

---

# 7. Benefits Assessment

Describe the **value delivered by the solution**.

| Benefit Category | Description |
| ---------------- | ----------- |
| Operational      |             |
| Financial        |             |
| Risk Reduction   |             |
| Strategic        |             |

---

# 8. Architectural Principles

List the **design principles guiding the solution**.

Examples:

* Separation of responsibilities
* Security-first design
* Observability by default
* Automation over manual operations
* Scalability and resilience

---

# 9. Implementation Plan

## Phase 1 — Discovery & Planning

Activities:

* Stakeholder alignment
* Requirements validation
* Architecture design

Deliverables:

* Finalized design
* Implementation plan

---

## Phase 2 — Initial Implementation

Activities:

* Core solution deployment
* Initial configuration
* Operational validation

Exit Criteria:

* Stable operation
* Functional validation

---

## Phase 3 — Controlled Deployment

Activities:

* Limited production rollout
* Monitoring and validation

Exit Criteria:

* No operational disruptions
* Stable performance

---

## Phase 4 — Full Adoption

Activities:

* Organization-wide rollout
* Documentation and training

Deliverables:

* Operational runbooks
* Onboarding procedures

---

# 10. Risk Assessment

| Risk                      | Impact | Mitigation |
| ------------------------- | ------ | ---------- |
| Implementation complexity |        |            |
| Operational knowledge gap |        |            |
| Cost growth               |        |            |
| Adoption resistance       |        |            |

---

# 11. Success Criteria

Define measurable indicators of success.

Examples:

* Reduced operational incidents
* Improved system observability
* Faster troubleshooting
* Reduced operational overhead

---

# 12. Timeline Overview

| Phase                 | Duration |
| --------------------- | -------- |
| Discovery             |          |
| Planning              |          |
| Implementation        |          |
| Controlled Deployment |          |
| Full Adoption         |          |

---

# 📚 Reference Materials

List supporting documentation:

* Architecture documentation
* Vendor documentation
* Internal standards
* Best practice guides

---

# 📋 Prompt for Use

> I am going to provide you with a **proposed solution, architecture idea, or technical strategy**.
> Please convert the information into the **Solution Assessment Template**.

Guidelines:

* Identify the **problem being solved**
* Describe the **desired outcome**
* Extract the **solution components and responsibilities**
* Evaluate **operational impact**
* Build a **cost assessment**
* Identify **benefits and risks**
* Structure the **implementation plan into phases**
* Define **success criteria**

Output:

Return a **fully structured markdown document using this template**.

