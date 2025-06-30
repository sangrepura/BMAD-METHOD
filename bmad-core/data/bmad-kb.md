# BMAD Knowledge Base (v1.1)

## Overview

BMAD-METHOD (Breakthrough Method of Agile AI-driven Development) is a framework that combines AI agents with Agile development methodologies. The v4 system introduces a modular architecture with improved dependency management, bundle optimization, and support for both web and IDE environments.

## How BMAD Works

### The Core Method

BMAD transforms you into a "Vibe CEO"—directing a team of specialized AI agents through structured workflows. Here's how:

1.  **You Direct, AI Executes**: You provide vision and decisions; agents handle implementation details.
2.  **Specialized Agents**: Each agent masters one role (PM, Developer, Architect, etc.).
3.  **Structured Workflows**: Proven patterns guide you from idea to deployed code.
4.  **Active Verification, Not Passive Approval**: Using structured `checklists`, you actively verify that an agent's work meets the requirements before proceeding, ensuring quality at every step.

### The Two-Phase Approach with Feedback Loops

BMAD uses a hybrid model that combines the strengths of upfront planning with the flexibility of agile feedback.

**Phase 1: Planning & Design (Web UI - Cost Effective)**
* Use large context window models (like Gemini) to collaboratively generate comprehensive documents (PRD, Architecture) with specialized agents.
* This phase establishes a strong, well-reasoned plan.
* **Optional Feedback Sprints (New):** To de-risk the plan, this phase now includes optional but highly recommended "Feedback Sprints." After key documents are drafted (like the UI/UX Spec), you can direct the `ux-expert` to create a simple, clickable prototype to test with real users. This ensures the core concept is validated **before** full development begins.

**Phase 2: Development & Implementation (IDE - Implementation)**
* The approved planning documents are "sharded" into manageable user stories.
* Specialist agents execute these focused stories sequentially in a clean environment.
* **Optional Technical Spikes (New):** If the architecture contains a high-risk technical challenge, the `architect` can initiate a "technical spike"—a single, focused story for the `dev` agent to build a proof-of-concept for that specific problem. This validates technical feasibility early.

### The Development Loop

```text
1. SM Agent (New Chat) → Creates next story from sharded docs
2. You → Review and approve story
3. Dev Agent (New Chat) → Implements approved story
4. QA Agent (New Chat) → Reviews and refactors code
5. You → Verify completion
6. Repeat until epic complete