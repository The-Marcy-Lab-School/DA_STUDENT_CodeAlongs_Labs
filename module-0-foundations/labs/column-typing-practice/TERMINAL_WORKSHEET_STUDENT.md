# Lab — Column-Typing & Collection-Concern Practice

## Open the Raw File First

*Context: Same lab dataset from DATASET.md — a different file than the project's own co2-data, on purpose.*

*Complete the TODOs below as you work through this step.*

```bash
head -n 5 data/energy_sample.csv
```

## Preview Each Column on Its Own

*Complete the TODOs below as you work through this step.*

```bash
cut -d, -f1,2 data/energy_sample.csv | head -n 5
# continue: preview the remaining columns in pairs
```

## Classify Each Column, With a Reason

*⚠️ Not auto-validated: This step is a group discussion/classification exercise, not a command with a checkable output — the code_along field models the expected reasoning, not something to run.*

*Complete the TODOs below as you work through this step.*

```bash
# for each column, write: name, type, and the specific
# reason from the actual data you saw above
```

## Name a Real Collection-Process Concern

*Context: grep -c "" counts lines - a quick way to confirm exactly how many rows you're actually working with before drawing conclusions.*

*Complete the TODOs below as you work through this step.*

```bash
grep -c "" data/energy_sample.csv
```
