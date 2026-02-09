# Creative Ideas Campaign Generation

## What Is This?

The Creative Ideas campaign is one of the highest-performing campaign types. Instead of pitching your service generically, you show them 3 specific ideas of how you'd help THEIR company.

**Why it works:**
- Shows > Tells (you're demonstrating capability, not claiming it)
- Tailored to them (not a template)
- Low commitment (they're just evaluating ideas, not buying yet)
- Sparks curiosity ("Hmm, how would they do that?")

**From the field:** "One of the best performing campaigns we've ever made."

---

## The Critical Constraint: Feature-Box Your Ideas

**The Problem:** If you let AI generate ideas without constraints, it will hallucinate capabilities you don't have.

**The Solution:** Define 3-5 specific features/capabilities you ACTUALLY offer (the "constraint box"), then generate ideas using ONLY those features.

### Bad (Unconstrained)
```
Prompt: "Generate 3 marketing ideas for this SaaS company"

AI Output:
• Build a referral program with gamification
• Create a podcast series
• Launch a TikTok influencer campaign

Problem: You don't do any of these things.
```

### Good (Constrained)
```
Input: Our capabilities are:
1. SEO content writing
2. Paid social ads (Meta/LinkedIn)
3. Email nurture sequences

Prompt: "Generate 3 marketing ideas using ONLY these capabilities"

AI Output:
• SEO content series around [keyword cluster] based on competitor gaps
• Paid social campaign targeting [audience] using [platform feature]
• Email nurture for [segment] addressing [pain]

Result: All credible, all deliverable.
```

---

## Step-by-Step Process

### Step 1: Define Your Constraint Box

List 3-5 specific features/capabilities you offer. Be concrete.

**Examples by service type:**

**Marketing Agency:**
- Paid social ads (Meta, LinkedIn, Google)
- SEO content creation
- Email marketing automation
- Landing page optimization
- Conversion rate optimization

**Outbound Agency:**
- Multi-channel sequences (email, LinkedIn, calls)
- Data enrichment from 40+ sources
- AI-personalized first lines
- List building by ICP
- A/B testing and optimization

**Product/Dev Shop:**
- API integrations
- Custom dashboards
- Workflow automation
- Data migration
- Performance optimization

**Content/Creative:**
- Product videos
- Case study creation
- Thought leadership content
- Social media content
- Email copywriting

---

### Step 2: Research Their Company

Spend 5-7 minutes gathering context:

**What to look for:**
1. **What they sell** (product/service, who buys it)
2. **Current marketing/sales approach** (based on website, LinkedIn, ads)
3. **Gaps or opportunities** (what they're NOT doing, or doing poorly)
4. **Competitive landscape** (who else is in their space)
5. **Recent changes** (funding, launches, hiring, pivots)

**Tools:**
- Company website (about, products, blog)
- LinkedIn (company page posts, job listings)
- SimilarWeb (competitor overlap, traffic)
- Their email list (sign up and see their nurture)
- Paid ads (Facebook Ad Library, LinkedIn Ads)

**Variables to capture:**
- {{industry}}, {{target_customer}}, {{competitor}}
- {{content_gap}}, {{keyword_cluster}}, {{customer_segment}}
- {{current_approach}}, {{missing_channel}}

---

### Step 3: Generate Ideas (One Per Feature)

For each idea, use ONE feature from your constraint box.

**Formula:**
```
[Action verb] + [Feature from constraint box] + [Specific to their company] + [Why it would help]
```

**Template:**
```
• [Do X] using [Feature Y] targeting [their specific thing]—would help with [their pain/goal]
```

---

### Examples

#### Example 1: Marketing Agency → SaaS Company

**Constraint box:**
1. Paid social ads
2. SEO content
3. Email nurture

**Research:**
- Target customer: Sales leaders at mid-market companies
- Competitor: HubSpot
- Content gap: No case studies on homepage
- Keyword opportunity: "CRM alternatives"

**Generated ideas:**
```
{{First name}} – I was back on your site today and had some marketing ideas for you.

• Paid social campaign targeting sales leaders using LinkedIn's "job function" targeting—would help with reaching decision-makers directly instead of relying on organic only

• SEO content series around "CRM alternatives" and "[competitor] vs [your product]" based on keyword gaps we found—could capture high-intent searches

• Email nurture sequence for trial users who haven't converted yet, addressing common objections we see in your G2 reviews—would improve trial-to-paid conversion

But of course, I wrote this without knowing anything about your current bottlenecks and goals.

If it's interesting, we could hop on a call and I'd be happy to share what's working in the SaaS industry. Especially in the sales tools niche.
```

**Why it works:**
- Each idea uses ONE feature (paid social, SEO, email)
- Each idea is specific to THEM (sales leaders, CRM alternatives, G2 objections)
- Each idea explains the benefit ("would help with X")
- Humble disclaimer invites conversation

---

#### Example 2: Content Shop → E-commerce Brand

**Constraint box:**
1. Product videos
2. UGC content creation
3. Email copy
4. Landing page optimization

**Research:**
- Target customer: Fashion-conscious men
- Current approach: Static product photos only
- Competitor: Premium menswear brands with lifestyle content
- Gap: No video content, email blasts are generic

**Generated ideas:**
```
{{First name}},

I was on your site and had a few creative ideas for [Company]:

• Product videos showing your [product category] in different settings (office, weekend, travel)—we helped similar brands increase add-to-cart rates by 23% when buyers could see products in context

• UGC campaign collecting customer photos/videos wearing your styles—creates social proof and gives you content for Instagram/email without in-house production

• Email sequences segmented by style preference (classic vs modern vs casual) based on browsing behavior—would make campaigns feel personalized instead of one-size-fits-all

These are just initial thoughts without knowing your priorities.

Would it make sense to chat about what could move the needle for [Company]?
```

**Why it works:**
- Feature-constrained (videos, UGC, email)
- Backed by proof ("23% increase")
- Segment-specific (style preferences)
- Clear benefit for each idea

---

#### Example 3: Dev Shop → B2B SaaS (Pricing Page Insight Example)

**Constraint box:**
1. Product demo videos
2. Interactive calculators
3. API integrations
4. Custom onboarding flows

**Research (using Claygent + ZenRows):**
- Scraped pricing page
- Found: Starter plan (basic features) vs Pro plan (API access, integrations)
- Gap: No visual explanation of how integrations work
- Objection (from G2): "Setup was confusing"

**Generated ideas:**
```
Subject: Starter vs. Professional plan

{{First name}} – had a question about the Starter vs. the Professional plan.

It seemed like Starter is focused on getting people access to the platform and the value for the Pro plan is to get access to premium features like the API so people can integrate with their CRM.

Do you have a product video that shows how easy those integrations are and how much more sales leaders would get if they upgraded?

Some other ideas that could help with upgrades:
• Interactive ROI calculator on pricing page showing time saved with Pro features—helps justify cost to decision-makers
• Custom onboarding flow for Pro trials that highlights integration benefits in first 3 days—reduces "I don't see the value" churn

We've been working with other sales tech platforms to make product videos. We have attributed a 4.7x increase in upgrades since adding the product video to the marketing site.

Would it be worth a chat to make a video for you?
```

**Why it works:**
- Research-driven (scraped pricing page)
- Feature-constrained (video, calculator, onboarding)
- Tied to business outcome (4.7x upgrades)
- Specific to their pricing structure

---

## Step 4: Format the Email

### Structure:

**Subject:** 2-4 words (e.g., "Marketing ideas", "Quick ideas", "Creative ideas")

**Opening:** Reference their site/situation
```
{{First name}} – I was back on your site today and had some [marketing/creative/product] ideas for you.
```

**Ideas:** 3 bullet points, each with:
- What you'd do
- Using which feature
- Why it would help
```
{{Creative Ideas}}
• Idea 1...
• Idea 2...
• Idea 3...
```

**Disclaimer:** Acknowledge you don't have full context
```
But of course, I wrote this without knowing anything about your current bottlenecks and goals.
```

**CTA:** Offer to share more insights
```
If it's interesting, we could hop on a call and I'd be happy to share what's working in the {{industry}} industry.
```

---

## Step 5: Quality Check

Before sending, verify:

**✅ Each idea uses ONE feature from your constraint box**
- If not → Rewrite to use actual capabilities

**✅ Each idea is specific to THEIR company**
- Generic: "Create content for social media"
- Specific: "Create product videos for your [product category] showing use in different settings"

**✅ Each idea explains the benefit**
- Bad: "Run paid ads"
- Good: "Run paid ads targeting [audience]—would help with [goal]"

**✅ Ideas are credible (not hallucinated)**
- Test: Could you actually deliver this?
- If no → It's hallucinated, remove it

**✅ Disclaimer is included**
- This is critical—it invites conversation instead of feeling presumptuous

---

## Common Mistakes to Avoid

### Mistake 1: Unconstrained Ideas
```
❌ "Launch a TikTok campaign, start a podcast, build an affiliate program"
```
**Problem:** You don't do these things. When they say "yes," you're stuck.

**Fix:** Only suggest things from your constraint box.

---

### Mistake 2: Generic Ideas
```
❌ "Improve your SEO, run paid ads, send more emails"
```
**Problem:** Could apply to anyone. Not impressive.

**Fix:** Make it specific to them:
```
✅ "SEO content around '[their keyword gap]' based on competitor analysis"
```

---

### Mistake 3: No Benefit Explanation
```
❌ "Create product videos"
```
**Problem:** Why would they care?

**Fix:** Add the "so what":
```
✅ "Create product videos showing use in context—helped similar brands increase add-to-cart 23%"
```

---

### Mistake 4: Too Many Ideas
```
❌ "Here are 7 ideas..."
```
**Problem:** Overwhelming. They won't read all of them.

**Fix:** 3 ideas maximum. Quality > quantity.

---

### Mistake 5: No Research
```
❌ Ideas pulled from thin air with no company context
```
**Problem:** Feels templated, not custom.

**Fix:** Spend 5-7 minutes researching. Reference specific things about them.

---

## When to Use Creative Ideas Campaign

**Best for:**
- ✅ Services that are visual/tangible (marketing, content, dev)
- ✅ When you have multiple capabilities to showcase
- ✅ Follow-up emails (Email 2 in sequence)
- ✅ When prospects need to "see it to believe it"

**Not ideal for:**
- ❌ Products that are hard to explain in bullets
- ❌ When you only have 1 capability (use case study instead)
- ❌ Highly technical B2B with long sales cycles (use insight-based instead)

---

## Variants

### Variant 1: Ideas + Case Study
Add a metric after ideas:
```
We've helped other [industry] companies with similar approaches—one saw [metric] in [timeframe].
```

### Variant 2: Ideas + Resource Offer
End with:
```
If you're not ready to chat, I have some resources on [topic] that might be useful. Want me to send those over?
```

### Variant 3: Ideas + Competitive Insight
Start with:
```
I noticed [competitor] is doing [thing] well. Here are some ways you could differentiate...
```

---

## Template: Creative Ideas Workflow

```
1. Define constraint box (3-5 features you ACTUALLY offer)
   - Feature 1: _______________
   - Feature 2: _______________
   - Feature 3: _______________

2. Research company (5-7 min)
   - Target customer: _______________
   - Current approach: _______________
   - Gap/opportunity: _______________
   - Competitor: _______________

3. Generate ideas (one per feature)
   - Idea 1: [Action] using [Feature 1] targeting [specific thing]—would help with [benefit]
   - Idea 2: [Action] using [Feature 2] targeting [specific thing]—would help with [benefit]
   - Idea 3: [Action] using [Feature 3] targeting [specific thing]—would help with [benefit]

4. Format email:
   Subject: [2-4 words]
   Opening: "I was back on your site..."
   Ideas: 3 bullets
   Disclaimer: "But of course, I wrote this without knowing..."
   CTA: "If interesting, could hop on a call..."

5. QA:
   ✅ Ideas are feature-constrained?
   ✅ Ideas are specific to them?
   ✅ Benefits are explained?
   ✅ Disclaimer included?
```

---

## Final Reminder

**The constraint box is non-negotiable.**

If you let AI run wild without constraints:
- You'll promise things you can't deliver
- You'll lose credibility when they say yes
- You'll waste their time (and yours)

**Feature-constrain your ideas. Always.**

Do that, and this campaign type will be one of your best performers.