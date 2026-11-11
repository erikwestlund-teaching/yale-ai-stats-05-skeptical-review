# Neighborhood Health Survey: Codebook

File: `inputs/raw/neighborhood_health_survey.csv`

These are **fully simulated** teaching data, built to have the same columns as the 2021–2023 NHANES analysis file. Don't draw substantive conclusions from them.

- One row per participant, 6,000 rows, 57 columns.
- Missing numeric values are `NA`. Some missing categorical values are **empty strings**, not `NA`. For example, `education_adults_20_plus` is blank for people under 20.
- The file includes survey design columns (`interview_weight`, `mec_exam_weight`, `masked_variance_stratum`, `masked_variance_psu`).

## Key columns

| Column | Meaning |
|---|---|
| `respondent_id` | Simulated participant ID |
| `gender` | `female`, `male` |
| `age_years` | Age in years (0–80; 80 means 80 or older) |
| `age_group` | `0-17`, `18-29`, `30-44`, `45-64`, `65-79`, `80+` |
| `race_ethnicity` | Six categories |
| `education_adults_20_plus` | Highest education, adults 20+ only |
| `family_income_to_poverty` | Ratio of family income to the poverty line (capped at 5) |
| `household_size` | People in the household |
| `interview_exam_status` | `interviewed_and_examined` or `interviewed_only` |
| `systolic_mean`, `diastolic_mean` | Mean of up to three blood pressure readings (mm Hg) |
| `adult_bp_category_simplified` | `normal_range`, `elevated_range`, `stage_1_range`, `stage_2_range` (blank if not measured) |
| `mean_daily_sodium_mg` | Mean daily sodium intake across dietary recall days (mg) |
| `mean_daily_energy_kcal` | Mean daily energy intake (kcal) |
| `interview_weight`, `mec_exam_weight` | Survey weights |
| `masked_variance_stratum`, `masked_variance_psu` | Survey design variables |

Blood pressure is only measured for examined participants, so `systolic_mean` is missing for about a third of rows.
