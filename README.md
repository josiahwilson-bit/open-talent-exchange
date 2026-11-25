<p align="center"><em>· EST. MMXXVI · SAN DIEGO ·</em></p>

<h1 align="center">O P E N&nbsp;&nbsp;T A L E N T&nbsp;&nbsp;E X C H A N G E</h1>

<p align="center"><em>Offers and needs, matched one approval at a time.</em></p>

<p align="center">— ◆ —</p>

A talent exchange is a board, not a marketplace. On one side, people offer a skill. On the other, projects name a gap. A coordinator pairs one offer with one need, the owner approves the named match, and the match counts only when both sides confirm. What comes back is feedback and credit — never points, never pay.

## The board

| 01 · OFFER | 02 · NEED | 03 · PROPOSE | 04 · APPROVE | 05 · CONFIRM | 06 · SESSION | 07 · FEEDBACK |
| --- | --- | --- | --- | --- | --- | --- |
| A person offers a skill | A project names a gap | The coordinator pairs one offer with one need | The owner approves the named match | Both sides confirm | The work sample or session happens | One thing that worked · one blocker · one question · credit |

## The rules

1. **Cards, not currency.** No points, no pay, no subscription. Feedback and optional credit only.
2. **Three fields stay separate.** Interest, permission to follow up, and offered work are recorded as three separate fields, never merged into one commitment.
3. **One match at a time.** The coordinator proposes; the owner approves each named match. No score assigns anyone by itself.
4. **Both sides confirm.** A match counts only when the person offering and the person who needs them both confirm.
5. **Empty seats stay visible.** An unfilled role is shown as a named gap, never filled in with a guess.
6. **Paid work lives elsewhere.** A named buyer with a real decision goes through the commercial pipeline, not this board.
7. **Private stays private.** This repository holds rules and routing only. People's cards live in the owner's private board.

## On the board now

- **Open need:** one independent QA reviewer for the FETCH Quest 2 pinned replay — opt in on [FETCH issue #3](https://github.com/josiahwilson-bit/fetch-open/issues/3).
- **Offers on record:** none yet.
- **Matches:** none yet.

## Routing channels (design)

- **CLI** — scans the sources and proposes the match and the slot.
- **Google Apps Script** — runs the scheduled check; a time-driven trigger can drift within its hour, so there is exactly one scheduled runner.
- **Google Calendar** — read for availability when a slot is proposed; a hold is created only after the owner approves the exact time and audience.

Deviation is the gap between the proposed slot and what actually gets booked. Relationship scaling is read from how long each person waits between steps. Both are measured, never assumed. See [ARCHITECTURE.md](ARCHITECTURE.md).

<p align="center"><sub>OPEN TALENT EXCHANGE · A FETCH FACTORY BOARD · RULES AND ROUTING ONLY</sub></p>
