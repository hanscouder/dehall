# DEHALL

DEHALL is a starting point for a "dehallucination reasoning layer" that supports RAG (Retrieval-Augmented Generation), fact checking, grounding, and self verification.

## Purpose

- Develop an additional layer that checks and substantiates answer generation
- Align facts with sources
- Produce answers with source references
- Self-check for consistency and correctness

## Structure

- `skills/` contains code and modules for the different components
- `instructions/` contains design documents, prompt templates, and conceptual specifications

## First step

1. Describe the four core components in `instructions/dehall.md`
2. Build a base pipeline in `skills/dehall_skeleton.py`
3. Iteratively expand the RAG, grounding, and verification logic from there

## Copilot integration

You do not build this layer as a direct addition inside GitHub Copilot itself.
Instead, create a wrapper or module that supports Copilot or an LLM call.

- `instructions/` is primarily for specifications and prompt design
- `skills/` is for actual code and pipelines

## Next step

- Add concrete retrieval adapters later for vector stores, knowledge sources, or APIs
- Add verification and fact-checking rules
- Write examples of prompt templates and use cases
