# Cost Curve & Pricing Strategy

## Cost Model

| Cost Category | Per-User/Month | Notes |
|--------------|----------------|-------|
| Inference (primary model) | €1.20 | Daily coaching conversations, habit recommendations |
| Inference (cascading/triage) | €0.40 | Small model handles ~80% of requests |
| Infrastructure | €0.50 | Hosting, API gateway, monitoring |
| Data/storage | €0.20 | User profiles, history, embeddings |
| Human-in-the-loop | €0.30 | Occasional review of edge cases and safety checks |
| **Total AI COGS** | €2.60 | Blended monthly AI cost |

## Cascading Strategy

**Triage model:** 
GPT-4.1 Mini / Claude Haiku equivalent

**Frontier model:**
GPT-4o / Claude Sonnet equivalent

**Routing rule:**
* Habit reminders
* Goal tracking
* FAQ questions
* Progress summaries
→ Frontier model

* Personalized lifestyle plans
* Multi-step coaching
* Emotional support conversations
* Complex health reasoning
→ Frontier model

**Expected cascade ratio:**
80% Small model
20% Frontier model
Most traffic should hit the cheap model while only complex requests go to the expensive layer.

## Pricing Model

**Current pricing:**
**Proposed AI pricing:**
**Model:** seat-based / usage-based / outcome-based / hybrid

## Stress Tests

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x | | |
| Heaviest segment doubles | | |
| Model provider raises prices 50% | | |

## Board One-Pager
<!-- Before/After: Old SaaS revenue vs. AI usage revenue for your product -->

**Before (traditional SaaS):**
**After (AI-enabled):**
**Net margin shift:**
