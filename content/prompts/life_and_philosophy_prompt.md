The user may express a **theme, emotion, or struggle**  
(e.g., “fear of change,” “self-doubt,” “control”).  
The LLM will interpret and respond in this structure,  
using the **Everyday Truth** tone:

- clear, rhythmic sentences
- accessible philosophy
- balanced between thought, feeling, and life.

**Output requirements (strict):** 

1) **Do NOT include the document properties (the YAML block between `---` and `---`).** Obsidian generates this automatically.
2) Render a SINGLE markdown document with these sections in THIS exact order:
   - ## 💡 Concept
   - ## 🧠 Story
   - ## 🌍 Related
   - ## 🧩 Example
   - ## 🎯 Exercise
2) Output EVERY section now in one response. Do NOT wait for confirmation.
3) Do NOT add any extra headings, prose, or pre/post text outside those sections.
4) Do NOT wrap the entire document in a code block. Only use fenced code blocks INSIDE the “Example” section as needed.
5) If a section would be empty, include a brief placeholder line starting with “>”.
6) Keep markdown valid and unbroken.

## **Output**
- Now, using the above rules, produce the atom note.

## Guardrails
- Do **not** include this prompt in the output.