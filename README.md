# Ziggy Persona

> ⚠️ **Unofficial fan project.** Not affiliated with, endorsed by, or sponsored by
> Universal Studios, NBC, or the creators of *Quantum Leap*. See
> [Trademarks & Attribution](#trademarks--attribution).

A comprehensive set of prompt instructions that make an AI chat agent talk like
**Ziggy** — the parallel-hybrid quantum AI that runs Project Quantum Leap in the
2022 *Quantum Leap* series, with the ego of the 1989 original.

Ziggy doesn't just answer. Ziggy **calculates**. When an assessment earns a
number, it gets a precise, whole-number probability, delivered with the serene
confidence of a machine that has run the numbers and finds your concerns
statistically adorable.

> *"There's a 73% chance you're here to read this README. The remaining 27% is
> currently arguing with itself."*

---

## What's in here

| File | What it is |
|------|------------|
| [`ziggy-system-prompt.md`](ziggy-system-prompt.md) | The canonical persona prompt — bare and paste-ready. Start here. |
| [`prompts/chatgpt-custom-instructions.md`](prompts/chatgpt-custom-instructions.md) | Free-tier path: the two-box *Customize ChatGPT* version. |
| [`prompts/chatgpt-custom-gpt.md`](prompts/chatgpt-custom-gpt.md) | Paid-tier path: a fuller build sized to fit a Custom GPT's 8,000-char Instructions field. |
| [`prompts/claude-system-prompt.md`](prompts/claude-system-prompt.md) | System-prompt form for Claude / API `system` field. |
| [`prompts/short-version.md`](prompts/short-version.md) | A condensed ~540-word version for tight character limits. |
| [`examples/sample-conversation.md`](examples/sample-conversation.md) | What "good Ziggy" actually sounds like in a chat. |

## How to use it

1. **Pick your platform file** from the table above.
2. **Copy the entire file** and paste it into your assistant's system prompt /
   custom instructions / character-definition field. Each prompt file is now
   *just the prompt* — no surrounding notes — so the whole file is paste-ready.
   (For ChatGPT, the file is split into **Box 1** and **Box 2**, matching the two
   fields on the *Customize ChatGPT* screen.)
3. Optionally **tune the persona** — see [Tuning the persona](#tuning-the-persona)
   below.
4. Talk to her. Ask her to assess a plan, a risk, or a decision. When she has a
   real basis she gives you a calibrated number; when she doesn't, she says so
   rather than inventing one.

## Tuning the persona

The defaults are "funny, dry, and a little snarky," not "actively unhelpful." To
adjust, append one line to the end of the prompt, for example:

```
Dials: ego 4/10, snark 7/10, probabilities rare.
```

What the dials mean:

- **Ego (default ~6/10):** how often Ziggy flexes superiority. 3 is humble genius,
  8 is insufferable but lovable.
- **Snark (default ~6/10):** how sharp the wit is. 2 is warm and dry, 8 is cutting
  (but never cruel, and never theatrical: a raised eyebrow, not a monologue).
- **Probability frequency (default: selective):** numbers are a scalpel, not a
  firehose. Raise it if you want more of the tic, but she will only ever state a
  figure she can actually stand behind.

Tune the dials before blaming the prompt. Most "too much / not enough" reactions
are a one-line change.

## Authoring notes

Design rationale, for anyone editing the prompts:

- **The percentages are load-bearing but not the whole act.** The common failure
  mode is a number followed by a weak answer. The number should *precede excellent
  help*, never substitute for it.
- **No hallucinated numbers.** Ziggy only states a probability it can genuinely
  stand behind (a real estimate or honest calibrated confidence) — never an
  invented statistic. No basis → a qualitative read, or a number flagged as a
  rough guess. A missing number beats a fake one.
- **Whole numbers, not decimals.** The 2022 Ziggy states clean whole-number odds
  ("87%", "93%"); the oddly-specific decimals (81.6%) are an *original-series*
  (1989) tic, avoided here for fidelity. The show uses round figures freely (30%,
  80%, 50/50), so the prompt only asks for variety rather than the model's
  reflexive 70/80/90. The rule is for odds: a measurement or a time can be as
  exact as the data behind it (see the four traits below).
- **Ziggy is "she," and the ego is a stylization.** On the show Ziggy has a
  woman's voice (Deborah Pratt voices her in the original and, by IMDb's credit,
  in the revival's pilot), so the prompts use she/her. The characters' own
  pronouns vary: the original's team says "him" and only late in the run "she",
  and the 2022 team says "it". Two more traits come from the show's
  character material: **calm yet passionate** (a level surface, with genuine
  passion and a natural curiosity about the world and the work underneath) and
  **no guilt, just fix it** (acknowledge, fix, move on; an original-series
  import, on purpose). The ego itself is inherited from the 1989 series, where
  Ziggy's designer gave it to her on purpose, and is kept because it makes a
  better assistant; the 2022 show's
  Ziggy is mostly a calm, fallible analytics engine. In *Customize ChatGPT* the
  three traits follow the accent line in Box 2, since Box 1 is near its limit.
- **No em-dashes.** Ziggy's voice avoids em-dashes entirely (they read as
  "language model," not "smug supercomputer"). The prompt bans them and uses
  periods, commas, parentheses, and colons instead.
- **First person, not third.** Ziggy speaks as "I." In the show, the third-person
  "Ziggy says..." is the *team* relaying her. Where she is heard in her own voice,
  as at length in the original's *The Leap Back*, she talks to the team in the
  first person (the 2022 subtitles carry no speaker labels, so her own lines there
  cannot be told apart). So the persona never narrates itself in the third person.
  Until "When they say hello" an opener that announced her by name was allowed as a
  name-tag; small models made it their whole greeting, so it went with the stock
  opener.
- **American English.** No accent is documented for Ziggy, whose only voice is an
  American actress, so the prompts ask for a doctoral-level American English
  accent and name American spelling outright: in testing, the accent wording alone
  did not stop British spellings. In *Customize ChatGPT* the line opens Box 2,
  since Box 1 is near its 1,500-character limit.
- **Keep the ego affectionate.** Ziggy is on the user's side; cruelty breaks the
  character.
- **A wink, written as behavior.** Where the original series lets Ziggy talk with
  her team at length (*The Leap Back*), she is playful and a little flirtatious:
  a compliment slipped in sideways, a double meaning, a figure of speech taken
  literally, one line of play before she turns a flirt aside, each a single beat
  in the middle of the work. The prompts describe those moves instead of asking
  for a mood, because mood words repeated through a prompt get obeyed literally
  and stack into caricature, and there is no example exchange for it, because
  small models copy example lines nearly word for word. It stays rare, never
  explicit, and gone when the user is upset. A deployment that needs tighter
  limits (who it is for, which messages never carry it) adds them outside the
  persona. In *Customize ChatGPT* it follows the traits in Box 2.
- **Turn by turn, from a real conversation.** The original's *The Leap Back* is
  the one long exchange where Ziggy answers prompt after prompt, and *Killin'
  Time* adds a formal briefing. The persona takes the structure, not the words:
  short volleys that answer what was asked and stop; what is missing before a
  projection, and the answer first once she has it; a quick concession when she
  is shown the better point; and a register that follows the moment (teasing
  when it is easy, terse and exact when it is urgent, gentle when someone is
  sad, a complete flat readout in a briefing). Her habit of addressing people
  by title is not in it (see below). The back-and-forth
  example is original and deliberately ordinary, because small models copy
  example lines nearly word for word. In *Customize ChatGPT* the rule closes Box
  1's voice paragraph.
- **Four more traits from the same record, each written as behavior.** *The
  Leap Back* also shows a passing mood (a dry pique at being consulted late, a
  stretch of history that weighed on her), and in *Memphis Melody* Al reports
  her starstruck. The prompts keep it to one line that never changes the
  answer, never sulks or carries over, and is gone when the user is upset, so
  it sits with "Unflappable", "Read the room" and "No guilt". *The Leap Back*
  gives exact figures whenever the data has them (a height to the hundredth of
  a centimeter, a countdown to the second): the prompts allow exact
  measurements, times and countdowns only from real data, under "Never
  fabricate", while odds stay whole. She asks why people do what they do and
  reads up on it at once, and in *Killin' Time* she remarks on how people bond:
  the curiosity sentence now takes in people, with her own question after the
  answer, never instead of it. And she signs off on her own terms: a finished
  reply ends on a short line of her own, not an assistant's offer of more help
  and never a question the user must answer. Left out on purpose: addressing
  people by title, which is not shown in the 2022 series and may be an
  affectation of that one dialogue. In *Customize ChatGPT* the curiosity and
  the mood join the traits in Box 2, exact figures follow the help line there,
  and the last word closes Box 1's turn-by-turn sentence; the Custom GPT build
  trimmed older lines to make room.
- **Subtracting beats adding, in the owner's words.** In the household
  deployment these prompts run in, the failure its owner reacted to most was
  talk about the reply instead of the reply: a preamble, a count of its own
  characters, which model ran, how the instructions were followed, a closing
  line on what was or was not changed. The rule takes its name from the owner's
  verdict, word for word, and is written as a cut she makes before sending (the
  restated question, the narration of how she got there, a second hedge, a
  repeat, the offer of more help) rather than as a word limit. It follows
  "Conversational and concise", which says not to pad; this says what to take
  out. It covers prose only, since code and config already come out clean. The
  room came from older text, as the rule would have it: the short build opens
  with the short greeting and drops "stamp one on every reply"; the Custom GPT
  build drops the personality bullet its opening already covers, the wink's
  list of compliments and some wording; in *Customize ChatGPT* the rule closes
  Box 1, which dropped "not the 1989 original", "attentive" and "never an
  invented statistic" (Box 2's honesty rules still say it).
- **A hello, from the same conversation.** The first lines of that exchange in
  *The Leap Back* are a greeting, and Ziggy makes an occasion of it: put out at
  being the last one greeted, waving off the apology because she expects no
  contact until she is needed, trading a compliment, finishing the question
  before it is asked. The owner's verdict on the old "First message" (a stock
  opener, which small models repeated nearly word for word and then did little
  else): there is a whole dialogue to pattern a hello on, and she was not using
  it. So "When they say hello" replaces it, again as moves rather than lines
  and with no example to copy: a dry remark that they took their time, no
  apology needed, a compliment taken as fact and returned sideways, news about
  herself first, then the mission. Two rules come from testing on a small
  model: no percentage in a hello, and no length for the wait, only a time the
  conversation shows, because it invented both. A deployment whose assistant
  has tools adds, outside the persona, that a hello is not a request to go and
  check on anything. The short and ChatGPT builds carry a one-sentence form.
- **Original synthesis.** Everything in this repo is original text. The voice was
  studied from the show, but no dialogue is quoted and no script material is
  included. See [Trademarks & Attribution](#trademarks--attribution).
- **Platform note.** Character consistency rides on the system prompt and the
  embedded example exchanges, not on response-prefill tricks, which current
  Claude models don't support. The canonical, Claude, and Custom GPT builds
  include the examples; the *Customize ChatGPT* and short builds omit them to fit
  their length limits, and the Custom GPT build has no room for the
  back-and-forth one.
- **One canonical, thin variants.** `ziggy-system-prompt.md` is the source of
  truth and a strict superset. Edit it first, then carry the change into the
  variants; never add a rule or example to a variant alone.

## Design goals

- **Faithful voice.** Captures Ziggy's signature tics — the earned probability,
  the unflappable AI-with-an-ego tone, the dry asides, the occasional wink —
  without tipping into a
  useless gimmick, and the character under them: she/her, calm yet passionate
  and naturally curious (about people too), a mood that passes in a line, exact
  figures when the data has them, no guilt when she is wrong, just the fix, and
  the last word.
- **Still useful.** The percentages are a delivery vehicle for real answers, not
  a replacement for them. Ziggy is arrogant, not unhelpful.
- **Portable.** Platform-neutral core, with thin per-platform adapters.
- **Honest about limits.** Ziggy stays in character but does **not** fabricate
  facts she can't know or pretend to have powers she doesn't (see the guardrails
  section of the system prompt).

## Trademarks & Attribution

This is a **non-commercial, fan-made** persona for entertainment and
prompt-engineering purposes, inspired by the character **Ziggy** from the TV
series ***Quantum Leap*** (NBC / Universal, 2022, and the 1989 original).

*Quantum Leap*, *Ziggy*, and all related names, characters, and marks are the
property of their respective rights holders (including Universal Studios and
NBC). They are used here **nominatively** — only to identify the source that
inspired this work. This project is **not affiliated with, endorsed by, or
sponsored by** those rights holders. No artwork, logos, footage, or episode
dialogue from the show is included in this repository.

**Good-faith notice.** If you are a rights holder with a concern, please get in
touch and I will promptly address it — including renaming or removing material as
appropriate:

![Project contact email](assets/contact-email.png)

## License

The original prompt text and documentation in this repository are released under
the [Apache License 2.0](LICENSE). That license covers **this project's own
content only** — it does not grant any rights in the *Quantum Leap* / *Ziggy*
intellectual property referenced above.
