---
phase: 3
artifact: prd
project: <project_name>
owner: <product_owner>
updated: <YYYY-MM-DD>
sources: []
links:
  profile: ./PROFILE.yaml
  context: ./CONTEXT.md
  idea: ./IDEA_NOTE.md
  poc: ./POC_PLAN.md
---

Product Summary
- <one_paragraph_summary>

Users and Use Cases
- Primary users: <roles>
- Top use cases:
  - <use_case_1>
  - <use_case_2>

Requirements
- Must have:
  - <requirement_1>
  - <requirement_2>
- Nice to have:
  - <nice_1>
  - <nice_2>

Acceptance Criteria
- Scenario: <scenario_name>
  - Given <context>
  - When <action>
  - Then <observable_outcome>

Non-Functional Requirements
- Performance: <targets>
- Security: <considerations>
- Reliability: <targets>
- Observability: <logs_metrics>

Rollout Plan
- Milestones:
  - M1: <goal>
  - M2: <goal>
- Release criteria: <criteria>

Phase 3 Prompt Starters
```text
Define MVP requirements:
- List must-haves and acceptance criteria.
- Capture non-functional requirements and rollout plan.
Outputs: PRD.md with clear, testable acceptance criteria.
```


