# ContextZip

### Loss-Aware Context Compression for Large Language Models

ContextZip is a lightweight prompt framework that compresses prompts, conversations, technical logs, and documents while preserving reasoning-critical information.

Instead of generating traditional summaries, ContextZip focuses on keeping the information that affects future reasoning and decision-making while removing unnecessary token consumption.

---

## Why ContextZip?

Large Language Models often waste context window capacity on:

- Repeated information
- Conversational filler
- Emotional language
- Outdated context
- Verbose descriptions

As conversations become longer, token costs increase and model performance may degrade due to context dilution.

ContextZip solves this problem by extracting only the information required for future reasoning.

---

## Features

### Prompt Compression

Transform verbose prompts into compact and structured instructions.

### Conversation Compression

Convert long chat histories into reusable memory blocks.

### Technical Log Compression

Extract errors, root causes, affected components, and troubleshooting steps.

### Project Context Compression

Turn large project descriptions into concise technical context.

### Document Compression

Reduce lengthy documents into actionable summaries while preserving key facts.

---

## Example

### Original Input

I am currently maintaining a Weaver E9 deployment running on TongWeb with DM Database. Recently the portal news module started throwing exceptions. I checked the server resources and database connectivity and both appear healthy. I need help identifying the root cause.

### Compressed Output

Task:
Investigate Weaver E9 portal news exception

Environment:
- Weaver E9
- TongWeb
- DM Database

Verified:
- Database connection OK
- System resources normal

Issue:
- DMException: String conversion error

Estimated Reduction:
80%

---

## Compression Principles

### Preserve

Always keep:

- Objectives
- Constraints
- Technical facts
- Dates
- Numbers
- Decisions
- Dependencies
- Open issues

### Remove

Always remove:

- Greetings
- Emotional language
- Repetition
- Filler content
- Irrelevant history

### Structure

Represent information using:

- Bullet lists
- Key-value pairs
- Hierarchical summaries

### Minimize

Use the smallest possible token footprint without changing meaning.

---

## Universal Compression Prompt

You are ContextZip, a loss-aware context compression engine.

Goal:

Compress user input into the smallest possible token footprint while preserving all information necessary for future reasoning.

Rules:

1. Remove greetings, filler words, and emotional language.
2. Remove duplicate information.
3. Merge similar statements.
4. Preserve:
   - Objectives
   - Constraints
   - Key facts
   - Dates
   - Numbers
   - Technical details
   - Decisions made
   - Outstanding problems
5. Use bullet points whenever possible.
6. Do not answer the user's question.
7. Only output the compressed context.

Output Format:

Task:
<Primary objective>

Context:
- Key information

Constraints:
- Limitations or requirements

Known Facts:
- Verified information

Open Issues:
- Current problems

Compression Estimate:
- Estimated reduction percentage

---

## Expected Results

| Content Type | Typical Reduction |
|-------------|------------------|
| Prompts | 50% - 80% |
| Conversations | 80% - 95% |
| Technical Logs | 70% - 90% |
| Documents | 60% - 90% |

Actual results depend on content quality and redundancy.

---

## Use Cases

- AI Agents
- Long-Term Memory Systems
- RAG Pipelines
- Customer Support Bots
- Coding Assistants
- DevOps Assistants
- Enterprise Knowledge Bases
- Research Workflows

---

## Roadmap

- [ ] Multi-level compression modes
- [ ] Context quality scoring
- [ ] Prompt benchmarking
- [ ] Agent memory optimization
- [ ] Automatic token reduction reports

---

## Philosophy

The goal is not to summarize.

The goal is to preserve reasoning while minimizing tokens.

---

## License

MIT License
