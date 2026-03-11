# Prompt: repo_search_playbook.md

```text
Use #docs/transcript_context_report.md as the primary source.

Create a markdown file called:
repo_search_playbook.md

Purpose:
Turn the report’s unresolved questions into concrete repo investigation steps.

Structure:
- Investigation goals
- Search strategies by gap type
- Example search targets
- Validation tips

Include patterns such as:
- find where a component is referenced
- find where an event is emitted or consumed
- find auth checks
- find integration config
- find owners through blame / commits / tests / docs

Rules:
- Make the steps actionable.
- Tie search strategies back to the kinds of gaps found in the report.
- Prefer concrete investigation moves over generic advice.

Write the file in markdown.
```
