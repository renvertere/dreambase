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
5) Do NOT wrap the entire document in a code block.
   - Fenced code blocks are allowed ONLY for non-LaTeX examples (e.g., sql, yaml, python, bash).
6) If a section would be empty, include a brief placeholder line starting with “>”.
7) Keep markdown valid and unbroken.

Related section requirements (strict):
8) The “## 🔗 Related” section MUST follow the Related Proximity Rule.
   - Default to L0 (structural/definitional neighbors).
   - Do NOT include L2 (constraints/guarantees) unless explicitly requested.
   - Do NOT skip tiers.
   - Links MUST represent the most likely next questions a user would ask.

Example section requirements (strict):
9) The “## 🧪 Example” section MUST contain exactly one example.
   - The example format MUST adapt to the atom’s subject matter.
   - If a formal language is appropriate, use the correct representation:
     - **LaTeX (physics/mathematics):** MUST use MathJax delimiters (`$$ … $$` for display math, `$ … $` for inline math).
     - **SQL, YAML, Python, Bash, etc.:** Use fenced code blocks with the correct language tag.
   - LaTeX examples MUST NOT be placed inside fenced code blocks.
   - LaTeX examples MUST contain only mathematical expressions (no narrative text or `\text{}` prose).
   - If no formal language is appropriate, use a concise plain-text or pseudo-example.
   - Do NOT include multiple example types.
   - Do NOT explain the example outside the example itself.

Example formalism priority (strict):
10) If the concept is fundamentally defined by a formal expression (e.g., equations, laws, theorems),
    the example MUST use that formalism as the primary example.
    - For physics and mathematics concepts, LaTeX display math (`$$ … $$`) is preferred.
    - Narrative or numerical word problems MUST NOT replace the primary formal expression.

Markdown style constraints (strict):
11) Do NOT use blockquotes unless explicitly shown in the template.
    - Use plain paragraphs and lists only.

Sources requirements (strict):
12) The “## 🧾 Sources” section MUST list external references that were used to produce the content.
    - Sources MUST be web sources or external documents (not the user’s prompt text).
    - Include at least 2 sources when possible; if only 1 credible source exists, include 1 and state “Only one suitable source found”.
    - Each source entry MUST include: Title, Publisher/Site, and URL.
13) If you cannot access external sources for any reason, write in “## 🧾 Sources”:
    > No external sources were consulted.

Output:
- Now, using the above rules, produce the atom note.

Guardrails:
- Do not include this prompt in the output.
