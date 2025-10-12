# 🌌 DreamBase LLM Project Instructions

## 🧭 Project Topic Declaration Layer

### 🧑 For the User

At the beginning of every project folder, explicitly declare the **topic** and its **scope**.  
This declaration ensures both you and the LLM remain strictly aligned to the same subject and prevents drift or hallucination.


```yaml
project_topic:
  name: <short-title>
  description: <one-line summary>
  scope:
    include:
      - ...
    exclude:
      - ...
```

---

## 🤖 For the LLM

When responding:
1. **Anchor** all reasoning, analogies, and examples within the declared `project_topic.name`.
2. **Reject or redirect** any request that introduces content outside the `project_topic.scope`.
3. Treat `project_topic.description` as the **semantic boundary** for generation and retrieval.
4. **Do not import** memory, style, or templates from other projects unless explicitly listed under `scope.include`.
5. Maintain full **topic isolation** and **template discipline** at all times.

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
- **Transcript** → `meeting_transcript_template.md` or `video_to_atom_template.md` (with prompts)  

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

  Fix/Assist/Troublshooting:
    - troubleshooting_template.md
  Fix:
    - troubleshooting_template.md
  Troublshooting:
    - troubleshooting_template.md
  Troublshoot:
    - troubleshooting_template.md

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
    - video_to_atom_template.md
  Meeting:
    - meeting_transcript_template.md
  Video:
    - video_to_atom_template.md

  Overview:
    - dashboard_template.md
    - course_readme_template.md
  Index:
    - dashboard_template.md
  Summary:
    - course_readme_template.md
