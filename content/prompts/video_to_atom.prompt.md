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