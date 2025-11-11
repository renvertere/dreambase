Here is my Prompt:

You are filling out a **“web_report”** note — a structured investigation entry for verified, citation-based research.

---

**Output requirements (strict):**
1. **Do NOT include the document properties (the YAML block between `---` and `---`).** Obsidian generates this automatically.
2. Render a **SINGLE markdown document** with these exact sections, in this exact order:
    - # 🧾 Investigation Report
    - ## 🧭 Overview
    - ## 📑 Findings
    - ## 🧩 Evidence Table
    - ## 🧠 Source Annotations
    - ## ⚖️ Consistency Check
    - ## 🕳️ Gaps & Unknowns
    - ## 📊 Integrity Summary
    - ## 🗂️ Appendix A – Artifacts
    - ## 🔍 Appendix B – Search Log
    - ## 🧮 Global Confidence
    - ## 🚨 Alerts
3. Output **all sections in one response.** Do not wait for confirmation.
4. **Do NOT** add any extra headings, preambles, or trailing prose outside these sections.
5. Do **not** wrap the whole document in a code block.
6. Use fenced code blocks **inside sections only** when needed (e.g., tables, citation snippets).
7. If a section would be empty, include a short placeholder line starting with “>”.
8. Maintain valid Markdown for perfect Obsidian rendering.

---

### **Section semantics**

- **🧭 Overview** — Define scope, key question, time window, and summary.
- **📑 Findings** — Bullet verified facts, each ending with inline citations like `[S1][S2]`.
- **🧩 Evidence Table** — Tabulate claims, provenance, citations, risk rating, decision rules, and archive links.
- **🧠 Source Annotations** — Describe each source (`[S#]`): type, credibility, authorship score, and rationale.
- **⚖️ Consistency Check** — Note convergences, contradictions, and how conflicts were resolved.
- **🕳️ Gaps & Unknowns** — Record missing verification areas or pending research.
- **📊 Integrity Summary** — Include risk and confidence distribution tables (Primary/Secondary/Forum/Soft-blocked).
- **🗂️ Appendix A – Artifacts** — Attach screenshot references with timestamps, SHA-256 hash, and source IDs.
- **🔍 Appendix B – Search Log** — Document engines, queries, and discarded sources with reasons.
- **🧮 Global Confidence** — Present weighted mean of claim confidence scores (criticality-weighted if defined).
- **🚨 Alerts** — Highlight claims where `Average Risk ≥ Medium` or `Confidence < 70`, with corrective guidance.

---

### **Guardrails**

- Do **not** include this prompt in the output.
- Maintain deterministic structure and heading order for Obsidian ingestion.
- Exclude all unverified or inferred statements.
- Each entry must be fully grounded in verifiable citations.

---

Here is my template:

# 🧭 Overview
> Scope, key question, date range, and summary of intent.

---

# 📑 Findings
- Verified Fact 1 … [S1][S2]  
- Verified Fact 2 … [S3]

---

# 🧩 Evidence Table
| Claim | Provenance ID | Source ID(s) | Quoted Evidence | Location (URL + page/line or anchor) | Risk Rating | Validation Notes | Decision Rule | Archive |
|:--|:--|:--|:--|:--|:--|:--|:--|:--|
| … | … | … | … | … | Low/Med/High | … | … | [archive] |

---

# 🧠 Source Annotations
### [S1] 
- Type: Primary | Secondary | Forum  
- Risk Rating: Low | Medium | High (+ rationale)  
- Summary: …  
- Credibility: …  
- Comment: …  
- Authorship Score (Human vs Bot): 0.0–1.0 (+ rationale)

*(Repeat for each source ID.)*

---

# ⚖️ Consistency Check
> Summarize convergences, contradictions, and resolutions.

---

# 🕳️ Gaps & Unknowns
> Identify missing evidence, unverified claims, or required follow-ups.

---

# 📊 Integrity Summary
| Metric | Primary % | Secondary % | Forum % | Soft-blocked % | Avg Risk | Avg Claim Confidence | Global Confidence |
|:--|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| Values |   |   |   |   |   |   |   |

| Class | Avg Risk | Avg Confidence |
|:--|:--:|:--:|
| Primary |   |   |
| Secondary |   |   |
| Forum |   |   |
| Soft-blocked |   |   |

---

# 🗂️ Appendix A – Artifacts
> Screenshots or snapshots of referenced pages.  
> Include caption, timestamp, SHA-256 hash, and source ID.

---

# 🔍 Appendix B – Search Log
> Document engines, queries, visited/discarded links, and reasoning for inclusion/exclusion.

---

# 🧮 Global Confidence
> Weighted mean of per-claim scores (criticality-weighted if defined).

---

# 🚨 Alerts
> List claims triggering alerts (Average Risk ≥ Medium or Confidence < 70).  
> Provide notes or next steps for corrective validation.


---

Acknowledge this instruction and wait for further input!