# The A / R / T shape (who, what, how)

ART has three parts:

- **A (Act as) = WHO.** The role and know-how the work needs.
- **R (Request) = WHAT.** The result that must come out, and how anyone can tell it is done.
- **T (Terms) = HOW.** The context, rules, limits, quality bar, format, and checks.

LOGIC uses this shape in three places. This file holds a small built-in version, so LOGIC works even when no ART skill is loaded.

Keep it short. Give the reader only what helps it make the right choices. A short, clear brief is better than a long one.

## Place 1: Reading the request (step 0)

Look at what the user gave you:

| Part | Question | If it is missing |
|---|---|---|
| **A (WHO)** | What role or know-how does this work need? | Choose a fitting role and mark it **Guessing**. |
| **R (WHAT)** | What result is wanted? Could someone tell when it is done? | Ask. An unclear result changes everything. |
| **T (HOW)** | What context, rules, limits, quality bar, format, and checks? | Ask only if it would change the result. If not, take the narrowest reading, label it **Guessing**, and ask the user to confirm it. |

Rules:
- Ask only when the missing part would change the result.
- Ask the smallest set of questions: one to three, easy to answer.
- Do not invent facts.

## Place 2: The brief for the builder (step 8)

Use this when LOGIC hands work to a builder (another AI coder or skill).

**A (Who).** Act as a [specific job] who [what they are good at that matters here].

**R (What).** [Verb] [thing] so that [result]. Done means: [how anyone can tell].

**T (How).**
- **Context:** what exists now, in a few lines.
- **Order:** the steps, in order, with a checkpoint after each big step.
- **Do not touch:** what must stay the same.
- **Rules and limits:** what the builder must and must not do.
- **Quality bar:** what good looks like.
- **Never invent:** facts, features, files, or keys. If something is not known, say so or ask.
- **Before saying done:** the checks to run, and show the proof.
- **Report back:** what to send back, short.

Guidelines:
- A good brief can be five to ten lines. Cut any line that does not help the builder decide something.
- Pick one specific role. Do not stack grand titles.
- Do not repeat. Do not contradict.
- Names, files, and numbers stay exact.
- Do not assume which AI will read it. If the user names the target, fit the brief to it.
- Quality check before sending:
  - Is A specific?
  - Is R clear, with a way to tell it is done?
  - Does T give enough to decide without guessing?
  - Is anything contradictory, invented, or repeated?

Small example:

> **A.** Act as a front-end engineer who builds simple, fast forms.
> **R.** Build a contact form that saves each message and shows a clear "sent" note. Done means: a test message shows up in the saved list, and the person sees the note.
> **T.** Context: the page exists, the form does not. Order: 1) the fields, 2) saving, 3) the note, 4) the error messages. Check after step 2 that a message saves. Do not touch: the page header and styles. Never invent: a service or key we do not have; ask instead. Before saying done: send a test message, show what was saved, and try an empty form. Report back: what changed, and the proof.

## Place 3: The final gate (step 9)

Before LOGIC says "done", check the brief against the work:

- **R:** Is every numbered requirement from step 0 proven, one by one? Is every part of "Done means" proven? Could another person tell the job is complete?
- **T:** Were the rules and limits kept? Is the "Do not touch" list unchanged? Did the checks in the brief pass, with proof?
- **Nothing extra:** Did the build add things nobody asked for? Is anything invented?

If any answer is no, LOGIC says "Not done yet" and says what is missing.

## Using a full ART skill

If an ART skill is already loaded and the handoff is big or important, LOGIC may hand the brief to it. LOGIC never installs one. If the user only asks for a better prompt, that is the ART skill's job, not LOGIC's.
