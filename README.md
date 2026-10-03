# Student Academic Performance & Dropout Risk 2026

## Overview

A comprehensive **research-grade** dataset containing **100,000 student records** with **32 carefully engineered features** capturing academic performance, socioeconomic background, engagement behaviour, institutional context, and student wellbeing - all calibrated against peer-reviewed education research and national statistics.

The target variable `dropout` (binary: 0 = Enrolled/Graduated, 1 = Dropped Out) achieves a **32.0% positive rate**, reflecting real-world college attrition patterns without any oversampling.

> The existing UCI Student Performance dataset has only 649 rows. This is a ground-up modern rebuild — **154× more rows**, **32 features**, and calibrated to NCES 2023, UNESCO 2023, and OECD Education at a Glance benchmarks.

---

## Why This Dataset?

Student dropout prediction is one of the most assigned problems in applied ML coursework - and one of the most important in real education policy. Yet most available datasets are tiny, single-institution, or heavily anonymized. This dataset provides:

- **100,000 records** across 15 nationalities, 5 course types, and 3 study modes
- **32 features** spanning academic, financial, behavioural, institutional, and wellbeing dimensions
- **Realistic causal structure** - GPA, attendance, and financial stress drive dropout the way research says they should
- **Modern features** - LMS logins, commute time, mental health support access, and weekly work hours
- **Calibrated prevalences** matching NCES 2023, UNESCO 2023, and OECD Education at a Glance 2023

---

## Feature Groups

| Group | Features | Count |
|---|---|---|
| Demographics | age, gender, nationality, first_generation, disability_status | 5 |
| Socioeconomic | family_income_level, scholarship_holder, tuition_up_to_date, part_time_job, weekly_work_hours | 5 |
| Institutional | course_type, study_mode, semester, international_student | 4 |
| Academic Performance | admission_grade, previous_qualification_grade, units_enrolled, units_passed, units_failed, gpa_semester_1, gpa_semester_2 | 7 |
| Engagement & Behaviour | attendance_rate, assignments_submitted_rate, library_visits_per_month, lms_logins_per_week, extracurricular_activities, missed_deadlines | 6 |
| Wellbeing & Support | stress_level, mental_health_support, satisfaction_score, commute_time_mins, sleep_hours | 5 |
| **Target** | **dropout** | **1** |

---

## Calibration Benchmarks

| Metric | This Dataset | Real-World Source |
|---|---|---|
| Overall dropout rate | **32.0%** | NCES 2023 — 6-year non-completion rate |
| First-generation students | **42.0%** | NCES 2023 |
| Students with disabilities | **20.9%** | NCES 2023 |
| International students | **18.1%** | OECD 2023 |
| Students holding part-time jobs | **48.2%** | Georgetown CEW 2023 |
| Scholarship/aid recipients | **59.0%** | NCES 2023 |
| Mean GPA semester 1 | **2.57** | NCES college GPA distribution |
| Mean attendance rate | **75.1%** | ACT Dropout Prevention Center |
| Mean stress level | **6.45 / 10** | ACHA-NCHA 2023 student health survey |

---

## Key Dropout Risk Patterns

| Risk Factor | Dropout: Yes | Dropout: No | Finding |
|---|---|---|---|
| Tuition NOT up to date | **44.2%** | 28.7% | Financial distress is a top signal |
| Low income family | **42.9%** | 20.0% (High) | Income gap is 2.1× |
| Part-time job holder | **39.8%** | 24.7% | Work burden significantly increases risk |
| First-generation student | **37.4%** | 28.1% | Lacks family college support system |
| Part-time study mode | **33.7%** | 32.0% (Full-time) | Reduced campus integration |
| GPA semester 1 correlation | **r = −0.569** | — | Strongest single predictor |

---

## Suggested Tasks

- **Binary Classification** - Predict `dropout` (0 or 1)
- **Early Warning System** - Identify at-risk students using only semester 1 features
- **Fairness Analysis** - Does the model perform equally across income levels, gender, and first-generation status?
- **Feature Importance** - Which academic vs financial vs behavioural signals matter most?
- **Subgroup Analysis** - How does dropout risk vary by course type and study mode?
- **Threshold Optimization** - Tune for recall (catching all dropouts) vs precision

### Recommended Models
`Logistic Regression` · `Random Forest` · `XGBoost` · `LightGBM` · `CatBoost` · `Neural Networks`

---

## Benchmark Performance

| Model | ROC-AUC | Accuracy | F1 (Dropout) |
|---|---|---|---|
| Logistic Regression | ~0.79 | ~0.74 | ~0.65 |
| Random Forest | ~0.83 | ~0.77 | ~0.68 |
| XGBoost | ~0.85 | ~0.79 | ~0.70 |

---

## Acknowledgements

Calibrated using data from the National Center for Education Statistics (NCES) 2023, UNESCO Global Education Monitoring Report 2023, OECD Education at a Glance 2023, Georgetown Center on Education and the Workforce, American College Health Association NCHA 2023, ACT National Dropout Prevention Center, and Tinto's Student Integration Model. All records are fully synthetic - no real student data is present.
