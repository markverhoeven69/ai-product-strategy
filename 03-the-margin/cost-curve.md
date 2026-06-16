# Cost Curve & Pricing Strategy

## Cost Model

| Cost Category | Per-User/Month | Notes |
|--------------|----------------|-------|
| Inference (primary model) | €0.25 | Daily coaching conversations, habit recommendations |
| Inference (cascading/triage) | €0.20 | Small model handles ~80% of requests |
| Infrastructure | €0.50 | Hosting, API gateway, monitoring |
| Data/storage | €0.20 | User profiles, history, embeddings |
| Human-in-the-loop | €0.20 | Occasional review of edge cases and safety checks |
| **Total COGS** | €1.35 | Blended monthly operating cost per active user |

**Assumption:** 150 AI interactions per active user per month, with 80% routed to a low-cost model and 20% routed to a frontier model.

---

### Input Margin Calculator

| Input                          | Waarde     | Toelichting                          |
| ------------------------------ | ---------- | ------------------------------------ |
| Avg AI Requests / User / Month | 150    | 3-5 interacties per dag              |
| Blended Cost per Request       | $0.003 | 80% mini-model, 20% frontier-model   |
| Revenue per User / Month       | $19.99 | Premium AI coaching subscription     |
| Non-AI COGS / User / Month     | $1.35  | Hosting, support, analytics, storage |

---

## Cost Curve

## Build Your Cost Curve

| Feature                                                   | Complexity | Model Tier | Cost/Request | Volume % | Weighted   |
| --------------------------------------------------------- | ---------- | ---------- | ------------ | -------- | ---------- |
| Habit reminders, goal tracking, summaries                 | Simple     | Small      | $0.002       | 80%      | $0.0016    |
| Lifestyle plans, emotional support, long-context coaching | Complex    | Frontier   | $0.007       | 20%      | $0.0014    |
| **Blended Cost**                                          |            |            |              | **100%** | **$0.003** |

---

## Cascading Strategy

**Triage model:** 
GPT-4.1 Mini / Claude Haiku equivalent

**Frontier model:**
GPT-4o / Claude Sonnet equivalent

**Routing rule:**

→ Small model

* Habit reminders
* Goal tracking
* FAQ questions
* Progress summaries
  
→ Frontier model

* Personalized lifestyle plans
* Multi-step coaching
* Emotional support conversations
* Health information synthesis and long-context reasoning

**Expected cascade ratio:**
* 80% Small
* 20% Frontier

Most traffic should hit the cheap model while only complex requests go to the expensive layer.

---

## Bundling Strategy (Leaders, Fillers & Killers)

### Leader
Features users primarily come for:

* AI Lifestyle Coach
* Personalized daily recommendations
* Goal-based action plans

These are the core value drivers and justify subscription pricing.

### Fillers
Low-cost features that increase perceived value:

* Daily summaries
* Motivational messages
* Habit streak tracking
* Sleep insights
* Progress reports

These cost little but improve retention and ARPU.

### Killers
Keep as premium add-ons:

* Deep agentic health planning
* Long-form report generation
* Continuous monitoring workflows
* Image-based nutrition analysis
* Personalized nutrition planning
* Integration with wearables and automated coaching loops

These create disproportionate inference costs and should not be bundled into the base plan.

Killer usage estimate: 15–25%
Decision: Sell as premium add-on

### 70% Rule
Bundle if >70% of users use it:

#### Bundle
* Daily coach chat
* Progress summaries
* Goal tracking
* Recommendations

#### Premium Add-on
* Advanced health reports
* Wearable integrations
* AI health agent
* Deep analysis workflows

---

## Pricing Model

### Current pricing
€9.99/month premium subscription

### Proposed AI Pricing

#### Essential — €12.99/month

Includes:

* AI lifestyle coach
* Daily guidance and check-ins
* Goal tracking
* Weekly summaries
* Habit and progress insights

Target user:
Users seeking ongoing lifestyle support and accountability.

#### AI Coach Pro — €19.99/month

Includes everything in Essential, plus:

* Extended coaching conversations
* Personalized action plans
* Predictive insights and recommendations
* Priority access to frontier AI models

Target user:
Users actively working toward health, fitness, sleep, or productivity goals.

#### AI Health Agent — €34.99/month

Includes everything in Pro, plus:

* Deep analysis workflows
* Personalized nutrition planning
* Wearable integrations
* Continuous monitoring and coaching loops
* Autonomous planning and follow-up actions

Target user:
Power users seeking highly personalized and proactive coaching.

### Model: Hybrid Subscription

Primary Revenue Model:

* Seat-based subscription

Secondary Revenue Model:

* Usage-based access for premium AI workflows
* Premium AI Health Agent tier

Future Opportunities:

* Outcome-based coaching programs
* Goal-specific transformation packages
* Partner-sponsored health interventions

### Pricing Philosophy

The core coaching experience remains subscription-based, while high-cost AI workflows are monetized through premium tiers. This aligns customer value with AI consumption and protects long-term margins.

**Goal:** Move toward outcome-oriented pricing while maintaining predictable subscription revenue and sustainable AI economics.

### Pricing Strategy
- Strategy posture: Maximize
- Pricing model: Hybrid (base + usage)
- Unit of work metered: Lifestyle coaching sessions completed
- Base fee ($/month): 12.99
- Price per unit: $0.1
- Estimated units/user/month: 70
- Implied revenue/user/month: $19.99

### Decision Note
This pricing structure aligns with how users perceive value from an AI lifestyle coach. Customers are not paying for prompts or tokens; they are paying for personalized coaching interactions that help them achieve meaningful lifestyle improvements.

A hybrid model combines predictable subscription revenue with the flexibility to monetize higher-cost AI workflows separately. The core coaching experience remains accessible through the base subscription, while advanced capabilities such as autonomous coaching, wearable integrations, and deep analysis workflows are positioned as premium offerings.

This approach supports healthy unit economics by aligning AI consumption with customer value, protecting margins through model cascading, and avoiding the over-bundling of expensive agentic features into the base plan.

The pricing strategy follows a maximize posture, focusing on capturing increasing value as users progress from basic lifestyle guidance to highly personalized AI-assisted coaching and behavior-change support.

---

## Stress Tests

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x | Margin drops from 93% → 88% | Increase routing to small model, tighten prompts |
| Heaviest segment doubles | Margin drops from 93% → 90% | Introduce usage limits and premium tier |
| Model provider raises prices 50% | Margin drops from 93% → 91% | Multi-provider strategy and renegotiate contracts |

Our economics remain resilient even under adverse AI cost scenarios.

---

## Board One-Pager

**Before (traditional Lifestyle App):**
* Revenue/User/Month: €9.99
* COGS/User/Month: €0.80
* Gross Margin: ~92%
* Value proposition:

Static habit tracking and lifestyle content.

**After (AI-enabled):**
* Revenue/User/Month: €19.99
* COGS/User/Month: €1.35
* Gross Margin: ~90-93%
* Value proposition:

Personalized AI coaching and behavior-change support.

**Net margin shift:**
* Revenue increase: +100%

Operating costs increase modestly, while remaining a small fraction of revenue due to model cascading and premium feature segmentation.

Net result:

* Significantly higher customer value
* Higher retention
* Stronger differentiation
* Sustainable margins through cascading architecture

### Narrative for the Board
We intentionally accept higher variable AI costs because AI transforms the product from a static wellness app into a personalized lifestyle coach. Cascading architecture keeps costs predictable while premium outcome-based pricing captures the additional value created.
