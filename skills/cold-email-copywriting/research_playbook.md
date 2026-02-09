# Research Playbook: Finding Custom Signals (With Tools)

## The Research Mindset

**Bad research:** "Let me find their role and company size so I can plug them into my template."

**Good research:** "What is happening in their world RIGHT NOW that makes my solution urgent?"

The best cold emails feel like you've been watching their company for weeks. That only happens when you find signals that are:
1. **Specific** (not "you're growing" but "you hired 12 SDRs in Q4")
2. **Recent** (last 90 days ideally, last 6 months max)
3. **Directionally aligned** with the pain your product solves

---

## Before Research: Define Your Perfect Signal

Complete this sentence for every campaign:
> "The ideal prospect would show evidence of **[specific behavior/change/problem]** because it means they're experiencing **[pain]** right now."

**Examples:**
- *Product video company:* "...show evidence of **pricing tiers with upgrade paths** because it means they're **trying to drive plan upgrades**."
- *Outbound automation tool:* "...show evidence of **SDR/BDR hiring or manual research mentions** because it means they're **scaling outbound**."
- *Reputation management:* "...show evidence of **negative Google reviews** because it means they're **losing business to bad online perception**."

---

## Research Priority (10 Minutes Max)

### Tier 1: Case Studies (3 min) - START HERE

**Where to look:**
1. Company website → /customers, /case-studies, /success-stories
2. Blog → search for "case study" or customer names
3. Press page → customer announcements

**What to extract:**
- Customer type/industry
- Problem they solved
- Specific metric/outcome
- Timeframe

**Variables to capture:**
- {{case_study_company}}
- {{case_study_result}} ("increased close rates 23%")
- {{case_study_metric}} ("close rates", "churn", "MRR")
- {{case_study_customer_type}} ("Series B SaaS", "e-commerce brands")
- {{case_study_timeframe}} ("within 90 days", "first quarter")

**How to use in email:**
"We helped {{case_study_customer_type}} achieve {{case_study_result}} {{case_study_timeframe}}—curious if {{pain}} is on your radar?"

---

### Tier 2: Custom Signals (6-7 min) - THE DIFFERENTIATOR

This is where the magic happens. Hunt for campaign-specific signals using tools.

#### Tool 1: Claygent (AI Web Scraper)

**What it does:** AI agent that finds and summarizes web pages for you.

**Best use cases:**
- Find pricing pages
- Find case study pages
- Summarize company descriptions
- Find recent news/press
- Extract specific page elements

**Example workflow (Pricing Page):**
```
1. Claygent prompt: "Find the pricing page for {{company_domain}}"
2. Claygent returns: URL of pricing page
3. Feed that URL to ZenRows (see below) for full text scrape
4. AI column: "Summarize the difference between Starter and Pro plans"
5. Use in email: "Had a question about the Starter vs. Professional plan..."
```

**Example workflow (Case Studies):**
```
1. Claygent prompt: "Find 3 customer case studies on {{company_domain}}"
2. Claygent returns: URLs or summaries
3. Extract: customer type, outcome, metric
4. Use in email: "We've helped companies like [type] achieve [outcome]..."
```

**Pro tip:** Claygent is cheap. Use it liberally for initial discovery, then scrape with ZenRows for details.

#### Tool 2: ZenRows (Full Page Scraper)

**What it does:** Scrapes full HTML/text from any page (bypasses anti-bot protections).

**Best use cases:**
- Scrape pricing pages (get ALL tier details, not just summary)
- Scrape about pages
- Scrape blog content
- Scrape job descriptions

**Why use with Claygent:**
- Claygent finds the page → ZenRows gets the full text → AI column processes it

**Example (from real campaign):**
```
Problem: Need pricing tier differences to write specific email

Workflow:
1. Claygent: "Find pricing page for {{domain}}"
2. ZenRows: Scrape that URL, return full text
3. AI column: "What's the difference between Starter and Professional plans? Focus on features and who each plan is for."
4. Output: "Starter = platform access, Pro = API integrations for CRM"
5. Email: "Had a question about Starter vs Pro. Seemed like Starter is for access, Pro is for API integrations. Do you have a product video showing how easy those integrations are?"
```

**Pro tip:** ZenRows gets you nuance that Claygent summaries might miss.

#### Tool 3: Serper (Google Search API)

**What it does:** Programmatic Google searches (news, places, reviews, etc.).

**Best use cases:**
- Google Places CID (for local businesses)
- Google Reviews (negative reviews = opportunity)
- Recent news mentions
- Competitor mentions

**Example workflow (Google Reviews):**
```
1. Serper Google Places: Search by company website → get Google CID
2. Filter JSON: Match website to ensure correct business
3. Serper Reviews: Use CID to get reviews (can sort by lowest rated, most recent)
4. Extract: Reviewer name, complaint, date
5. Email: "Is that review {{reviewer_name}} left about {{complaint}} accurate?"
```

**Example workflow (News):**
```
1. Serper News: "{{company_name}} funding OR acquisition OR expansion"
2. Filter: Last 6 months only
3. Extract headline, date
4. Email: "Saw you raised ${{amount}} in {{month}}—how are you scaling outbound without proportionally scaling headcount?"
```

**Pro tip:** Local businesses are GOLDMINES for review-based outreach.

#### Tool 4: SimilarWeb (Competitor Intelligence)

**What it does:** Traffic data, competitor overlap, keyword rankings.

**Best use cases:**
- Competitor traffic comparison
- Keyword overlap (who's stealing your SEO)
- Traffic trends (growing/declining)

**Example (from real campaign):**
```
1. SimilarWeb: Compare {{company_domain}} to {{competitor_domain}}
2. Extract: Shared keywords, traffic overlap
3. Email: "Saw on SimilarWeb that {{competitor}} is taking some of the same digital real estate keywords your company ranks for. One of the first things we do is understand the competitive landscape..."
```

**Pro tip:** Works best for companies with decent web traffic (5K+ visits/month).

#### Tool 5: Clay's Sitemap Tool

**What it does:** Pulls all URLs from a website's sitemap.

**Best use cases:**
- Find specific page types (pricing, about, careers)
- Discover hidden pages (case studies, resources)
- Find blog post topics

**Example workflow:**
```
1. Clay sitemap: Pull all URLs from {{domain}}
2. Filter: URLs containing "pricing" or "case-study"
3. Scrape those pages with ZenRows
4. AI process: Extract relevant data
```

**Pro tip:** Faster than Claygent if you know what you're looking for.

#### Tool 6: LinkedIn (Manual or Scraper)

**What to look for:**
- Recent posts by target (topic, engagement, frequency)
- Company page follower count
- Hiring activity (open roles)
- Employee count changes
- Profile updates (new role, tenure)

**Variables to capture:**
- {{recent_post_topic}}, {{recent_post_date}}
- {{number_of_followers}} (personal), {{company_followers}} (company page)
- {{hiring_roles}}, {{open_roles_count}}
- {{tenure_years}}, {{role_title}}

**Example (from real campaign):**
```
LinkedIn scrape:
- Recent post: "SEO best practices" (6 days ago)
- Previous post: 6 days before that (gap = inconsistent)
- Follower count: 4,000+

Email: "Saw you posted about SEO best practices and the time you posted before that was 6 days ago. With 4,000+ followers I figured building your brand on LinkedIn might be a priority..."
```

#### Tool 7: BuiltWith / Wappalyzer (Tech Stack)

**What it does:** Detects technologies used on a website.

**Best use cases:**
- CRM, marketing automation, analytics tools
- Payment processors
- Hosting/infrastructure

**Variables to capture:**
- {{stack_crm}}, {{stack_marketing}}, {{stack_analytics}}

**Example:**
```
BuiltWith: Detects HubSpot + Stripe
Email: "Saw you're on HubSpot + Stripe—have you figured out how to sync payment data back to CRM automatically, or still manual?"
```

---

### Tier 3: Standard Variables (3-4 min) - BACKUP

If you don't find Tier 1/2 signals, fall back to these:

**LinkedIn basics:**
- Role, tenure, recent posts
- Company page updates

**Company website:**
- About page, team page
- Blog recent topics
- Press mentions

**Hiring page:**
- Open roles (especially in sales, marketing, ops)
- Role descriptions (pain points hidden in JDs)

---

## Signal Freshness Rules

Not all signals are equal. Prioritize recent signals:

| Signal Type | Fresh Until | Example |
|-------------|-------------|---------|
| Funding news | 90 days | "Raised $50M in Series B" |
| LinkedIn posts | 30 days | "Posted about X 3 weeks ago" |
| Hiring activity | 60 days | "4 open SDR roles posted last month" |
| G2 reviews | 90 days | "Recent review mentioned..." |
| Pricing changes | 90 days | "Pricing page updated in Q4" |
| Negative review | 180 days | "Review from 3 months ago about..." |
| Product launch | 120 days | "Launched new feature last quarter" |

**If older than these windows:** Still usable, but acknowledge the age ("Saw you raised $X last year—curious how outbound is scaling since then?")

---

## Campaign-Specific Research Checklist Template

For each new campaign, define your custom research plan:

```
Campaign: [Product/Offer]
ICP: [Role + Company Type]
Core Pain: [What they're struggling with]

Perfect Signal Sentence:
"The ideal prospect shows evidence of [behavior] because it means [pain]."

Custom Signals to Hunt (Priority Order):
1. [Signal type] → [Tool to use] → [Variable to capture] → [How it proves pain]
2. [Signal type] → [Tool to use] → [Variable to capture] → [How it proves pain]
3. [Signal type] → [Tool to use] → [Variable to capture] → [How it proves pain]

Time Budget:
- 3 min: Case studies (if available)
- 6 min: Hunt top custom signal
- 1 min: Backup standard variables

Fallback Strategy (if no custom signal found):
[Whole offer strategy OR skip prospect]
```

---

## Example Research Plans by Use Case

### Use Case 1: Selling Outbound Automation

**Perfect signal:** "Shows evidence of SDR/BDR hiring OR manual research mentions because it means they're scaling outbound."

**Research plan:**
1. **LinkedIn hiring** (3 min)
   - Tool: LinkedIn jobs or Clay enrichment
   - Look for: "SDR", "BDR", "Account Executive" roles
   - Variable: {{hiring_roles}}, {{open_roles_count}}
   
2. **Company site** (2 min)
   - Tool: Manual or Claygent
   - Look for: Customer types they sell to
   - Variable: {{ai_customer_description}}
   
3. **Tech stack** (2 min)
   - Tool: BuiltWith footer check
   - Look for: Sales tools (HubSpot, Outreach, SalesLoft)
   - Variable: {{stack_crm}}

**Email angle:** "Noticed {{SDR_name}} is an SDR on the team. Are you thinking about how they could leverage better data and GPT-4 for prospecting?"

---

### Use Case 2: Selling to SaaS (Product Videos)

**Perfect signal:** "Shows evidence of pricing tiers with upgrade paths because it means they're trying to drive revenue expansion."

**Research plan:**
1. **Pricing page** (4 min)
   - Tool: Claygent (find page) → ZenRows (scrape) → AI (summarize)
   - Look for: Starter vs Pro differences, integration mentions
   - Variable: {{pricing_tiers}}, {{upgrade_features}}
   
2. **Case studies** (3 min)
   - Tool: Claygent or manual
   - Look for: 3 examples with metrics
   - Variable: {{case_study_result}}
   
3. **LinkedIn** (3 min)
   - Tool: Manual
   - Look for: Recent posts, role tenure
   - Variable: {{recent_post_topic}}, {{tenure_years}}

**Email angle:** "Had a question about Starter vs Professional plan. Seemed like Starter is for access, Pro is for API integrations. Do you have a product video showing how easy those integrations are?"

---

### Use Case 3: Selling Reputation Management

**Perfect signal:** "Shows evidence of negative Google reviews because it means they're losing business to bad perception."

**Research plan:**
1. **Google Reviews** (5 min)
   - Tool: Serper (Places → CID → Reviews)
   - Look for: 1-2 star reviews with specific complaints
   - Variable: {{negative_review}}, {{reviewer_name}}, {{complaint}}
   
2. **Company basics** (2 min)
   - Tool: Manual
   - Look for: Business type, location
   - Variable: {{company_type}}, {{location}}
   
3. **Response pattern** (3 min)
   - Tool: Manual review scan
   - Look for: Do they respond to reviews? How?
   - Insight: "They're not responding" = opportunity

**Email angle:** "Is that review {{reviewer_name}} left about {{complaint}} accurate? We help remove untrue/unfair reviews and you only pay when it's successfully taken down."

---

### Use Case 4: Selling Marketing Services

**Perfect signal:** "Shows evidence of competitor keyword overlap OR traffic decline because it means they're losing share."

**Research plan:**
1. **SimilarWeb** (4 min)
   - Tool: SimilarWeb API or manual
   - Look for: Competitor overlap, traffic trends
   - Variable: {{competitor}}, {{traffic_trend}}
   
2. **LinkedIn** (3 min)
   - Tool: Manual
   - Look for: New marketing hire, tenure, role changes
   - Variable: {{tenure_years}}, {{role_title}}
   
3. **Content audit** (3 min)
   - Tool: Manual site browse
   - Look for: Blog frequency, content gaps
   - Variable: {{content_gap}}

**Email angle:** "Saw on SimilarWeb that {{competitor}} is taking some of the same digital real estate keywords. One of the first things we do is understand competitive landscape..."

---

## The "So What?" Test

Before using a signal in your email, ask:

1. **Is this signal recent?** (< 6 months ideally)
2. **Does this signal connect to MY offer?** (Hiring engineers ≠ relevant for sales tool)
3. **Would THEY care that I noticed this?** (Public info everyone has = not impressive)
4. **Can I tie it to a specific pain?** (Signal without pain = just trivia)

**Good signal:** "4 open SDR roles posted last month" → proves they're scaling outbound
**Bad signal:** "You have 200 employees" → so does everyone else in your list

---

## When to Skip a Prospect

If after 10 minutes you:
- ❌ Found no Tier 1 or Tier 2 signals
- ❌ Can't tie any signal to your offer
- ❌ Can't describe their specific situation with data

**Then:**
- Don't send a generic email just to hit volume
- Don't make up a signal or assume pain
- ✅ Mark as "needs more research" and revisit in 30-60 days
- ✅ OR use whole-offer strategy if targeting is still solid

**The rule:** If you can't point to a specific, recent signal that connects to your offer, either use whole-offer strategy or skip the prospect.

---

## Research Workflow Summary

```
1. Define perfect signal (1 sentence)
   ↓
2. Hunt case studies (3 min)
   ↓
3. Hunt custom signals with tools (6-7 min)
   - Claygent + ZenRows: Pricing, case studies, content
   - Serper: Reviews, news, places
   - SimilarWeb: Competitors, traffic
   - LinkedIn: Posts, hiring, followers
   ↓
4. Capture variables in {{brackets}}
   ↓
5. Ask "So What?" test
   ↓
6. If strong signal found → Draft custom email
   If weak signal → Use whole-offer strategy
   If no signal → Skip or revisit later
```

**Total time: 10 minutes per prospect (if targeting is good)**

Now go hunt signals that matter.