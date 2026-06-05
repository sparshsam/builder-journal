name: Build Task
description: Scope and track a build task or feature implementation
title: "[Build] "
labels: [build]
assignees: []
body:
  - type: markdown
    attributes:
      value: |
        Use this template to define a build task. Check the relevant roadmap in `plans/` first.
  - type: input
    id: project
    attributes:
      label: Project
      description: Which project does this build task belong to?
      placeholder: e.g., FridgeWise
    validations:
      required: true
  - type: textarea
    id: purpose
    attributes:
      label: Purpose
      description: What does this task accomplish?
      placeholder: Describe the purpose and motivation.
    validations:
      required: true
  - type: textarea
    id: scope
    attributes:
      label: Scope
      description: List the specific deliverables.
      placeholder: |
        - [ ] Deliverable 1
        - [ ] Deliverable 2
    validations:
      required: true
  - type: textarea
    id: non_goals
    attributes:
      label: Non-Goals
      description: What is explicitly out of scope?
      placeholder: "Out of scope for this task:"
    validations:
      required: false
  - type: dropdown
    id: risk
    attributes:
      label: Risk Level
      options:
        - Low
        - Medium
        - High
      default: 0
    validations:
      required: true
  - type: textarea
    id: security
    attributes:
      label: Privacy / Security Considerations
      description: What data is involved? What must not be exposed?
      placeholder: "Data handled: ...\nMust not expose: ..."
    validations:
      required: false
  - type: textarea
    id: notes
    attributes:
      label: Agent Notes
      description: Anything another agent should know before working on this.
    validations:
      required: false
  - type: textarea
    id: definition_of_done
    attributes:
      label: Definition of Done
      description: What constitutes completion?
      placeholder: |
        - [ ] MVP scope implemented
        - [ ] Tests pass
        - [ ] Security boundaries respected
        - [ ] Public-safe language verified
    validations:
      required: true
