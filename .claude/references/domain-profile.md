# Domain Profile

<!--
Filled for the project "Subsidios y voto al oficialismo" (2026-10-16). Entries marked [ASSUMED]
are defaults chosen before the research interview; /discover interview should confirm or replace them.
All agents read this file to calibrate their field-specific behavior.
-->

## Field

**Primary:** Political Economy (distributive politics, retrospective voting, clientelism)
**Adjacent subfields:** Public Finance (intergovernmental transfers, subsidies), Development (cash transfers), Political Science (electoral behavior)

---

## Target Journals (ranked by tier)

| Tier | Journals |
|------|----------|
| Top-5 | AER, Econometrica, JPE, QJE, REStud |
| Top field | AEJ: Applied, AEJ: Economic Policy, JPubE, JEEA, APSR, AJPS |
| Strong field | JDE, Journal of Politics, EJPE, BJPolS, QJPS, Economics & Politics |
| Specialty | Public Choice, Electoral Studies, JEPP, Latin American Economic Review |

---

## Common Data Sources

<!-- [ASSUMED] Country not yet fixed; the Explorer replaces this generic list once it is. -->

| Dataset | Type | Access | Notes |
|---------|------|--------|-------|
| Official electoral results by municipality / precinct | admin | public | Electoral authority; harmonize party labels and coalitions across elections |
| Subsidy / transfer spending by territorial unit | admin | public or restricted | Budget execution or program registries; check whether it records allocation or actual payment, and timing relative to elections |
| Program beneficiary registries | admin | restricted | Needed for individual- or household-level designs (e.g., eligibility scores) |
| Census / household surveys | survey | public | Baseline covariates and pre-treatment characteristics (Table 1) |
| Opinion surveys (Latinobarómetro, LAPOP, national polls) | survey | public | Reported government support; complements vote shares |

---

## Common Identification Strategies

| Strategy | Typical Application | Key Assumption to Defend |
|----------|-------------------|------------------------|
| RDD on eligibility score | Program assignment by a poverty/income index (Manacorda, Miguel & Vigorito 2011) | No manipulation of the score; continuity of potential outcomes at the cutoff |
| Close-election RDD on political alignment | Transfers to aligned vs. non-aligned mayors (Brollo & Nannicini 2012) | No sorting in close races; alignment is the only discontinuous attribute |
| DiD / event study with staggered rollout | Program expansion across municipalities over time | Parallel trends in incumbent vote share; heterogeneity-robust estimators |
| IV / formula-based allocation | Spending driven by rules or exogenous shifts (Levitt & Snyder 1997 use other districts' spending) | Exclusion restriction: instrument affects votes only through spending |
| Panel with unit and election FE | Spending changes and vote-share changes (Kriner & Reeves 2012) | Spending not targeted on anticipated vote swings (reverse causality from tactical allocation) |

---

## Field Conventions

- Main outcome: incumbent (oficialismo) vote share at the territorial unit; also turnout and reported support where surveys exist
- Define "oficialismo" explicitly by level (national, subnational) and handle coalitions and party switches consistently
- Spending measured per capita and timed relative to the election (pre-election year vs. earlier)
- Cluster standard errors at the level where spending is assigned (municipality / province), or by score bins in RDD
- Always discuss tactical allocation (spending targeted at swing or core voters) as the main endogeneity threat
- Distinguish credit claiming / clarity of responsibility across government levels

---

## Notation Conventions

| Symbol | Meaning | Anti-pattern |
|--------|---------|-------------|
| $V_{mt}$ | Incumbent vote share in unit $m$, election $t$ | Don't use $Y$ for vote share and another outcome interchangeably |
| $S_{mt}$ | Subsidy spending per capita in unit $m$ before election $t$ | Don't mix levels and per-capita amounts under one symbol |
| $A_{mt}$ | Political alignment of the local executive with the incumbent | -- |

---

## Seminal References

| Paper | Why It Matters |
|-------|---------------|
| Levitt & Snyder (1997, JPE) | Instruments House-district spending; spending raises incumbent vote share |
| Bickers & Stein (1996, AJPS) | Pork-barrel dynamics and challenger entry |
| Manacorda, Miguel & Vigorito (2011, AEJ: Applied) | RDD on PANES eligibility; cash transfers raise government support |
| Brollo & Nannicini (2012, APSR) | Close-race RDD; aligned mayors get more transfers before elections |
| Kriner & Reeves (2012, APSR) | Federal spending rewards incumbent presidents at county level |
| Kriner & Reeves (2015, APSR) | Presidential particularism in allocation (swing and core counties) |
| Vergne (2009, EJPE) | Election-year shift toward subsidies and current spending in developing countries |
| Finan & Mazzocco (2021, JEEA) | Structural model of legislators' electoral allocation of public funds |
| Vergioglou (2023, JEPP) | EU regional investment subsidies and eurosceptic vote |

---

## Theoretical Foundational References

<!-- Fill only if the paper adds a formal model (e.g., Cox & McCubbins 1986; Dixit & Londregan 1996 on swing vs. core targeting). -->

| Topic | Anchor references |
|-------|------------------|
| [Swing vs. core voter targeting] | [to confirm in /discover lit] |

---

## Paper Author Team

| Author | Foundational on |
|--------|----------------|
| [Author surnames] | [--] |

---

## Field-Specific Referee Concerns

- "Spending is allocated strategically" — reverse causality from tactical targeting of swing or core units
- "Who gets the credit?" — which level of government voters attribute the subsidy to
- "Is it the subsidy or the economy?" — confounding with local economic conditions
- "Turnout vs. persuasion" — whether effects come from mobilization or vote switching
- "Clientelism vs. programmatic transfers" — discretionary vs. rule-based allocation

---

## Quality Tolerance Thresholds

| Quantity | Tolerance | Rationale |
|----------|-----------|-----------|
| Point estimates | 1e-6 | Numerical precision |
| Standard errors | 1e-4 | Bootstrap / clustering variability |
| Vote shares | 0.1 pp | Rounding in official results |
