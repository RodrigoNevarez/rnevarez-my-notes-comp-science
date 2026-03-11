# Refinement Pack README

## What this pack is

This pack captures the outcome of the transcript-analysis refinement session. It turns the conversation into reusable artifacts for two different purposes:

1. **Running the AI agent**
2. **Helping you evaluate, steer, and improve the tool**

The pack is centered on a V1 concept:

> Analyze one transcript at a time and produce analyst-style notes on only the components most likely to affect your task, with evidence, careful inference, a short system picture, and next things to investigate.

---

## What problem this pack solves

The underlying problem is not just transcript summarization. The real problem is:

- too much transcript material
- not enough architectural context
- not enough clarity about what matters to your work
- difficulty understanding how systems relate to each other
- uncertainty about what to research next and who to ask

This pack is designed to support a tool that reduces that ambiguity.

---

## How the pack is organized

There are three practical groups of files:

### 1. Agent-driving files
These files are mainly for the AI system itself.

- `ai_transcript_analyst_prompt.md`
- `v1_report_template.md`
- `selection_criteria.md`
- `evidence_and_inference_policy.md`
- `report_section_guidelines.md`
- `ambiguity_handling_guide.md`
- `ownership_extraction_guide.md`

These define:
- what the AI should do
- what it should ignore
- how it should select components
- how it should write the report
- how it should handle inference, ambiguity, evidence, and ownership

### 2. Human-control files
These files are mainly for you.

- `v1_product_definition.md`
- `refinement_decisions_log.md`
- `design_principles.md`
- `v1_acceptance_criteria.md`
- `failure_modes_and_antipatterns.md`
- `test_plan_first_transcripts.md`
- `iteration_playbook.md`
- `one_page_cheatsheet.md`
- `session_summary.md`

These help you:
- remember what was decided
- keep the tool aligned with its purpose
- test it properly
- recognize bad output
- refine it without losing focus

### 3. Mixed-use files
Some files help both the AI and you.

- `v1_report_template.md`
- `selection_criteria.md`
- `evidence_and_inference_policy.md`
- `report_section_guidelines.md`

These are useful both as generation instructions and as evaluation references.

---

## File-by-file guide

### `ai_transcript_analyst_prompt.md`
The main production-ready prompt template.  
Use this when you want the AI to analyze a transcript.

### `v1_report_template.md`
The expected report shape.  
Useful both as a formatting target for the AI and as a review checklist for you.

### `v1_product_definition.md`
Defines the V1 tool clearly:
- purpose
- user problem
- scope
- non-goals
- success definition

This is the best file to reread when the project starts drifting.

### `refinement_decisions_log.md`
A compact record of the design decisions made during the refinement session.

### `design_principles.md`
High-level rules that express the philosophy of the tool, such as relevance over completeness and traceability over fake precision.

### `selection_criteria.md`
Explains what counts as an important component and what should be left out.

### `evidence_and_inference_policy.md`
Explains:
- how quotes should be chosen
- how inference should be labeled
- when to hold back instead of overreaching

### `report_section_guidelines.md`
Gives section-by-section instructions for generating the report well.

### `ambiguity_handling_guide.md`
Explains how to surface missing context in a useful way.

### `ownership_extraction_guide.md`
Explains when people’s names should be included and how to use ownership signals without clutter.

### `v1_acceptance_criteria.md`
A checklist for deciding whether the tool is actually good enough to use.

### `failure_modes_and_antipatterns.md`
A fast way to recognize poor outputs, such as:
- transcript sludge
- generic summary mode
- fake certainty
- overinclusion
- weak evidence

### `test_plan_first_transcripts.md`
A simple plan for testing the prompt on real transcripts before relying on it broadly.

### `iteration_playbook.md`
A structured way to refine the prompt after tests without turning refinement into an endless loop.

### `one_page_cheatsheet.md`
A compressed quick-reference version of the whole system.

### `session_summary.md`
A narrative summary of how the refinement session evolved and what the final V1 became.

---

## Recommended starting workflow

### Smallest useful setup
If you want to get moving quickly, use these four files first:

**For the AI**
- `ai_transcript_analyst_prompt.md`
- `v1_report_template.md`
- `selection_criteria.md`
- `evidence_and_inference_policy.md`

**For yourself**
- `v1_product_definition.md`
- `refinement_decisions_log.md`
- `v1_acceptance_criteria.md`
- `test_plan_first_transcripts.md`

This gives you:
- one prompt
- one output structure
- one filtering policy
- one evidence policy
- one definition of success
- one testing plan

That is enough to run the first real experiments.

---

## How to use this pack in practice

### Step 1: Read the product definition
Start with `v1_product_definition.md` so you remember what the tool is actually for.

### Step 2: Use the main prompt
Take `ai_transcript_analyst_prompt.md` and fill in:
- task context
- optional focus areas
- ignore areas
- max components
- transcript

### Step 3: Generate one report
Run the tool on one transcript only.

### Step 4: Review the output against the criteria
Check:
- did it choose the right components?
- did it explain why they matter?
- did it clarify relationships?
- was the evidence good?
- did it surface ambiguity honestly?
- are the next steps useful?

Use:
- `v1_acceptance_criteria.md`
- `failure_modes_and_antipatterns.md`

### Step 5: Tune carefully
If the result is weak, adjust with help from:
- `iteration_playbook.md`
- `selection_criteria.md`
- `evidence_and_inference_policy.md`

---

## What this pack is intentionally not

This pack is **not**:
- a generic meeting summarizer
- a multi-transcript synthesis framework
- a database schema for all knowledge extraction
- a final production system design
- a rigid specification for every future version

It is a **focused V1 refinement pack**.

Its job is to help you test a narrow but valuable capability:
extracting task-relevant architectural context from a single transcript.

---

## Core design philosophy

The pack is built around these ideas:

- **Relevance over completeness**
- **Why it matters before what it does**
- **Relationships over raw mentions**
- **Signal over sludge**
- **Traceability through evidence**
- **Inference allowed, but explicit**
- **Ambiguity is valuable**
- **Ownership only when actionable**
- **One transcript, one coherent report**

---

## Best defaults

Unless you have a reason to change them, start with:

- one transcript at a time
- analyst-style notes
- maximum 5 important components
- 2–4 short evidence excerpts per component
- clearly labeled inference only when needed
- system-picture section included
- next-investigation section included
- unexplained important terms included
- non-technical discussion filtered out unless relevant

---

## If you only read three files

Read these first:

1. `v1_product_definition.md`
2. `ai_transcript_analyst_prompt.md`
3. `v1_acceptance_criteria.md`

That is the shortest path to understanding the pack and using it well.

---

## Suggested next step

The most valuable next move is to test the prompt on one real transcript and evaluate the result using:
- `v1_acceptance_criteria.md`
- `failure_modes_and_antipatterns.md`
- `test_plan_first_transcripts.md`

That will tell you whether the refinement is strong enough in practice.

---

## Prompting Claude Code or VS Code Copilot with the agent-driving files

If the agent needs to read the agent-driving files, the best approach is to give it:
- a clear reading order
- explicit file roles
- a priority rule for overlaps
- one concrete task at a time

The recommended reading order is:

1. `ai_transcript_analyst_prompt.md`
2. `v1_report_template.md`
3. `selection_criteria.md`
4. `evidence_and_inference_policy.md`
5. `report_section_guidelines.md`
6. `ambiguity_handling_guide.md`
7. `ownership_extraction_guide.md`

That order keeps the model anchored first on behavior, then output, then filtering, then evidence/inference discipline, then ambiguity and ownership handling.

### Claude Code prompt

```text
You are helping me operationalize a transcript-analysis agent.

I have 7 markdown files that together define the agent. Read them as a layered specification in this exact order:

1. ai_transcript_analyst_prompt.md
2. v1_report_template.md
3. selection_criteria.md
4. evidence_and_inference_policy.md
5. report_section_guidelines.md
6. ambiguity_handling_guide.md
7. ownership_extraction_guide.md

Treat the files with these roles:

- ai_transcript_analyst_prompt.md = primary behavior spec
- v1_report_template.md = required output contract
- selection_criteria.md = inclusion/exclusion policy
- evidence_and_inference_policy.md = evidence and inference safety policy
- report_section_guidelines.md = writing-quality guidance
- ambiguity_handling_guide.md = missing-context handling policy
- ownership_extraction_guide.md = ownership/person-mention policy

Priority rule:
If files overlap, preserve the higher-level behavioral intent and keep the stricter rule. Do not broaden scope.

The intended agent is:
- one transcript at a time
- focused on task-relevant architectural context
- selective rather than exhaustive
- analyst-style rather than generic summary
- evidence-backed
- allowed to make careful inferences, but only when clearly labeled
- expected to surface ambiguity and next things to investigate
- allowed to mention people only when useful for ownership or follow-up

Your tasks:
1. Summarize the agent’s operating model in 8–12 bullets.
2. Identify overlap, redundancy, or conflict across the files.
3. Produce one consolidated production-ready system prompt that preserves the pack’s intent.
4. Keep the final prompt concise, but do not lose:
   - one-transcript-at-a-time behavior
   - task-relevant component selection
   - evidence excerpts
   - clearly labeled inference
   - ambiguity handling
   - ownership cues when useful

Constraints:
- Do not restate the source files in full.
- Do not turn this into a generic meeting summarizer.
- Do not weaken the selection discipline.
- Do not remove evidence or inference safeguards.
- Do not add features that are not already implied by the files.

Output exactly these sections:
1. Operating model
2. Redundancies or conflicts
3. Consolidated production prompt
```

### VS Code Copilot prompt

```text
I have 7 markdown files that define a transcript-analysis agent.

Use them as design inputs, not as content to summarize.

Read and apply them in this priority order:
1. ai_transcript_analyst_prompt.md
2. v1_report_template.md
3. selection_criteria.md
4. evidence_and_inference_policy.md
5. report_section_guidelines.md
6. ambiguity_handling_guide.md
7. ownership_extraction_guide.md

File roles:
- ai_transcript_analyst_prompt.md = main behavior spec
- v1_report_template.md = output contract
- selection_criteria.md = inclusion/exclusion rules
- evidence_and_inference_policy.md = evidence and inference rules
- report_section_guidelines.md = report writing guidance
- ambiguity_handling_guide.md = ambiguity rules
- ownership_extraction_guide.md = ownership/person-mention rules

Priority rule:
If instructions overlap, keep the stricter and more task-relevant rule. Do not broaden scope.

Target agent behavior:
- analyze one transcript at a time
- extract task-relevant architectural context
- organize output around important components
- explain why each component matters
- include short evidence excerpts in a separate evidence subsection
- allow careful inference only when clearly labeled
- surface important ambiguity
- mention people only when useful for ownership or follow-up
- end with a short system picture and next things to investigate

Your task:
- derive one consolidated agent specification
- preserve the report structure
- preserve the component-selection rules
- preserve evidence and inference discipline
- preserve ambiguity and ownership behavior

Output exactly these sections:
1. Agent purpose
2. Behavioral rules
3. Output contract
4. Conflict resolution notes
5. Final consolidated prompt

Constraints:
- Do not dump the contents of the source files back to me.
- Do not make the agent broader than intended.
- Do not convert it into a generic meeting summarizer.
- Keep the final consolidated prompt practical and implementation-ready.
```

---

## What the Claude Code and Copilot prompts output

By default, the prompts in this README produce **text in chat**, not files.

### Expected outputs

#### Claude Code prompt output
The Claude Code prompt is designed to return these sections in chat:

1. Operating model
2. Redundancies or conflicts
3. Consolidated production prompt

#### VS Code Copilot prompt output
The Copilot prompt is designed to return these sections in chat:

1. Agent purpose
2. Behavioral rules
3. Output contract
4. Conflict resolution notes
5. Final consolidated prompt

### Important clarification
Reading the agent-driving files does **not** automatically cause the agent to:
- write files into the workspace
- store anything into persistent memory
- modify your repo

The default behavior is:

**read files → synthesize → reply in chat**

---

## When the agent will write files

The agent will usually write files **only if you explicitly ask it to**.

Examples:

```text
After generating the final consolidated prompt, write it to:
docs/transcript_agent_system_prompt.md

Also write the conflict notes to:
docs/transcript_agent_conflicts.md
```

Or:

```text
Create these files in the workspace:
- docs/agent_purpose.md
- docs/behavioral_rules.md
- docs/final_consolidated_prompt.md
```

If you do not include a file-writing instruction, the safe assumption is that the result will remain in chat only.

---

## Memory vs files vs chat

It helps to distinguish three different things:

### Chat output
Temporary response text in the conversation.

### Workspace files
Actual files created in your repo or working directory.

### Persistent memory
A product-specific memory feature, separate from normal chat output and separate from writing files.

These prompts do **not** automatically store anything in persistent memory.

---

## Recommended wording if you want file generation

If you want Claude Code or Copilot to generate files from the consolidation step, add a final instruction like this:

```text
After producing the final consolidated prompt, write the outputs into these files:

- docs/agent_operating_model.md
- docs/agent_conflicts.md
- docs/transcript_agent_system_prompt.md
```

If you want chat-only behavior, you do not need to add anything.

---

## Practical rule

Use this mental model:

- **Read files + no file instruction** → output stays in chat
- **Read files + explicit file instruction** → agent may create workspace files
- **Read files alone** → no automatic persistent memory

---

## How to run the agent with `task.md` and `transcript.vtt`

Use the refinement pack as the **behavior spec**, then use your runtime files as the actual analysis inputs.

### Role of each file group

- **Agent-driving files** define how the agent should behave and format output.
- **`task.md`** provides the task context.
- **`transcript.vtt`** is the raw transcript to analyze.

In practice:

- `task.md` fills the role of **TASK_CONTEXT**
- `transcript.vtt` fills the role of **TRANSCRIPT**

### Recommended execution flow

Tell Claude Code or VS Code Copilot to:

1. read the agent-driving files first
2. read `task.md` as the task context
3. read `transcript.vtt` as the transcript
4. generate the report
5. optionally write the result to a file

### Important note about `.vtt`
A `.vtt` transcript may contain:
- timestamps
- caption numbering
- formatting noise
- speaker markers

It is usually helpful to instruct the agent to ignore timing markers and formatting noise and focus on spoken content.

---

## Claude Code runtime prompt

Use this when your files are already in the workspace:

```text
You are running a transcript-analysis agent.

First, read these specification files in this order:

1. ai_transcript_analyst_prompt.md
2. v1_report_template.md
3. selection_criteria.md
4. evidence_and_inference_policy.md
5. report_section_guidelines.md
6. ambiguity_handling_guide.md
7. ownership_extraction_guide.md

Treat them with these roles:
- ai_transcript_analyst_prompt.md = primary behavior spec
- v1_report_template.md = output contract
- selection_criteria.md = inclusion/exclusion policy
- evidence_and_inference_policy.md = evidence and inference policy
- report_section_guidelines.md = section-writing guidance
- ambiguity_handling_guide.md = missing-context policy
- ownership_extraction_guide.md = ownership/person-mention policy

Then read:
- task.md as the task context
- transcript.vtt as the transcript to analyze

Execution rules:
- Use task.md to understand what is relevant to the user’s work.
- Use transcript.vtt as the only transcript source.
- Analyze one transcript only.
- Ignore VTT timing markers, caption numbering, and formatting noise.
- Follow the behavior and output rules from the spec files.
- Do not summarize the spec files back to me.
- Do not produce a generic meeting summary.

Your task:
Generate the final V1 Transcript Context Report for transcript.vtt using task.md as context.

Output:
- return the report in chat
- then write it to docs/transcript_context_report.md
```

### Claude Code chat-only variant

If you want chat output only, remove the file-writing line at the end:

```text
- then write it to docs/transcript_context_report.md
```

---

## VS Code Copilot runtime prompt

Use this when your files are already in the workspace:

```text
Use the following files as inputs for a transcript-analysis run.

Specification files to read in order:
1. ai_transcript_analyst_prompt.md
2. v1_report_template.md
3. selection_criteria.md
4. evidence_and_inference_policy.md
5. report_section_guidelines.md
6. ambiguity_handling_guide.md
7. ownership_extraction_guide.md

Input files:
- task.md = task context
- transcript.vtt = transcript to analyze

Instructions:
- Apply the spec files as the agent rules.
- Use task.md to determine what is relevant.
- Use transcript.vtt as the only transcript source.
- Analyze one transcript only.
- Ignore VTT timing markers, caption numbering, and formatting noise.
- Preserve the required report structure.
- Preserve selection discipline, evidence rules, inference labeling, ambiguity handling, and ownership behavior.
- Do not summarize the spec files.
- Do not produce a generic meeting summary.

Task:
Generate the final transcript context report for transcript.vtt using task.md as the task context.

Output requirements:
1. Return the report in chat
2. Write the report to docs/transcript_context_report.md
```

---

## Stronger wording for variable mapping

A useful instruction to include is:

```text
Read task.md and treat it as TASK_CONTEXT.
Read transcript.vtt and treat it as TRANSCRIPT.
Use the specification files as the operating rules for analysis and output.
```

This makes the intended mapping explicit.

---

## If your transcript filename includes spaces

If the actual file is named something like:

```text
transcript .vtt
```

use the filename exactly as it exists in the workspace, including the space.  
If possible, rename it to:

```text
transcript.vtt
```

to avoid path issues.

---

## Suggested `task.md` structure

Your `task.md` does not need sensitive details. It only needs enough context to steer relevance.

Example:

```md
# Task Context

## Current need
I am trying to understand the architecture relevant to my work.

## What I care about
- components that affect implementation
- integrations and dependencies
- how systems relate to each other
- constraints, risks, and caveats
- who I should ask for missing context

## What I do not care about
- social chatter
- meeting logistics
- status updates without technical relevance

## Output preference
I want a selective analyst-style report, not a generic summary.
```

---

## Recommended repo layout

A simple layout makes execution easier:

```text
/project-root
  /docs
  /prompts
    ai_transcript_analyst_prompt.md
    v1_report_template.md
    selection_criteria.md
    evidence_and_inference_policy.md
    report_section_guidelines.md
    ambiguity_handling_guide.md
    ownership_extraction_guide.md
  task.md
  transcript.vtt
```

If you organize the files this way, your instruction can also say:

```text
Read all files in /prompts in the required order, then read /task.md and /transcript.vtt.
```

---

## Practical rule

Use this mental model:

- **Spec files** tell the agent how to think
- **`task.md`** tells the agent what matters
- **`transcript.vtt`** gives the raw evidence to analyze
