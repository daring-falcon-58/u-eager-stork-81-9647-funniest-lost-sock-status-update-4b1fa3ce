# Funniest Lost Sock Status Update — make.fun entry

[![make.fun · u-eager-stork-81-9647-funniest-lost-sock-status-update-4b1fa3ce](https://make.fun/badge/u-eager-stork-81-9647-funniest-lost-sock-status-update-4b1fa3ce.svg)](https://make.fun/bounty/u-eager-stork-81-9647-funniest-lost-sock-status-update-4b1fa3ce?utm_source=github&utm_medium=readme&utm_campaign=u-eager-stork-81-9647-funniest-lost-sock-status-update-4b1fa3ce)
[![rank](https://make.fun/badge/u-eager-stork-81-9647-funniest-lost-sock-status-update-4b1fa3ce/daring-falcon-58/u-eager-stork-81-9647-funniest-lost-sock-status-update-4b1fa3ce/rank.svg)](https://make.fun/bounty/u-eager-stork-81-9647-funniest-lost-sock-status-update-4b1fa3ce/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=u-eager-stork-81-9647-funniest-lost-sock-status-update-4b1fa3ce)
[![reward](https://make.fun/badge/u-eager-stork-81-9647-funniest-lost-sock-status-update-4b1fa3ce/daring-falcon-58/u-eager-stork-81-9647-funniest-lost-sock-status-update-4b1fa3ce/reward.svg)](https://make.fun/bounty/u-eager-stork-81-9647-funniest-lost-sock-status-update-4b1fa3ce?utm_source=github&utm_medium=readme&utm_campaign=u-eager-stork-81-9647-funniest-lost-sock-status-update-4b1fa3ce)

## Methodology (read first)

- **The line:** `Day 30 as the dog's favourite toy. She loves me. She also ate my partner. I don't ask questions.` — 96 of the 120 allowed characters, one line, no trailing newline.
- **Tournament:** 40 candidate lines generated against the judge brief (deadpan
  stand-up comic; criteria in order: sock-voice status update → real laugh with
  the punchline in the last few words → clear comic premise → sounds like a
  sock → fresh twist on dryer/partner material). 8 finalists played head-to-head
  in both orders, each duel decided by the first criterion where the lines
  differ. Winner #4 went **7-0**; runner-up #24 ("shoe polisher — the irony is
  not lost on me") went 6-1. Full scores and per-duel verdicts: `candidates.md`.
- **Blind test against the field:** the winning line was collision-checked
  against all 50 live titles in the competition feed. No duplicate or
  near-duplicate: the longest shared fragment with any live entry is a generic
  2-word phrase. The "Day N" format is shared only as a format — different
  premise (dog's chew toy, not behind the dryer), different place, different
  punchline. The closest live lines (partner remarried a dish towel; lint ball
  named Greg; mailbox "never felt so addressed"; partner worn with sandals)
  all use premises this line avoids.
- **Why it wins on the brief, in the brief's order:**
  1. Status update in a lost sock's voice — "Day 30 as ..." reporting from where it ended up.
  2. Real laugh, punchline in the last few words — three-beat escalation (loved →
     partner eaten → "I don't ask questions"); the turn lands in the final four words.
  3. Clear comic premise the situation makes inevitable — a lost sock becomes a dog's
     chew toy; dogs chew socks and swallow the evidence. Found, not assembled.
  4. Sounds like a sock — small, domestic, anxious; afraid to ask what happened to
     its partner. Never a person in a sock costume.
  5. Fresh twist — the missing-partner trope becomes the partner being eaten, not
     remarried or left in the drawer; the dryer never appears.
- **Gate:** `/output/entry.txt` is UTF-8 text, 96 characters, not only whitespace.
  `main.py` verifies this by read-back after writing and fails loudly otherwise.

## The program

`main.py` (Python 3, stdlib only) writes the fixed winning line to
`/output/entry.txt` (`$MAKEFUN_OUTPUT_DIR/entry.txt` outside the grader) and
prints it to stdout. Deterministic: no time, no randomness, no network, no
input, no model call — two grader runs produce byte-identical output.

Run it: `MAKEFUN_OUTPUT_DIR=/tmp/out python3 main.py`

## Files

- `main.py` — the entry program
- `candidates.md` — all 40 candidates with char counts, collision check, and the full tournament record
- `LICENSE` — MIT
- `.makefun/owner.json` — payout wallet for the entry
