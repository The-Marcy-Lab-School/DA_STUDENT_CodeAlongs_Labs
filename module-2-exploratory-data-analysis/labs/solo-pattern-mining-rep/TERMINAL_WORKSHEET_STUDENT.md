# Lab — Solo Pattern-Mining Rep

**Estimated time:** ~90 minutes (10 min intro · 65 min collaborative work · 15 min shareout)

## Scenario

You're the analyst on a small research team studying a penguin colony. Someone senior has already run a number across the whole dataset and wants to put it in next week's write-up: "here's how these two measurements relate in these birds." Before that sentence goes out with your name anywhere near it, somebody has to check whether the pattern actually holds up inside the groups that make up the data, or whether it only looks that way because of who's in the pile. Today that's you — and nobody is handing you a pair of columns or a template. You pick what to look at, you decide whether the aggregate number is honest, and you write down what you'd want to know before trusting it. Sit with your group and ask them when you're stuck, but this one is your own hunt: your own pair, your own finding, your own committed file.

*Work with your group, but complete and push/commit your own copy of this lab — collaboration is encouraged, a shared submission isn't.*

## Your Objectives

- **Reload the Data and Drop Rows Missing `sex`**
  - *Same `penguins.csv` from Days 2-10, at `../../data/penguins.csv` from this lab folder. A fresh notebook session starts with nothing in memory, even if this file looks familiar.*

- **Pick Two Numeric Columns Nobody Compared in Lecture, and Measure Their Relationship Across All 333 Birds**
  - *A correlation near 0 means little relationship; near +1 or -1 means a strong one, in either direction.*

- **Recompute the Exact Same Relationship Separately Within Each Species, and Compare**
  - *Same confound-check habit from the earlier pattern-mining lecture — an aggregate number can hide a real per-group story.*
  - *Hint: A correlation needs two columns at once, which is one of the few things `.groupby()` won't hand you in a single obvious call. A plain loop over `df["species"].unique()`, filtering `df` down to one species each time through, is a perfectly good route.*

- **Write 3-4 Sentences on Which of Your Two Numbers Tells the Honest Story, Plus One Checkable Question About It**
  - *"Checkable" has the specific meaning from the Day 10 lecture — a question someone could actually go and answer, not a general worry about whether the data is any good.*

## Share Out

Go around and have Fellows name the two columns they picked — put the pairs up where everyone can see them, since almost nobody will have chosen the same one. Then the real question: whose all-birds number survived being recomputed inside each species, and whose didn't? Sort the pairs on the board into those two piles and look at them together. What do the pairs that changed have in common that the steady ones don't? Last, read a few of the checkable questions out loud and ask the room which ones somebody could actually go answer this week — and which ones sound rigorous but couldn't be checked by anyone.
