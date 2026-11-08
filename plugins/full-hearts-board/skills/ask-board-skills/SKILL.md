---
name: ask-board-skills
description: This skill should be used when a session mentions "board meeting", "the board", "board agenda", "board minutes", "board packet", "revive the board", "the board-meeting skills", "which board skill", or asks how the board skills fit together. It is a self-triggering index — read it to decide which sibling skill (setup-board, plan-board-year, prep-board-meeting, run-board-meeting, write-minutes, follow-up-board) fits the moment, even when the user never names one. Once the right skill is clear, invoke that one instead, since it carries the actual guidance.
---

# Board meetings: pick the right skill

A board meeting is a short chain of jobs. Each skill does one job and hands off to the next, so only the guidance that matters right now gets loaded.

## Why these skills exist

Small-nonprofit boards stop meeting when the meetings stop feeling useful: no clear agenda, the same items carried forward for months, and the operators doing the work anyway. These skills fix that by giving the board real decisions, one owner and one date per action, and a short meeting.

## Pick by moment

| The moment | Skill |
|---|---|
| First time, or the board's people or rules changed | `setup-board` |
| Planning the year's meetings, the January election, the 990 review | `plan-board-year` |
| A meeting is coming and an agenda and packet are needed | `prep-board-meeting` |
| It is meeting day and someone has to run it | `run-board-meeting` |
| The meeting just ended and minutes are needed | `write-minutes` |
| After minutes: actions, recap email, email approvals, overdue items | `follow-up-board` |

## Shared working folder

All board skills read and write one folder, `board/`, in the working directory (or the board's shared Drive folder when Drive is connected):

- `board/board-profile.md` — people, offices, rules, rhythm (from `setup-board`)
- `board/year-plan.md` — the year's meeting dates (from `plan-board-year`)
- `board/meetings/YYYY-MM-DD/` — `agenda.md`, `packet.md`, `minutes.md`, `actions.md`

If `board/board-profile.md` exists, never ask for anything it already holds. If it does not exist and the task needs it, run `setup-board` first.

## Rules every board skill follows

1. A meeting needs at least one decision. If there is nothing to decide, send an email update instead.
2. Every action has one owner and one due date.
3. Board papers and minutes are public by default unless the board votes to keep a part confidential, so never put donor or staff details in them.
4. Plain words. Short sentences. Exact dates.
5. Not legal advice. When a bylaw or law question is close, say so and suggest the person confirm with the corporation's lawyer or the state.
