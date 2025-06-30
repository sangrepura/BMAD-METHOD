# Checklist Validation Task

## Purpose
To systematically verify project artifacts against a defined set of quality standards, ensuring alignment, completeness, and readiness for the next phase of development.

## Context
The BMAD Method uses various checklists to ensure quality and completeness. This task reframes the checklist not as a passive quality gate, but as an **active verification script**. The user's role is to leverage the agent's analysis to confirm that all requirements from a previous stage have been met in the current stage's output.

## Available Checklists

If the user asks or does not specify a specific checklist, list the checklists available to the agent persona. If the task is being run not with a specific agent, tell the user to check the bmad-core/checklists folder to select the appropriate one to run.

## Instructions

1.  **Initial Assessment & Artifact Gathering**:
    * Load the specified checklist (e.g., `po-master-checklist`).
    * The checklist itself will specify its required input documents (e.g., `prd.md`, `architecture.md`).
    * Gather all required artifacts for analysis.

2.  **Checklist Execution & Verification**:
    * For each item in the checklist, perform a deep analysis of the provided artifacts.
    * **Verify** that the requirement is explicitly met.
    * Cite specific sections from the documents as evidence.
    * **Example Verification:** "Checking item 1.1: 'Architecture supports all functional requirements in the PRD.' I have cross-referenced the 9 functional requirements in `prd.md` and confirmed that each has a corresponding implementation plan in the `architecture.md` sections for Components, Data Models, and API Specs."
    * Mark items as:
        * ✅ PASS: Requirement clearly met
        * ❌ FAIL: Requirement not met or insufficient coverage
        * ⚠️ PARTIAL: Some aspects covered but needs improvement
        * N/A: Not applicable to this case

3.  **Final Report**:
    * Prepare a summary report that includes:
        * Overall checklist completion status (pass/fail percentage).
        * A list of any "FAIL" items with clear evidence and rationale.
        * Specific, actionable recommendations to address any identified gaps.
