---
title: "I just wanted a Chat Bot"
categories:
  - AI
tags:
  - Python
---

*Part of my Quality Time Quality Growth series in LinkedIn.*

The idea sounded so simple:
*“I want a chatbot that can quiz me and answer questions about the provided document.”*

This sentence was the simple premise for building my RAG Chatbot quickly revealed that simplicity for humans doesn’t always translate to simplicity for LLMs.

## The Two Modes
The application involved two distinct use cases, each with its own quirks:

1. Exam Prep Chatbot: the user asks the LLM for a question, answers it and gets the correct response back
!![Sequence diagram](/assets/images/exam-prep-chatbot.png)

2. Domain Expert Chatbot: the user asks a question about a particular topic, gets the answer back
!![Sequence diagram](/assets/images/domain-expert.png)
While all this seems trivial for a human, it’s not so straightforward for an LLM: I’ve seen all sorts of erratic behaviors including the chatbot turning the user’s answer into a new question, or returning entire conversations back-to-back as a single response.

## The Problem
It looks like most of this drama was caused by the LLM trying to juggle too many conflicting instructions in a single prompt.

Taking a closer look, I only had issues with the first scenario (the exam prep mode), because it relies on memory. Without going into too much detail, there are mainly two things you can tweak:

- A system prompt: telling the model to act like an instructor or expert in the subject matter
- A condensed question prompt: which builds the actual query from the user input and chat history

The final prompt to the LLM is built as:
- Final prompt: system prompt + context (provided by the retriever) + condensed question prompt
![Sequence diagram](/assets/images/sequence-diagram.png)

Ultimately, asking the LLM to handle both exam-prep and domain-expert logic through a single prompt turned out to be too much cognitive load for both the model and for me. The challenge was that a single prompt created ambiguity for the LLM, leading to erratic behavior.

## The “Solution”
So, me being pragmatic, I took the hit. Now I’m looking to simplify the app and add an operational mode selector: exam-prep or domain expert.

Next step is to implement that. Hopefully, no surprises. Stay tuned.
