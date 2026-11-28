# Roast My Agent

Paste your agent's instructions and get roasted. Kindly. Every joke points at
a real line in your instructions, every joke comes with the fix, and the roast
ends with a rewritten version you can paste back into Copilot Studio, Agent
Builder or your declarative agent manifest.

It is a review with better jokes. Makers can run it on each other's agents at a
show-and-tell without anyone leaving the room upset, because it roasts the
text and never the person.

## What you get back

- **The roast:** three to seven problems, each as a joke, the evidence quoted
  from your instructions, and the fix.
- **One genuine compliment**, because there is always something.
- **The glow-up:** your instructions rewritten with every fix applied, keeping
  your facts, rules and tool names. For declarative and Agent Builder agents it
  stays within the 8,000 character limit and shows the count.
- **What it could not judge**, such as whether a tool is really configured.

Ask for `mild`, `medium` or `extra spicy`. Spicier gets sharper wording, never
meaner targets.

## Example

> **Roast:** "Help users with anything they need." Bold. Your agent's job
> description is also the plot of every superhero film.
> **Evidence:** the only line that defines the role.
> **Fix:** name the domain, the users and the three tasks it handles, and say
> what is out of scope.

## Where the problems come from

The twelve problems it looks for are in `references/roast-checklist.md`, each
tied to Microsoft Learn guidance on writing agent instructions: vague scope,
no rule for tools versus knowledge, instructions for tools the agent does not
have, nicknames instead of exact tool names, contradictions, no "must not" list,
no failure handling, and the published size limits for declarative agents.
It only roasts what the text shows, and says so when the instructions are
actually good.

## Good to know

- Give it the list of tools, topics and knowledge sources too, and it can catch
  instructions that point at something that does not exist.
- It reads instructions, not conversations. Test the rewritten version in the
  test pane before you publish it.
- If your instructions contain a key or personal data, it will not repeat it and
  will tell you to take it out.
