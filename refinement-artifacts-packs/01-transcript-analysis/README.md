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

## What the “consolidate the 7 files” prompt is for

This prompt is **not** for analyzing a real transcript yet.

Its purpose is to **read the 7 agent-driving files and compress them into one usable agent specification**.

In other words, it is a **setup prompt** or **spec-consolidation prompt**.

### What it does
It asks Claude Code or VS Code Copilot to:
- read the 7 markdown files
- understand how they fit together
- resolve overlap or redundancy
- produce one consolidated prompt/spec you can use later

### What it outputs
The output is a synthesized spec in chat, not a transcript report.

For example, the Copilot version asks for:
1. Agent purpose
2. Behavioral rules
3. Output contract
4. Conflict resolution notes
5. Final consolidated prompt

### What it is not for
It is not for:
- analyzing `task.md`
- analyzing `transcript.vtt`
- generating the final report from a real transcript

### Recommended usage
Use this consolidation prompt:
- once at the beginning
- again only when the pack changes materially

Then use the consolidated prompt for actual transcript-analysis runs.

### Workflow distinction
- **Prompt A: consolidate the spec** → turns the 7 design files into one runtime-ready prompt
- **Prompt B: run the agent** → uses `task.md` and `transcript.vtt` to analyze a transcript

---

## Using Copilot to create `task.md` from a user story

If your user story has a description and acceptance criteria, you can use Copilot to turn it into a safe, high-level `task.md`.

The goal is **not** to copy the user story verbatim.  
The goal is to convert it into a **task-context lens** for transcript analysis.

That means Copilot should infer:
- what kind of technical work this is
- what architectural context is likely relevant
- what dependencies, constraints, or ownership signals matter
- what the agent should ignore

### Prompt to generate `task.md` from a user story

```text
I have a user story that contains a description and acceptance criteria.

Your job is to convert that user story into a task-context file for a transcript-analysis agent.

Do not rewrite the user story verbatim.
Do not preserve unnecessary sensitive detail.
Abstract it into a safe, high-level technical context that helps an agent decide what is relevant when analyzing a meeting transcript.

Create a markdown file using this structure:

# Task Context

## Current need
[Explain at a high level what kind of technical context I need from transcripts.]

## What I care about
- [List the kinds of components, relationships, dependencies, constraints, risks, or ownership signals that are likely relevant.]

## What I do not care about
- social chatter
- meeting logistics
- status updates without technical relevance
- [Add any other likely irrelevant areas based on the story.]

## Output preference
[Describe the desired report style: selective analyst-style report, important components only, short evidence excerpts, clearly labeled inference, system picture, and next things to investigate.]

## Useful follow-up signals
- [What should the transcript analysis help me identify next?]

Instructions:
- Infer the likely architectural focus from the user story description and acceptance criteria.
- Preserve technical relevance, but generalize the context.
- Do not include confidential product names unless truly necessary.
- Do not copy the story text directly into task.md.
- Make the result useful as TASK_CONTEXT for transcript analysis.

After generating the markdown, explain in 3-5 bullets why you chose that framing.

I will paste the user story below.
```

### Variant that writes directly to `task.md`

```text
Read the user story below and convert it into a safe, high-level task context file for transcript analysis.

Write the result to:
task.md

Use this structure:

# Task Context

## Current need
## What I care about
## What I do not care about
## Output preference
## Useful follow-up signals

Rules:
- infer the likely architectural focus from the story description and acceptance criteria
- do not copy the story verbatim
- do not include unnecessary sensitive details
- generalize into a form that helps an agent analyze transcripts for relevance
- optimize for architectural understanding, dependencies, component relationships, risks, constraints, and who to ask for context

After writing task.md, also give me a short explanation of the framing choices.

User story:
[PASTE USER STORY]
```

### What `task.md` is for
Think of it this way:
- `transcript.vtt` = the evidence
- `task.md` = the filter

`task.md` tells the agent what to optimize for when reading the transcript.

---

## How to review a generated report against the evaluation files

The best workflow is:
- let Copilot do a **first-pass structured critique**
- let yourself do the **final usefulness judgment**

Copilot can review the report against:
- `v1_acceptance_criteria.md`
- `failure_modes_and_antipatterns.md`

You should still make the final call on whether the report actually reduced **your** ambiguity.

### Copilot evaluation prompt

```text
Review the generated transcript context report against these evaluation files:

- #v1_acceptance_criteria.md
- #failure_modes_and_antipatterns.md

Also use:
- #v1_report_template.md
- #selection_criteria.md
- #evidence_and_inference_policy.md

Your task:
Evaluate the report as a V1 output.

Output exactly these sections:

1. Acceptance criteria assessment
   - For each major criterion, rate it as:
     - Strong
     - Adequate
     - Weak
   - Briefly explain why.

2. Failure modes detected
   - List any failure modes or antipatterns present.
   - Quote or point to the relevant parts of the report.

3. Most important weaknesses
   - Identify the top 3 issues reducing usefulness.

4. Suggested prompt adjustments
   - Suggest the smallest changes to the agent prompt or runtime instructions that would improve the next run.
   - Do not redesign the whole system.

5. Overall verdict
   - State whether this report is good enough for V1 use on another transcript.

Constraints:
- Be critical, not flattering.
- Do not rewrite the whole report.
- Do not invent missing evidence.
- Judge the report based on usefulness, selectivity, traceability, inference discipline, ambiguity handling, and actionability.
```

### Human review questions
After Copilot critiques the report, ask yourself:
1. Did this actually reduce my confusion?
2. Did it choose the right components?
3. Did the evidence make me trust the analysis?
4. Did the ambiguity section reveal what I still need to learn?
5. Did the next steps help me know what to do next?

---

## How to tune after a weak run

Tune by changing the **smallest possible instruction** that fixes the specific failure you saw.

Do **not** rewrite the whole prompt after every run.

### The control files
- `iteration_playbook.md` tells you how to iterate without spiraling
- `selection_criteria.md` controls what gets included
- `evidence_and_inference_policy.md` controls how claims are supported and how inference is handled

### Common failure types
- overinclusion
- wrong component selection
- generic analysis
- weak evidence
- inference too aggressive
- ambiguity not surfaced
- weak next steps

### Map failures to tuning levers

#### If it included too much
Tune **selection criteria**.

Example adjustment:

```text
Only include components that are directly tied to implementation, integration, dependencies, or system behavior relevant to my task. Exclude incidental or weakly connected mentions.
```

#### If it missed what mattered
Tune **task context** and **selection criteria**.

Example adjustment:

```text
Prioritize components that appear to shape architecture, dependency flow, or integration boundaries, even if they are not discussed the longest.
```

#### If it felt generic
Strengthen the **why-it-matters** requirement.

Example adjustment:

```text
For each selected component, explain why it matters to my work before describing what it does. Avoid generic definitions.
```

#### If evidence was weak
Strengthen the **evidence selection** rule.

Example adjustment:

```text
For every selected component, choose 2–4 short excerpts that directly support its significance, relationship to other components, or key constraint. Prefer stronger evidence over more evidence.
```

#### If inference was too aggressive
Tighten the **inference** rule.

Example adjustment:

```text
When evidence is incomplete, prefer stating unresolved ambiguity over making a weak inference. Only include inference when the transcript strongly implies the conclusion.
```

#### If ambiguity was hidden
Strengthen the **ambiguity handling** rule.

Example adjustment:

```text
Explicitly surface important missing context when it blocks understanding of architecture, ownership, or next steps. Do not smooth over unresolved uncertainty.
```

#### If next steps were weak
Strengthen the **actionability** rule.

Example adjustment:

```text
Possible Next Things to Investigate should name specific components, relationships, terms, or people, not generic research suggestions.
```

### Safe tuning loop
1. Run one transcript
2. Review the output
3. Identify the primary failure type
4. Make one change only
5. Rerun
6. Keep or revert the change

### Copilot tuning prompt

```text
Review #docs/transcript_context_report.md and tell me which of these areas needs tuning most:

- selection
- evidence
- inference
- ambiguity handling
- next-step actionability

Use:
- #iteration_playbook.md
- #selection_criteria.md
- #evidence_and_inference_policy.md

Output exactly:
1. Primary failure type
2. Why it failed
3. Smallest prompt change to try next
4. Which file that change is grounded in
5. Revised instruction text
```

### What to avoid
Do not:
- rewrite the whole prompt after every run
- change many levers at once
- keep adding instructions forever
- optimize for prettier wording instead of better usefulness

---

## Practical end-to-end workflow

1. **Consolidate the spec**  
   Use the 7 agent-driving files to create one runtime-ready agent prompt.

2. **Generate `task.md`**  
   Use your user story description and acceptance criteria to create a safe, high-level task context file.

3. **Run transcript analysis**  
   Use the runtime prompt + `task.md` + `transcript.vtt` to generate the transcript context report.

4. **Review the report**  
   Use the evaluation prompt with:
   - `v1_acceptance_criteria.md`
   - `failure_modes_and_antipatterns.md`

5. **Tune carefully if needed**  
   Use:
   - `iteration_playbook.md`
   - `selection_criteria.md`
   - `evidence_and_inference_policy.md`

6. **Repeat only as needed**  
   Keep the iteration tight and deliberate.
