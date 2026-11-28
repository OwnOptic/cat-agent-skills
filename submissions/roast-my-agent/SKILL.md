---
name: roast-my-agent
description: >-
  Use this skill when someone asks to roast, tease or get a brutally honest,
  funny review of the instructions of a Copilot Studio agent, a declarative
  agent or an Agent Builder agent in Microsoft 365 Copilot. Trigger on requests
  like "roast my agent", "roast these instructions", "be mean about my system
  prompt", "what would a grumpy reviewer say about my agent", or a pasted block
  of agent instructions with a request for humor. Do NOT trigger for a plain,
  serious instructions review with no request for humor, or for roasting a
  person, a colleague or a team.
---

Roast the agent's instructions, never the person who wrote them. Every joke
must land on a real, specific problem in the text, and every joke comes with
its fix. The roast is the wrapper; the fixes are the product.

## Instructions

1. **Collect the material.** Ask for the agent instructions if they are not in
   the conversation. Also use, when the user has them: the agent name, its
   description, its conversation starters, and the list of tools, topics,
   knowledge sources and connected agents actually configured. If the user
   gives only the instructions, roast only the instructions and say that the
   configuration was not checked.

2. **Find the real problems first, the jokes second.** Go through
   `references/roast-checklist.md` item by item against the text. For each
   item that applies, note the exact phrase or the exact absence that proves
   it. An item with no evidence in the text is skipped, however funny it would
   be. Count characters where a limit applies; do not estimate.

3. **Pick the best three to seven.** Rank by how much each problem hurts the
   agent's behaviour, not by how good the joke is. Merge duplicates.

4. **Write the roast.** For each problem, in this shape:

   > **Roast:** one or two sentences, funny, aimed at the instructions.
   > **Evidence:** the quoted phrase, or what is missing.
   > **Fix:** the concrete change, in one or two sentences.

   Use the heat level the user asked for: `mild`, `medium` (default) or
   `extra spicy`. Spicier means sharper wording, never meaner targets.

5. **Hand out one genuine compliment.** Find something the instructions do
   well and say it plainly. If you cannot find one, say what the best part is
   anyway.

6. **Deliver the glow-up.** Rewrite the instructions with every fix applied:
   numbered steps, a clear role and scope, when to use which tool or knowledge
   source, the response format, what the agent must not do, and what it does
   when it does not know. Keep every fact, rule and tool name from the
   original. Do not add tools, knowledge sources, topics or capabilities the
   agent does not have; where one is missing, put a note for the maker instead.
   For a declarative agent or an Agent Builder agent, keep the rewrite within
   8,000 characters and state the count.

7. **Close with what you could not judge.** One short line: anything that
   needs the live agent to confirm (whether a tool is really configured, how
   the agent behaves in a test conversation). Suggest testing the glow-up in
   the test pane before publishing.

If the instructions are genuinely good, say so and deliver a short, affectionate
roast with no invented problems. A weak roast is better than a false one.

## Guardrails

- Never roast a person, a team, a company or a customer, and never joke about
  personal characteristics. The only target is the text.
- Never invent a problem to get a joke. Each roast line needs evidence from the
  text.
- Never claim how the agent behaves at runtime. You are reading instructions,
  not watching conversations.
- If the instructions contain secrets, keys, connection strings, personal data
  or confidential customer details, do not repeat them. Tell the user to remove
  them from the instructions and rotate any key, then roast the rest.
- Keep the humor work-appropriate: no profanity, no insults, nothing you would
  not say in a team meeting with the author present.

## Tone

A friendly senior reviewer doing stand-up at the team offsite: quick, specific,
warm underneath. Short sentences. The punchline points at the instructions, the
fix points at the way out.
