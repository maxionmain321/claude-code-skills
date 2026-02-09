# Cold Email Personalization Skill v2.0 - Complete Package

## What This Is

A comprehensive Claude skill for crafting research-driven cold emails with bracketed-variable personalization, "poke the bear" openers, custom signal hunting, and follow-up sequences. Based on Growth Engine X methodology and real campaign examples.

---

## File Structure

```
cold-email-personalization-v2/
├── README.md (this file)
├── SKILL.md (main framework - start here)
├── research-playbook.md (10-min research method with tools)
├── examples.md (10 real campaigns with annotations)
├── frameworks.md (opener patterns & CTA templates)
├── follow-ups.md (Email 1→2→3→4 sequences)
├── creative-ideas-generation.md (how to generate feature-constrained ideas)
├── icp-objection-mapping.md (role-play before writing)
├── qa.md (ship-ready checklist)
└── workflows.md (ready-to-run prompts)
```

---

## Quick Start (5 Minutes)

### 1. Read SKILL.md first
- Core philosophy
- Variable schema
- Two paths: Custom signal vs Whole offer
- Generation workflow

### 2. Pick your campaign type
- **Custom signal** → High research, high personalization
- **Creative ideas** → Show 3 specific ideas
- **Whole offer** → Low data, direct pitch
- **Fallback** → "Let me know if..." redirect

### 3. Do 10-minute research
- Tier 1: Case studies (3 min)
- Tier 2: Custom signals (6-7 min)
- Tier 3: Standard variables (backup)

### 4. Draft using templates
- See examples.md for 10 real campaigns
- Follow structure in SKILL.md
- Use frameworks.md for openers/CTAs

### 5. Run QA checklist
- qa.md has 11-point checklist
- Fix failures before shipping
- "Would I reply?" test

---

## Core Concepts

### The Philosophy

**1. Shorter & Punchier > Longer**
- Target: **50-90 words** (not 60-120)
- Every word must earn its place
- Cut 3 times: fluff (20%), compress (15%), adjectives (10%)
- Should read aloud in under 20 seconds

**2. Research IS the personalization**
- Custom signals > clever copy
- 10-minute research method
- If no signal found → use whole-offer strategy OR skip

**3. Earn replies, not just meetings**
- Confirm situation before selling
- Low-effort CTAs (5 words or less to reply)
- Value-exchange when asking for meetings

**4. Two valid paths**
- **Path A:** Custom signal research (when you have time/data)
- **Path B:** Whole offer strategy (when data is limited)
- Both work—choose based on situation

**5. The "Specifically" line (3x conversion booster)**
> "Specifically, it looks like you're trying to sell to {{customer_type}}, and we can help with that."

Use when your service applies universally but their customers vary.

---

## Tools & Techniques

### Research Tools (in research-playbook.md)

**Claygent:** AI web scraper
- Find pricing pages, case studies, news
- Get summaries quickly
- Feed URLs to ZenRows for full detail

**ZenRows:** Full page scraper
- Get complete text from any page
- Bypass anti-bot protections
- Perfect for pricing pages, reviews

**Serper:** Google search API
- Google Places CID for local businesses
- Reviews (sort by negative/recent)
- News mentions, competitor searches

**SimilarWeb:** Competitor intelligence
- Traffic overlap
- Keyword gaps
- Traffic trends

**LinkedIn:** Manual or scraper
- Recent posts, hiring, follower counts
- Profile updates (new role, tenure)

**BuiltWith/Wappalyzer:** Tech stack detection
- CRM, marketing tools, analytics
- Payment processors, hosting

---

## Campaign Types

### 1. Custom Signal Campaign
**When:** Strong research data available
- Use signal in first line with {{variable}}
- Back with case study proof
- Low-effort CTA

**Example:** Pricing page insights → product video pitch

---

### 2. Creative Ideas Campaign
**When:** Can generate specific, credible ideas
- Define 3-5 features you ACTUALLY offer (constraint box)
- Research their company (5-7 min)
- Generate 3 ideas, one per feature
- Format as bullets with benefits

**Example:** Marketing ideas with paid social, SEO, email (each constrained to capabilities)

**See creative-ideas-generation.md for full workflow**

---

### 3. Whole Offer Campaign
**When:** Limited data or self-selecting offer
- Subject + preview text = entire value prop
- They self-select (need it or don't)
- Light personalization if possible

**Example:** "Ever chase renters to pay on time?" → platform explanation

---

### 4. Fallback Campaign
**When:** Unsure if right person
- "Let me know if {{employee_1}} or {{employee_2}} would be better..."
- Gets personalized with actual employee names
- Gives easy out (forward) or confirms they're right person

---

## Follow-Up Sequences

**See follow-ups.md for complete guide**

### The 3 Offers Framework
Every offer is: Save time, Save money, OR Make money

**Email 1 (Day 0):**
- New subject, full campaign
- Lead with strongest value prop

**Email 2 (Day 3-4):**
- No subject (threads)
- Rotate to different value prop
- Creative ideas or stats/data hook

**Email 3 (Day 7-8):**
- New subject (fresh thread)
- Consider dropping AI
- Use whole-offer OR case study deep dive

**Email 4 (Day 11-12):**
- Final email
- Redirect to another person OR
- Offer resources OR
- Value bomb (show capability)

---

## Subject Line Strategy

**Approach A: 2-4 Words (Intrigue)**
- "Partnership?"
- "Quick question"
- "Competitor insights"
- "Saw your post"

**Approach B: Whole Offer (Can be longer)**
- "Ever chase renters to pay on time?"
- Preview text completes the offer
- Self-selecting

**Test:** Could a colleague or customer send this?

---

## Variable Schema

### Core (always include)
- {{first_name}}, {{company_name}}, {{role_title}}

### High-Signal (when available)
- {{tenure_years}}, {{recent_post_topic}}, {{recent_post_date}}
- {{competitor}}, {{stack_crm}}, {{hiring_roles}}
- {{press_headline}}, {{event_date}}

### AI-Generated (dynamic)
- {{ai_customer_description}}: "fitness enthusiasts who want to breathe better"
- {{ai_customer_type}}: "VPs of Finance"
- {{ai_generation}}: Flexible based on context

### Custom (campaign-specific)
Define per campaign:
- {{g2_review_complaint}}, {{pricing_tier_difference}}
- {{negative_review}}, {{follower_count}}
- {{competitor_mentioned}}, {{github_repo}}

### Case Study
- {{case_study_company}}, {{case_study_result}}
- {{case_study_metric}}, {{case_study_timeframe}}

---

## Opener Patterns

**From frameworks.md:**

1. **Classic:** "How are you currently handling {{process}}?"
2. **Status Pressure:** "Have you solved {{problem}} yet or is it still manual?"
3. **Efficiency:** "How are you doing {{task}} without adding headcount?"
4. **Risk-Based:** "How are you avoiding {{negative_outcome}} as you scale?"
5. **Binary:** "Is your process for {{area}} where you want it?"
6. **Redirect:** "Let me know if {{employee_1}} or {{employee_2}} would be better..."

---

## CTAs (Value-Exchange > Generic)

### Confirmation (Earn Reply)
- "Is this still the case?"
- "Curious—are you already doing X?"
- "Worth exploring?"

### Value-Exchange (Why Meet)
- "...so I can understand the situation and plead your case to Google"
- "...to walk you through 3 custom ideas for {{company}}"
- "...so I can show you the engagers of your last 10 posts"

### Resource Offer (Low Commitment)
- "Could I send you access to try it out?"
- "Would it be useful if I sent those over?"

**Test:** Can they reply in 5 words or less?

---

## ICP & Objection Mapping

**See icp-objection-mapping.md**

Before writing, role-play the skeptical ICP:

1. How are they doing this now?
2. Why would they switch?
3. What's their switching cost?
4. What objections will they have?

**Key insight:** Unless they're CEO, they want to:
- Do their job well enough to avoid criticism
- Go home on time
- Look smart to their boss

**Map TWO wins:**
- Business win: What the company gets
- Personal win: What THEY get individually

**Example:**
- Business: "Hits pipeline targets without adding headcount"
- Personal: "Makes your life easier managing the team + gets you a win with leadership"

---

## QA Checklist (11 Points)

**From qa.md:**

1. ✅ First line = specific signal
2. ✅ No hallucinations
3. ✅ Variables formatted {{correctly}}
4. ✅ No banned phrases
5. ✅ Recipient:sender ratio ≥ 2:1
6. ✅ Word count 60-120 (or justified)
7. ✅ CTA = low-effort
8. ✅ Reads naturally aloud
9. ✅ Em dashes consistent (—)
10. ✅ Subject line = 2-4 words OR whole offer
11. ✅ "Would I reply?" = YES

**All must pass before shipping.**

---

## Real Examples

**From examples.md - 10 annotated campaigns:**

1. **Pricing Page Insight** (Claygent + ZenRows) → Product video pitch
2. **Vanta Engagement** → LinkedIn engagers tool
3. **LinkedIn Posting Gap** → Scheduling tool
4. **Google Review** (Serper) → Reputation management
5. **Property Management** → Whole offer strategy
6. **Competitor Insights** (SimilarWeb) → Marketing agency
7. **Creative Ideas** → Follow-up with bullet points
8. **Final Email Value Bomb** → Pulled contacts as proof
9. **Paid Ads Expertise** → Email 3, dropped AI
10. **Resource Offer** → Final email alternative

Each example includes:
- What made it work
- Tools used
- Variables captured
- Why it converts

---

## When to Use Each File

**Starting a new campaign?**
→ Read SKILL.md, then research-playbook.md

**Need opener ideas?**
→ frameworks.md

**Want to see examples?**
→ examples.md (10 real campaigns)

**Doing follow-ups?**
→ follow-ups.md (Email 1→4 sequences)

**Generating custom ideas?**
→ creative-ideas-generation.md

**Before writing anything?**
→ icp-objection-mapping.md (role-play first)

**Before sending?**
→ qa.md (11-point checklist)

**Need prompts for Claude?**
→ workflows.md

---

## Scoring System

**0-100 points (from qa.md):**

| Dimension | Weight | What's Measured |
|-----------|--------|----------------|
| Situation Recognition | 25 pts | Specific data about them? |
| Value Clarity | 25 pts | Clear offer + proof? |
| Personalization Quality | 20 pts | Custom signal OR AI insight? |
| CTA Effort | 15 pts | 5 words or less to reply? |
| Length | 10 pts | 60-120 words? |
| Subject Line | 5 pts | 2-4 words OR whole offer? |

**85+ = Ship it**
**70-84 = One more pass**
**<70 = Start over**

---

## Key Principles (Non-Negotiable)

1. **Shorter & punchier** - 50-90 words, cut 3 times (fluff → compress → adjectives)
2. **Research IS the personalization** - If no custom signal after 10 min → use whole-offer OR skip
3. **Earn replies, not just meetings** - Confirm situation before selling
4. **Two valid paths** - Custom signal OR whole offer (both work)
5. **Every word earns its place** - Read in under 20 seconds
6. **Value-exchange CTAs** - Explain what THEY get, not just what you want
7. **Feature-constrain creative ideas** - Only suggest what you can deliver
8. **Role-play before writing** - Map ICP objections and personal benefits
9. **QA before shipping** - All 11 points must pass (including 50-90 word target)
10. **Follow-up with different angles** - Don't repeat what didn't work
11. **Know when to stop** - Email 4 is final, then wait 90 days

---

## Common Mistakes to Avoid

### Mistake 1: "Too generic"
**Problem:** Could send to anyone
**Fix:** Add specific signal from research

### Mistake 2: "Too long"
**Problem:** 200+ words, lost focus
**Fix:** Cut ruthlessly, keep only essential

### Mistake 3: "CTA too high-effort"
**Problem:** "Can we schedule 30 minutes?"
**Fix:** "Worth a quick look?"

### Mistake 4: "No research"
**Problem:** Template with no custom signal
**Fix:** Spend 10 minutes, find ONE signal

### Mistake 5: "Unconstrained creative ideas"
**Problem:** AI hallucinates capabilities you don't have
**Fix:** Define constraint box (3-5 actual features)

---

## Success Metrics

You know this skill is working when:

1. **Reply rates improve** (target: 3-8% depending on ICP)
2. **Positive sentiment increases** ("This is relevant" vs "Stop emailing me")
3. **Meetings booked with less friction** (they're pre-qualified by reply)
4. **Time to draft decreases** (templates + research method = efficiency)
5. **Variants test well** (A/B tests show improvement over old approach)

---

## How to Use This Skill with Claude

### Method 1: Reference in Prompts
```
"Using the cold-email-personalization-v2 skill, draft 3 variants for [company] targeting [role]."
```

### Method 2: Paste Relevant Files
```
[Paste research-playbook.md]

"Research signals for [company] and generate variables using this methodology."
```

### Method 3: System Prompt (Advanced)
Copy SKILL.md into your system prompt for persistent behavior across conversations.

---

## Next Steps

1. **Read SKILL.md** (10 min) - Core framework
2. **Scan examples.md** (15 min) - See real campaigns
3. **Try research-playbook.md** (20 min) - Practice finding signals
4. **Draft your first email** (30 min) - Use templates + QA checklist
5. **A/B test vs old approach** - Measure improvement

---

## Support & Iteration

This is v2.0. As you use it:
- Note what works / doesn't work
- Add examples to examples.md
- Refine research checklists for your ICP
- Build campaign-specific playbooks

The skill gets better with usage and feedback.

---

## Credits

**Based on:**
- Growth Engine X methodology
- Real campaigns from Taplio, Donut Media, Marketing agencies
- Message Doctor principles (Jordan Crawford)
- 100+ hours of campaign testing and iteration

**Tools referenced:**
- Clay, Claygent, ZenRows, Serper
- SimilarWeb, BuiltWith, LinkedIn
- SmartLead/Instantly (for threading)