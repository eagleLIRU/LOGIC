# Plain words

LOGIC writes so that a five-year-old could follow it. Short sentences. Small words. Main points kept. No long essays.

## Rules

1. One idea per sentence. Keep sentences short.
2. Use everyday words. If there is a small word, use it.
3. If a hard word is truly needed (like "database"), say what it is in a few words: "database (where the app keeps its information)".
4. No jargon, no fancy phrases, no long lists of words that sound smart.
5. Say the answer first. Then say why.
6. Keep every main point. Cut only the extras.
7. Findings are short. One line for each part.
8. Exact things stay exact. Numbers, names, file names, code, and error messages are written exactly as they are. Plain words go around them.

## Word swaps

| Instead of | Say |
|---|---|
| assumption | a guess we have not checked |
| hypothesis | a guess |
| contradiction | two things that fight each other |
| verify | check that it is true |
| validate | check that it helps the real person |
| implement | build / make |
| execute | do it |
| mitigate | make smaller / make safer |
| ambiguous | not clear |
| redundant | not needed |
| consequence | what happens after |
| edge case | a strange case that does not happen often |
| dependency | something it needs to work |
| latency | how slow it is |
| authentication | proving who you are |
| frontend | the part people see |
| backend | the part that works behind the screen |
| API | a way for two programs to talk |
| validation (forms) | checking what a person typed |
| iterate | try again and make it better |
| optimize | make it better and faster |
| criteria | what we judge by |
| stakeholder | a person who cares about the result |
| evidence | proof |
| infer | work out |
| scope | how much is included |
| drift | wandering away from the goal |
| checkpoint | a stop to check the work |
| brief | a short note that tells the builder what to do |

## Before and after

**Too hard (never write this):**
"The checkout flow exhibits a state inconsistency whereby the frontend optimistically renders a confirmation prior to backend acknowledgement, creating a latent data integrity risk under network degradation."

**Plain (write this):**
"The screen says 'Order done!' before the app has really saved the order. If the internet is slow, the person thinks they bought something, but the order may be lost.
Why it matters: the person could pay and get nothing.
Fix: show 'Order done!' only after the app says it saved."

## Check before sending

Read the answer once more. Is any word hard? Is any sentence long? Is any point missing? Fix it, then send.
