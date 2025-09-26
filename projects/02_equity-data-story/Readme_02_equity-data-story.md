## TL;DR
We used public FSABD data to reproduce the Chronic Absenteeism indicator, disaggregated to subgroup, and computed equity gaps to focus action. The report translates those KPIs into specific interventions (Tier-1 messaging, 3/6/9 check-ins, targeted supports) with a 30/60/90 monitoring plan. All methods are reproducible and privacy-minded (small-N suppression; no PII).


**Audience:** Board members, principals, family/community partners  
**Focus:** [District/County], Year: [YYYY]

## Objectives
- Explain current chronic absenteeism levels and trends.
- Surface **equity gaps** by student subgroup.
- Recommend **3–5 targeted actions** with clear owners & timelines.

## Methods
- Data source: `data/processed/kpi_chronic_*` from Project 01  
- KPIs: chronic_absent_rate (fraction), non_chronic_rate, gap_vs_all  
- Privacy: small-N suppression (<10) applied in rollups

## Outputs
- Slides PDF: `/slides/Equity_Data_Story.pdf`  
- Figures: `/assets/` (subgroup profile, equity gaps, trend)

## Recommendations (example)
- **Tier 1 family engagement**: proactive outreach & attendance texting
- **Tier 2 supports**: transportation/health referrals, check-ins at 3/6/9 absences
- **Early warning**: monthly chronic-risk list from SIS; principal review cadence

## What this demonstrates
- Ability to turn complex KPIs into **plain-English stories**
- Equity-minded analysis (disaggregation, gap vs All)
- Actionable policy recommendations & implementation framing
