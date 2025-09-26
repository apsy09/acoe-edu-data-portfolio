# California K–12 Dashboard (Replica) — Chronic Absenteeism
**Purpose:** Demonstrate the ability to ingest public K–12 data, compute equity-minded KPIs, and present decision-useful visuals aligned with California accountability practices.

**Audience:** District/County leaders, school boards, community partners

**Why it matters for ACOE:**  
- County/district roll-ups mirror **agency-wide reporting** needs.  
- Disaggregation + `gap_vs_all` foreground **equity**.  
- Small-N suppression + de-identification reflect **FERPA-minded data governance**.  
- Clear visuals + a tiny app show **storytelling for non-technical stakeholders**.

---

## Objectives
- Reproduce a simplified **California School Dashboard** view for **Chronic Absenteeism**.  
- Roll up from finest grain to **District, County, State** with **weighted** calculations.  
- Surface **equity gaps** (subgroup vs *All Students*).  
- Export reproducible tables and presentation-ready figures.

---

## Data
- **Source:** California Dept. of Education (CDE) chronic absenteeism files (public).  
- **Grain:** School (preferred), or District if that’s what’s available.  
- **Key fields used:**  
  `academic_year, aggregate_level, county/district/school codes & names, reporting_category (subgroup), chronicabsenteeismeligiblecumulativeenrollment (cohort), chronicabsenteeismcount, chronicabsenteeismrate`

> Place raw CSVs in `data/raw/`. The notebook normalizes headers and types.

---

## Methods (Notebooks)
1. **`notebooks/01_ingest_clean.ipynb`**  
   - Auto-detect delimiter & header, normalize column names, parse academic year, clean subgroup labels.  
   - Outputs cleaned files to `data/interim/*_clean.(csv|parquet)`.

2. **`notebooks/02_kpi_calculations.ipynb`**  
   - Selects **base grain** (School if available).  
   - **Weighted KPI:** `chronic_absent_rate = sum(chronic_absent_count) / sum(cohort)`  
   - **Derived KPI:** `non_chronic_rate = 1 - chronic_absent_rate`  
   - **Equity gap:** `gap_vs_all = subgroup_rate - all_students_rate` (same geo/year)  
   - **Privacy:** Blank rates where `cohort < 10`.  
   - Saves:
     - `data/processed/kpi_chronic_wide_all_levels.csv`  
     - `data/processed/kpi_chronic_long_all_levels.csv`  
     - Per-level splits: `kpi_chronic_wide_{district|county|state}.csv`

3. **`notebooks/03_viz_exports.ipynb`**  
   - Exports PNGs + companion CSVs to `projects/01_california-dashboard-replica/assets/`, e.g.:  
     - `top15_districts_chronic_<YEAR>.png`  
     - `best15_districts_chronic_<YEAR>.png`  
     - `largest_equity_gaps_<YEAR>.png`  
     - `trend_chronic_<district>.png`  
     - `subgroup_profile_<district>_<YEAR>.png`

---

## Quick Repro Steps
```bash
# 1) create & activate env
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\Activate.ps1
pip install --upgrade pip

# 2) install deps
pip install pandas numpy matplotlib streamlit

# 3) run notebooks in order (01 → 02 → 03)
# (Use JupyterLab or VS Code. Ensure raw data is in data/raw/)
