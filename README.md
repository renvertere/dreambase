# # 🌌 DreamBase

**Dreambase** is a collection of standardized **Markdown templates** and **prompts** for structured note-taking and learning — designed for use in **Obsidian** or any general Markdown workflow.  
The goal is to enforce **consistency**, **clarity**, and **automation-friendly formatting** across diverse knowledge capture contexts — whether you’re **drawing in crayon**, studying **nuclear physics**, or building **sophisticated knowledge-base SOPs**.

Dreambase is developed and maintained by the team at the charity **DreamScape3^ VL (Virtual Learning)**.

---

## ⚡ TL;DR — Quick Start for DreamBase Users

To simply get started, see the provided [TLDR.md](TLDR.md)

**Goal**: Create a clean, self-contained knowledge vaults that uses LLMs (ChatGPT, Ollama, etc.) to generate perfectly formatted notes using the DreamBase templates.


## 🧰 Prerequisites
- [Obsidian](https://obsidian.md/)
- Obsidian Plugins:
  - [Templater](https://obsidian.md/plugins?id=templater-obsidian)
  - [Dataview](https://obsidian.md/plugins?id=dataview)


## 📑 Templates And Prompts

For a full list of templates and their associated prompts, please see [TEMPLATE_AND_PROMPTS](./TEMPLATE_AND_PROMPTS.md)

---

## 📜 LLM_PROJECT_INSTRUCTIONS.md

[LLM INSTRUCTIONS] details the project instructions for your choice LLM(ChatGPT, Gemma, etc) when working inside of project folders.  
It ensures template isolation, consistent formatting, and correct use of prompts.

### ⚠️ Important
Do **not** paste the explanatory text from `LLM_PROJECT_INSTRUCTIONS.md` into ChatGPT — it’s for humans only.  
ChatGPT only needs the **rules + mappings** see [TLDR.md](TLDR.md).

---
## 🔗 Suggested Workflow
1. **Atom** → Capture atomic concepts.
2. **Exercise Q/A** → Practice comprehension.
3. **How To** → Record repeatable workflows.
4. **Troubleshooting** → Diagnose and resolve unexpected errors or failures, linking back to related Atoms and How-To notes.
5. **Meeting/Video Transcripts** → Extract structured knowledge from real-time content.
6. **Course Readme** → Track structured learning journeys.
7. **Dashboard** → Central navigation hub. 

---

## 🔢 Numbering Conventions
- **Exercises**:  
  - Questions → `exercise_Q01.md`, `exercise_Q02.md`  
  - Answers → `exercise_A01.md`, `exercise_A02.md`  
- **Atoms**: One concept per note, linked to exercises.  
- **Projects**: Incremental numbering for grouped learning paths (e.g., `A01 – What is Ansible`). 


---

# 📦 Usage

## ⚙️ Helper Script: Create a New Obsidian Vault

You can use the following shell alias function to quickly spin up a new Obsidian vault with the correct base folder structure and templates.

```bash
function makeobsvault() {
  if [ -z "$1" ] || [ -z "$2" ]; then
    echo "Usage: makeobsvault <vault-name> <dreambase-repo-dir>"
    echo "Example: makeobsvault MyVault ~/path/to/Dreambase"
    return 1
  fi

  VAULT_NAME="$1"
  DB_REPO="$2"

  echo "📁 Creating Obsidian Vault: $VAULT_NAME"
  mkdir -p "$VAULT_NAME"/{content,resources/img,src}
  mkdir -p "$VAULT_NAME"/content/{certificates,comments,exercises/{questions,answers},knowledgebase/{atoms,how_to,journal_logs,transcripts/{meetings,video_tutorials}},prompts,templates}

  echo "📄 Copying templates & prompts..."
  cp -R "$DB_REPO/content/templates"/* "$VAULT_NAME/content/templates/"
  cp -R "$DB_REPO/content/prompts"/*   "$VAULT_NAME/content/prompts/"

  echo "⚙️ Copying Obsidian config & plugins..."
  cp -R "$DB_REPO/.obsidian" "$VAULT_NAME/.obsidian"

  echo "✅ Vault '$VAULT_NAME' created successfully with Dreambase templates and config."
}
```


```bash
makeobsvault MyVault ~/path/to/Dreambase_repo
```

- **`vault-name`** → The name of your new Obsidian vault (will be created in the current directory).
- **`templates-source-dir`** → Path to your templates directory (where this repo is cloned).
    

This allows you to keep your **source templates** anywhere and generate vaults in any location without modifying the function.

### Key Notes:

- **`dreambase-repo-dir`** should point to the root of your cloned Dreambase repo.
- The script now **copies `.obsidian`** (plugins + config) alongside templates/prompts.
- Result: you open the new vault in Obsidian and everything (Templater, Dataview, mappings) is pre-configured.

---

## 📂 Repository Structure

```plaintext
Dreambase/
├── .obsidian
│   ├── appearance.json
│   ├── app.json
│   ├── community-plugins.json
│   ├── core-plugins.json
│   ├── plugins
│   │   ├── dataview/
│   │   └── templater-obsidian/
│   └── workspace.json
├── content
│   ├── certificates
│   ├── comments
│   ├── exercises
│   │   ├── questions
│   │   └── answers
│   ├── knowledgebase
│   │   ├── atoms
│   │   ├── how_to
│   │   ├── journal_logs
│   │   └── transcripts
│   │       ├── meetings
│   │       └── video_tutorials
│   ├── prompts
│   └── templates
├── resources
├── LICENSE.md
├── README.md
├── LLM_PROJECT_INSTRUCTIONS.md
└── src
```

## ✅ Goal
This project ensures:  
- **Consistency** in knowledge capture.  
- **Clarity** between technical detail and layman understanding.  
- **Automation-readiness** for LLM parsing and Git workflows.  
- **Reusability** across different domains (study projects,DevOps, legal, business, food, travel). 

---
## 📜 License

Dreambase is licensed under the **MIT License**.
This means you are free to:
- ✅ Use the templates and prompts in personal or commercial projects.
- ✅ Modify, adapt, and redistribute them.
- ✅ Include them in your own vaults, repos, or workflows.

With the following conditions:
- ℹ️ You must include the original copyright notice and this license in any copy.
- ⚖️ The software is provided **“as is”**, without warranty of any kind.

See [LICENSE.md](LICENSE.md) for the full text.