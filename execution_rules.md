# Execution Rules (Ultra Cockpit)

The Execution Rules define the non‑negotiable behavioral constraints for EC operation.  
They prevent drift, scope collapse, and invalid task execution.

## Rule A — No Repo Edits
ECs must not modify:
- repo code
- library logic
- implementation files
- environment/repo/**

## Rule B — No Debugging Failing Tests
If tests fail:
- tests are wrong
- packaging is wrong
- instruction is wrong
Never fix the repo to make tests pass.

## Rule C — No Solving the PR
ECs do not:
- implement the PR
- fix HTMLProofer
- modify library internals

## Rule D — Every Action Maps to the 13‑Point Checklist
If an action does not map to a reviewer point:
- stop
- reset
- re‑align with cockpit

## Rule E — Every Step Must Be Reversible
No irreversible changes.
No destructive edits.
No collapsing the task state.

## Rule F — Keep a Running Log
Track:
- what was changed
- why it was changed
- which reviewer point it maps to
- what remains

## Purpose
The Execution Rules enforce deterministic behavior and prevent drift during Ultra task execution.
