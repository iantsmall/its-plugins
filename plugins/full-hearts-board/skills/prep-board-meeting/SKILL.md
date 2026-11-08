---
name: prep-board-meeting
description: This skill should be used when a board meeting is coming up and the agenda, packet, or notice email needs to be made — "prep the board meeting", "make the agenda", "board packet", "what should the board decide". It builds a decisions-first agenda and a one-page packet from the master task tracker and the last meeting's actions, then drafts the notice email.
---

# Prep a board meeting

Read `board/board-profile.md` and `board/year-plan.md`. If the profile is missing, run `setup-board` first. Ask the person for the meeting date if it is not in the year plan.

## Step 1: Gather

- **Last meeting:** read `board/meetings/<last date>/actions.md` and minutes. List each action as done, open, or overdue.
- **Master task tracker:** if a Master Plan sheet is linked in the profile and Google Sheets is connected, read the Overview and Tasks tabs. Pull what is overdue, blocked, or due before the next meeting, and every row marked "Needs check" in the conflict column.
- **Money:** ask the Treasurer for the current balances and anything over the spending line. Never fill in numbers from old minutes. If the Treasurer has not sent figures, mark the line "Treasurer to supply".
- **Items the board must see:** anything the year plan says belongs at this meeting.

## Step 2: Find the decisions

A decision is a question the board can answer with a vote, such as "approve the 2027 budget" or "choose GetBuddy or self-hosted". Test each candidate:

1. Does it need a board vote under the delegation line in the profile? If not, it is a report, not a decision.
2. Is there a clear question and a recommended answer?
3. Can the board vote on it today with what is in the packet?

Keep no more than three decisions. If there are none, tell the person and suggest an email update instead of a meeting.

**Carry-over rule:** an item that has already been on two agendas in a row must be decided, dropped, or split into smaller items with owners and dates this time. Mark it "carried over twice" on the agenda.

## Step 3: Build the agenda (45 minutes unless the profile says otherwise)

| Minutes | Item |
|---|---|
| 0–3 | Call to order, quorum check, conflicts declared |
| 3–8 | Consent items: approve last minutes, accept routine reports (one vote for all) |
| 8–35 | Decisions (up to three), each with a time limit |
| 35–42 | Read back actions: owner and date for each |
| 42–45 | Next meeting date, adjourn |

Money and project status are read in the packet before the meeting, not read aloud. Meeting time is for questions and votes.

Write each decision as a block:

- **Question:**
- **Why now:**
- **Options:** (two or three)
- **Recommended answer and who recommends it:**
- **Proposed motion:** "I move that Full Hearts [do X] by [date], with [name] responsible."
- **What happens after:** the task, owner and date.

## Step 4: Build the one-page packet

One page, plain words:

1. Where things stand, by area (from the tracker: not started, in progress, blocked, done)
2. Overdue and blocked, with the reason and what would unblock each
3. Money snapshot, from the Treasurer
4. Decisions needed, each with its recommended motion
5. Conflicts to declare or recuse on

**Public by default:** board papers are open to the public after the meeting unless the board votes to keep a part confidential, per the bylaws in the profile. Keep donor details, staff records and private personal information out of the packet. If a topic needs privacy, put it in a separate item marked "confidential, motion needed" and say why.

## Step 5: Notice email

Draft, never send, an email to the directors. Use Gmail drafts if connected. Include the date, time, video link, the agenda, the packet, and the line "Please reply with your questions by [date] so we can use meeting time for decisions." Send it at least 7 days ahead; the bylaw minimum is in the profile.

## Output

Save `board/meetings/YYYY-MM-DD/agenda.md` and `packet.md`. If Drive is connected and the person wants it, also create a document in the board folder. Offer `run-board-meeting`.
