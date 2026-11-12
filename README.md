# Fire Department Response Times: Career vs. Volunteer Departments

Final project for STAT 3120 (Kennesaw State University), May 2023.
Authors: Nakai Zemer and Gabriel Salisbury.

**Question:** is there a statistically significant difference in mean response time (dispatch to arrival) between career and volunteer fire departments, and how does it relate to population density?

**Data:** 2019 NFIRS incident data (public), rolled up to one row per department (11,884 departments).

## Headline results

| Test | Result |
|---|---|
| Difference in mean response time, volunteer minus career (Welch t-test) | 2.23 min, t = 57.93, df = 9066.2, p < .0001 |
| Population density vs. mean response time (Pearson r) | -0.3124 overall; -0.2217 career; -0.2686 volunteer (all p < .0001) |
| Department type (4 levels) vs. fast/slow (<= 7.5 min) (chi-square) | chi-sq = 2310.4, df = 3, p < .0001 |

With this many departments, p-values are tiny almost by default, so effect sizes (minutes of difference, size of r) are the more informative numbers.

## Files

- `Final Project Presentation.pdf` / `.pptx` - the main write-up (6 slides): variable dictionary, results, and incident exclusion criteria.
- `stat_3120_final_project.qmd` / `.html` - analysis code and rendered output (R, Quarto).
- `datasets/nfirs_dept.csv` - department-level dataset used for all tests.
- `datasets/nfirs_dept_df.csv`, `datasets/response_times_by_dept_type_desc_stats.csv` - derived tables.
- `*.png` - figures produced along the way.

## Data note

`datasets/nfirs_dept.csv` is the input to the analysis. The 1.6 GB incident-level extract it was built from (`basicincident_2019.fst`) is not included in this repository. Incident exclusion criteria are documented on the last slide of the presentation.

## Writeup on the web

https://kai.do/projects/fire-department-response-times/
