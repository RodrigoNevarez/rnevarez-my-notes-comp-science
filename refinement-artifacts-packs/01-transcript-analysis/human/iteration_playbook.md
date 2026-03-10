# Iteration Playbook

## Goal
Refine the prompt in a disciplined way without turning prompt work into its own endless project.

## After each test run
Ask:
1. Did the report reduce ambiguity?
2. Did it choose the right components?
3. Did it over-summarize the meeting?
4. Did it explain relationships well?
5. Did the evidence support the analysis?
6. Did the next steps feel actionable?

## Common prompt adjustments

### If too many components are included
- lower `MAX_COMPONENTS`
- strengthen the task-relevance filter
- tighten `IGNORE_AREAS`

### If the analysis is too generic
- strengthen “why it matters”
- reinforce architectural relationships
- add more concrete task context

### If inference becomes too aggressive
- strengthen the ambiguity rule
- explicitly prefer unresolved ambiguity over weak inference

### If evidence is weak
- require 2–4 excerpts for each included component
- remind the model to select only the strongest support

### If ownership is noisy
- reinforce that names are only for follow-up value

## Iteration cap
Do not keep tuning forever.
A good rule:
- test prompt
- inspect failure modes
- revise
- retest
- stop after a few meaningful iterations unless a major issue remains

## Scaling rule
Only move to broader transcript usage once:
- selectivity is good
- architectural understanding is improved
- evidence is traceable
- next-step guidance is consistently useful
