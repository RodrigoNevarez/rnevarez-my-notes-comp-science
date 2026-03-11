# Knowledge Gap Artifacts Pack

## What this pack is

This pack contains reusable markdown prompts and artifact templates for turning transcript-analysis knowledge gaps into durable, useful follow-up documents.

The goal is to help you convert ambiguity into:
- reusable notes
- validation paths
- team questions
- system maps
- assumptions logs
- safer implementation boundaries

## How to use this pack

1. Generate your main transcript report first.
2. Save it as `docs/transcript_context_report.md`.
3. Use the prompts in this pack with Copilot or Claude Code to generate the follow-up artifacts you need.
4. Do not try to generate all artifacts every time.
5. Start with the highest-leverage ones first.

## Best starter set

If you want the most value quickly, start with:
- `architecture_gap_log_prompt.md`
- `system_relationship_map_prompt.md`
- `questions_for_team_prompt.md`
- `minimum_context_to_move_prompt.md`

## Typical workflow

1. Generate the transcript context report.
2. Generate 2–4 follow-up artifacts.
3. Review them yourself.
4. Use them to drive:
   - repo investigation
   - teammate questions
   - implementation boundaries
   - prompt tuning
   - personal system understanding

## Included files

- `architecture_gap_log_prompt.md`
- `system_relationship_map_prompt.md`
- `component_cards_prompt.md`
- `internal_glossary_prompt.md`
- `ownership_map_prompt.md`
- `decision_assumptions_log_prompt.md`
- `integration_points_prompt.md`
- `risk_register_context_prompt.md`
- `repo_search_playbook_prompt.md`
- `questions_for_team_prompt.md`
- `validated_architecture_notes_prompt.md`
- `transcript_insights_index_prompt.md`
- `working_mental_model_prompt.md`
- `prompt_tuning_notes_prompt.md`
- `minimum_context_to_move_prompt.md`
- `artifact_recommender_prompt.md`

## Recommended source file

Most prompts assume this file exists:

`docs/transcript_context_report.md`

If your report is somewhere else, update the path in the prompts.
