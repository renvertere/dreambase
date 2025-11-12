---
id: <% tp.date.now("YYYYMMDDHHmm") %>
title: <% tp.file.title %>
type: atom
tags:
  - note
  - concept
  - web-report
source:
aliases:
  - N/A
related:
created: <% tp.date.now("YYYY-MM-DD") %>
---
# 🧾 <% tp.file.title %>
> Investigation entry generated via web_report protocol.

# 🧭 Overview
> Scope, key question, date range, and summary of intent. 
> Clearly define what the investigation covers and what outcome or verdict is expected.

---

# 📑 Findings

> Each fact includes **Confidence (0–100%)** — how confident _we are_ that it’s correct — and **Risk Level** — how likely it could mislead.

- Verified Fact 1 … [S1][S2]  [S2]
- Verified Fact 2 … [S3]

---

# 🧩 Evidence Table

> **Legend:**
> 	- **Risk Level:** chance this claim or source is unreliable (Low / Medium / High)
> 	- **Confidence:** how confident we are that the claim is correct (0–100%)
> 	- **Importance:** how much this claim matters to the report’s conclusion (1–5)
> 	- **Decision Rule:** note used to accept or reject evidence



| Claim | Provenance ID | Source ID(s) | Quoted Evidence | Location (URL + page/line or anchor) | Risk Rating | Validation Notes | Decision Rule | Archive |
|:--|:--|:--|:--|:--|:--|:--|:--|:--|
| … | … | … | … | … | Low/Med/High | … | … | [archive] |

---

# 🧠 Source Annotations

> **Legend:**
> 	- **Authorship Score (0.0–1.0):** likelihood of being human-written (1.0 = confirmed human)
> 	- **Risk Rating:** how likely the source is biased or unreliable
> 	- **Credibility:** qualitative measure based on transparency and reputation

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
> Summarize convergences, contradictions, and how conflicts were resolved.

---

# 🕳️ Gaps & Unknowns
> Identify missing evidence, unverified claims, or areas requiring follow-up research.

---

# 📊 Integrity Summary

> Legend:
> 	- Risk = how trustworthy each group of sources is
> 	- Confidence = how sure we are about their claims
> 	- Global Confidence = overall reliability after balancing confidence and importance

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
> Document search engines, queries, visited or discarded links, and why each was included or excluded.

---

# 🧮 Global Confidence
> Legend:
> 	Global Confidence = combined score showing how solid the whole report is, after giving more influence to more important claims.
> 	(Plain formula: higher-importance facts count more toward the overall confidence.)
> 	“This score summarizes the entire investigation’s reliability; it’s not mathematical precision but an evidence-weighted confidence statement.”



---

# 🚨 Alerts
>List claims triggering alerts (Average Risk ≥ Medium or Confidence < 70).
>Provide brief notes or next steps for corrective validation.