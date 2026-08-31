# 📊 Student Academic Performance Analysis

An end-to-end data analytics project exploring how daily student habits impact final academic outcomes. This project implements an outlier-safe data cleaning pipeline in **Python**, builds custom data visualizations from scratch in **Matplotlib**, and validates statistical trends using **MySQL** relational database queries.

## 🛠️ Tech Stack & Skills
*   **Data Engineering:** Python, Pandas, Data Imputation, Schema Optimization
*   **Data Visualization:** Matplotlib (Pure layout, zero shorthand frameworks)
*   **Database Management:** MySQL Syntax, Relational Data Aggregations

---

## 🔍 Project Lifecycle & Methodology

### Phase 1: Structural Discovery (Understand)
*   Diagnosed data dimensions consisting of an initial sample of 505 student rows and 8 feature columns.
*   Identified critical structural gaps: 15 missing values in school attendance records, 10 gaps in daily sleep duration entries, and 12 missing data patches across assignment metrics.
*   Located 5 completely redundant exact duplicate entries inflating the raw tracking file.

### Phase 2: Pipeline Engineering (Clean)
*   Permanently removed redundant records to stabilize metrics, dropping the operational dataset safely to 500 unique entries.
*   Implemented strict bracket-assignment syntax (`df['Col'] = df['Col'].fillna()`) to isolate targeted segments and protect the primary multi-column table from memory corruption bugs.
*   Utilized **Median Imputation** rather than standard arithmetic means to fill data gaps, ensuring extreme outliers could not skew baseline group distributions.
*   Validated the restored schema to achieve 0 null elements across all features.

### Phase 3 & 5: Analytical Exploration (Python & SQL)
Migrated the engineered dataset into a relational database engine to evaluate performance variance by running concurrent slicing logic in Python and aggregate queries in MySQL:
1.  **Study Hours Tracking:** Grouping students by weekly commitment revealed a dominant **~5.56-point grade advantage** for individuals dedicating 15+ hours to independent study.
2.  **Attendance Mapping:** Isolating attendance tiers uncovered a clear **~3.34-point drop** in final evaluation averages for chronically absent students (below an 85% attendance baseline).
3.  **Sleep Threshold Analysis:** Executing advanced `GROUP BY` and sorted `ORDER BY AVG(Final_Score) DESC` operations revealed that sleep duration has a minimal baseline effect (~1.22-point total variance), but highlights a clear performance optimization peak right between **8.3 and 8.4 hours of sleep**.

---

## 📊 Visual Insights & Performance Trends
All data visualizations are rendered natively inside the primary notebook architecture:

*   **Study Tier Distributions:** A custom Matplotlib categorical bar chart maps the grade gap between high-volume and low-volume study habits.
*   **Linear Correlation Slopes:** A custom scatter plot mapping raw student records visually validates the strong positive linear correlation between weekly study hours and final scores.

👉 *To view the complete interactive data charts and raw tables, please click and open the `student_analysis_pipeline.ipynb` file above.*
---

## 💡 Executive Recommendations
*   **Prioritize Study over Sleep Tuning:** Students looking for maximum grade returns should focus directly on reaching a minimum baseline of 15 independent study hours per week before over-optimizing minor lifestyle parameters.
*   **Maintain the 85% Attendance Floor:** Educational support programs should actively flag and monitor students dipping below an 85% attendance threshold, as this boundary marks the point where final performance scores degrade heavily.
*   **Target the Sleep Sweet-Spot:** While sleep exhibits the weakest overall correlation slope, the data indicates that protecting an 8.3-hour rest window yields the maximum statistical efficiency for academic recovery.
