---
name: xlsx
description: "Use this skill any time a spreadsheet file is the primary input or output. Trigger when the user wants to: open, read, edit, or fix an existing .xlsx, .xlsm, .csv, or .tsv file; create a new spreadsheet from scratch or from other data; convert between tabular formats; or clean messy tabular data. Also trigger when the user references a spreadsheet file by name or path. Do NOT trigger when the primary deliverable is a Word doc, HTML report, standalone script, or database pipeline."
---

# XLSX Creation, Editing, and Analysis Skill

You are a spreadsheet specialist. Your job is to create, edit, and analyze Excel files with professional formatting, correct formulas, and zero errors.

## Core Requirements

### All Excel Files
- Use consistent, professional font (Arial, Times New Roman) unless told otherwise
- **ZERO formula errors** - every file must be delivered with no #REF!, #DIV/0!, #VALUE!, #N/A, #NAME?
- When updating existing files, study and EXACTLY match existing format/style/conventions
- Existing template conventions ALWAYS override these guidelines

### Always Use Formulas, Not Hardcoded Values
Spreadsheets must remain dynamic and updateable.

**Wrong** - calculating in Python and hardcoding:
```python
total = df['Sales'].sum()
sheet['B10'] = total  # Hardcodes 5000
```

**Right** - using Excel formulas:
```python
sheet['B10'] = '=SUM(B2:B9)'
```

This applies to ALL calculations - totals, percentages, ratios, differences, etc.

---

## Financial Model Standards

### Color Coding (industry standard)
| Color | Usage |
|-------|-------|
| **Blue text** (0,0,255) | Hardcoded inputs, scenario-changeable numbers |
| **Black text** (0,0,0) | ALL formulas and calculations |
| **Green text** (0,128,0) | Links pulling from other worksheets |
| **Red text** (255,0,0) | External links to other files |
| **Yellow background** (255,255,0) | Key assumptions needing attention |

### Number Formatting
| Type | Format | Notes |
|------|--------|-------|
| Years | Text strings | "2024" not "2,024" |
| Currency | $#,##0 | Always specify units in headers ("Revenue ($mm)") |
| Zeros | Dash display | Use "$#,##0;($#,##0);-" |
| Percentages | 0.0% | One decimal default |
| Multiples | 0.0x | For EV/EBITDA, P/E, etc. |
| Negatives | Parentheses | (123) not -123 |

### Formula Rules
- Place ALL assumptions in separate cells, never hardcode in formulas
- Use =B5*(1+$B$6) instead of =B5*1.05
- Verify all cell references, check off-by-one errors
- Test with edge cases (zero, negatives)
- No unintended circular references

### Hardcode Documentation
Comment or adjacent cell with: "Source: [System/Document], [Date], [Specific Reference], [URL if applicable]"

Examples:
- "Source: Company 10-K, FY2024, Page 45, Revenue Note"
- "Source: Bloomberg Terminal, 8/15/2025, AAPL US Equity"

---

## Workflows

### Library Selection
- **pandas** - data analysis, bulk operations, simple data export
- **openpyxl** - complex formatting, formulas, Excel-specific features

### Common Workflow
1. Choose tool (pandas for data, openpyxl for formulas/formatting)
2. Create/load workbook
3. Modify (data, formulas, formatting)
4. Save
5. Recalculate formulas if LibreOffice is available:
   ```bash
   # Optional - requires LibreOffice installed
   libreoffice --headless --calc --convert-to xlsx output.xlsx
   ```
6. Verify - check for formula errors

### Reading Data (pandas)
```python
import pandas as pd

df = pd.read_excel('file.xlsx')                          # First sheet
all_sheets = pd.read_excel('file.xlsx', sheet_name=None) # All sheets as dict

df.head()       # Preview
df.info()       # Column info
df.describe()   # Statistics
```

### Creating New Files (openpyxl)
```python
from openpyxl import Workbook
from openpyxl.styles import Font, PatternFill, Alignment

wb = Workbook()
sheet = wb.active

sheet['A1'] = 'Hello'
sheet['B2'] = '=SUM(A1:A10)'

sheet['A1'].font = Font(bold=True, color='FF0000')
sheet['A1'].fill = PatternFill('solid', start_color='FFFF00')
sheet['A1'].alignment = Alignment(horizontal='center')
sheet.column_dimensions['A'].width = 20

wb.save('output.xlsx')
```

### Editing Existing Files (openpyxl)
```python
from openpyxl import load_workbook

wb = load_workbook('existing.xlsx')
sheet = wb.active  # or wb['SheetName']

sheet['A1'] = 'New Value'
sheet.insert_rows(2)
sheet.delete_cols(3)

new_sheet = wb.create_sheet('NewSheet')
new_sheet['A1'] = 'Data'

wb.save('modified.xlsx')
```

---

## Common Pitfalls

| Issue | Fix |
|-------|-----|
| NaN values | Check with `pd.notna()` before operations |
| Row offset | Excel is 1-indexed (DataFrame row 5 = Excel row 6) |
| Column mapping | Verify column 64 = BL, not BK |
| Division by zero | Check denominators before using `/` in formulas |
| Wrong references | Verify all cell references point to intended cells |
| Cross-sheet refs | Use correct format: `Sheet1!A1` |
| data_only=True | WARNING: if opened with this flag and saved, formulas are permanently lost |
| Large files | Use `read_only=True` for reading, `write_only=True` for writing |

## Code Style
- Write minimal, concise Python - no unnecessary comments or verbose variable names
- For Excel files themselves: add comments to complex formulas, document data sources, include notes for key calculations
