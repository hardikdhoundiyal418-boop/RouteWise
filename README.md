# RouteWise — Intelligent Multimodal Travel Planner
**Tagline:** One Journey. Smarter Routes. Greener Choices.

> Status: Proposed Concept for IIIT Delhi Open Innovation Round 1
> Category: Smart Mobility, AI, Sustainable Transportation

## Overview
RouteWise is a proposed intelligent travel-planning app that helps users compare routes and transport modes by:
- Fastest travel time
- Lowest estimated cost
- Lower estimated environmental impact
- Transfers & convenience
- User preferences (balanced)

Combines walking, cycling, metro, buses, trains, road transport (Walk+Metro+Bus etc.).

**Important:** Concept + UI mockup + architecture proposal only. Not deployed. All times/fares marked sample illustrative.

## Pitch Deck
Located in /docs/RouteWise_Premium_Redesign.pptx — 9 slides, dark tech theme #0A1930 / #10D48E / #60A5FA

## Problem
Travellers need unified decision-support platform that compares available routes and transport modes according to individual priorities, without manually evaluating multiple sources.

Current: fragmented maps, fare info scattered, traffic/schedule uncertainty, environmental impact hard to compare.

## Solution Flow
1. Enter origin & destination
2. Retrieve route & transport options via routing/transit providers
3. Compare duration, cost, transfers, emissions
4. Rank by user priorities
5. Select & view journey steps

UI shows 3 cards:
- FASTEST: 32 min sample, Walk+Metro+Walk, 1 transfer
- LOWEST EST COST: Rs 38 est sample, 48 min sample, Bus+Metro
- LOWER EMISSION: 41 min sample, Cycle+Metro+Walk, lower est impact*

*Estimates depend on mode/distance/occupancy assumptions.

## Target Users
- Students & College Commuters
- Daily Office Commuters
- Budget-Conscious Travellers
- Environmentally Conscious Travellers

## Architecture (Proposed)
Frontend: React/Next.js
Backend: Python FastAPI
Routing & Transit: Maps/routing provider, schedules, traffic/fare where available
TinyFish: Search, page fetch, web-agent workflows (supplementary)
Recommendation: Compare, apply priorities, rank, explain
Storage: PostgreSQL + Cloud hosting, env vars for keys

Security: Server-side API keys only, validation, error handling, source verification.

## TinyFish Integration (Competition Requirement)
Use Cases: Web Search (service announcements), Page Fetching (extract with source links), Web-Agent workflows (structured supplementary info)

Workflow: USER INPUT -> BACKEND -> ROUTING APIS + TINYFISH -> VALIDATION -> RECOMMENDATION -> RESULTS UI

Safeguards: Validate freshness, associate source, handle failures/rate limits, verify docs/endpoints/auth/pricing. TinyFish supplementary only, not replacement for routing engine.

See docs/TINYFISH_INTEGRATION.md

## Feasibility & Roadmap
Phase 1: Concept & UI Prototype
Phase 2: Routing Integration & Ranking
Phase 3: TinyFish Integration & Validation
Phase 4: Expanded City Coverage & Optimisation

## Team 
Team Name:IMMORTAL
Members: [Saksham Saxena - Product], [Athrv Aggarwal - UX], [Hardik Dhoundiyal - Backend]
Contact:hardikdhoundiyal418@gmail.com | Unstop ID:hardikdhoundiyal418@gmail.com

No invented users/partnerships/savings claimed.
