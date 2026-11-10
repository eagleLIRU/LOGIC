# Mapping patterns

The Map step turns something into a simple chain. Pick the shape that fits. Then mark each link: Known, Probably, Guessing, Don't know, or Wrong.

The general chain:

**Goal → Inputs → Guesses → Rules → Actions → Results**

Or in a sentence: "Because A, we do B, which should make C, so D."

## Chains for common things

| Thing | Chain |
|---|---|
| Idea | Problem → guess → the fix we plan → what we hope happens |
| Software | What the person wants → what they do → what the app does → what they get |
| Business | Customer problem → product → what the customer does → value → money |
| Argument | Proof → thinking → conclusion |
| Decision | Goal → choices → what we judge by → what happens after |
| Request (Map 1) | Job → size → in scope / out of scope → WHO, WHAT, HOW the user gave → what is missing → next move |
| Plan or build | Goal → steps in order → a checkpoint after each big step → proof that it is done |

For anything else (a rule, a talk, a sum, a process), start with the general chain and bend it to fit. What matters is how the parts connect, not the names.

## People questions

These are real questions, not silly ones. They matter for the answer.

- Screen: Can the person understand this?
- Business: Will customers accept this?
- Safety: Could someone get hurt?
- People: How will this feel to the other person?

## Example: an argument

"All renters must have an account. John is a renter. So John must have an account."

- Proof: renters must have an account (Guessing until we check the rule). John is a renter (Don't know until we check).
- Thinking: the steps fit together.
- Answer: the steps are fine, but both starting facts are unchecked. So the answer is only as strong as those facts.

## Example: leave it alone

Plan: try an API call again a bit later if it fails.

- Chain: calls sometimes fail for a short time (Probably, from the error logs) → try again after a short wait → the call works the next time → fewer errors for people.
- Test: every link holds. Nothing fights. Doing nothing leaves the problem.
- Answer: "Your plan is fine. I checked the main parts. I see no reason to change it."

## Example: works, but causes a problem later

Plan: "Remove the help inbox because it costs money."

- Chain: help costs money → remove it → save money.
- Test: does that help the goal? If the goal is keeping happy customers, no.
- Answer: "This saves money now, but it causes a problem later. It only makes sense if keeping customers is not part of the goal. We have not checked that."

## Example: reading a request (Map 1)

Request: "Test the buttons and check that the parts talk to each other."

- Job: test.
- Size: Standard.
- In scope: the buttons, and the links between the parts. Out of scope: changing anything (not asked).
- WHO: not said. A careful tester fits. (Guessing)
- WHAT: find which buttons or links break.
- HOW: not said. Check by running it. (Guessing)
- Missing: which product, and where it runs. This changes the result, so ask.
- Next move: ask the one question, then study the product (Map 2).
