---
layout: splash
title: "About"
permalink: /about/
author_profile: true
---
## About Me
Over the past 15 years I've worked across video streaming (Accedo, Verimatrix), VR/MR (YBVR), and sustainability tech (osapiens) — building automation frameworks, integrating test suites into CI/CD pipelines, setting up cloud-based test environments, and leading small QE teams. The thread across all of it has been the same: figuring out where systems are likely to break, and building the infrastructure to catch it early. 

That background is what I'm now building on as I specialize in quality systems for API-driven backends: the CI pipelines, test strategies, and environment infrastructure that make teams confident in what they ship. I'm building hands-on depth in microservices testing and exploring how AI can make those systems smarter, from evaluating AI features to using AI to support quality decisions.

## How I see the role evolving
For years QA teams were treated as gatekeepers, responsible for validating developers' work after the fact. I've always believed this model is inefficient and underutilizes experienced quality engineers. I talked about this in my talk at the BrowserStack Meetup Madrid - [From Gatekeeper to  Enabler - My Journey to Modern QA](https://www.linkedin.com/posts/anusha-majidi_im-really-happy-to-share-that-yesterday-ugcPost-7376903365936476160--iV4)

The direction I see the industry moving — especially with AI accelerating development — is toward quality engineers enabling teams rather than policing them. That means building testing infrastructure, improving feedback loops, and designing systems that are testable from the start.


## What I've built
I started exploring AI in quality engineering because I wanted to understand what it actually takes to test AI systems hands on. That led me to build a RAG chatbot, wrap it in a FastAPI service, and then build an automated evaluation system around it using DeepEval and MLflow. The evaluation pipeline reduced manual review cycles from 4 hours to 30 minutes, surfaced failure patterns I wouldn't have caught otherwise, like ungrounded correctness. It also taught me how complex the requirements to test an AI-powered system can be.
I spoke about this work at [Automation Guild 2026](https://testguild.com/automation-guild-2026/), shared my learnings in [this blog post](https://eliaspardo.github.io/ai/lessons-learned-from-building-an-ai-evaluation-system/) and wrote up the full experience as a [case study](https://eliaspardo.github.io/case-studies/2026-02-21-from-4-hours-to-30-minutes-building-an-automated-ai-evaluation-system/).
I'm not claiming to be an AI testing expert. What I am is a quality engineer who has shipped real AI evaluation infrastructure and is deliberately building deeper capabilities in this space. And I’m doing so in a real project, working on code.

## What I'm working on now
I'm currently building a microservices quality lab using my RAG Chatbot as a system under test: a local-first test environment with unit, contract, and E2E smoke tests across service boundaries. The plan is to progressively layer on CI pipelines with quality gates, environment reproducibility, async failure-mode testing, and eventually an AI agent that consumes real test artifacts (logs, traces, reports) to assist with failure analysis.
The goal is to have a complete, demonstrable quality system — from local test execution to CI enforcement — that shows how I think about test architecture decisions.

## What I bring to a team
* **Quality systems design**: I think in terms of workflows, feedback loops, test boundaries, and failure modes.
* **Test infrastructure experience**: CI/CD integration, environment management, test data strategies, contract testing across projects - now consolidating this into a focused specialty.
* **AI in Quality Engineering**: Hands-on experience building applications and evaluation pipelines for AI systems, with a clear trajectory toward using AI to improve testing itself.
* **Collaboration**: I work best in small, high-trust teams where quality is a shared concern. I'd rather own test capabilities than test results.

## Where to find me
* **Github**: [profile](https://github.com/eliaspardo)
* **LinkedIn**: [profile](https://www.linkedin.com/in/eliaspardo/)
* **BrowserStack QA Meetup**: [meetup page](https://www.meetup.com/browserstack-qa-meetup-group-madrid/)
* **Email**: [mail](mailto:eliaspardo@gmail.com)

[Download my resume](https://docs.google.com/document/d/e/2PACX-1vT5NEwX3aO6s2qtw3WEmOrre1E6yISugE0u95-NmELvCUdQYAmjiwUHC6L8RPqhJqSU8MBa-GGVDicB/pub){: .btn .btn--primary}
