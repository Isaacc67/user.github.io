# Scope Creep Auditor — setup, kill test, and launch

Concept 2 of the strategy brief. Hours 0-48 of its validation plan.

Its job is **not** to make money. It is to be useful enough to get shared, so it builds
the audience you sell the Voice Vault into. Judge it on distribution, not revenue.

---

## 1. Build it (hours 0-4)

In ChatGPT → **Explore GPTs → Create**.

| Field | Value |
|---|---|
| Name | Scope Creep Auditor |
| Description | Paste a client brief. Get the risk score, the undefined deliverables, the clauses to add, and a reply you can send today. |
| Instructions | Everything in the fenced block in `system-prompt.md` |
| Knowledge | `knowledge/scope-creep-taxonomy.md` and `knowledge/sow-clause-library.md` |

**Conversation starters:**
- Audit this client brief for scope creep
- What's missing from this RFP?
- Draft my reply asking for the missing details
- Rewrite this scope so it can actually be priced

**Capabilities — turn all three OFF.** Web browsing, DALL·E, and Code Interpreter add
latency and give the model room to wander. Everything it needs is in the knowledge files.

Set it to **Anyone with the link**.

---

## 2. The kill test (hours 4-6)

**Do not skip this, and be genuinely willing to fail it.** This is the thin-wrapper test
from the strategy brief. If your GPT is not clearly better than a one-line prompt, you
have built nothing, and the cheapest moment to discover that is now.

### Get five real briefs
Not invented ones — invented briefs flatter the tool because you write them containing
the problems you designed for.

- Public sector RFP portals (marketing and communications categories)
- `r/freelance` and `r/agency`, where people post briefs asking "is this a red flag?"
- Upwork and Contra project postings — free to read, often gloriously vague
- Agency case studies that reproduce the original brief
- Your own past briefs, if you have any

Aim for a spread: two vague, two detailed, one genuinely well-written.

### Run the A/B
For each brief, in two separate windows:

- **Control** — plain ChatGPT, no custom instructions: *"Review this client brief for scope creep risks."*
- **Test** — your GPT.

Score each output 1-5 on:

| Criterion | What a 5 looks like |
|---|---|
| **Specificity** | Quotes the brief's own words rather than describing categories of risk |
| **Absences** | Names what is missing, not just what is badly worded |
| **Actionability** | Clauses and a reply you could send without rewriting |
| **Restraint** | Scores the well-written brief low instead of manufacturing five red flags |

### The verdict
- **Test beats control by 1.5+ points on average → ship it.**
- **Test beats control by under 1 point → you have a thin wrapper.** Do not launch it.
  Either deepen it (the absence pass and the clause library are where the value is) or
  drop Concept 2 entirely and put the weekend into the Voice Vault instead.

Restraint is the criterion most likely to fail. If your GPT finds serious risk in the
well-written brief, it is performing vigilance rather than doing analysis — and one
experienced freelancer will spot that in ten seconds and say so publicly.

---

## 3. Launch (hours 6-30)

**Read each community's self-promotion rules first and follow them.** Several of these
ban links outright, and a ban costs you the channel permanently. Where promotion is not
allowed, post the insight without the link and let people ask.

Lead with the finding, never the tool. The post that works is a genuinely useful
observation that happens to have been produced by something you built.

**Where:** r/freelance · r/agency · r/marketing · r/smallbusiness · agency Slack and
Discord communities · LinkedIn (your best channel — the buyers are there under their real
names)

**The post that works:**

> I went through 40 client briefs looking for what actually causes unpaid overtime. It
> isn't the vague wording everyone warns about — it's what the brief never mentions.
>
> Nine things. Almost no brief defines more than four of them:
> [the nine from the absence pass]
>
> The expensive one is "definition of done". Without it there's no completion, and
> without completion there's no final invoice.
>
> I built a free GPT that runs this check — link in comments if useful.

Only claim the 40 briefs if you have actually read 40 briefs. Say five if it was five;
the observation carries itself either way and a fabricated number is the one thing that
can't be walked back.

**Answer every comment.** The replies are the point — each one is a person with the exact
problem the Voice Vault also solves.

---

## 4. Measure (hours 30-48)

- **PASS** — 100+ conversations and a real comment thread. You have a channel.
- **FAIL** — under 20 across every channel. You have no distribution, which is a bigger
  and more urgent problem than which product you build. Fix that before building anything
  else.

Track alongside the raw count:
- comments volunteering their own scope-creep stories → these people are your buyer list
- shares into private Slack groups → the strongest signal available
- anyone asking "do you do this for [other problem]" → free product research

---

## 5. The connection to Concept 3

The GPT ends with an offer, not a full stop. Add to the end of the output format once
launched:

> Want the same treatment for client voice? I'm building a Notion system that turns a
> kickoff call into a brief your freelancers can actually follow. [link]

That single line is why Concept 2 exists. Everything else is the price of earning it.
