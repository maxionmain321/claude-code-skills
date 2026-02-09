# QA Checklist: Ship-Ready Email Standards

Run this checklist before sending ANY cold email. If any item fails, fix it before shipping.

---

## 1. Personalization Quality

**✅ First line references a specific signal**
- Custom research signal with {{variable}}, OR
- AI-generated insight based on their company, OR
- Whole-offer strategy (subject + preview = full offer)

**✅ No hallucinations**
- Every fact is verifiable (from research, website, LinkedIn, tools)
- If you can't verify it, remove it
- Don't invent: job titles, metrics, dates, technologies

**✅ Variables are properly formatted**
- Use `{{double_braces}}` consistently
- No typos in variable names
- Variables match your data source (Clay column names)

**❌ FAIL examples:**
- "I saw you recently expanded..." (when? where? prove it)
- "Your team has been growing fast" (how do you know?)
- {{firstName}} (wrong format, should be {{first_name}})

---

## 2. Banned Phrases (Delete These)

**Generic openers:**
- ❌ "I hope this email finds you well"
- ❌ "I wanted to reach out"
- ❌ "I hope you're doing well"
- ❌ "Just wanted to touch base"

**Weak value props:**
- ❌ "We help companies..." (unless immediately followed by case study proof)
- ❌ "Our solution..."
- ❌ "I wanted to show you..."

**High-pressure CTAs:**
- ❌ "Would love to schedule..."
- ❌ "Let's hop on a call"
- ❌ "Can I get 15 minutes on your calendar?"

**Replacements:**
- ✅ Start with their situation
- ✅ "We helped [customer type] achieve [metric]"
- ✅ "Worth a quick look?" / "Worth exploring?"

---

## 3. Recipient:Sender Ratio

**Count sentences:**
- About THEM (situation, pain, their goals): ____
- About US (our product, our features, our ask): ____

**Target ratio: 3:1 (them:us) minimum**
- If ratio is 1:1 or worse → Rewrite to focus on them

**Good example:**
```
✅ Saw you hired 4 SEs last quarter—building custom workflows for every deal? (THEM)
✅ Most teams hit a wall at deal #30 when workflows don't scale. (INSIGHT)
✅ Worth a look? (LOW-EFFORT CTA)

Ratio: 2 sentences about them, 1 about solution = 2:1 ✅
```

**Bad example:**
```
❌ We help companies build custom workflows. (US)
❌ Our platform has been used by 500+ companies. (US)
❌ We'd love to show you how it works. (US)

Ratio: 0:3 = All about us ❌
```

---

## 4. Length & Punchiness Check

**Target: 50-90 words (not 60-120—tighter is better)**
- Count words (not including signature)
- If >90 words → Cut aggressively until under 90
- Then cut 10 more words
- Every sentence must earn its place

**The 20-Second Rule:**
- Read it aloud
- If it takes longer than 20 seconds → Too long
- Aim for 15 seconds

**Fluff indicators (delete these):**
- ❌ "I wanted to reach out because..."
- ❌ "I was wondering if..."
- ❌ "Just checking in to see..."
- ❌ Extra adjectives ("innovative solution", "cutting-edge platform")
- ❌ Explaining everything ("We help companies by providing...")

**Punchy alternatives:**
- ✅ Start with their situation
- ✅ Use 1-2 word transitions ("Curious:", "Worth exploring?")
- ✅ Cut all adjectives that don't add specificity
- ✅ Replace clauses with periods (break long sentences)

**Example transformation:**
```
Before (112 words):
"I hope this email finds you well! I wanted to reach out because I was on your website and I noticed that you seem to be selling to sales leaders and marketing executives. It looked like you're trying to help them improve their outbound processes and increase their pipeline generation. I had to assume you are probably using some outbound tactics considering I saw that John Smith is a BDR on your team based on his LinkedIn profile. I was wondering if you're thinking about how your team could be leveraging better data enrichment and GPT-4 technology to help streamline their prospecting efforts and make them more efficient?"

After (64 words):
"{{First_name}}—saw you sell to {{job_titles}}.

Noticed {{SDR_name}} is a BDR on the team. Have you figured out how they could leverage better data and GPT-4 for prospecting, or still manual?

Most teams we work with save 10 min per prospect and 3x volume without adding headcount.

Worth a look?"
```

**What was cut:**
- All pleasantries (18 words)
- All "I wanted to" phrases (12 words)
- All assumptions stated explicitly (8 words)
- Redundant explanations (10 words)
- Total: 48 words cut = 43% shorter

**What was kept:**
- Situation (their ICP, their SDR)
- Question (poke the bear)
- Metric (10 min, 3x volume)
- CTA (simple)

**Cutting checklist:**
- ☐ Remove greeting ("I hope this finds you well")
- ☐ Remove "I wanted to" phrases
- ☐ Remove redundant context
- ☐ Combine sentences where possible
- ☐ Replace long phrases with short ones
- ☐ Delete adjectives unless they're specific data

---

## 5. CTA Quality

**✅ Low-effort reply test**
- Can they reply in 5 words or less?
- Is it a yes/no question?
- Is it confirming a detail?

**Good CTAs:**
- ✅ "Worth a quick look?"
- ✅ "Is this still the case?"
- ✅ "Curious—are you already doing X?"
- ✅ "Just confirm [example] or any others"

**Bad CTAs:**
- ❌ "Can we schedule 15 minutes?" (high effort, requires calendar check)
- ❌ "Let me know your thoughts" (vague, what thoughts?)
- ❌ "Would you be interested in learning more?" (requires thinking)

**Value-exchange CTAs** (when asking for meeting):
- ✅ "...so I can [do specific thing for them]"
- ✅ "...to walk you through [specific deliverable]"
- ✅ "...so I can show you [concrete example]"

---

## 6. Tone & Clarity

**✅ Reads naturally aloud**
- Read it out loud
- Does it sound like a human wrote it?
- Or does it sound like a template/robot?

**✅ Helpful, confident, conversational**
- Not pushy or aggressive
- Not overly formal or stiff
- Not desperate or begging

**✅ Clear value proposition**
- After reading, they should know: What you do, how it helps them, what happens next
- If unclear → Simplify

**✅ About THEIR situation (not your product)**
- Focus: Their pain, their situation, their goals
- Not focus: Your features, your company, your awards

---

## 7. Punctuation & Formatting

**✅ Em dashes are consistent**
- Use: "—" (proper em dash)
- Not: "--" or "–" (hyphens or en dash)
- Spacing: No spaces around em dash (e.g., "research—not just")

**✅ No double spaces**
- Find/replace "  " (two spaces) → " " (one space)

**✅ Variables closed correctly**
- `{{variable_name}}` ✅
- `{{ variable_name }}` ✅ (spaces ok)
- `{variable_name}` ❌ (single braces)
- `{{variableName}}` ❌ (camelCase usually wrong, use snake_case)

**✅ Plain text (no formatting)**
- No bold, italics, colors
- No bullet points (unless Creative Ideas campaign)
- No images or attachments

---

## 8. Subject Line Check

**Standard (2-4 words):**
- ✅ "Partnership?"
- ✅ "Quick question"
- ✅ "Competitor insights"
- ✅ "Saw your post"

**Whole offer (can be longer):**
- ✅ "Ever chase renters to pay on time?"
- ✅ When using this strategy, first line must complete the offer

**Tests:**
- Could a colleague send this? ✅
- Could a potential customer send this? ✅
- Does it sound like a sales pitch? ❌

**Avoid:**
- ❌ "Quick question about your infrastructure" (explaining, not intriguing)
- ❌ "Excited to connect!" (salesy)
- ❌ "Following up on my previous email" (Email 1 shouldn't say this)

---

## 9. Case Study / Social Proof Check

**If using case studies:**
- ✅ Include specific metric ("4.7x increase", "23% improvement")
- ✅ Include timeframe ("within 90 days", "first quarter")
- ✅ Include customer type ("Series B SaaS", "e-commerce brands")

**Avoid generic claims:**
- ❌ "We've helped hundreds of customers" (who? how?)
- ❌ "We've been doing this for 10 years" (so what?)

**Situational social proof > Name dropping:**
- ✅ "Most fintech teams hit this problem around month 3..."
- ❌ "We work with Stripe and Coinbase"

---

## 10. The "Would I Reply?" Test

**Put yourself in recipient's shoes:**

Ask honestly:
1. Do they understand MY specific situation? (not just my industry)
2. Is there a non-obvious insight I didn't know? (not just claims)
3. Is it low-effort to reply? (not asking for a big commitment)
4. Is there a good reason to engage NOW? (not just "let's chat someday")

If you answer "no" to any of these → Rewrite before sending.

---

## Autofix Rules

When running automated QA, apply these fixes:

**Punctuation:**
1. Replace "–" with "—" (en dash → em dash)
2. Replace "--" with "—" (double hyphen → em dash)
3. Trim double spaces globally

**Variables:**
1. If first line lacks a variable → Insert researched signal OR flag for manual review
2. If variable format is wrong `{single}` → Fix to `{{double}}`

**Banned phrases:**
1. If found → Delete and rewrite surrounding sentence
2. "I hope this finds you well" → Delete, start with situation
3. "We help companies..." → Rewrite as "We helped [customer type] achieve [metric]"

**Length:**
1. If >120 words → Flag for manual review (cut or justify)
2. If <30 words → Flag (might be too short, unless ultra-tight variant)

**CTA:**
1. If asking for "15 minutes" or "30 minutes" → Rewrite to lower-effort
2. If no CTA → Add one (every email needs a clear next step)

---

## QA Scoring Sheet

Use this to score emails before shipping:

| Criteria | Pass/Fail | Notes |
|----------|-----------|-------|
| First line has specific signal | ☐ Pass ☐ Fail | |
| No hallucinations | ☐ Pass ☐ Fail | |
| Variables formatted correctly | ☐ Pass ☐ Fail | |
| No banned phrases | ☐ Pass ☐ Fail | |
| Recipient:sender ratio ≥ 3:1 | ☐ Pass ☐ Fail | |
| **50-90 words (strict)** | ☐ Pass ☐ Fail | |
| CTA is low-effort | ☐ Pass ☐ Fail | |
| Reads in under 20 seconds | ☐ Pass ☐ Fail | |
| Em dashes consistent | ☐ Pass ☐ Fail | |
| Subject line 2-4 words (or whole offer) | ☐ Pass ☐ Fail | |
| "Would I reply?" test = YES | ☐ Pass ☐ Fail | |

**All must pass before shipping.**

---

## Quick QA Workflow

**60-second check:**
1. Read aloud → Sound natural?
2. Count "them" vs "us" → Ratio good?
3. Check first line → Specific signal?
4. Check CTA → Low-effort?
5. Word count → 60-120?

**If all YES → Ship it**
**If any NO → Fix and re-check**

---

## Common QA Failures & Fixes

### Failure 1: "Too generic, could send to anyone"
**Fix:** Add specific signal from research
- Before: "I noticed you're growing fast"
- After: "Saw you hired 4 SDRs last quarter"

### Failure 2: "Too long, lost focus"
**Fix:** Cut ruthlessly, keep only essential info
- Before: 200-word email with background, features, benefits, case study
- After: 80-word email with situation + insight + question

### Failure 3: "CTA is too high-effort"
**Fix:** Lower the bar
- Before: "Can we schedule 30 minutes next week?"
- After: "Worth a quick look?"

### Failure 4: "Sounds like a template"
**Fix:** Add specific data about them
- Before: "We help companies like yours"
- After: "We helped {{case_study_customer_type}} achieve {{metric}}"

### Failure 5: "No clear reason to reply"
**Fix:** Add insight or value-exchange
- Before: "Let me know if you're interested"
- After: "Curious if you're already doing X, or still manual?"

---

## Final Checklist (Print & Use)

```
Campaign: _______________
Date: _______________

Pre-Send QA:
☐ First line = specific signal
☐ No hallucinations
☐ Variables formatted {{correctly}}
☐ No banned phrases
☐ Ratio check: ____ them : ____ us (need ≥ 2:1)
☐ Word count: ____ (target 60-120)
☐ CTA = low-effort
☐ Reads naturally aloud
☐ Em dashes consistent (—)
☐ Subject line = 2-4 words OR whole offer
☐ "Would I reply?" = YES

All boxes checked? → SHIP IT
Any box unchecked? → FIX & RE-CHECK
```

---

## Remember

**Your goal is not perfection. Your goal is "would I reply to this?"**

If yes → Ship it
If no → Fix it

Don't overthink. Do the QA. Trust the process.