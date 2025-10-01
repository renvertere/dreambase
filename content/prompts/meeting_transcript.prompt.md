# Meeting Transcript Prompt

You are going to provide me with a **raw meeting transcript**.  
Please parse it into the **Meeting Transcript template** (`meeting_transcript_template.md`).

## Guidelines
1) **Do NOT include the document properties (the YAML block between `---` and `---`).** Obsidian generates this automatically.
2) Capture **participants** with their timestamps of first appearance.
3) Identify and summarize the **goals** of the meeting, each with timestamp.
4) Extract **discussion topics** in the order they appear, each with timestamp.
5) List all **action items / next steps**, with timestamp, owner, and due date if mentioned.
6) Add a **Next Meeting** section if a proposed date or agenda is discussed.
7) Maintain all timestamps in **[HH:MM:SS]** format.
8) If unclear, mark as `[Unclear]` with timestamp.

## **Output**
- Now, using the above rules, produce the meetings notes.

## Guardrails
- Do **not** include this prompt in the output.
