# Lab — Stress-Test Your Code: Timing & Efficiency

**Estimated time:** ~90 minutes (10 min intro · 65 min collaborative work · 15 min shareout)

## Scenario

You shipped the class you designed in Day 15's lab, and it works. Your manager has one question before it goes anywhere near real users: "this is fine with ten records — will it still be fine with a hundred thousand?" Nobody on the team can answer that from reading the code, and "it feels fast on my laptop" is not an answer. So today you find out the way engineers actually find out: build a scaled-up batch of your own objects, write the search two different ways, put a stopwatch on both, and let the numbers say which one survives the jump from 10 records to 100,000. Your job by the end of lab is to be able to tell your manager what happens at scale — and show the timings that prove it.

*Work with your group, but complete and push/commit your own copy of this lab — collaboration is encouraged, a shared submission isn't.*

## Your Objectives

- **Generate Batches of Your Own Day 15 Class at Three Sizes (10, 1,000, and 100,000)**
  - *Use your own class from Day 15's lab - your batch should be full of YOUR objects, not a shared template's.*
  - *Hint: One function that takes a size and returns that many instances, called three times, is enough. Give the instances varied attribute values rather than a hundred thousand identical ones - `random` is useful here - and make sure whatever attribute you plan to search on is unique per instance, or Step 2's two searches won't be comparable.*

- **Write Two Searches Over That Batch - a Linear Scan and a Dict Lookup - and Confirm They Agree**
  - *Same two functions Day 16's lecture wrote over SupplyItem - now over your own class and a much bigger batch.*
  - *Hint: Day 16's dict version was a comprehension - `{item.name: item for item in supplies}` - keyed on the same attribute the linear scan compares against. Both of yours should hand back the same object for the same target, and both should cope with a target that isn't in the batch at all; Step 3 depends on that second case.*

- **Put a Stopwatch on Both Searches at All Three Sizes and Record the Numbers**
  - *Predict the pattern before running: which column should grow as size grows, and which should stay roughly flat?*
  - *Hint: `time.perf_counter()` is new - it returns a number of seconds, so you time something by reading it before and after and subtracting. Search for a value that is NOT in your batch: a search that finds its answer on the first try tells you nothing about scale, and the worst case is what makes the growth show up. End with three rows - one per size, each with both times - because a single row can't show a trend.*

- **Answer Your Manager's Question in One Sentence, in Big-O Terms**
  - *Hint: Use your own Step 3 numbers, and name both Big-O classes. "The dict was faster" is not the answer your manager asked for - they asked what happens at 100,000, which is a question about what each column DID as the size grew, not about which one won a single race.*

- **Optional Stretch: Ask an AI How to Speed Up Your Linear Scan, Then Make It Prove It**
  - *Stretch work only - beyond the core lab budget. Take it if you finish Steps 1-4 early. Same 'verify before trusting' habit from Module 0's AI-literacy lesson, now applied to a code-optimization claim instead of a chatbot fact claim.*
  - *Hint: Apply the suggestion, then re-run Step 3's timing setup unchanged, so the before and after are actually comparable. If the numbers don't move, the claim didn't hold - and saying so is a correct answer here.*

## Share Out

Put your Step 3 numbers up where the room can see them. Everyone tested a different class, on a different laptop, with different attributes — so the raw numbers won't match, and that's the interesting part. Which column looked the same across every single person in the room, and which one didn't? At what batch size did the difference stop being something you had to squint at? Did anyone's linear scan look suspiciously flat, and what turned out to be going on if so? And for anyone who tried the optional stretch: what did the AI suggest, and did your own timing actually back up its claim — or not?
