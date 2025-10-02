---
title: "<% tp.file.title %>"
type: sop
tags:
  - sop
  - procedure
  - operations
created: <% tp.date.now("YYYY-MM-DD") %>
review_date: 
owner: 
approver: 
version: 1.0
---
# 📋 Standard Operating Procedure — <% tp.file.title %>

## 🧾 Purpose
> State **why this SOP exists** and what objective it supports.
> Example: “This SOP defines the process for performing a nightly backup of the production Database to ensure business continuity and compliance with data retention policies.”  

## 📍 Scope
> Define where this procedure applies, to whom, and under what conditions.
> Example: “This procedure applies to all Database instances managed by the DBA team in the production environment. It does not cover non-production systems such as dev/test databases.”  


## 🧰 Prerequisites
- Required tools
- Required permissions or roles
- Systems / environments in scope
- References to related standards/policies

## 🧑‍💻 Procedure

1. **Step 1** — Detailed instruction  
   ```bash
   # Example command or configuration
   ```
2. **Step 2** — Detailed instruction
3. **Step N** — Continue until procedure is complete

## ✅ Verification

> How to confirm procedure was followed successfully.
- Logs / output to check
- Expected system state
- Validation steps

## ⚠️ Safety / Risks

> List hazards, risks, or security implications.
> Example: “Restoring the wrong database instance may result in permanent data loss.”
> 	Risk: Overwriting active database during restore
> 	Mitigation: Verify instance name and environment before execution
> 	Risk: Incomplete restore due to corrupted backup
> 	Mitigation: Validate backup integrity using RMAN `VALIDATE BACKUPSET`

- Risk 1
- Mitigation 1

## 📅 Roles & Responsibilities
- **Owner** — Accountable for SOP updates
- **Executor** — Person/team who performs steps
- **Reviewer** — Confirms compliance
## 🔗 References
- [[How To: Related Guide]]
- [[Policy: Security Standard]]
- External link if needed

## ⏱ Benchmark / Time Indicator

> Record the **expected duration** of the procedure and track **actual completion times** each time the SOP is used.  
> Example: “Expected: 45 minutes. Actual: ___ minutes.”

|Date|Executor|Expected Duration|Actual Duration|Notes|
|---|---|---|---|---|
|2025-10-02|DBA Team|45 min|50 min|Extra validation step|

## 📝 Revision History

|Version|Date|Author|Changes Made|
|---|---|---|---|
|1.0|<% tp.date.now("YYYY-MM-DD") %>|Author|Initial draft|
