# VinceCam

Project workspace for VinceCam. This file is the entry point for anyone (human or
Claude) picking the project up cold.

## What this is

_(One paragraph: what VinceCam is and who it's for. Fill in.)_

## Layout

| Path | Holds |
| --- | --- |
| `overall/` | The base idea (`BASE_IDEA.md`) — source of truth every module should match |
| `src/` | Application code |
| `src/resume-extract/` | Parse/extract structured data from a resume |
| `src/preferences/` | Capture and store stated user preferences |
| `src/enjoyment/` | Model what the user actually enjoys doing |
| `src/trajectory/` | Model career trajectory / progression |
| `src/scoring-engine/` | Combine the above into a job-fit score |
| `src/job-logic/` | Job-side business logic (listings, matching rules, etc.) |
| `UNDERSTANDING.md` | The living model of how the system works — read this first |
| `DECISIONS.md` | Why things are the way they are, dated |
| `LOG.md` | Running work journal, newest entry at the top |

## Working agreements

- **Read `UNDERSTANDING.md` before making changes**, and update it when a change
  invalidates something written there. A stale understanding doc is worse than none.
- Record non-obvious choices in `DECISIONS.md` at the time you make them, with the date
  and the alternative you rejected.
- Stack, build, and run commands are recorded in `UNDERSTANDING.md` under "How to run it"
  as soon as they exist.
