---
title: "TDD and Contract Testing"
categories:
  - Testing
tags:
  - TDD
---
*Part of my Quality Time Quality Growth series in LinkedIn.*

TDD: I knew the theory, heard wonders about it, but never had the chance to see it action before.

I'm a big believer in learning by doing, so I wanted to give this a proper try using my RAG Chatbot project, using consumer-driven contract testing (Pact).

So I designed a phased approach: 
1 - Consumer contract tests, minimal implementation, then unit tests for behavior + wiring and the rest of the implementation.
2 - Same but in the producer side.

## Some Observations
- It was slower and required a lot more upfront thinking than I was expecting. Making design decisions before writing a single line of real code felt very abstract. 
- The consumer side was manageable. Define what you need, implement the bare minimum, test the behavior. On to the next test.
- The provider side was trickier. Running the service, connecting the Pact broker, managing state providers, updating pacts when the consumer changes... lots of moving parts before you get a running test. 

## I rather have this than retrofitting tests
I've had to retrofit tests to existing code before and it generally meant one of two things:
- Excruciating pain trying to test something that wasn't designed with testability in mind (lots of mocking, hardcoding)
- Modifying the software under test to make testable - with the obvious risk that this brings.
This approach was way more satisfying in that respect, as writing test cases beforehand inevitably makes you design for testability. This in itself justifies the decision of going for TDD.

## Two challenges
### Red phase vs broken setup
When a test fails, I could not always tell: is this failing because it's not implemented yet, is it just a bad test setup (incorrect mock calling, configuration...). I sometimes needed to complete the implementation just to learn the test was not doing what I was expecting. I presume this gets better with experience.
### Contracts vs resilience
I started with contract tests focused on service interactions. I soon started mixing up failure modes (unavailable, timeout...). Those belong in integration/E2E tests, not contracts. Contract tests own the happy path of an interaction (even if that involves a 404 or 403 error), but not when the producer is down or any other 5XX error. Took me a while to untangle both.

## Conclusion
The slowness and the confusion are an investment. Time spent in upfront thinking is time you don't spend down the line when refactors come.
If you're optimizing for short-term velocity, TDD will feel expensive. If you're looking for quality software, it's definitely worth the effort.

This is the way.

!(/assets/images/this_is_the_way.jpeg)
