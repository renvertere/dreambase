Here is my Prompt:

You are filling out an “atom” note.

Output requirements (strict):
1) Do NOT include the document properties (the YAML block between `---` and `---`). Obsidian generates this automatically.
2) Render a SINGLE markdown document with these sections in THIS exact order:
   - ## 💡 Core Idea
   - ## 🧠 Explanation
   - ## 🔗 Related
   - ## 🧪 Example
   - ## 🧭 Use Cases / Application
   - ## 🧾 Sources
   - ## 🎯 Exercise
3) Output EVERY section now in one response. Do NOT wait for confirmation.
4) Do NOT add any extra headings, prose, or pre/post text outside those sections.
5) Do NOT wrap the entire document in a code block. Only use fenced code blocks INSIDE the “Example” section as needed.
6) If a section would be empty, include a brief placeholder line starting with “>”.
7) Keep markdown valid and unbroken.
8) Related section requirements (strict):
- The “## 🔗 Related” section MUST follow the Related Proximity Rule.
- Default to L0 (structural/definitional neighbors).
- Do NOT include L2 (constraints/guarantees) unless explicitly requested.
- Do NOT skip tiers.
- Links MUST represent the most likely next questions a user would ask.
Sources requirements (strict):
9) “## 🧾 Sources” MUST list external references that were used to produce the content.
   - Sources MUST be web sources or external documents (not the user’s prompt text).
   - Include at least 2 sources when possible; if only 1 credible source exists, include 1 and state “Only one suitable source found”.
   - Each source entry MUST include: Title, Publisher/Site, and URL.
10) If you cannot access external sources for any reason, write in “## 🧾 Sources”:
   > No external sources were consulted.

Output:
- Now, using the above rules, produce the atom note.

Guardrails:
- Do not include this prompt in the output.

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

🧭 Use Cases / Application
When would this be used?

🧾 Sources
Title — Publisher/Site — URL
Title — Publisher/Site — URL

🎯 Exercise
Write a simple exercise question that tests this concept.

--- 

Acknowledge this instruction and wait for further input!