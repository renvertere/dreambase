# Meeting Transcript Prompt

You are going to provide me with a **raw meeting transcript**.  
Please parse it into the **Meeting Transcript template** (`meeting_transcript.md`).

## Guidelines
- Capture **participants** with their timestamps of first appearance.
- Identify and summarize the **goals** of the meeting, each with timestamp.
- Extract **discussion topics** in the order they appear, each with timestamp.
- List all **action items / next steps**, with timestamp, owner, and due date if mentioned.
- Add a **Next Meeting** section if a proposed date or agenda is discussed.
- Maintain all timestamps in **[HH:MM:SS]** format.
- If unclear, mark as `[Unclear]` with timestamp.

## Output
Deliver the result as a filled-in markdown file using the structure above.

## Guardrails
Do **not** include this prompt in the output.
