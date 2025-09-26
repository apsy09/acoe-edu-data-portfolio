# LCAP Strategic Plan Mini-Simulator

**Goal:** Turn KPI baselines into targets and forecast the impact of concrete interventions; export a one-pager suitable for LCAP/board updates.

## How it works
- Reads `data/processed/kpi_chronic_wide_all_levels.csv`
- Loads goals from `config/goals.yaml` and levers from `config/interventions.csv`
- Builds **baseline → target → projected** for **All Students** and subgroups
- Outputs CSVs and PNGs to `/assets/` + a printable Markdown one-pager

## Run
Open `notebooks/04_lcap_sim.ipynb` and run top-to-bottom. Edit `config/` to change district/year, targets, and levers.

## What this demonstrates
- **LCAP alignment**: baselines, targets, focus student groups
- **Decision support**: scenario planning (conservative/expected/stretch)
- **Equity lens**: explicit subgroup gap targets
- **Governance**: reproducible, privacy-minded workflow
