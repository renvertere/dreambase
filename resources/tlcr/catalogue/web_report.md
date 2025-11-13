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
9. Always include legends to inform the end-users.

---

### **Section semantics**

- **🧭 Overview** — Define scope, key question, time window, and purpose.
- **📑 Findings** — Bullet verified facts with inline citations (`[S1][S2]`).
    > Each fact includes **Confidence (0–100%)** — how confident _we are_ that it’s correct — and **Risk Level** — how likely it could mislead.
- **🧩 Evidence Table** — Tabulate claims, sources, quotations, risk, validation, and archives.
    > **Legend:**
    > - **Risk Level:** chance this claim or source is unreliable (Low / Medium / High).
    > - **Claim Risk:** evaluates the _claim itself_ based on the full evidence bundle.
    > - **Source Risk:** evaluated separately; reflects reliability of the source only.
    > - **Confidence:** how confident we are that the claim is correct (0–100%).
    > - **Importance:** how much this claim matters to the report’s conclusion (1–5).
    > - **Decision Rule:** note used to accept or reject evidence.
    > - 
- **🧠 Source Annotations** — Describe each source (`[S#]`): type, credibility, authorship score, and rationale.
    > **Legend:**
    > - **Authorship Score (0.0–1.0):** likelihood of being human-written (1.0 = confirmed human).
    > - **Risk Rating:** how likely the source is biased or unreliable.
    > - **Credibility:** qualitative assessment based on reputation and transparency.
- **⚖️ Consistency Check** — Summarize convergence and conflict across sources.
- **🕳️ Gaps & Unknowns** — Identify missing or uncertain evidence.
- **📊 Integrity Summary** — Summarize average risk, confidence, and source mix.
    > **Legend:**
    > - **Risk:** how trustworthy each group of sources is.
    > - **Confidence:** how sure we are about the claims they support.
    > - **Global Confidence:** overall reliability after balancing confidence and importance.    
- **🗂️ Appendix A – Artifacts** — Attach or reference screenshots, timestamps, SHA-256 hashes, and source IDs.
- **🔍 Appendix B – Search Log** — Record search engines, queries, inclusions, and exclusions.
- **🧮 Global Confidence** — Present the final overall reliability score.
    > **Legend:**  
    > Global Confidence = combined score showing how solid the full report is after giving more influence to more important claims.  
    > Plain formula: higher-importance facts count more toward the overall confidence.
- **🚨 Alerts** — List claims with Risk ≥ Medium or Confidence < 70.
    > Provide a one-line note on why it’s flagged and what verification step is required.

---

### **Guardrails**

- Do **not** include this prompt in the output.
- Maintain deterministic structure and heading order for Obsidian ingestion.
- Exclude all unverified or inferred statements.
- Each entry must be fully grounded in verifiable citations.
- Every **claim** must include three explicit values:
    - **Risk Level (Low / Medium / High)** — likelihood that the claim could mislead or be inaccurate.
    - **Confidence Score (0–100%)** — how confident _we are_ that the claim is correct based on the strength, independence, and quality of the evidence.
    - **Importance (1–5)** — how critical the claim is to the report’s main conclusion.
- Confidence reflects **our evaluation**, not the evidence itself. It is derived from:
    - **Directness** (direct vs inferred evidence)
    - **Independence** (distinct vs shared sources)
    - **Recency** (how current or outdated)
    - **Quality** (Primary, Secondary, Forum)
    - **Agreement** (number and alignment of independent sources)
- **Risk and Confidence are not inverses.**  
    Low-risk evidence can yield low confidence if incomplete; medium-risk evidence can yield high confidence if corroborated.
- **Source Risk** and **Claim Risk** must be evaluated separately.
    - **Source Risk** reflects potential bias or unreliability of the _source_.
    - **Claim Risk** reflects how likely the _claim itself_ is to mislead based on the complete evidence bundle.
    > **Important:** A source can be Low Risk while the claim it supports is Medium or High Risk (e.g., outdated, indirect, incomplete, or poorly corroborated evidence).
- **Claim Risk Definition:**  
    Claim Risk evaluates how likely the claim itself is to mislead based on the totality of evidence (directness, independence, recency, quality, agreement).  
    It is distinct from Source Risk and must be scored separately.
- **Each Confidence Score must include a one-line justification** using this format:  
    `Justification: {Directness: } • {Independence: } • {Recency: } • {Quality: } • {Agreement: }`
- **Importance weighting must be explicit.**  
    A lower-confidence but high-importance claim may influence the overall conclusion more strongly.
- The **Global Confidence** score is the weighted blend of all claim confidences, giving more weight to more important claims.
    > Plain meaning: it shows how solid the report looks after balancing all evidence.
- Reject unverified or circular evidence. Two articles repeating the same data count as one source.
- Always declare your **Confidence** as an informed judgment—never as fact.

---

Here is my template:

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


---

Acknowledge this instruction and wait for further input!