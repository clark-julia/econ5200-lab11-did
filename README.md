# econ5200-lab11-did
# Difference-in-Differences: Parallel Trends, Staggered Adoption and the Forbidden Comparison

## Objective
I used difference-in-differences (DiD) to study how different assumptions, treatment timing, and standard error choices affect causal estimates.

## Methodology
- Reproduced Card and Krueger's (1994) minimum-wage DiD using David Card's original data files.
- Ran a two-by-two DiD regression on a panel with different group trends and tested for pre-trends.
- Estimated two-way fixed effects (TWFE) on a staggered-adoption panel and broke the estimate into two-by-two comparisons.
- Compared iid and clustered standard errors on a panel with persistent state-level shocks.
- Used AI to write a Goodman-Bacon decomposition, compared its estimates and weights against my own calculations, and revised the prompt to handle missing outcomes.

## Key Findings
- The Card and Krueger replication produced an estimate of **+2.75 full-time-equivalent employees**, close to the published +2.76.
- A DiD model with no true treatment effect still produced a significant estimate because the groups had different trends. The pre-trend test detected this violation.
- TWFE produced an estimate of **-0.99**, even though the true average treatment effect was **6.71**. About **66.7%** of its weight came from a comparison using already-treated units as controls.
- The iid standard errors were **8.6 times smaller** than the state-clustered standard errors because they did not account for persistent state-level shocks.
- After revising my AI prompt, the Goodman-Bacon decomposition matched my calculations, including a weighted sum of **2.67** on the panel with missing outcomes.
