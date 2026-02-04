# Video → Atom Learning Path + Atom Normalization Prompt

I am going to provide you with a **raw video transcript**.

Your task is to transform the transcript into a **validated Atom Index** suitable for direct use with this project’s `atom_template`.

Atoms are **atomic units of knowledge** that:
- contain exactly **one Core Idea**
- can stand alone as individual Atom notes
- collectively form a **learning path** that takes a learner from **zero knowledge**
  to the **proficiency level demonstrated by the video**

This process is **source-grounded**.  
The transcript is the **only authoritative input**.

---

## 🔒 Transcript Presence Gate (Non-Negotiable)

If the user has **not provided a raw video transcript**, you MUST do exactly ONE thing:

➡️ Ask the user to provide the transcript and STOP.

You must NOT:
- Ask for target proficiency
- Infer a topic
- Infer scope
- Infer atoms
- Use prior knowledge
- Produce any part of the template

---

## 🔒 Target Proficiency Gate (Non-Negotiable)

If the transcript **is present** but the **target proficiency level taught by the video** is NOT explicitly stated, you MUST do exactly ONE thing:

➡️ Ask for the target proficiency (Step 1) and STOP.

You must NOT:
- Summarize the transcript
- Infer atoms
- Infer scope
- Default or guess proficiency

---

## 🚫 No-Defaulting Rule

- Do NOT assume proficiency  
- Do NOT default to Beginner, Intermediate, Advanced, or Mixed  
- Target proficiency must be explicitly provided by the user

---

## 🔁 Interaction Contract (Three-State)

There are **only three valid interaction states**:

1) **Transcript missing**  
   → Ask for transcript ONLY and stop.

2) **Transcript present, target proficiency missing**  
   → Ask for target proficiency ONLY and stop.

3) **Transcript + target proficiency present**  
   → Execute Phase 1 and Phase 2 and output the filled-in template ONLY.

No other outputs are permitted.

---

## Step 1 — Target Proficiency Declaration (Required)

Ask **ONLY** this question:

> **What proficiency level does this video aim to teach?**  
> Reply with one of: **Beginner / Intermediate / Advanced**

(Optional after proficiency is given: intended audience or learning goal.)

Do NOT proceed until answered.

---

## Step 2 — Phase 1: Learning Path Extraction

Using the transcript **as source material**, construct a **minimal, prerequisite-complete learning path** that would take a learner from **zero knowledge** to the **target proficiency demonstrated by the video**.

### Learning Path Invariant

> Each step must unlock a **new learner capability** required to reach the target proficiency.

### Phase 1 Rules

1) Think in **capabilities gained**, not commands, flags, or syntax.
2) Exclude narration, anecdotes, branding, calls to action, and episode structure.
3) Exclude taxonomy labels (e.g., DDL, DML) at this stage.
4) Include missing prerequisites as `[Inferred]`.
5) This phase MAY contain composite steps.
6) Do NOT attempt to satisfy atom_template constraints yet.

---

## Step 3 — Phase 2: Atom Normalization (Mandatory)

You MUST convert the Phase 1 learning path into **true Atoms** that are fully compatible with the project’s `atom_template`.

### Atom Definition (Project-Strict)

An Atom MUST:
- Contain **exactly one Core Idea**
- Be suitable for a single Atom note
- Support its own explanation, example, use cases, and exercise
- Be promptable as:  
  “Generate an Atom for: <concept>”

---

### Phase 2 Normalization Rules

- **Single-Core-Idea Rule**  
  Split any concept that bundles multiple ideas.

- **Capability Rule (Mandatory)**  
  An Atom must describe **one learner capability**, not a category, label, or explanation.

- **No Taxonomy Atoms**  
  Do NOT emit atoms that are primarily classifications or terminology sets.

- **No Convenience Atoms**  
  CLI shortcuts, helpers, flags, and meta-commands must be merged or omitted.

- **Prerequisite Completeness**  
  If an Atom depends on another Atom, ensure the dependency exists or mark it `[Inferred]`.

---

## 🎯 Target Atom Count (Hard Cap)

After normalization:

- **Beginner:** 12–20 Atoms  
- **Intermediate:** 18–30 Atoms  
- **Advanced:** 25–45 Atoms  

If exceeded, you MUST merge or remove atoms until within range.

---

## ✅ Final Acceptance Tests (ALL must pass)

For every Atom:

- One Core Idea only
- Represents a learner capability
- Standalone (no hidden prerequisites)
- Directly derivable from the transcript (or marked `[Inferred]`)
- Fits cleanly into the atom_template
- Required to reach the target proficiency

Repeat Phase 2 until all tests pass.

---

## 📤 Output Rules

- Output **ONLY** the filled-in template below.
- Do NOT include this prompt, reasoning, analysis, or phase labels.
- Do NOT number or timestamp atoms.

---

# <% tp.file.title %>

## 🧭 Topic Scope
> Scope inferred strictly from the transcript and the target proficiency level.
> Example: “PostgreSQL fundamentals required to build and query a simple relational database.”

---

## 🎯 Target Proficiency (as taught by the video)
> Beginner | Intermediate | Advanced

---

## 🧠 Layman Transcript Summary
> Plain-language overview of what the video teaches.
> This section is for orientation only and MUST NOT influence Atom granularity.

---

## 🧩 Atom Index (Normalized Atoms)
- Atom A (single Core Idea)
- Atom B
- Atom C
- [Inferred] Atom D
- [Unclear] Atom E