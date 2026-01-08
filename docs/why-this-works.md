# Why This Works When Bedrock Doesn’t 😈

Minecraft Bedrock addon management fails not because users are bad — but because **the system provides no rules**.

This project works because it does.

---

## Bedrock’s Core Problem

Bedrock:

* Has no standard addon format
* Does not enforce directory structure
* Allows arbitrary nesting
* Permits unicode chaos in filenames
* Requires manual UUID plumbing

In short: **Bedrock delegates correctness to humans**.

That was a mistake.

---

## Humans Guess. Computers Shouldn’t.

Most Bedrock guides say things like:

> “Just drop it in behavior_packs and see if it works.”

This system rejects that philosophy.

Guessing is replaced with:

* Manifest inspection
* Deterministic rules
* Explicit failure modes

If something is unclear, the system stops.

---

## AI Is Good at Rules — If You Give It Any

Left alone, AI will hallucinate.

With `AGENTS.md`, it will:

* Follow strict installation rules
* Refuse unsafe actions
* Preserve vanilla content
* Explain every change it makes

This isn’t automation.

It’s **delegated responsibility with guardrails**.

---

## Bedrock Treats Worlds as Fragile Afterthoughts

This system treats worlds as:

* Isolated
* Sacred
* Recoverable

Nothing is enabled globally by accident.
Nothing is deleted without intent.

---

## The Magic Is Boring

There is no proprietary format.
No wrapper packs.
No mod loader.

Just:

* Files
* Rules
* Determinism

The “magic” is simply **not being sloppy**.

---

## This Is a Contract, Not a Tool

`AGENTS.md` is not documentation.

It is a **contract** between:

* Humans
* AI agents
* The filesystem

Everyone follows the same rules.

That’s why this works.

---

## Final Thought

Bedrock didn’t fail because it was too strict.

It failed because it wasn’t strict at all.

We fixed that.
