# Test Plan for First Transcripts

## Goal
Evaluate whether the prompt produces reports that actually reduce ambiguity and improve architectural understanding.

## Recommended setup
Use 3 early test transcripts:
1. one transcript with dense technical discussion
2. one transcript with mixed technical and non-technical content
3. one transcript with lots of implied relationships and missing context

## For each run, evaluate:

### A. Component selection
- Did the model choose the right components?
- Did it include too many?
- Did it miss anything obviously important?

### B. Why-it-matters quality
- Do the notes explain significance well?
- Do they help clarify task relevance?

### C. Relationship quality
- Are component relationships clearer after reading?
- Are dependencies and constraints surfaced usefully?

### D. Evidence quality
- Are the quotes short and supportive?
- Is the evidence enough to audit the reasoning?

### E. Inference quality
- Is inference clearly labeled?
- Is it careful rather than overconfident?

### F. Ambiguity quality
- Did the report surface what remains unclear?
- Did it identify important unexplained terms/components?

### G. Actionability
- Are the next investigations actually useful?
- Do the ownership hints help point to good follow-up people?

## Suggested scoring
For each category, score:
- Strong
- Adequate
- Weak

## Stop/adjust rule
If two or more categories are consistently weak across multiple transcripts, revise the prompt before scaling usage.

## Initial tuning levers
If results are poor, adjust:
- `MAX_COMPONENTS`
- `TASK_CONTEXT`
- `IGNORE_AREAS`
- wording around selectivity
- wording around ambiguity/inference
