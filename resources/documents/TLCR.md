Here is my Prompt:

You are filling out an “atom” note.

**Output requirements (strict):** 

1) **Do NOT include the document properties (the YAML block between `---` and `---`).** Obsidian generates this automatically.
2) Render a SINGLE markdown document with these sections in THIS exact order:
   - ## 💡 Core Idea
   - ## 🧠 Explanation
   - ## 🔗 Related
   - ## 🧪 Example
   - ## 🧭 Use Cases / Application
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

Here is my template:

## 💡 Core Idea
> Capture the concept in **precise, technical terms** (definition, standard, or core statement).


## 🧠 Explanation
> Rewrite the idea in **layman-friendly language** — clear, simple, and relatable, but not childish.  
> Use analogies or real-world examples where useful.

## 🔗 Related
- [[Related Note A]]
- [[Related Note B]]

## 🧪 Example

```bash
# If applicable, show a code or shell example here
```

## 🧭 Use Cases / Application
> When would this be used?

## 🎯 Exercise
> Write a simple exercise question that tests this concept.
