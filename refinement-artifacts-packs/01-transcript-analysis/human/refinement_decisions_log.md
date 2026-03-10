# Refinement Decisions Log

## Decisions locked in

### Problem framing
- The immediate deliverable is clarity.
- The tool exists to reduce ambiguity, not just summarize transcripts.

### Priority of value
- Primary priority: task relevance
- Secondary priority: architectural/system understanding
- Supporting value: project direction
- Ownership is included when it helps follow-up

### Output style
- Analyst notes, not a rigid schema-first user-facing output
- Fixed top-level template with adaptive detail inside each section

### Input scope
- One transcript at a time

### Selection logic
- Only include components likely to affect the user’s task
- Do not try to list everything mentioned
- Ignore low-value or incidental components

### Technical emphasis
- Focus on systems/components
- Emphasize how components relate to each other
- Organize around components, not relationships alone
- For each component, explain why it matters first

### Evidence policy
- Include a separate Evidence subsection for each component
- Use several quotes, but keep them short
- Prefer selective evidence over transcript dumping

### Inference policy
- Include inference when it adds value
- Label inference clearly
- Allow careful inference in the system picture as well

### Ambiguity handling
- Include ambiguity only when it adds value
- Call out important terms/components that are insufficiently explained
- End with possible next things to investigate

### Ownership handling
- Mention people’s names and likely ownership when relevant
- Use this mainly to identify who to ask for more context

### Noise filtering
- Ignore non-technical discussion unless it affects task relevance, ownership, decisions, or system understanding

## Strategic summary
V1 is a one-transcript analyst that surfaces only the most task-relevant technical components, explains why they matter, shows evidence, identifies ambiguity, and suggests what to investigate next.
