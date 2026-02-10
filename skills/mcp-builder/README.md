# MCP Builder Skill

Guide for creating MCP (Model Context Protocol) servers that enable LLMs to interact with external services.

## What This Skill Does

When triggered, Claude becomes an MCP server development specialist that walks you through the full build process:

1. **Research & Planning** - Study API docs, plan tool mapping, choose transport
2. **Implementation** - Project structure, shared utilities, tool-by-tool build
3. **Review & Test** - Code quality, MCP Inspector testing
4. **Evaluation** - Generate test questions to validate LLM usability

## When to Use

Trigger when you mention:
- "MCP server"
- "build MCP"
- "MCP tool"
- "model context protocol"
- "integrate API with Claude"

## Key Decisions

| Choice | Recommendation |
|--------|---------------|
| Language | TypeScript (best SDK support) |
| Remote transport | Streamable HTTP |
| Local transport | stdio |
| Schema validation | Zod (TS) / Pydantic (Python) |
| Testing | MCP Inspector |

## Setup

Add to your `.claude/skills/` directory:

```
.claude/skills/mcp-builder/
  SKILL.md    # Full guide (Claude reads this)
  README.md   # This file
```

Claude will automatically use this skill when you ask about building MCP servers.
