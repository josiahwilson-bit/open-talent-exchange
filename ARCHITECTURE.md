# Architecture — Open Talent Exchange

*Design v0.1 · 2026-11-25*

## Card model

**Offer card** — who is offering, the skill, what exactly is offered, any conditions, a source link, and the time it was captured.

**Need card** — the role, the task, the acceptance checks, the expected duration, and a source link.

Capture keeps three fields separate on every card: **interest**, **permission to follow up**, and **offered work**. A conditional offer ("I can review if it runs on my laptop") is recorded as a conditional offer with the condition attached — never promoted into a commitment.

## Match lifecycle

PROPOSED → OWNER_APPROVED → CONFIRMED_BOTH_SIDES → SUBMITTED → VERIFIED → ACCEPTED

Side exits: DECLINED (either the owner or a side declines) and EXPIRED (the evidence or the window went stale before confirmation).

- A proposal approves nothing by itself; it orders the owner's review queue.
- Owner approval binds to the exact named pairing — one offer card, one need card.
- A match counts only when both sides confirm.
- The volunteer submits the finished work for review; for the current need, the written report.
- The submission is checked against its sources and the task's stated checks.
- The owner accepts the verified work, which completes the exchange.
- Accepted matches collect feedback as one thing that worked, one blocker, one question, plus an optional credit line.

## Routing

| Signal | Routes to | Action |
| --- | --- | --- |
| Direct opt-in on a need | Volunteer Coordinator | Propose the match to the owner |
| Written result submitted | Independent QA → Editor | Check against the acceptance criteria |
| Qualified buyer with a real decision | Commercial Scope Coordinator | Leaves this board — commercial pipeline rules apply |

## Channels

- **CLI** — the local rehearsal lane: scan, route, propose. Runs against one need before any cloud trigger exists.
- **Google Apps Script** — the scheduled scan, deployed from this repo's source. One scheduled runner only, to avoid duplicate callouts.
- **Google Calendar** — free/busy is read when a slot is proposed. After the owner approves the exact time and audience, availability is rechecked and the event is created. An owner-only hold and a participant invitation are distinct actions.

## Measures

- Signal → proposal time, and proposal → decision time.
- Wait per person per step (relationship scaling).
- Deviation: proposed slot vs. booked slot.
- Counts are always shown alongside rates. An unchecked value is UNKNOWN, never zero-filled.

## Privacy

No personal cards, contact details, or consent records live in this repository. Those stay in the owner's private board and are linked by reference only.
