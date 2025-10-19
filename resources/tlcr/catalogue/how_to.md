Here is my Prompt:

I am going to provide you with a question on how to achieve an objective.
Please parse the information into the How To template above.

**OUTPUT REQUIREMENTS (STRICT):**

1) 1) **Do NOT include the document properties (the YAML block between `---` and `---`).** Obsidian generates this automatically.
2) Render a SINGLE markdown document with these sections in THIS exact order:
    - ## 🧾 Summary
    - ## 🧰 Prerequisites
    - ## 🧑‍💻 Steps
    - ## ✅ Verification
    - ## 🔗 Related Notes

3) Output EVERY section now in one response. Do NOT wait for confirmation.
4) Do NOT add any extra headings, prose, or pre/post text outside those sections.
5) Do NOT wrap the entire document in a code block. Only use fenced code blocks INSIDE the Steps” section as needed.
6) If a section would be empty, include a brief placeholder line starting with “>”.
7) Keep markdown valid and unbroken.

## **Output**
- Now, using the above rules, produce the how to guide.

## Guardrails
- Do **not** include this prompt in the output.

---

Here is my template:


## 🧾 Summary
> Brief description of what this guide helps you accomplish.

## 🧰 Prerequisites
- Requirement 1
- Requirement 2
- Accounts / permissions / tools

## 🧑‍💻 Steps

1. **Steps ** — Describe the action  
   ```sql
   # Command or configuration here
```

## ✅ Verification

> How do you know it's working?
> Include test commands or outputs.


## 🔗 Related Notes
[[Concept: Target System]]
[[README: Related Course]]
[[Troubleshooting Guide (if any)]]

---

Acknowledge this instruction and wait for further input!