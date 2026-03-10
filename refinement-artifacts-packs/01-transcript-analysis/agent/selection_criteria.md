# Selection Criteria

## Include a component when it is likely to affect:
- implementation
- integration
- dependencies
- system behavior
- architectural understanding
- the user’s ability to figure out what to do next

## Strong inclusion signals
Include a component when the transcript suggests that it:
- plays a meaningful role in the architecture
- interacts with other components in a way that matters
- creates a dependency or constraint
- introduces risk, caveats, or important tradeoffs
- appears relevant to the user’s likely task
- is repeatedly referenced as important
- is tied to missing context the user needs

## Exclude a component when it is:
- incidental
- too vague to be useful
- mentioned in passing without architectural significance
- not connected to task relevance
- pure meeting logistics or administrative noise

## Prioritization rule
If too many components qualify, prefer the ones that best help the user:
1. understand the architecture
2. understand relationships between parts
3. identify important dependencies or constraints
4. identify the best next research paths
5. identify who may hold missing context

## Quota discipline
Do not fill a maximum component count unless the transcript genuinely supports it.
