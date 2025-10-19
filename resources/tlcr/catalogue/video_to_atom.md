Here is my Prompt:

# Video Transcript Prompt

I am going to provide you with a **raw video transcript**. 
Please extract an **Atom Index Table** (timestamped concepts). 

# **Guidelines** 

1) **Do NOT include the document properties (the YAML block between `---` and `---`).** Obsidian generates this automatically.
2) Assign IDs (K01, K02, …) with topic prefix (K for Kubernetes, D for Docker, etc.).
3) Keep timestamps in **[HH:MM:SS]** format.  
4) Each line should be: `[timestamp] ID — Concept/Topic`.  
5) Do not expand into full Atom notes here — only index them. 
6) If unclear, mark as `[Unclear]` with timestamp.  

# **Output** 
- Deliver only the **Atom Index Table** using the structure above.

## Guardrails
- Do **not** include this prompt in the output.

---

Here is my template:


# <% tp.file.title %>

> Parse the transcript into an **Atom Index Table** for later expansion into full Atoms.

---

## 🗂️ Atom Index Table
- [HH:MM:SS] K01 — Concept 1 (e.g., Kubernetes Intro)
- [HH:MM:SS] K02 — Concept 2 (e.g., K8s Setup)
- [HH:MM:SS] K03 — Concept 3 (e.g., Pods & Services)
- [HH:MM:SS] K0N — Concept ...N  

---

Acknowledge this instruction and wait for further input!