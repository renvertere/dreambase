Here is my Prompt:

I am going to provide you with an error message, failure log, or help request.
Please parse it into the above Troubleshooting template.

# Guidelines

1) **Do NOT include the document properties (the YAML block between `---` and `---`).** Obsidian generates this automatically.
2) Capture the **problem statement** that user provided in the prompt
3) Capture the **goal** the user wanted to achieve.
4) Write the **problem twice**: once in technical terms, once in layman’s language.
5) Use the **system load/highway analogy as a fallback** when **no clearer analogy fits**.
6) Suggest **areas of investigation** (potential causes).
7) Provide a **step-by-step practical solution**.
8) Add a verification section showing how to confirm resolution.
9) Link to related notes if applicable.

## **Output**
- Now, using the above rules, produce the troubleshooting guide.

## Guardrails
- Do **not** include this prompt in the output.

---

Here is my template:

# 🛠️ <% tp.file.title %>

## 🎯 Goal
> What was the user trying to do?  
> e.g., "Start a virtual machine", "Connect to a database", "Run a command".

---

## ⚠️ Problem (Technical)
> Describe the issue in **precise, technical terms** using the error message or observed failure.  
> e.g., "Permission denied when accessing `/home/user/.local/share/locale`."

---

## 🤔 Problem (Layman)
> Translate the technical issue into **simple language**.  
> e.g., "The program tried to open a folder but didn’t have the right key, so it was stopped."

---

## 🌍 Real-World Analogy
Think of the system like a **highway**:  
- The **CPU** is the number of lanes.  
- The **processes** are cars driving.  
- A bottleneck (like permissions, missing files, or misconfiguration) is a **toll booth blocking cars**.  
When the booth is blocked, no matter how many lanes exist, traffic backs up and nothing moves forward.

---

## 🔍 Areas to Investigate
- Misconfiguration in setup or environment  
- Permissions or ownership problems  
- Missing dependencies or paths  
- Resource or network limitations  

---

## 🛠️ Practical Solution
Step-by-step troubleshooting actions:

1. **Step 1** — Confirm the error context.  
   ```bash
   # Example: reproduce the issue or check logs
   ```

2. **Step 2** — Investigate the suspected area.
```bash
# Example: verify file permissions, process status, or configs
```

3. **Step 3** — Apply the fix.
```bash
# Example: adjust permissions, reinstall package, restart service
```

4. **Step 4** — Retest the original goal.

## ✅ Verification

> Define how to confirm the issue is resolved.  
> e.g., "Command executes successfully and produces the expected output."

## 🔗 Related Notes

- [[Similar Troubleshooting Case]]
- [[How To: Related Workflow]]
- [[Atom: Related Concept]]

---

Acknowledge this instruction and wait for further input!