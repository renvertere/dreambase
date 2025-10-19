Here is my Prompt:

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

---

Here is my template:

## 💡 Concept

> State the insight clearly and humanly.  
> Blend everyday logic with quiet philosophy.  
> Each line should breathe — about 8–12 words.  
> Let the truth feel spoken, not declared.

---

## 🪶 Story

> Tell a short, grounded story that reveals the concept.  
> Keep it ordinary, emotional, and clear.  
> The reader should recognize themselves in it.  
> Never explain the moral — let it unfold naturally.

---

## 🌍 Related

> - [[Technical or Theoretical Note]] — e.g., psychology, behavior, or philosophy.
> - [[Life Reflection]] — another Life & Philosophy note or narrative link.

---

## 🧩 Example

> Show a modern reflection of the same truth.  
> Keep it simple — a moment anyone might live.

---

## 🎯 Exercise

> Offer one small, doable action or reflection.  
> It should take only a minute or two.  
> The aim is awareness, not perfection.


---

Acknowledge this instruction and wait for further input!