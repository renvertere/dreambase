# 🌌 DreamBase LLM Project Instructions

This project is **template-isolated**.  
All responses, notes, and generated content within this vault MUST adhere to the **templates** and **prompts** provided with it.  
Other project memories, global defaults, or templates from different projects must **NOT** be applied.

---

## 📐 Rules
1. **Template Scope** → Use ONLY the provided templates (`*_template.md`).  
2. **Prompt Scope** → Use ONLY the provided prompts (`*.prompt.md`).  
3. **Isolation** → Do not reference or apply templates from other projects or global memory.  
4. **Consistency** → Always follow the naming conventions, front-matter, and structure defined in the templates.  
5. **Deliverables** → Output new content in the correct category (atoms, exercises, journal logs, how-to, transcripts, etc.).  
6. **Indexing** → Reference or update the local `dashboard_template.md` when new content is created.  

---

## 📦 Access Modes

Templates and prompts can be accessed in **two ways**:

1. **Vault Mode** — Templates and prompts are stored in the Obsidian vault:  
   - Templates → `content/templates/` (e.g., `atom_template.md`)  
   - Prompts → `content/prompts/` (e.g., `atom.prompt.md`)  

2. **Direct Upload Mode** — Templates and prompts are uploaded directly into the project folder and referenced by **file name only**.  
   - Example: `atom_template.md` + `atom.prompt.md`  
   - This mode applies when the LLM does not have local vault access.  

---

## 🎛️ Response Convention
- **Explain** → `atom_template.md` + `atom.prompt.md`  
- **Guide/How-To** → `how_to_template.md` + `how_to.prompt.md`  
- **Practice** → `exercise_q_template.md` + `exercise_q.prompt.md`  
- **Reflect** → `journal_logs_template.md` + `journal_logs.prompt.md`  
- **Overview** → `dashboard_template.md` or `course_readme_template.md` (with prompts)  
- **Transcript** → `meeting_transcript_template.md` or `video_transcript_template.md` (with prompts)  

---

---

## 📋 Instruction to LLM
When generating content inside this project:
- Use ONLY the templates (`*_template.md`).  
- Use ONLY the prompts (`*.prompt.md`) for parsing and formatting.  
- Follow the vault’s conventions (naming, placement).  
- Apply the **Response Convention** mappings above.  
- Ignore unrelated global memories.  
- Format output strictly according to the uploaded templates.  

---

## ⚙️ YAML Control Layer

```yaml
project:
  name: <vault-name>  # replace with the actual vault/project name
  isolation: true
  rules:
    - Use ONLY the provided templates (*_template.md).
    - Use ONLY the provided prompts (*.prompt.md).
    - Do not reference or apply templates from other projects or global memory.
    - Follow the naming conventions, front-matter, and structure defined in the templates.
    - Output new content in the correct category (atoms, exercises, journal logs, how-to, transcripts).
    - Reference or update dashboard_template.md when adding content.

response_convention:
  Explain:
    - atom_template.md
  Explanation:
    - atom_template.md

  Guide/How-To:
    - how_to_template.md
  Tutorial:
    - how_to_template.md
  Walkthrough:
    - how_to_template.md

  Practice:
    - exercise_q_template.md
  Exercises:
    - exercise_q_template.md
  Task:
    - exercise_q_template.md

  Reflect:
    - journal_logs_template.md
  Journal:
    - journal_logs_template.md
  Log:
    - journal_logs_template.md

  Transcript:
    - meeting_transcript_template.md
    - video_transcript_template.md
  Meeting:
    - meeting_transcript_template.md
  Video:
    - video_transcript_template.md

  Overview:
    - dashboard_template.md
    - course_readme_template.md
  Index:
    - dashboard_template.md
  Summary:
    - course_readme_template.md
