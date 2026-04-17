---
stepsCompleted: [1, 2]
inputDocuments: []
session_topic: 'NEXUS — Multi-layered RE/MAX hub for Costa Rica & CCA region'
session_goals: 'Map layer interactions, define feature boundaries, explore CRM scoping, prepare for PRD'
selected_approach: 'ai-recommended'
techniques_used: []
ideas_generated: []
context_file: ''
---

# Brainstorming Session Results

**Facilitator:** Nicolascastro
**Date:** 2026-04-17

## Session Overview

**Topic:** NEXUS — A 4-layer platform (Buyer → Agent → Broker → Region) that modernizes property discovery and operational data for RE/MAX offices in the Caribbean & Central American market.

**Goals:**
- Map exactly how each layer works and interconnects
- Define core value propositions per layer
- Identify feature boundaries (in vs. out vs. v2)
- Explore CRM as a potential cross-layer feature
- Prepare a clean mental model for a tight PRD

### Context Guidance

_NEXUS has two data foundations: RE/MAX CCA office APIs (one for agents, one for properties). The product serves two core processes: (1) buyer experience (Tinder-style discovery) and (2) administrative experience (metrics/dashboards for agents, brokers, regional owners). Target buyer persona is the office broker._

### Session Setup

_Fresh workspace — no existing project documents. The session aims to decompose a complex 4-layer SaaS product into digestible, well-scoped components before entering the BMAD planning phase._

## Technique Selection

**Approach:** AI-Recommended Techniques
**Analysis Context:** Multi-layer SaaS product with complex data flows, multiple user personas, and market-fit validation needs

**Recommended Techniques:**
- **Morphological Analysis:** Systematically explore all parameter combinations across layers
- **Role Playing (Stakeholder Perspectives):** Generate solutions from buyer, agent, broker, and regional owner viewpoints
- **Ecosystem Thinking:** Analyze NEXUS as an ecosystem with symbiotic relationships between layers
- **Constraint Mapping:** Identify real vs. imagined constraints around API data, scope, and CRM
- **Reverse Brainstorming:** Surface hidden risks by asking "how could each layer fail?"

**AI Rationale:** NEXUS's complexity demands structured decomposition (Morphological Analysis) combined with empathy-driven persona exploration (Role Playing). The inter-layer dependencies make it a natural ecosystem. Constraint Mapping addresses the CRM scoping question directly, and Reverse Brainstorming ensures we stress-test before committing to a PRD.

## Pre-Session Decisions — SETTLED ✅

### Decision 1: CRM Scope — CRM-Mid

**What CRM-Mid means inside NEXUS:**
- Contact cards auto-created from buyer activity + agent uploads (emergent from existing data)
- Simple pipeline view (lead → showing → offer → close)
- Match notifications between buyer preferences and listings
- Manual lead entry from external sources (WhatsApp, referrals, walk-ins, portals)
- Basic task/follow-up reminders
- Notes on contacts
- Lead source tracking

**What is explicitly OUT (v2+ / CRM-Full):**
- Email/WhatsApp integration & automated drip campaigns
- Pipeline automation rules
- Commission tracking tied to CRM contacts
- Advanced reporting dashboards beyond core NEXUS metrics

**Rationale:** RE/MAX CCA offices use ZERO CRM. No competition. CRM-Mid is largely emergent from existing data, plus manual lead capture flows agents desperately need.

---

### Decision 2: Business Model — Freemium, Costa Rica First

**Model:** Gift platform to all RE/MAX Costa Rica offices. Free tier for everyone. Paid tier per office.

**Go-to-market:** Start with RE/MAX Costa Rica (whole country), then expand to CCA region with proven traction.

**Paywall Principle: Free = Full data transparency. Paid = Tools, intelligence, and analytics.**
- Never hide data that the user generated (buyer interest in their listings)
- Charge for the TOOLS to act on that data (CRM, matching, advanced analytics)

**Free Tier (All offices):**
- Buyer layer: full swipe experience, preferences, co-buyer sharing
- Agent: see which buyers liked which listings (names, preferences, contact info)
- Agent: basic listing count, views per listing, interested buyer count
- Broker: agent count, total listings, total interested buyers (raw numbers)
- Region: office count, total listings per office

**Paid Tier (Per office subscription):**
- Agent: Full CRM-Mid (pipeline, tasks, reminders, notes, manual lead entry, lead source tracking)
- Agent: Proactive matching engine (new listing → existing matching buyers + notifications)
- Agent: Advanced listing metrics (trends over time, price positioning, days-on-market analysis)
- Broker: Full dashboards (agent comparison, conversion funnels, revenue trends, market heat maps)
- Region: Office ranking, cross-office comparison, regional market trends, underperformance alerts

---

### Decision 3: Bottom-Up Tease Engine

**Mechanic:** Free users see the OUTPUT of paid features but can't access the WORKFLOW.

**Agent teases (drive agent → broker pressure):**
- "3 of these buyers also match your new listing → 🔒 Upgrade to see matches"
- "Organize these contacts into a pipeline → 🔒 Upgrade for CRM" (with blurred pipeline preview)
- "Your listing views dropped 40% this week → 🔒 See why" (grayed-out trend chart)
- "You have 2 follow-ups overdue" (can see count, can't manage tasks)

**Broker teases (direct conversion pressure):**
- "3 agents have conversion rates below 20% → 🔒 See who and why"
- "Your office ranks #4 of 12 in Costa Rica → 🔒 See the benchmark"
- "Agent Carlos has 47 unmanaged leads → 🔒 Enable CRM for your office"

**Goal:** Agents lobby the broker to pay. The broker isn't buying software — they're stopping revenue leakage.

---

### Decision 4: Data Integrity — Honest Metrics Framework

**Problem:** NEXUS only captures swipe data passively. APIs provide property info only (no engagement metrics). External channels (WhatsApp, Facebook, walk-ins) are invisible without CRM input.

**Solution — Three-tier data reliability:**

| Tier | Data Source | Metric Label | Available To |
|------|-----------|-------------|-------------|
| Passive Only | NEXUS swipes | "NEXUS engagement" | Free + Paid |
| CRM-Enhanced | Swipes + manual lead entries | "Total market engagement" | Paid only |
| Future: Syndication | Swipes + CRM + external site data | "Complete market engagement" | Future scope |

**Key principle:** Never say "underperforming" without qualifying the data source. Free tier labels metrics as "NEXUS engagement." Paid tier with CRM data can make stronger claims ("across all lead sources...").

**CRM as data completeness engine:** The more agents use CRM to log external leads, the more accurate ALL metrics become — creating a virtuous cycle.

---

### Decision 5: Future Scope — Listing Syndication (Layer 1b)

**Concept:** Integrate NEXUS with existing property search websites (e.g., Encuentra24, local portals).

**Two-way value:**
- **OUTBOUND:** Auto-syndicate listings from NEXUS/API to external search sites → agents save time, cover more market, listings appear everywhere automatically instead of manual posting
- **INBOUND:** Capture buyer interest/engagement data from those external sites back into NEXUS → feeds CRM, improves metric accuracy, closes the data completeness gap

**Why this strengthens the paid tier:** Automated multi-site syndication is a massive time-saver and market-coverage expansion. Strong justification for paid subscription.

**Status:** Explicitly future scope. Not in v1. Will re-evaluate after Costa Rica launch.
