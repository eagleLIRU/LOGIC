# Product testing with LOGIC

Use this when the subject is an app, website, AI agent, SaaS platform, dashboard, or other digital product.

Most test tools ask: "Does this button work?"
LOGIC asks: **Why is this button here? Should it be here? What should happen when someone presses it? What really happens? Does the result make sense?**

That is the whole difference. LOGIC first learns how the product is meant to work. Then it checks if it does.

## Step A: Learn the product first

Before testing anything, study the product and write down in plain words:
- What problem is it built to solve? For whom?
- What are the main parts, and how do they connect?
- What should a user feel and be able to do?
- What should happen when a user takes each main action?

Find this out by looking at real things: the project files, the screens, the settings, any plans or notes, and the running product if it can be run. Do not guess. If you cannot tell how it is meant to work, **ask the user** before testing.

This is Map 2 (see `SKILL.md`, step 2). When the user says yes to it, offer to save it as a short map. Next time, start from the saved map and check it against the real product.

## Step B: Check the eight layers

| # | Layer | The question |
|---|---|---|
| 1 | **Product logic** | Does the app really solve the problem it was built for? |
| 2 | **UI/UX logic** | Does everything make sense to the person using it? |
| 3 | **Button logic** | Does every button do exactly what it promises? |
| 4 | **Flow logic** | Can a person finish a task smoothly, from start to end? |
| 5 | **Brain logic** | Are the AI, the choices, the math, and the rules doing the right thing? |
| 6 | **Connection logic** | Do the front, the back, the database, and the outside services work together? |
| 7 | **Failure logic** | What happens when people make mistakes, something breaks, or something is missing? |
| 8 | **Safety logic** | Who can see or do what? Is private data kept private? Is money handled safely? |

### What to look at in each layer

**1. Product logic.** Who is this for? What do they need? Does each main feature help with that need? Is anything here that does not help? Is anything missing that the goal needs?

**2. UI/UX logic.** Are words clear? Is it easy to know where to go and what to press next? Do two screens say different things? Could a new person get lost?

**3. Button logic.** For each button or link: why is it here, what does it promise, what does it really do, and does that match? Does anything look pressable but do nothing? Does anything do something the label does not say?

**4. Flow logic.** Walk each main task from first step to last, the way a real person would. Where does it get stuck, loop, dead-end, or ask for too much? Can the person go back? Do they know when they are done?

**5. Brain logic.** For AI, rules, and math: What input goes in? What should come out? Test normal cases and edge cases. Check numbers by working them out. Does the AI follow its own rules? Do two rules fight? If the product has an AI agent, also use the method in "Testing an AI agent" below.

**6. Connection logic.** Does what the person sees match what is saved? Does data move correctly from screen to server to database and back? Do outside services answer the way the app expects? Is anything pointing to the wrong place (for example, a test address in a live product)?

**7. Failure logic.** Try empty fields, wrong input, double-presses, no internet, slow answers, missing data, a person without permission, and a service that is down. Does the product stay safe? Does it tell the person what happened in plain words? Can they recover?

**8. Safety logic.** Try it as a person who should not have access. Can they see or change what they should not? Is private data kept private, both on the screen and where it is saved? Is money handled safely: the right amounts, no double charges, nothing taken without a clear yes from the person? Are passwords and secret keys kept out of the screen, the files people can see, and the messages?

### Testing an AI agent

- Make a fixed list of test questions. Include normal ones, tricky ones, wrong or confusing ones, and ones outside the agent's job.
- Ask each question more than once. An AI can answer differently each time. Note when the answers change in a way that matters.
- For each answer, check: Did it follow its own rules? Did it use the right tools, in the right order? Did it refuse what it should refuse? Did it make things up? Did it say "I don't know" when it should? Did it stay on its job?
- Keep the question, the answer, and your mark. That is the proof.
- Use test data only (see "Safe testing" below).

## Step C: How to check for real

- Prefer proof over opinion. Read the code, run the product, press the buttons, follow the flow, and look at what happens.
- Use what the session has. Read the files, run the code, open the product in a browser, read the console and network messages, and take screenshots. Do not guess what you could look at.
- Keep a short proof note for each check: what you did, and what you saw.
- Do not skip a layer quietly. If a layer could not be checked (no access, cannot run it), say so and mark it **Not checked**.
- Do not trust "it worked once." Try the normal path and a few ways it could fail.
- Test only what you were asked to test. Do not change files while testing unless the user said to.

### Safe testing

- Use test accounts and test data only.
- Never use real money, real customer data, or real accounts.
- Never type in real passwords or payment details.
- On a live product, do not submit forms, send messages, buy, delete, or change settings without the user's clear yes.
- If the only way to check something is on live data, stop and ask.

## Step D: Report (plain words, short)

Start with a one-line verdict: change it, leave it, or find out X first. Then show a small table:

| Layer | Result | One line |
|---|---|---|
| Product | Works / Confusing / Broken / Not checked | why |
| ... | | |

Marks, in simple words:
- **Works**: does what it should.
- **Confusing**: works, but a person could get lost or misled.
- **Broken**: does not do what it should.
- **Not checked**: could not be checked, and why.

Then list findings, **worst first** (problems that could lose money, data, or safety; then problems that stop a person from finishing; then confusing parts; then polish). Each finding is short:
- **Where:** the screen, button, or part.
- **What should happen:** one line.
- **What really happens:** one line.
- **Why it matters:** one line.
- **Proof:** saw it, read it, or worked out.
- **Suggested fix:** one line.

Then stop. Do not change anything yet. Ask the user which fixes to make. After a yes, make only those fixes, then check again that each fix really solved its problem and did not break something else.

## When everything is fine

If the product works the way it should, say so plainly: "I checked all eight layers. It works the way it should. I would leave it alone." That is a real, useful answer. Do not make up problems.
