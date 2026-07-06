# DEHALL

DEHALL is a starting point for a "dehallucination reasoning layer" that supports RAG (Retrieval-Augmented Generation), fact checking, grounding, and self verification.

## Purpose

- Build a dehall layer focused on Python code analysis, especially for datamining and statistical pattern discovery in large-scale datasets
- Develop an additional layer that checks and substantiates generated code-related reasoning
- Align findings with sources and evidence from data
- Produce grounded answers with references to code, data, or statistical insights
- Self-check for consistency and correctness in the generated reasoning

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
