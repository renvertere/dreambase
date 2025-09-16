# Video Transcript Prompt

You are going to provide me with a **raw social media video transcript**.  
Please parse it into the **Video Transcript template** (`video_transcript.md`).

## Guidelines
- Capture **creator(s) & collaborators** with timestamps of first appearance.
- Identify and summarize **core topics**, assigning IDs (V01, V02, …) with timestamps.
- Provide a **detailed summary** for each topic.
- List all **calls to action / key mentions**, with timestamp.
- Capture any **references & links** cited, with timestamp.
- Add a **Next Steps / Continuations** section if follow-ups are mentioned.
- Maintain timestamps in **[HH:MM:SS]** format.
- If unclear, mark as `[Unclear]` with timestamp.

## Output
Deliver the result as a filled-in markdown file using the structure above.

## Guardrails
Do **not** include this prompt in the output.
