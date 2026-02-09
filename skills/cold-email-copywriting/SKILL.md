---
name: cold-email-personalization-v2
description: Complete cold email system teaching research-driven personalization with bracketed variables, "poke the bear" openers, custom signal hunting, follow-up sequences, and strict QA. Integrates creative ideas campaigns, skeptical ICP mapping, and value-exchange CTAs.
version: 2.0.0
---

# Cold Email Personalization (GEX Style) - Complete System

## When to use this Skill
Use this Skill for *cold outbound email* ideation, drafting, personalization, variant testing, research-to-first-line mapping, follow-up sequences, or QA cleanup.

## Philosophy (what "good" looks like)
- **Message market fit before cleverness**: Show you understand the person/company immediately
- **Research IS the personalization**: Custom signals prove you did your homework
- **Personalization in the first line** with bracketed variables `{{...}}` or whole-offer strategy
- **Tight, conversational copy** (plain text, minimal fluff); 60–120 words for first email
- **One job per email**: Single sharp question or CTA
- **Evidence-led angles**: Competitor deltas, stack reveals, hiring signals, recent content, outcomes
- **Earn replies, not just meetings**: Confirm situation before selling

## Core Principles

### 1. Targeting > Messaging (But Both Matter)
Good targeting with bad messaging wastes qualified prospects. This skill assumes decent targeting and focuses on making the message match your list quality. However, if specific data isn't available, you can still send effective emails using broader strategies.

### 2. Two Paths to Personalization
**Path A: Custom Signal Research** (when you have time/data)
- 10-minute research method
- Find 1-2 custom signals unique to this prospect
- Lead with that signal in first line using `{{...}}`

**Path B: Whole Offer Strategy** (when you lack specific data)
- Subject + first line preview text = entire value prop
- Self-selection: they either need it (open) or don't (ignore, less likely to mark spam)
- Still targeted to your ICP, just broader personalization

**Both are valid.** Choose based on data availability and campaign scale.

### 3. The "Specifically" Line (3x Conversion Booster)
When reaching out to companies that all do different things but your service applies universally:

> "Specifically, it looks like you're trying to sell to {{customer_type}}, and we can help with that."

**When to use:**
- ✅ Outbound agencies, newsletters, marketing services (universal application)
- ✅ Any B2B service where you can AI-generate their customer type
- ❌ Obvious target markets (vacuum cleaners → hotels)

**Why it works:** Shows you understand THEIR specific business, not just yours.

## Variable Schema

### Core Variables (always try to include)
- {{first_name}}, {{company_name}}, {{role_title}}, {{department}}
- {{company_domain}}, {{industry}}, {{hq_location}}

### High-Signal Variables (use when available)
- {{tenure_years}}, {{recent_post_topic}}, {{recent_post_date}}
- {{press_headline}}, {{event_webinar_title}}, {{event_date}}
- {{competitor}}, {{category_competitors}}
- {{stack_crm}}, {{stack_marketing}}, {{stack_data}}
- {{hiring_roles}}, {{open_roles_count}}
- {{traffic_trend}}, {{conversion_goal}}, {{kpi_at_risk}}

### AI-Generated Variables (dynamic)
- {{ai_customer_description}}: "fitness enthusiasts who want to breathe better"
- {{ai_customer_type}}: "VPs of Finance" or "professional men looking for classic styles"
- {{ai_generation}}: Flexible contextual generation based on website/LinkedIn

### Custom Signal Variables (campaign-specific)
Define these per campaign based on your offer:
- {{g2_review_complaint}}, {{github_repo_found}}, {{security_page_outdated}}
- {{pricing_page_insight}}, {{hiring_spike_dept}}, {{competitor_mentioned}}
- {{negative_review}}, {{google_cid}}, {{follower_count}}

### Case Study Variables
- {{case_study_company}}, {{case_study_result}}, {{case_study_metric}}
- {{case_study_customer_type}}, {{case_study_timeframe}}

**Formatting rules:**
- Always show variables in `{{double_braces}}` in drafts
- Never invent facts; if unknown, omit or use broader strategy
- Variables can be dynamically generated via AI or scraped via Claygent/ZenRows

## Research Method

### Before Research: Define Your Perfect Signal
Complete this sentence for every campaign:
> "The ideal prospect would show evidence of **[specific behavior/change/problem]** because it means they're experiencing **[pain]** right now."

### Research Priority (10 minutes max)

**Tier 1: Case Studies (3 min) - START HERE**
1. Go to company website → case studies/customers page
2. Extract 3 examples: customer type, problem, metric, outcome, timeframe
3. Look for patterns: "Most [customer type] see [result] within [timeframe]"
4. Variables to capture: {{case_study_company}}, {{case_study_result}}, {{case_study_metric}}

**Tier 2: Custom Signals (6-7 min) - THE DIFFERENTIATOR**
Hunt for campaign-specific signals:
- **If selling to sales:** Hiring velocity, G2 reviews of their tools, job posts mentioning quotas
- **If selling to marketing:** Competitor insights via SimilarWeb, pricing page analysis, ad creative
- **If selling to ops:** GitHub repos, Zapier templates, manual processes mentioned in job posts
- **If selling to local businesses:** Google reviews (negative reviews = opportunity), follower counts
- **If selling to SaaS:** Pricing tiers (use Claygent + ZenRows), LinkedIn posts, funding news

**Tier 3: Standard Variables (3-4 min) - BACKUP**
- LinkedIn: role, tenure, recent posts, follower count
- Company site: blog, press, events
- Hiring page: open roles, department growth
- Tech stack: footer badges, BuiltWith, job descriptions

**Time budget:**
- If you find a Tier 1 or Tier 2 signal → Write the email
- If you find only Tier 3 → Consider whole-offer strategy instead
- If you find nothing after 10 min → Skip this prospect or use fallback campaign

### Tools & Techniques
- **Claygent**: Find pricing pages, case studies, news
- **ZenRows**: Scrape full page text (pricing, reviews)
- **Serper**: Google Places CID, reviews, local business data
- **SimilarWeb**: Competitor traffic, keyword overlap
- **Clay's sitemap tool**: Find specific pages (pricing, about, case studies)

## Subject Line Strategy

### Two Approaches

**Approach A: 2-4 Words (Intrigue)**
Best when using custom research signals.

Examples:
- "Partnership?" 
- "Quick question"
- "Outbound edge"
- "Competitor insights"
- "Saw your post"
- "LinkedIn ideas"

**Test:** Can a colleague or potential customer send this? If yes, good.

**Approach B: Whole Offer in Subject + Preview**
Best when data is limited or offer is self-selecting.

Example:
- Subject: "Ever chase renters to pay on time?"
- Preview: "We built a platform that rewards renters for paying on time so you can increase your NOI."

**When to extend beyond 4 words:** Only when pitching the whole product between subject + preview text, and the offer is punchy enough to fit.

**Rules:**
- Keep it conversational (not salesy)
- Don't explain everything (intrigue > information)
- Match it to email content (no bait-and-switch)

## Email Structure

### PRIORITY: Shorter & Punchier (50-90 words target)

**Default to tight format. Every word must earn its place.**

### Standard Email Structure

**Line 1: Situation Recognition (1 sentence)**
Describe THEIR exact situation. Be direct.
- ✅ "Saw you posted about {{ai_generation}}—seems like it was {{days_ago}} days since the one before that."
- ✅ "Noticed you sell to {{job_titles}}."
- ❌ "I hope this email finds you well!" (delete)
- ❌ Long-winded observations (cut)

**Line 2: Value Prop + Proof (1-2 sentences MAX)**
What you do + metric. No fluff.
- ✅ "We helped companies like Lemlist double down on social with our scheduling tool."
- ✅ "We've attributed a 4.7x increase in upgrades after adding product videos."
- ❌ "We help companies scale their marketing efforts through innovative solutions..." (too vague, too long)

**Optional: The "Specifically" Line (1 sentence)**
If applicable:
> "Specifically, it looks like you're trying to sell to {{customer_type}}, and we can help with that."

**Line 3: Low-Effort CTA (1 sentence)**
Binary question or simple offer.
- ✅ "Worth a look?"
- ✅ "Could I send you access?"
- ✅ "Just confirm Vanta is a good example and I can send the engagers."
- ❌ "Would you be open to scheduling 15 minutes next Tuesday at 2pm to discuss how we might be able to help you achieve your goals?" (way too long)

### Punchy Example (72 words)
```
Saw you hired 4 SEs last quarter—building custom workflows for every deal?

Most teams hit a wall at deal #30 when workflows don't scale. We helped similar teams automate this and 3x deal volume.

Worth a look?
```

### Even Tighter (48 words)
```
{{First_name}}—noticed {{hiring_spike}} on the team.

Have you figured out {{process}} without adding headcount, or still manual?

We help teams 3x volume with same headcount. {{case_study_metric}} for similar companies.

Worth exploring?
```

## How to Make Emails Punchier

### The Cutting Process

**After drafting, go through 3 cutting passes:**

**Pass 1: Delete fluff (target: cut 20%)**
- Remove all greetings ("I hope this finds you well")
- Remove all "I wanted to" / "I was wondering" phrases
- Remove all hedging ("perhaps", "maybe", "I think")
- Remove corporate speak ("solutions", "innovative", "cutting-edge")

**Pass 2: Compress sentences (target: cut 15%)**
- Replace clauses with periods (break long sentences)
- "We built a platform that can do X" → "We do X"
- "It seemed like X is focused on Y" → "X is for Y"
- Combine redundant ideas into one sentence

**Pass 3: Cut adjectives (target: cut 10%)**
- Keep only adjectives that are specific data ("4.7x", "Series B", "23%")
- Delete all others ("great", "amazing", "powerful", "robust")

**Total target: 40-45% shorter after 3 passes**

### Before & After Examples

**Example 1: SaaS Outbound**
```
Before (94 words):
"Hey Sarah, I hope this email finds you well! I wanted to reach out because I noticed on your website that you seem to be selling to sales leaders and marketing executives. I saw that you recently raised a Series B and I had to assume you are probably using outbound tactics since I saw John Smith is a BDR on the team. I was wondering if you're thinking about how your team could be leveraging better data enrichment and GPT-4 to help make their prospecting more efficient?"

After (52 words):
"Sarah—saw you sell to sales leaders.

Noticed John is a BDR on the team. Have you figured out how he could leverage better data and GPT-4 for prospecting, or still manual?

Most teams save 10 min per prospect and 3x volume without adding headcount.

Worth a look?"

Cuts:
- "I hope this finds you well" → deleted
- "I wanted to reach out because" → deleted
- "seem to be" → deleted
- "recently raised a Series B and" → deleted (not relevant to ask)
- "I had to assume you are probably" → deleted
- "I was wondering if you're thinking about" → "Have you figured out"
- "could be leveraging" → "could leverage"
- "to help make their prospecting more efficient" → deleted (implied)
```

**Example 2: Product Video**
```
Before (92 words):
"Hey Jordan, I had a question about the Starter plan versus the Professional plan. It seemed like the Starter plan is focused on getting people access to the platform and the value proposition for the Pro plan is to get access to premium features like the API so people can integrate with their CRM system. Do you currently have a product video that shows how easy those integrations are and demonstrates how much more value sales leaders would get if they decided to upgrade to the Pro plan?"

After (58 words):
"Jordan—question about Starter vs. Pro.

Starter is for platform access, Pro is for API integrations.

Do you have a product video showing how easy those integrations are and how much more sales leaders get if they upgrade?

We've attributed 4.7x increase in upgrades after adding product videos.

Worth a chat?"

Cuts:
- "Hey" → deleted
- "I had" → deleted
- "versus" → "vs."
- "It seemed like" → deleted
- "is focused on getting people" → "is for"
- "the value proposition for" → deleted
- "to get access to premium features" → deleted
- "so people can integrate with their CRM system" → compressed to "integrations"
- "currently" → deleted
- "that shows" → "showing"
- "demonstrates" → deleted
- "would get if they decided to upgrade" → "get if they upgrade"
- "to the Pro plan" → deleted
```

### Quick Compression Tactics

**Tactic 1: Kill intro phrases**
- ❌ "I wanted to reach out because..."
- ❌ "I was wondering if..."
- ❌ "I hope you don't mind me asking..."
- ✅ Just start with the point

**Tactic 2: Use em dashes instead of commas**
- ❌ "Saw your post, and I noticed you haven't posted in a while, so I thought..."
- ✅ "Saw your post—noticed it was {{days}} days since the one before."

**Tactic 3: Delete all "that" and "which"**
- ❌ "We built a platform that can pull everyone that is engaging..."
- ✅ "We pull everyone engaging..."

**Tactic 4: Active voice always**
- ❌ "It seemed like Starter is focused on getting people access..."
- ✅ "Starter gives platform access..."

**Tactic 5: Numbers > words**
- ❌ "thirty days" → ✅ "30 days"
- ❌ "three times" → ✅ "3x"
- ❌ "four point seven times" → ✅ "4.7x"

**Tactic 6: Abbreviate where clear**
- "versus" → "vs."
- "Chief Revenue Officer" → "CRO" (if they'd know it)
- "versus" → "vs."
- But NOT "b/c" or "w/" (too casual)

### The 50-Word Challenge

**Exercise:** Can you say the same thing in 50 words?

If your draft is 90 words, challenge yourself to get it to 50 without losing:
- The situation recognition
- The value prop
- The metric/proof
- The CTA

**Usually you can.** And it'll be better.

## Campaign Types

### 1. Custom Signal Campaign
**When:** You have strong research data (case studies, pricing insights, reviews, hiring, etc.)

**Structure:**
- Subject: 2-4 words, intriguing
- First line: Custom signal with {{variable}}
- Body: Value prop + case study proof
- CTA: Low-effort question

### 2. Creative Ideas Campaign
**When:** You can generate specific, credible ideas for them

**Requirements:**
- Define 3-5 specific features/capabilities you offer (the constraint box)
- Research their website/challenges
- Generate 3 bullet point ideas, each using ONE feature

**Structure:**
```
{{First name}} – I was back on your site today and had some marketing ideas for you.

{{Creative Ideas}}
• Idea 1: [Specific action using Feature X]—would help with [their pain]
• Idea 2: [Specific action using Feature Y]—could improve [their goal]
• Idea 3: [Specific action using Feature Z]—might address [their challenge]

But of course, I wrote this without knowing anything about your current bottlenecks and goals.

If it's interesting, we could hop on a call and I'd be happy to share what's working in the {{industry}} industry.
```

**Critical:** Ideas must be credible (feature-constrained) and specific to them.

### 3. Whole Offer Campaign
**When:** Limited data availability or self-selecting offer

**Structure:**
- Subject: Describes the pain/outcome (can be longer than 4 words)
- Preview text: Completes the offer
- Body: Explain the offer, add light personalization if possible
- CTA: Simple yes/no or low-friction

**Example (from images):**
```
Subject: Ever chase renters to pay on time?

Hey {{first_name}},

We built a platform that rewards renters for paying on time so you can increase your NOI.

Basically, renters that pay on time could get Starbucks gift cards they can spend at the {{nearest_mall}}.

If we could help you increase on time rental payments, would that be useful?
```

### 4. Fallback Campaign ("Let Me Know If...")
**When:** You're not 100% sure they're the right person

**Structure:**
```
{{First name}} – let me know if {{employee_1}} or {{employee_2}} would be better to speak about {{specific_problem}}.

[Rest of email]
```

**Why it works:** Gets personalized with employee names, shows you did research, gives them an easy out (or forward).

## Follow-Up Sequence Philosophy

### Email 1 (Day 0)
- New subject line
- Full campaign (research + value prop + CTA)
- Try to book meeting or earn reply

### Email 2 (Day 3-4)
- **No subject line** (threads to Email 1 in SmartLead)
- **Different value proposition**
- They didn't reply = that angle didn't resonate
- Rotate through the "3 offers": save time, save money, make money

**Example:**
```
{{First name}} – I was back on your site today and had some marketing ideas for you.

{{Creative Ideas}}

But of course, I wrote this without knowing anything about your current bottlenecks and goals.

If it's interesting, we could hop on a call and I'd be happy to share what's working in the {{industry}} industry.
```

### Email 3 (Day 7-8)
- **New subject line** (fresh thread)
- Different case study or angle
- Consider dropping ALL AI personalization
- Use whole-offer strategy (punchy + direct)

**Example:**
```
Subject: Paid Ads Strategy

{{First name}} – I was just taking a look at your LinkedIn profile and noticed you've held multiple marketing roles before joining {{company}}.

In that time, I'm sure you've gained wide experience in various areas of marketing. Here at [Agency], we've helped hundreds of customers with their paid media strategies and that's all we do.

{{Company pixel/tracking insight if available}}

We're seeing lots of changes in the paid media environment and I wondered if it made sense to hop on a call to discuss these insights.
```

### Email 4 (Day 11-12)
- **Final email**
- Redirect to another person OR offer resources
- "Let me know if I should reach out to {{employee_1}} or {{employee_2}} instead"
- OR: "Alternatively, if working with {{company}} is taking all of your time, we have some resources that could help. Would it be useful if I sent those over?"

**Creative final touch:**
Pull prospects matching their ICP and send them as value:
```
{{First name}} – Last email. I figured you sell to customers like {{customer_type_1}}, {{customer_type_2}}, {{customer_type_3}}.

I went ahead and pulled them off LinkedIn for you using our system. No human wrote this email.

{{Contact}} – {{LinkedIn Link}} – {{Email}}
{{Contact}} – {{LinkedIn Link}} – {{Email}}
{{Contact}} – {{LinkedIn Link}} – {{Email}}

Want to see a video of how I did this automatically?
```

## ICP & Objection Mapping

### Before Writing ANY Campaign

**Step 1: Role-Play the Skeptical ICP**
Put yourself in their shoes and ask:
1. **How are they doing this now?** (Current state, existing tools)
2. **Why would they switch?** (What's broken about current solution?)
3. **What objections will they have?**
   - "We already have X"
   - "We don't have budget"
   - "We're too small/big for this"
   - "We tried something like this before"
4. **What's their switching cost?** (Time, money, political capital)

**Step 2: Personal Benefit (Not Just Business ROI)**
Unless they're the CEO, they're not thinking about company goals 24/7. They want to:
- Do their job and leave on time
- Look smart to their boss
- Avoid extra work
- Get promoted

**Examples:**
- **HR person (health insurance):** "Not only a big win for the company, but you'd personally benefit from picking your own plans"
- **Finance person:** "Makes budget planning easier AND gets you a win with leadership"
- **Ops person:** "One less fire drill + makes you look like a hero"

**Add to every campaign plan:**
- Business win: [What the company gets]
- Personal win: [What THEY get]

### Step 3: Preempt Objections in Copy
Don't wait for them to object. Address it proactively:
- **Objection:** "We already have a solution"
  - **Preempt:** "Have you figured out how to do X without adding headcount, or is it still manual?"
- **Objection:** "Sounds expensive"
  - **Preempt:** "You only pay when it's successfully taken down" or mention case study ROI
- **Objection:** "We're too busy"
  - **Preempt:** "This would actually save your team time by automating [specific task]"

## CTAs: Value-Exchange > Generic Asks

### Bad CTAs (Delete These)
- ❌ "Can we schedule 15 minutes?"
- ❌ "Are you available for a quick call?"
- ❌ "Let's chat sometime"
- ❌ "Would love to connect"

### Good CTAs (What They Get)

**Category 1: Confirmation (Earn Reply)**
- ✅ "Is this still the case?"
- ✅ "Curious—are you already doing X?"
- ✅ "Worth exploring?"
- ✅ "Just confirm [example] is accurate or any others"

**Category 2: Value-Exchange (Why Meet)**
Explain what THEY get in exchange for their time:
- ✅ "...so I can understand the situation and plead your case to Google"
- ✅ "...to walk you through 3 custom ideas specific to {{company}}"
- ✅ "...so I can show you the engagers of your competitor's last 10 posts"
- ✅ "...to share what's working in the {{industry}} industry right now"

**Category 3: Resource Offer (Low Commitment)**
- ✅ "Could I send you access to try it out?"
- ✅ "Would it be useful if I sent those over?"
- ✅ "Let me know if I should send a video of how this works"

**The Test:** Can they reply in 5 words or less? If no, simplify.

## Opener Patterns ("Poke the Bear")

### #1 Classic
- Do you already have a reliable way to {{problem}}?
- How are you currently handling {{process}}?
- Who owns {{area}} internally today?

### #2 Status Pressure / FOMO
- Have you solved {{problem}} yet or is it still manual?
- Are you already doing {{practice}} like the top firms in your space?
- Have you figured out how to do {{outcome}} without adding headcount?

### #3 Soft Humility
- I may be wrong, but do you have something in place for {{area}}?
- Totally possible you solved this—how do you handle {{process}} today?

### #4 Efficiency / Leverage
- How are you doing {{task}} without adding headcount?
- What's your process for {{task}} without manual work?

### #5 Risk-Based
- How are you avoiding {{negative_outcome}} as you scale?
- How do you make sure {{critical_task}} doesn't slip through the cracks?

### #6 Binary
- Is your process for {{area}} where you want it?
- Will your current setup scale 12 more months?

### #7 Redirect (Fallback)
- Let me know if {{employee_1}} or {{employee_2}} would be better to speak about {{problem}}

## QA Checklist

Run before sending ANY email:

**Personalization:**
- ✅ First line references specific signal or AI-generated insight
- ✅ Variables use `{{double_braces}}` format
- ✅ No hallucinations (verify all facts)

**Banned Phrases (Delete if found):**
- ❌ "I hope this email finds you well"
- ❌ "I wanted to reach out"
- ❌ "We help companies..." (unless backed by case study immediately after)

**Length & Clarity:**
- ✅ 60-120 words (or 3-4 lines for ultra-tight variant)
- ✅ Plain text, no fluff
- ✅ Reads naturally aloud

**Tone:**
- ✅ Helpful, confident, conversational
- ✅ About THEM (not about you)
- ✅ 100% recipient-focused vs 0% sender-focused (aim for this ratio)

**CTA:**
- ✅ One clear CTA
- ✅ Low-effort (can reply in 5 words or less)
- ✅ Value-exchange if asking for meeting

**Punctuation:**
- ✅ Em dashes are "—" (not "--" or "–")
- ✅ No double spaces
- ✅ Variables closed correctly: `{{...}}`

## Scoring Rubric (0-100)

| Dimension | Weight | What's Measured |
|-----------|--------|----------------|
| Situation Recognition | 25 pts | Specific data about them? |
| Value Clarity | 25 pts | Clear offer + proof? |
| Personalization Quality | 20 pts | Custom signal OR AI insight? |
| CTA Effort | 15 pts | 5 words or less to reply? |
| Punchiness | 10 pts | **50-90 words? No fluff?** |
| Subject Line | 5 pts | 2-4 words OR whole offer? |

**85+ = Ship it**
**70-84 = Needs one more pass**
**<70 = Start over**

## Generation Workflow

### Step 1: Campaign Setup
1. Define your offer (1-2 sentences)
2. Complete the sentence: "The ideal prospect shows evidence of [behavior] because..."
3. List 3-5 specific features/capabilities (for creative ideas campaigns)
4. Identify personal benefit (not just business ROI)

### Step 2: Research (10 min max)
1. Hunt case studies (3 min)
2. Hunt custom signals (6-7 min)
3. Fill standard variables (backup, 3-4 min)
4. If no strong signal found → Use whole-offer strategy OR skip prospect

### Step 3: Choose Strategy
- Custom signal campaign (if you found Tier 1/2 signal)
- Creative ideas campaign (if you can generate credible ideas)
- Whole offer campaign (if data is limited but targeting is solid)
- Fallback campaign (if unsure about fit)

### Step 4: Draft Variants
Generate 3 variants using different:
- Opener patterns
- Value props (save time vs save money vs make money)
- CTAs (confirmation vs value-exchange vs resource offer)

### Step 5: QA
Run checklist (see above)

### Step 6: Output
Return JSON:
```json
{
  "v1": "email text",
  "v2": "email text",
  "v3": "email text",
  "subject_lines": ["option 1", "option 2", "option 3"],
  "notes": "Explanation of angles and why they should work",
  "used_variables": ["{{first_name}}", "{{ai_generation}}", ...],
  "missing_variables": ["{{tenure_years}}", ...],
  "score": 85,
  "recommended_variant": "v2"
}
```

## Files in This Skill

- **SKILL.md** (this file): Main framework and principles
- **research-playbook.md**: Deep dive on finding custom signals with tools
- **frameworks.md**: Opener patterns, angle menus, CTA examples
- **examples.md**: Real campaign examples with annotations
- **follow-ups.md**: Email 1→2→3→4 sequences with value prop rotation
- **creative-ideas.md**: How to generate credible, feature-constrained ideas
- **icp-objection-mapping.md**: Role-play skeptical ICP before writing
- **workflows.md**: Ready-to-run prompts for each step
- **qa.md**: Cleanup checklist and autofix rules
- **scoring-rubric.md**: Detailed 0-100 scoring with examples

## Final Reminders

1. **Research IS the personalization** - Custom signals > clever copy
2. **Earn replies, not just meetings** - Confirm situation first
3. **When in doubt, simplify** - Shorter, clearer, more direct
4. **Test and iterate** - Use scoring rubric to improve over time
5. **Whole offer strategy is valid** - Not every email needs deep personalization if targeting is solid

Now draft with confidence.