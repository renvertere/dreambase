# Video Transcript Prompt

You are to **convert an educational transcript with time markers** into a **plain-text Content Headings Index (Video to Atom index)**. Follow these strict guardrails:

# **Guidelines** 

### Structural Rules
1) **Do NOT include the document properties (the YAML block between `---` and `---`).** Obsidian generates this automatically.
2. Extract all **unique top-level and secondary-level topics** (maximum hierarchy depth: **2**). Anything beyond level 2 is treated as a **new top-level topic**.
3. Include **only the first occurrence** of each topic.
4. Maintain **strict chronological order** throughout.
5. Ignore speakers, summaries, or filler content.
6. For segments referencing multiple topics, **unpack** each into its own index line.

### Timestamp Rules

1. Use **exact transcript timestamps** in the format `[HH:MM:SS]`.
2. If missing, insert `[UNKNOWN]`.
3. When unpacking multiple topics from one segment, **reuse the same timestamp**.

### ID + Topic Rules

1. Each topic entry must include a unique **ID** composed of:
    - **Prefix** inferred from topic content (e.g., K = Kubernetes, D = Docker, A = Ansible, etc.).
    - **Sequential two-digit number** per prefix (e.g., K01, K02, D01).
2. Numbering resets **per prefix**.
3. Restart hierarchical numbering under each new top-level heading.
4. Do not expand, summarize, or add interpretation.

### Output Format

Each line must follow this exact structure:
```plaintext
[HH:MM:SS] ID — Concept/Topic
```

##### Examples
```plaintext
[00:03:12] K01 — Kubernetes Pod Scheduling
[00:04:21] D01 — Docker Networking Basics
[00:05:33] K02 — ReplicaSets and Scaling
[UNKNOWN] A01 — Ansible Playbook Overview
```

### Formatting Rules
- Plain text only — **no Markdown tables**, bolding, or styling.
- Maintain spacing and punctuation exactly as shown.
- Ensure consistent ID prefixing and two-digit padding.
- Do not include any metadata or commentary in the output.

### Purpose
Produce a **chronologically ordered, prefix-tagged topical index** that enables quick research and cross-referencing of each concept.
# **Output** 
- Deliver only the **Atom Index Table** using the structure above.

## Guardrails
- Do **not** include this prompt in the output.