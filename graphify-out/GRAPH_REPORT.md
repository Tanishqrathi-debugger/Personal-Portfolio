# Graph Report - .  (2026-04-22)

## Corpus Check
- Corpus is ~24,117 words - fits in a single context window. You may not need a graph.

## Summary
- 24 nodes · 23 edges · 6 communities detected
- Extraction: 52% EXTRACTED · 43% INFERRED · 4% AMBIGUOUS · INFERRED: 10 edges (avg confidence: 0.81)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- [[_COMMUNITY_Interaction Effects|Interaction Effects]]
- [[_COMMUNITY_Failure-to-Success Narrative|Failure-to-Success Narrative]]
- [[_COMMUNITY_Design Vision and Messaging|Design Vision and Messaging]]
- [[_COMMUNITY_Portfolio Information Architecture|Portfolio Information Architecture]]
- [[_COMMUNITY_Script File Node|Script File Node]]
- [[_COMMUNITY_Hero Journey Visual|Hero Journey Visual]]

## God Nodes (most connected - your core abstractions)
1. `Transition Leap Across Chasm` - 5 edges
2. `Success Cliff` - 4 edges
3. `Smooth Scroll Navigation Handler` - 4 edges
4. `DOMContentLoaded Initializer` - 3 edges
5. `Intersection Fade-in Observer` - 3 edges
6. `Failure Cliff` - 2 edges
7. `Growth Through Risk-Taking Rationale` - 2 edges
8. `Personal Growth Journey` - 2 edges
9. `Navbar Scroll Effect` - 2 edges
10. `Portfolio Page Sections` - 2 edges

## Surprising Connections (you probably didn't know these)
- `Scroll Animation Interactivity Concept` --implements--> `Intersection Fade-in Observer`  [INFERRED]
  implementation_plan.md → portfolio\script.js
- `Smooth Scroll Navigation Handler` --references--> `Portfolio Page Sections`  [EXTRACTED]
  portfolio\script.js → portfolio\index.html
- `Scroll Animation Interactivity Concept` --implements--> `Smooth Scroll Navigation Handler`  [INFERRED]
  implementation_plan.md → portfolio\script.js
- `Navbar Scroll Effect` --references--> `Navbar Component`  [EXTRACTED]
  portfolio\script.js → portfolio\index.html
- `Intersection Fade-in Observer` --references--> `Fade-in Target Components`  [EXTRACTED]
  portfolio\script.js → portfolio\index.html

## Hyperedges (group relationships)
- **Failure-to-Success Transformation** — failure_to_success_failure_cliff, failure_to_success_jumping_person, failure_to_success_transition_leap, failure_to_success_success_cliff [EXTRACTED 1.00]
- **Scroll Navigation Experience Flow** — script_smooth_scroll_navigation, index_navigation_links, index_page_sections [INFERRED 0.86]
- **Resilience and Growth Narrative** — readme_portfolio_mission, index_failure_to_success_journey, index_basic_learnings_thoughts [INFERRED 0.74]

## Communities

### Community 0 - "Interaction Effects"
Cohesion: 0.29
Nodes (8): Scroll Animation Interactivity Concept, Fade-in Target Components, Navbar Component, Navigation Anchor Links, DOMContentLoaded Initializer, Intersection Fade-in Observer, Navbar Scroll Effect, Smooth Scroll Navigation Handler

### Community 1 - "Failure-to-Success Narrative"
Cohesion: 0.53
Nodes (6): Failure Cliff, Growth Through Risk-Taking Rationale, Jumping Person Silhouette, Personal Growth Journey, Success Cliff, Transition Leap Across Chasm

### Community 2 - "Design Vision and Messaging"
Cohesion: 0.4
Nodes (5): Premium Dark Glassmorphism Theme Concept, Theme Choice Rationale, Basic Learnings and Thoughts Section, Failure to Success Journey Section, Portfolio Market Presence Mission

### Community 3 - "Portfolio Information Architecture"
Cohesion: 0.67
Nodes (3): Planned Portfolio Section Architecture, Portfolio Page Sections, Resume CTA Block

### Community 4 - "Script File Node"
Cohesion: 1.0
Nodes (0): 

### Community 5 - "Hero Journey Visual"
Cohesion: 1.0
Nodes (1): Failure to Success Motivational Illustration

## Ambiguous Edges - Review These
- `Resume CTA Block` → `Planned Portfolio Section Architecture`  [AMBIGUOUS]
  implementation_plan.md · relation: implements

## Knowledge Gaps
- **8 isolated node(s):** `Failure to Success Motivational Illustration`, `Jumping Person Silhouette`, `Navbar Component`, `Navigation Anchor Links`, `Fade-in Target Components` (+3 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **Thin community `Script File Node`** (1 nodes): `script.js`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Hero Journey Visual`** (1 nodes): `Failure to Success Motivational Illustration`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **What is the exact relationship between `Resume CTA Block` and `Planned Portfolio Section Architecture`?**
  _Edge tagged AMBIGUOUS (relation: implements) - confidence is low._
- **Why does `Smooth Scroll Navigation Handler` connect `Interaction Effects` to `Portfolio Information Architecture`?**
  _High betweenness centrality (0.113) - this node is a cross-community bridge._
- **Why does `Portfolio Page Sections` connect `Portfolio Information Architecture` to `Interaction Effects`?**
  _High betweenness centrality (0.063) - this node is a cross-community bridge._
- **Are the 2 inferred relationships involving `Transition Leap Across Chasm` (e.g. with `Growth Through Risk-Taking Rationale` and `Personal Growth Journey`) actually correct?**
  _`Transition Leap Across Chasm` has 2 INFERRED edges - model-reasoned connections that need verification._
- **Are the 2 inferred relationships involving `Success Cliff` (e.g. with `Growth Through Risk-Taking Rationale` and `Personal Growth Journey`) actually correct?**
  _`Success Cliff` has 2 INFERRED edges - model-reasoned connections that need verification._
- **What connects `Failure to Success Motivational Illustration`, `Jumping Person Silhouette`, `Navbar Component` to the rest of the system?**
  _8 weakly-connected nodes found - possible documentation gaps or missing edges._