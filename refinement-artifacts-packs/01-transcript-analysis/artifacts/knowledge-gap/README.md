# Knowledge Gap Artifacts Pack

## What this pack is

This pack contains reusable markdown prompts for turning transcript-analysis knowledge gaps into durable, useful follow-up documents.

The goal is to convert ambiguity into:
- reusable notes
- validation paths
- targeted team questions
- system maps
- assumptions logs
- safer implementation boundaries
- longer-term personal architecture knowledge

These prompts are meant to be used **after** you have already generated a transcript context report.

---

## Core idea

Your transcript report surfaces:
- important components
- inferred or confirmed relationships
- gaps in knowledge
- likely owners
- next things to investigate

This pack helps you transform those outputs into artifacts that are easier to reuse later.

Think of the transcript report as a **diagnostic layer**.

Think of these artifacts as the **working memory and follow-up layer**.

---

## Recommended source file

Most prompts assume this file exists:

`docs/transcript_context_report.md`

If your report is saved elsewhere, update the path in the prompt before using it.

---

## How to use this pack

1. Generate your main transcript report first.
2. Save it as `docs/transcript_context_report.md`.
3. Choose only the follow-up artifacts you need right now.
4. Run the corresponding prompt in Copilot or Claude Code.
5. Review the generated artifact yourself before relying on it.
6. Reuse the artifact as part of your ongoing context system.

Do not try to generate all artifacts every time.  
Most transcripts only justify a small subset.

---

## Best starter set

If you want the most value quickly, start with:

- `architecture_gap_log_prompt.md`
- `system_relationship_map_prompt.md`
- `questions_for_team_prompt.md`
- `minimum_context_to_move_prompt.md`

Why these four first:
- they reduce ambiguity fastest
- they help you decide what blocks implementation
- they give you a map, a question list, and a safety threshold
- they are useful even if the report still has uncertainty

---

## When these artifacts are useful

These prompts are especially valuable when:
- you still feel lost after reading the transcript report
- the report surfaced many unresolved relationships
- ownership is unclear
- you need to move forward with partial knowledge
- you want to build reusable notes instead of re-learning the same things
- you need to turn ambiguity into concrete next steps

---

## File-by-file guide

### `architecture_gap_log_prompt.md`
**What it does**  
Creates a structured log of unresolved and partially resolved gaps.

**Why it is useful**  
This is one of the highest-value artifacts because it turns vague uncertainty into a manageable backlog. Instead of “I’m missing context,” you get a list of concrete unknowns with severity, hypotheses, validation paths, and status.

**Best use cases**
- you want to track open questions over time
- you need to distinguish blockers from minor unknowns
- you want one place to record how gaps were resolved

**What it produces**
- gap
- why it matters
- technical vs organizational type
- severity
- current hypothesis
- validation path
- status
- source of truth once resolved

---

### `system_relationship_map_prompt.md`
**What it does**  
Builds a readable map of the important systems/components and how they relate.

**Why it is useful**  
Your biggest pain point was understanding how things relate, not just what components exist. This artifact turns scattered analysis into a reusable structure showing confirmed, inferred, and unclear relationships.

**Best use cases**
- the report mentions many systems but the architecture still feels fuzzy
- you need a compact mental map
- you want a document you can update as understanding improves

**What it produces**
- overview
- component list
- relationship map
- confirmed relationships
- inferred relationships
- unclear relationships
- open questions

---

### `component_cards_prompt.md`
**What it does**  
Creates one compact markdown “card” per important component.

**Why it is useful**  
This is useful when the report has several important components and you want a reusable reference for each one. It is a good bridge between raw transcript analysis and a more stable internal knowledge base.

**Best use cases**
- you keep encountering the same components across transcripts
- you want component-by-component notes
- you need a compact reference format

**What it produces**
- component name
- why it matters
- what it seems to do
- related components
- constraints / risks / dependencies
- likely owners
- open questions

---

### `internal_glossary_prompt.md`
**What it does**  
Builds a glossary of important but insufficiently explained terms, acronyms, services, queues, jobs, or internal shorthand.

**Why it is useful**  
A lot of workplace ambiguity comes from language people assume is obvious. This artifact captures that hidden vocabulary so you stop relearning it from scratch.

**Best use cases**
- transcripts are full of acronyms or shorthand
- people reference systems as if everyone already knows them
- you need a vocabulary layer before architecture makes sense

**What it produces**
- term
- likely meaning or role
- why it matters
- whether it is confirmed, inferred, or unclear
- related components
- what still needs confirmation

---

### `ownership_map_prompt.md`
**What it does**  
Creates a practical map of which people seem closest to which components or areas.

**Why it is useful**  
This helps when the main issue is not just technical ambiguity, but knowing who to ask. It gives you a structured contact map rather than a loose memory of who said what.

**Best use cases**
- ownership is unclear
- you need to ask targeted follow-up questions
- you want to avoid asking the wrong person

**What it produces**
- component / area
- likely owner or strongest explainer
- why that person seems relevant
- best reason to ask them
- confidence note

---

### `decision_assumptions_log_prompt.md`
**What it does**  
Creates a log of assumptions you may need to operate under while ambiguity remains.

**Why it is useful**  
This is powerful because it helps you move forward safely without pretending uncertainty does not exist. It is especially useful when you need to implement before every architectural detail is confirmed.

**Best use cases**
- you need to proceed with partial knowledge
- you want to avoid hidden assumptions
- you need to track what could break if an assumption is wrong

**What it produces**
- assumption
- why you might rely on it
- what evidence supports it
- what could break if wrong
- how to verify it
- status

---

### `integration_points_prompt.md`
**What it does**  
Extracts the important handoffs, APIs, events, queues, jobs, and system boundaries.

**Why it is useful**  
This is useful when the architecture matters mainly because of cross-system interaction. It narrows the focus to the seams where implementation risk often lives.

**Best use cases**
- the task likely touches multiple systems
- event flow or service boundaries matter
- you need to trace where something enters, leaves, or transforms

**What it produces**
- systems involved
- interaction type
- what seems to flow across the boundary
- confirmed vs inferred status
- risks / constraints / unknowns
- what to verify next

---

### `risk_register_context_prompt.md`
**What it does**  
Turns unresolved technical ambiguity into a lightweight risk register.

**Why it is useful**  
Useful when the report surfaced uncertainties that could materially affect implementation or design decisions. It helps you prioritize unknowns by likely impact rather than just noticing them.

**Best use cases**
- several unknowns seem potentially dangerous
- you need to distinguish risk from curiosity
- implementation could be affected by hidden coupling or missing contracts

**What it produces**
- risk
- why it matters
- source of uncertainty
- likely impact
- mitigation / next step
- status

---

### `repo_search_playbook_prompt.md`
**What it does**  
Transforms knowledge gaps into concrete repo investigation steps.

**Why it is useful**  
This is one of the most actionable artifacts. Instead of “research X,” it gives you search patterns and practical investigation moves inside the codebase.

**Best use cases**
- you need to validate transcript claims in code
- you want to reduce ambiguity without asking people first
- you need a repeatable repo investigation method

**What it produces**
- investigation goals
- search strategies by gap type
- example search targets
- validation tips

---

### `questions_for_team_prompt.md`
**What it does**  
Converts unresolved high-value gaps into targeted, answerable questions for teammates.

**Why it is useful**  
This helps you avoid vague, exhausting questions. It turns uncertainty into concise follow-up prompts tied to components, context, and current hypotheses.

**Best use cases**
- you need to ask teammates for clarification
- you want fewer but better questions
- you want questions grouped by topic or component

**What it produces**
- question
- why you are asking it
- current hypothesis
- best person or role to ask
- related component or term

---

### `validated_architecture_notes_prompt.md`
**What it does**  
Creates a conservative architecture note containing only the parts that appear most reliable.

**Why it is useful**  
This artifact gives you a cleaner, more trustworthy reference than the raw transcript report. It is good when you want a “high-confidence only” version of what seems true.

**Best use cases**
- the report contains a mix of strong signals and weaker inference
- you want a stable note to consult later
- you need a more conservative summary before acting

**What it produces**
- high-confidence components
- high-confidence relationships
- likely flows and boundaries
- important caveats
- still unvalidated areas

---

### `transcript_insights_index_prompt.md`
**What it does**  
Creates one index entry for a transcript so you can compare insights across multiple analyses later.

**Why it is useful**  
This becomes valuable once you process multiple transcripts. It lets you keep a compact cross-transcript view without rereading entire reports.

**Best use cases**
- you expect to analyze several transcripts
- you want a searchable historical index
- you need to compare what became clearer over time

**What it produces**
- transcript identifier
- date if available
- important components surfaced
- key unresolved gaps
- important people / likely owners
- main architectural insight
- best next investigations

---

### `working_mental_model_prompt.md`
**What it does**  
Writes a plain-English explanation of how the system seems to work.

**Why it is useful**  
This is useful because formal notes are not always the best format for thinking. A mental-model document helps you explain the system to yourself in simpler terms.

**Best use cases**
- you understand fragments but not the whole
- you need a less formal explanation
- you want a document that reflects your current understanding, including uncertainty

**What it produces**
- what the system appears to be doing
- most important components
- how they connect
- what still feels uncertain
- what you currently believe is true

---

### `prompt_tuning_notes_prompt.md`
**What it does**  
Creates a structured note about what the agent did well, what it missed, and what small prompt changes might improve future runs.

**Why it is useful**  
This helps you refine the transcript-analysis workflow without random prompt drift. It makes prompt improvement more disciplined.

**Best use cases**
- the report felt weak or uneven
- you want to improve future runs
- you want to distinguish whether the issue was selection, evidence, inference, ambiguity, or actionability

**What it produces**
- what worked
- what failed
- failure mode classification
- likely root cause
- smallest prompt change to try
- issue type classification

---

### `minimum_context_to_move_prompt.md`
**What it does**  
Identifies the minimum context you need before you can move forward safely.

**Why it is useful**  
This is one of the most practical artifacts because it prevents ambiguity from becoming paralysis. It helps you separate blockers from things that can wait.

**Best use cases**
- you need to move forward before everything is known
- you need to distinguish must-know vs can-defer
- you want a safe-progress threshold

**What it produces**
- must know before implementing
- should know soon
- can defer for later
- current assumptions you can work with
- dangerous unknowns

---

### `artifact_recommender_prompt.md`
**What it does**  
Asks the model to recommend the best 3 follow-up artifacts based on the current report.

**Why it is useful**  
This is useful when you are not sure which artifact to generate next. Instead of guessing, you can have the model recommend the most leveraged next documents.

**Best use cases**
- you do not want to generate too many artifacts
- you want to prioritize follow-up work
- you want to match artifacts to the type of ambiguity in the current report

**What it produces**
- top 3 artifact recommendations
- why each is useful now
- what decisions each would support
- what parts of the report would populate it

---

## Recommended order of use

### If you are still highly confused
Start with:
1. `architecture_gap_log_prompt.md`
2. `system_relationship_map_prompt.md`
3. `minimum_context_to_move_prompt.md`

### If you need to ask people questions
Start with:
1. `questions_for_team_prompt.md`
2. `ownership_map_prompt.md`
3. `architecture_gap_log_prompt.md`

### If repo investigation is the next best move
Start with:
1. `repo_search_playbook_prompt.md`
2. `integration_points_prompt.md`
3. `decision_assumptions_log_prompt.md`

### If you want to build durable personal knowledge
Start with:
1. `component_cards_prompt.md`
2. `internal_glossary_prompt.md`
3. `validated_architecture_notes_prompt.md`
4. `transcript_insights_index_prompt.md`

---

## Practical advice

A good rule is:
- generate the main transcript report
- choose 2–4 artifacts
- use those artifacts to reduce ambiguity
- do not overproduce documents you will not maintain

The point is not to create paperwork.  
The point is to create reusable clarity.

---

## Most generally useful prompts

If you only want the most broadly useful prompts, use these first:

- `architecture_gap_log_prompt.md`
- `system_relationship_map_prompt.md`
- `questions_for_team_prompt.md`
- `minimum_context_to_move_prompt.md`
- `repo_search_playbook_prompt.md`

That set covers:
- unknowns
- architecture
- human follow-up
- safe progress
- technical investigation

---

## Final reminder

These artifacts are best treated as a **living context system**.

You do not need all of them for every transcript.
You do not need them to be perfect on the first pass.

They are useful because they help you:
- remember what is still unclear
- build a better mental model
- ask better questions
- investigate more effectively
- move forward more safely
