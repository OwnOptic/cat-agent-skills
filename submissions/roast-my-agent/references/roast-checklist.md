# Roast checklist

Each item names the problem, what proves it in the text, the fix, and the
Microsoft Learn source the fix comes from. Only roast an item when the text
shows it.

## Sources

- [DESIGN] Use the agent design framework, building blocks of agent design:
  https://learn.microsoft.com/microsoft-copilot-studio/guidance/agent-design-canvas-framework
- [GUIDE] Configure high-quality instructions for generative orchestration:
  https://learn.microsoft.com/microsoft-copilot-studio/guidance/generative-mode-guidance
- [ORCH] Apply generative orchestration capabilities, best practices for agent
  instructions:
  https://learn.microsoft.com/microsoft-copilot-studio/guidance/generative-orchestration
- [DABP] Best practices for building declarative agents:
  https://learn.microsoft.com/plugins/declarative-agent-best-practices

## Items

### 1. The fortune cookie
**Proof:** a role or scope so vague it fits any agent, such as "Help users with
support issues".
**Fix:** name the domain, the users, the tasks it handles and the boundaries.
**Source:** [DESIGN], common pitfalls: instructions that are too vague.

### 2. The choose-your-own-adventure
**Proof:** no rule for when to use knowledge, when to call a tool and when to
hand off to another agent.
**Fix:** one instruction per ambiguous case, for example "Use the FAQ documents
only if the question is not about billing".
**Source:** [DESIGN] common pitfalls; [GUIDE] help the agent determine the
appropriate tools and knowledge to call.

### 3. The imaginary friend
**Proof:** the instructions tell the agent to use a tool, a knowledge source or
a topic that is not in the configuration the user gave.
**Fix:** add the tool or knowledge source, or delete the instruction.
**Source:** [GUIDE]: agents can't act on instructions to use tools or knowledge
sources they don't have. [ORCH] 1.1: reference only tools and knowledge
available to the agent.
**Only when** the user supplied the configuration. Otherwise list it under what
you could not judge.

### 4. The nickname
**Proof:** a tool or topic referred to by a name that does not exactly match
the configured name ("the order thing" for **Purchase Order**).
**Fix:** use the exact name. In Copilot Studio, insert it from the `/` menu.
**Source:** [GUIDE]: slight differences in naming can negatively affect results;
[ORCH] 1.2.

### 5. The menu reader
**Proof:** a long passage that only restates which tools and knowledge sources
exist, with no guidance on when to use them.
**Fix:** cut the list. Keep only hints for the ambiguous cases.
**Source:** [GUIDE]: you don't need to define the available tools or knowledge
sources in the instructions; focus on cases where the right one might be
ambiguous.

### 6. The wall of text
**Proof:** a multistep process written as one paragraph, with no numbering and
no stated order.
**Fix:** number the steps and say they are followed in order. Markdown helps.
**Source:** [GUIDE]: number or list your instructions and specify that the
agent must follow them in order; [ORCH] 4.1.

### 7. The contradiction sandwich
**Proof:** two rules that cannot both hold, such as "always ask clarifying
questions" and "respond only with final answers".
**Fix:** keep one, or say when each applies.
**Source:** [DESIGN] common pitfalls: conflicting instructions.

### 8. The no-brakes agent
**Proof:** nothing the agent must not do: no limits on sensitive data, internal
identifiers, or legal or HR advice where the domain calls for them.
**Fix:** add an explicit "must not" list for the domain.
**Source:** [DESIGN] common pitfalls: no explicit "must not do" guidance.

### 9. The confident guesser
**Proof:** no rule for what happens when knowledge is missing or a tool call
fails.
**Fix:** "If the knowledge is missing or a tool call fails, don't guess. Say
what you could not find and give the next step."
**Source:** [DESIGN] failure handling example.

### 10. The surprise format
**Proof:** no response format or style at all, for an agent whose answers need
one (a table, a list, citations, next steps).
**Fix:** state the format and the style.
**Source:** [ORCH] 2.1 and 2.2.

### 11. The card whisperer
**Proof:** instructions that try to control when an Adaptive Card appears.
**Fix:** edit the card or its trigger configuration instead.
**Source:** [GUIDE]: agent instructions can't modify how Adaptive Cards are
triggered.

### 12. The overpacked suitcase (declarative agents and Agent Builder)
**Proof:** a counted limit exceeded: instructions over 8,000 characters, a
description over 1,000, a name over 30 in Agent Builder or over 100 in the
manifest.
**Fix:** move detail out, or cut it.
**Source:** [DABP] declarative agent components.
**Only** count, never estimate, and only for declarative agents or Agent
Builder agents. Copilot Studio limits are not covered here.
