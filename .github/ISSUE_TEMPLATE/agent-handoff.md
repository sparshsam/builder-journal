name: Agent Handoff
description: Record a handoff between agents working on ecosystem tasks
title: "[Handoff] "
labels: [handoff, coordination]
assignees: []
body:
  - type: markdown
    attributes:
      value: |
        Use this template when passing work from one agent to another.
  - type: input
    id: source_agent
    attributes:
      label: Source Agent
      description: Which agent is handing off?
      placeholder: e.g., Hermes
    validations:
      required: true
  - type: input
    id: target_agent
    attributes:
      label: Target Agent
      description: Which agent is receiving the handoff?
      placeholder: e.g., Codex
    validations:
      required: true
  - type: textarea
    id: current_state
    attributes:
      label: Current State
      description: What is done, in progress, or blocked?
    validations:
      required: true
  - type: input
    id: branch
    attributes:
      label: Branch
      description: Which branch contains the current work?
    validations:
      required: false
  - type: input
    id: pr
    attributes:
      label: PR
      description: URL to the pull request (if any).
    validations:
      required: false
  - type: textarea
    id: context
    attributes:
      label: Context
      description: Background, decisions, and constraints the receiving agent needs.
    validations:
      required: false
  - type: textarea
    id: known_issues
    attributes:
      label: Known Issues
      description: Any unresolved issues or edge cases.
    validations:
      required: false
  - type: textarea
    id: next_steps
    attributes:
      label: Next Steps
      description: What the receiving agent should do next.
      placeholder: |
        - [ ] Step 1
        - [ ] Step 2
    validations:
      required: true
  - type: textarea
    id: final_report
    attributes:
      label: Final Report (filled after completion)
      description: See `agents/handoff-template.md` for canonical format.
    validations:
      required: false
