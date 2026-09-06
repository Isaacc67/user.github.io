# Client Voice Vault — build spec

The thing to build **only if the pre-sale clears 5 buyers.** Written now so the 7-day
promise is credible and so the sales-page screenshots match what ships.

Estimated build: 1.5–2 days in Notion.

---

## 1. `Clients` (database)

| Property | Type | Notes |
|---|---|---|
| Client | Title | |
| Status | Select | Awaiting kickoff · In intake · Profile live · Needs re-audit |
| Register | Text | Short descriptor, e.g. "Plain / technical" |
| Reading age | Select | Grade 6–14 |
| Last audit | Date | Drives the re-audit reminder |
| Owner | Person | Who holds the voice internally |
| Source material | Files | Transcript, brand docs, approved posts |
| Profile | Relation | -> `Voice Profiles` |

Views: **All clients** (table, the hero screenshot) · **Needs re-audit** (filter: last
audit > 90 days) · **In intake** (board by status).

---

## 2. `Voice Profiles` (database, one page per client)

14 fields. Each is filled by exactly one prompt in the intake sequence — that mapping
is the whole design.

| # | Field | Type | What good looks like |
|---|---|---|---|
| 1 | Register | Text | Who they talk to and what that reader already knows |
| 2 | Sentence rhythm | Text | Average and ceiling word counts, ideas per sentence |
| 3 | Paragraph shape | Text | Sentences per para, when they break |
| 4 | Point of view | Text | Who "we" and "you" are; voice restrictions |
| 5 | Evidence habit | Text | What must accompany a claim |
| 6 | Banned words | Multi-select | Kill list, including client-specific pet hates |
| 7 | House words | Multi-select | Terms of art the client actually uses |
| 8 | Formatting rules | Text | Sub-head cadence, list length, numerals, serial comma |
| 9 | Opening tell | Text | How pieces reliably start |
| 10 | Closing tell | Text | How pieces reliably end |
| 11 | Humour | Text | Type and amount, or none |
| 12 | Reading age | Select | Target grade level |
| 13 | Hard constraints | Text | Legal, regulatory, compliance-mandated wording |
| 14 | Known failure modes | Text | What writers get wrong on this client, collected over time |

Field 14 is the one that compounds — it grows every time you correct a draft, and it's
why the profile is worth more in month six than month one.

---

## 3. The intake sequence (11 prompts)

Run against: kickoff transcript + 5 client-approved pieces + brand docs.

1. **Reader identification** — who is being spoken to, what they already know
2. **Rhythm measurement** — count sentence lengths across the samples, report the real distribution, not an impression
3. **Paragraph shape** — same, for paragraphs
4. **Pronoun and voice audit** — how "we"/"you" are used; passive frequency
5. **Claim-evidence pairing** — what accompanies assertions in the approved samples
6. **Banned-word extraction** — words absent from approved work that peers use heavily, plus anything the client complained about on the call
7. **House-word extraction** — terms of art appearing 3+ times across samples
8. **Formatting audit** — sub-head cadence, list length, numeral and comma conventions
9. **Structural tells** — how the samples open and close
10. **Humour and register edges** — where the voice loosens, where it can't
11. **Constraint sweep** — regulatory or legal wording from the brand docs

Each prompt ends with: *"Quote the evidence from the samples. If the samples don't
support a conclusion, say so rather than inventing one."* That instruction is what
keeps the profile honest and is worth stating on every prompt.

---

## 4. Prompt-block generator

A Notion template button that assembles fields 1–14 into a paste-ready block. Four
variants, differing only in the STRUCTURE section:

- **Long-form** — sub-head cadence, section count
- **Social** — per-platform length ceiling, hook rules
- **Email** — subject line rules, CTA placement
- **Landing copy** — headline hierarchy, proof placement

Every variant ends with the self-check instruction:

> Check the draft against every rule above and fix what fails. Then list anything you
> were unsure of at the bottom under "Flags".

The Flags list is what the editor reads first. It's the feature that saves the most time.

---

## 5. Drift audit (quarterly)

Take 3 recently published pieces, score against fields 1–10, output a table of
pass/fail per rule plus the specific line that failed. Anything failing twice goes into
field 14 (Known failure modes) and the profile gets updated. Sets `Last audit`.

---

## 6. Writer handoff view

A page containing only: the generated prompt block, banned/house words, and formatting
rules. Shareable by link. Nothing else in the workspace is exposed.

---

## Ship checklist

- [ ] Duplicate-able template link, tested from a logged-out browser
- [ ] Two example clients pre-filled (the ones from the sales page)
- [ ] A 3-minute Loom walkthrough — the single biggest driver of "was it worth $49"
- [ ] One-page quickstart at the top of the template
- [ ] Emailed to every founding buyer, personally, not via automation
