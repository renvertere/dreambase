---
title: template_overview_index
tags:
  - dashboard
  - index
created: 2025-10-12
updted:
---
# 🧭 Template Index

Central reference document describing every DreamBase template — their intent, structure, and ideal usage scenario.

---


# 🧱 DreamBase Template Purpose Index

| Template                               | Folder                        | Logic                  |
| -------------------------------------- | ----------------------------- | ---------------------- |
| **Template Purpose Index**             | `overview`                    | This document          |
| **Dashboard**                          | root (`index.md`)             |                        |
| **Atoms**                              | `atoms`                       | [[resources/template_overview/breakdowns/atoms]]              |
| **How-To**                             | `how_to`                      | [[resources/template_overview/breakdowns/how_to]]             |
| **Exercise (Q/A)**                     | `exercises_q` / `exercises_a` | [[exercise_q_and_a]]   |
| **Journal Logs**                       | `journal_logs`                | [[journal_logs]]       |
| **Course Readme**                      | `readme`                      | [[course_readme]]      |
| **Video To Atom Index**                | `video_to_atom`               | [[resources/template_overview/breakdowns/video_to_atom]]      |
| **Meeting Transcript**                 | `meeting_transcript`          | [[resources/template_overview/breakdowns/meeting_transcript]] |
| **SOP (Standard Operating Procedure)** | `standard_op_proc_template`   | [[resources/template_overview/breakdowns/standard_op_proc]]   |
| **Troubleshooting**                    | `troubleshooting_template`    | [[resources/template_overview/breakdowns/troubleshooting]]    |
| **Text 2 Image**                       | `t2i_schema_template`         | [[t2i_schema]]         |

---
## 📋 Prompts
Each template has a matching `.prompt.md` stored under `content/prompts/`.  
These prompts enforce **Guidelines** for the LLM when parsing raw inputs (transcripts, outlines, workflows) into structured notes.

Prompts enforce:  
- Technical vs layman explanations.  
- Timestamp validation.  
- Linking related notes.  
- Consistent atomic scope.  

- `atom.prompt.md` → For atomic technical concepts.
- `course_readme.prompt.md` → For course outlines.
- `how_to.prompt.md` → For step-by-step guides.
- `meeting_transcript.prompt.md` → For meeting transcripts.
- `video_transcript.prompt.md` → For video transcripts.
- `journal_logs.prompt.md` → For daily journaling.
- `exercise_q.prompt.md` → For exercise questions.
- `standard_op_proc_prompt.md` → For Standard Operating Procedures (SOPs).
- `troubleshooting_template.md` → Document the diagnosis and resolution of technical issues.
- `t2i_schema_template.md` → For Text 2 Image prompt creation.