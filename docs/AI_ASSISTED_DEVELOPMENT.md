# AI-Assisted Development Workflow

Yar AI Developer is also a practical record of how I work with AI during software development.

My approach is not "ask AI for code and paste it". I use AI as a development partner inside a verification loop.

## Typical loop

1. Define the real objective and constraints.
2. Break the task into smaller technical steps.
3. Ask AI for an implementation or diagnosis.
4. Review the proposed code and assumptions.
5. Run the result in the real environment.
6. Read the full error when something fails.
7. Identify the smallest proven root cause.
8. Correct only that cause.
9. Run targeted checks and production checks where appropriate.
10. Verify the real postcondition.
11. Record reusable lessons when the failure pattern is important.

## What I try to avoid

- treating the first generated answer as correct;
- hiding AI-generated errors;
- changing unrelated working code during a repair;
- calling a task complete from a partial test;
- weakening safety checks just to make an AI proposal pass;
- confusing provider failure with application architecture failure.

## Why this matters

AI makes it possible to move quickly across unfamiliar technologies, but speed is useful only when the result can be tested, explained and reproduced.

The project therefore combines AI-assisted implementation with Git history, targeted acceptance checks, integrity verification, rollback-oriented workflows and explicit diagnostics.
