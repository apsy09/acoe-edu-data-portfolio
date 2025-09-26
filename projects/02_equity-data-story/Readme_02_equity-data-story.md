“We used public FSABD data to reproduce the Chronic Absenteeism indicator, disaggregated to subgroup, and computed equity gaps to focus action. The report translates those KPIs into specific interventions (Tier-1 messaging, 3/6/9 check-ins, targeted supports) with a 30/60/90 monitoring plan. All methods are reproducible and privacy-minded (small-N suppression; no PII).”

{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "7f245e2e-849f-42a1-b200-a36ba748f506",
   "metadata": {},
   "outputs": [],
   "source": [
    "# Equity Data Story — Chronic Absenteeism"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "de17d3a8-3144-4121-9dc5-afdddd13d758",
   "metadata": {},
   "outputs": [],
   "source": [
    "**Audience:** Board members, principals, family/community partners  \n",
    "**Focus:** [District/County], Year: [YYYY]\n",
    "\n",
    "## Objectives\n",
    "- Explain current chronic absenteeism levels and trends.\n",
    "- Surface **equity gaps** by student subgroup.\n",
    "- Recommend **3–5 targeted actions** with clear owners & timelines.\n",
    "\n",
    "## Methods\n",
    "- Data source: `data/processed/kpi_chronic_*` from Project 01  \n",
    "- KPIs: chronic_absent_rate (fraction), non_chronic_rate, gap_vs_all  \n",
    "- Privacy: small-N suppression (<10) applied in rollups\n",
    "\n",
    "## Outputs\n",
    "- Slides PDF: `/slides/Equity_Data_Story.pdf`  \n",
    "- Figures: `/assets/` (subgroup profile, equity gaps, trend)\n",
    "\n",
    "## Recommendations (example)\n",
    "- **Tier 1 family engagement**: proactive outreach & attendance texting\n",
    "- **Tier 2 supports**: transportation/health referrals, check-ins at 3/6/9 absences\n",
    "- **Early warning**: monthly chronic-risk list from SIS; principal review cadence\n",
    "\n",
    "## What this demonstrates\n",
    "- Ability to turn complex KPIs into **plain-English stories**\n",
    "- Equity-minded analysis (disaggregation, gap vs All)\n",
    "- Actionable policy recommendations & implementation framing\n"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "5a0670c0-9213-4f54-9393-4914fad5b29e",
   "metadata": {},
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.11.5"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
