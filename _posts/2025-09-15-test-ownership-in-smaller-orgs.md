---
title: "Test Ownership in Smaller Orgs"
categories:
  - Leadership
---

What’s the best way to achieve quality in small organizations?

There’s no single answer, but one key aspect that keeps coming up is how testing is owned: should it sit mainly with developers, or should there be dedicated QA roles? 

This isn’t the whole story when it comes to quality, but it’s an important piece of the puzzle.

We all know how big tech let go of many of their dedicated quality roles in favor of sharing the responsibility across the team. This change seemed to go well for them, but aside from big tech, does this apply across smaller companies as well?

In my opinion, there are major factors that balance the scales in favor of large orgs:
 - Talent pool: Consisting of highly specialized and well-trained devs.
 - DevOps maturity and tech stack: Robust observability, microservices, and a high-maturity DevOps culture enable rapid, low-cost testing in production.
 - Brand resilience: Large orgs can sustain more damage to their reputation than smaller orgs, where a single quality issue could be a major blow.

But not everybody works at Google or Spotify. For smaller orgs, the game is completely different. They're often more sensitive to time-to-market, lack the safety net of a large user base, and can't afford to get it wrong. This is where dedicated testers become critical to manage risk and ensure product quality before launch.

Some general considerations before adopting developer-owned testing:
 - High-stakes systems: Mission-critical apps can’t afford hidden risks or overlooked issues.
 - Domain complexity: Specialized testers may be needed when devs lack deep domain expertise.
 - Regulatory demands: Industries with compliance requirements often need formalized reporting.
 - Testing imbalance: Developers usually emphasize unit/integration tests, leaving gaps at higher levels (E2E, exploratory).
 - Team sustainability – Pushing all testing onto devs can increase friction, frustration, and burnout.

Ultimately an org’s success comes down to their commitment to quality and risk awareness. Whether the ownership is delegated to a dedicated QA Engineer or spread out across the team depends on the specific context.



Some sources:
 - AB Testing episode where they shared that developer-owned testing had a higher positive correlation with quality than QA-owned testing. https://open.spotify.com/episode/6aCFOeES5WITId2IRwQv8T?si=7qpq1sVhTfCVs-8s7OxjLw 

 - How Big Tech does QA: https://newsletter.pragmaticengineer.com/p/how-big-tech-does-qa.