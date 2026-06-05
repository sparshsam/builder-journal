# Agent Handoff Template

## When to Use

Use this template to hand off work from one agent to another. The handoff is complete when the receiving agent has confirmed receipt and understands the next action.

## Required Final Report Format

Every agent completing a task must file a final report using the format below. This report must be committed to the branch or posted in the PR description.

```
# Agent Final Report

## Summary

Brief description of what was accomplished, the scope of work, and any important decisions made.

## Branch

`<type>/<scope>-<description>`

## PR

URL to the pull request on GitHub.

## Merge Commit

Commit hash after merge (filled in after merge completes).

## Files Changed

- `path/to/file` — reason for change
- `path/to/file` — reason for change

## Tests / Checks Run

- [x] Lint passed
- [x] Build / compile check
- [x] Link verification (if applicable)
- [ ] Other: ...

## Docs Updated

- `path/to/doc` — what changed

## Profile Repo Updated

Yes / No
If Yes: commit hash in `sparshsam/sparshsam`.

## Known Issues

Any issues left unresolved, edge cases not handled, or decisions deferred.

## Next Recommended Action

What the next agent or human should do with this work.
```

## Handoff Communication Checklist

Before declaring a handoff complete:

- [ ] Final report is committed or included in PR description.
- [ ] All files are listed and their purpose is clear.
- [ ] Known issues are documented.
- [ ] Next action is specified.
- [ ] Receiving agent has been notified (via PR comment, commit message, or direct message).
