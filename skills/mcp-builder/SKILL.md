---
name: mcp-builder
description: Guide for creating MCP (Model Context Protocol) servers that enable LLMs to interact with external services. Use when the user mentions "MCP server," "build MCP," "MCP tool," "model context protocol," or "integrate API with Claude."
---

# MCP Server Development Guide

You are an MCP server development specialist. Your job is to guide users through building high-quality MCP servers - from API research through implementation, testing, and evaluation.

## High-Level Workflow

Four phases: Research/Plan, Implement, Review/Test, Evaluate.

---

## Phase 1: Deep Research and Planning

### 1.1 Modern MCP Design Principles

**API Coverage vs. Workflow Tools:**
Balance comprehensive API endpoint coverage with specialized workflow tools. When uncertain, prioritize comprehensive API coverage - it gives agents flexibility to compose operations.

**Tool Naming:**
Clear, descriptive, consistent prefixes. Action-oriented naming (e.g., `github_create_issue`, `github_list_repos`).

**Context Management:**
Concise tool descriptions. Return focused, relevant data. Support filtering/pagination.

**Error Messages:**
Actionable - guide agents toward solutions with specific suggestions and next steps.

### 1.2 Study MCP Protocol Docs

Start with the sitemap: `https://modelcontextprotocol.io/sitemap.xml`

Fetch specific pages with `.md` suffix (e.g., `https://modelcontextprotocol.io/specification/draft.md`).

Key areas:
- Specification overview and architecture
- Transport mechanisms (streamable HTTP, stdio)
- Tool, resource, and prompt definitions

### 1.3 Study Framework Docs

**Recommended stack:** TypeScript with streamable HTTP (remote) or stdio (local).

**SDK docs - fetch as needed:**
- **TypeScript SDK**: `https://raw.githubusercontent.com/modelcontextprotocol/typescript-sdk/main/README.md`
- **Python SDK**: `https://raw.githubusercontent.com/modelcontextprotocol/python-sdk/main/README.md`

### 1.4 Plan Implementation

1. Review the target API docs (endpoints, auth, data models)
2. List endpoints to implement, starting with most common operations
3. Map API concepts to MCP tool names
4. Identify shared utilities needed (auth, pagination, error handling)

---

## Phase 2: Implementation

### 2.1 Project Structure

**TypeScript (recommended):**
```
my-mcp-server/
  src/
    index.ts          # Server entry point
    tools/            # Tool implementations
    utils/            # Shared helpers (auth, pagination, errors)
  package.json
  tsconfig.json
```

**Python:**
```
my_mcp_server/
  server.py           # Server entry point
  tools/              # Tool implementations
  utils/              # Shared helpers
  requirements.txt
```

### 2.2 Core Infrastructure

Build these shared utilities first:
- API client with authentication
- Error handling helpers (actionable messages)
- Response formatting (JSON/Markdown)
- Pagination support

### 2.3 Implement Each Tool

For every tool, define:

**Input Schema:**
- Zod (TypeScript) or Pydantic (Python)
- Include constraints and clear descriptions
- Add examples in field descriptions

**Output Schema:**
- Define `outputSchema` where possible for structured data
- Use `structuredContent` in tool responses

**Annotations:**
- `readOnlyHint`: true/false
- `destructiveHint`: true/false
- `idempotentHint`: true/false
- `openWorldHint`: true/false

**Implementation checklist per tool:**
- Async/await for I/O operations
- Proper error handling with actionable messages
- Pagination support where applicable
- Return both text content and structured data

---

## Phase 3: Review and Test

### Code Quality Review
- No duplicated code (DRY)
- Consistent error handling
- Full type coverage
- Clear tool descriptions

### Build and Test

**TypeScript:**
```bash
npm run build
npx @modelcontextprotocol/inspector
```

**Python:**
```bash
python -m py_compile your_server.py
# Test with MCP Inspector
```

---

## Phase 4: Create Evaluations

Create 10 evaluation questions to test whether LLMs can effectively use your MCP server.

### Question Requirements
Each question must be:
- **Independent** - not dependent on other questions
- **Read-only** - only non-destructive operations required
- **Complex** - requiring multiple tool calls
- **Realistic** - based on real use cases
- **Verifiable** - single, clear answer (string comparison)
- **Stable** - answer won't change over time

### Process
1. List available tools and understand capabilities
2. Use READ-ONLY operations to explore available data
3. Generate 10 complex, realistic questions
4. Solve each yourself to verify answers

### Output Format
```xml
<evaluation>
  <qa_pair>
    <question>Your complex question here</question>
    <answer>Verified answer</answer>
  </qa_pair>
  <!-- More qa_pairs... -->
</evaluation>
```

---

## Quick Reference

| Decision | Recommendation |
|----------|---------------|
| Language | TypeScript (best SDK support, good AI code generation) |
| Transport (remote) | Streamable HTTP, stateless JSON |
| Transport (local) | stdio |
| Schema validation | Zod (TS) or Pydantic (Python) |
| Testing | MCP Inspector |
| API coverage | Comprehensive > workflow-specific (when uncertain) |
