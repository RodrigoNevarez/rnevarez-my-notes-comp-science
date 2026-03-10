# V1 Product Definition

## Product name
AI Transcript Context Extractor

## Purpose
Turn dense meeting transcripts into analyst-style notes that surface the technical context most likely to help the user understand their work.

## Core user problem
The user does not yet have enough context to clearly understand the deliverable. Transcript overload is blocking architectural understanding and task clarity.

## Primary user need
The tool must help the user:
- understand which components matter to their work
- understand how those components relate to each other
- identify dependencies, risks, and constraints
- identify who may hold missing context
- identify what to investigate next

## V1 outcome
Given one transcript, generate a selective report that highlights only the components most likely to affect the user’s task and explains why they matter.

## V1 scope
V1 should:
- process one transcript at a time
- prioritize technical architecture and system relationships
- focus on task-relevant components only
- produce concise analyst-style notes
- include short evidence excerpts
- separate explicit facts from inference
- mention relevant owners/experts when useful
- surface important but insufficiently explained terms
- end with a short system picture and next-investigation list

## V1 non-goals
V1 should not:
- generate a generic meeting summary
- capture every component mentioned
- merge multiple transcripts into a single view
- use confidence scoring
- act like a rigid schema-first extractor for the user-facing output
- include non-technical discussion unless it materially affects context

## Key design choices
- Depth of understanding over speed of scanning
- Analyst notes over strict structured schema
- Components as primary anchors
- Why it matters before what it does
- Relevance to task before centrality to architecture
- Traceability through short evidence excerpts
- Careful inference allowed, but explicitly labeled

## User-facing output sections
1. Important Components
2. System Picture
3. Important but Insufficiently Explained
4. Possible Next Things to Investigate

## Success definition
The tool is successful if reading one report gives the user a clearer mental model of the architecture, stronger clues about what affects their work, and concrete next steps for reducing ambiguity.
