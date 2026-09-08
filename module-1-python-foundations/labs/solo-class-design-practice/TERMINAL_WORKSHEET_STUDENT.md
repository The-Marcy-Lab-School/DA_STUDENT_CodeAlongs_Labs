# Lab — Solo Class Design Rep

**Estimated time:** ~85 minutes (10 min intro · 55 min collaborative work · 20 min shareout)

## Scenario

A local community center runs a tool-lending library — neighbors can borrow things like drills, ladders, and pressure washers for a project, then return them. The volunteer coordinator wants a simple way to track each tool: what it is, how many are available to borrow right now, and whether it needs a safety check before going back out (some tools, like power tools, need a quick inspection after every use; others don't).

You are the person they've asked for help. No attribute names and no method signature are given anywhere in this lab — deciding what a class for this should track, and how to check it, from the paragraph alone is the actual exercise. There is no single correct design: two Fellows can end up with different attribute lists and both be right, as long as every choice traces back to something the coordinator actually said.

*Work with your group, but complete and push/commit your own copy of this lab — collaboration is encouraged, a shared submission isn't.*

## Your Objectives

- **Read the Stakeholder Need**
  - *Deliberately not the board-game or office-supply domain from lecture, and not one of the project's own 4 scenarios - a genuinely new stakeholder need.*

- **Decide Your Attributes — Each With a Reason From the Scenario**

- **Write __init__ and a Method, From Scratch**
  - *There's no single correct design here - your own class name, attribute names, and method can differ from anyone else's and still be correct, as long as each one traces back to the stakeholder paragraph.*

- **Instantiate 2+ Objects, Confirm Independent Storage**
  - *Same proof Day 13's lecture asked for, now on a class you designed yourself - predict what each print() will show before running it.*
  - *Hint: To actually prove independence, change one object's attribute directly, then call your method on both objects — the one you didn't touch should be unaffected.*

- **Justify Your Design Choice in 2-3 Sentences**

## Share Out

Two Fellows can design completely different classes for this same paragraph and both be right. Put 2-3 of your designs side by side: which attributes did everyone land on, and which did only one person pick? For every attribute that isn't on everyone's list, point at the phrase in the coordinator's request it came from — or admit there isn't one. Then the harder question: whose method would the coordinator actually reach for first, and why? Naming what makes a design fit a *stated need* is the same reasoning your project's own design write-up will ask you for.
