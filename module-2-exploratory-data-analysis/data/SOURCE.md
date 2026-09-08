# Data Sources — Module 2 Lecture/Lab Demos

Shared demo data for lecture/lab days (and any later day that wants a
running example) — never the project's own 4 domains (see `DATASET.md`'s
"never reuse" rule).

## `penguins.csv` — Palmer Station LTER penguin measurements

**344 rows, 8 columns.** Real biological measurements — species, island,
bill length/depth, flipper length, body mass, sex, year — for 3 penguin
species across 3 islands in the Palmer Archipelago, Antarctica.

**License**: CC0 1.0 Universal (public domain dedication), via the
`palmerpenguins` Python package (`pip install palmerpenguins`,
`allisonhorst/palmerpenguins` on GitHub) — original data courtesy of
Dr. Kristen Gorman and the Palmer Station Long Term Ecological Research
Network.

Generated once via `load_penguins()` from that package and saved here as
a plain CSV (`df.to_csv("penguins.csv", index=False)`) so lecture code
can load it with a plain `pd.read_csv()`, matching how a Fellow will
actually load the project's own data — no extra pip package required to
follow along.

**Real missing values, exactly as published, not modified**: `sex` has
11 missing rows; `bill_length_mm`, `bill_depth_mm`, `flipper_length_mm`,
and `body_mass_g` each have 2 missing rows (the same 2 rows across all
four — both from birds with no morphological measurements taken at all).

| Column | Type | Notes |
|---|---|---|
| `species` | string | Adelie, Chinstrap, or Gentoo |
| `island` | string | Torgersen, Biscoe, or Dream |
| `bill_length_mm` | float | 2 missing |
| `bill_depth_mm` | float | 2 missing |
| `flipper_length_mm` | float | 2 missing |
| `body_mass_g` | float | 2 missing |
| `sex` | string | male/female, 11 missing |
| `year` | int | 2007-2009 |

## `earthquakes.csv` — USGS Earthquake Catalog (January 2024, magnitude 2.5+)

**2,107 rows, 22 columns.** Real seismic events for January 2024 with
magnitude ≥ 2.5, pulled directly from the USGS FDSNWS event API
(`earthquake.usgs.gov/fdsnws/event/1/query`).

**License**: U.S. Government Work — public domain (17 U.S.C. §105), per
USGS's own terms — same legal basis as the project's own FEMA/CMS
sources.

Fetched once via:
```
https://earthquake.usgs.gov/fdsnws/event/1/query?format=csv&starttime=2024-01-01&endtime=2024-01-31&minmagnitude=2.5&orderby=time
```
saved as-is, no columns dropped or modified. A live query against the
same endpoint will return different/more rows over time (the catalog
gets revised) — this snapshot is what every Module 2 lecture/lab should
reference for reproducible numbers, not a fresh live pull.

**Real, verified skew** (via `df["col"].skew()`): `depth` is heavily
right-skewed (skew ≈ 3.17 — most quakes are shallow, a long tail of much
deeper ones) — the module's own chart-best-practices/right-skew teaching
variable. `mag` is close to symmetric (skew ≈ -0.24) — a useful contrast
variable in the same dataset, no second dataset needed to show both
shapes.

| Column | Notes |
|---|---|
| `time` | ISO timestamp of the event |
| `latitude` / `longitude` | event location |
| `depth` | km below surface; heavily right-skewed, real outliers |
| `mag` | magnitude; roughly symmetric in this slice |
| `place` | human-readable location description |
| `type` | almost always `"earthquake"` — a few other event types possible |

(22 columns total — the rest are technical/network metadata not needed
for any Module 2 demo; only `mag`, `depth`, `place`, `time`, `latitude`,
`longitude` are expected to actually appear in lecture code.)
