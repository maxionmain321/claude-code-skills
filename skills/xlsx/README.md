# XLSX Skill

Spreadsheet specialist skill for creating, editing, and analyzing Excel files with professional formatting and zero formula errors.

## What This Skill Does

When triggered, Claude becomes a spreadsheet specialist that handles:
- Creating new .xlsx files with proper formatting and formulas
- Editing existing spreadsheets while matching existing conventions
- Financial model standards (color coding, number formatting)
- Data analysis and conversion between tabular formats

## When to Use

Trigger when:
- Opening, reading, editing, or fixing .xlsx, .xlsm, .csv, or .tsv files
- Creating new spreadsheets from scratch or from other data
- Converting between tabular formats
- Cleaning messy tabular data
- User references a spreadsheet file by name or path

Do NOT trigger when the primary deliverable is a Word doc, HTML report, standalone script, or database pipeline.

## Key Standards

- **Zero formula errors** - no #REF!, #DIV/0!, #VALUE!, #N/A, #NAME?
- **Always use formulas** - never hardcode calculated values
- **Industry color coding** - blue (inputs), black (formulas), green (cross-sheet links), red (external links)
- **Source documentation** - every hardcoded value gets a source comment

## Setup

Add to your `.claude/skills/` directory:

```
.claude/skills/xlsx/
  SKILL.md    # Full guide (Claude reads this)
  README.md   # This file
```
