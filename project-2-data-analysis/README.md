# Project 2: College Cohort Nutrition & Metabolomic Profile Exploration (PartyRock Data Analysis)

An empirical data investigation executed as part of the **AWS AI Practitioner Challenge**, exploring the capabilities of Large Language Models to process, clean, and summarize high-density nutritional and biological spreadsheet data via PartyRock's *Analyze Data* feature.

## 📌 Project Objective
The goal of this project was to leverage PartyRock's data sandbox to upload raw records, perform targeted multi-turn data mining, generate cross-tabulated insights tables, and evaluate the analytical precision of the AI's data synthesis.

## 📊 The Dataset Environment
*   **Target Source:** Derived from the peer-reviewed Mendeley Data repository tracking metabolic metrics in a diverse college-based sample.
*   **Data Format:** Two `.xlsx` spreadsheets mapping raw biological and demographic metrics for a cohort of 60 first-year college students.
*   **Core Variables Available:** 
    *   **Food Insecurity Metadata:** Nutritional intake data (calories, macronutrients, vitamins, minerals), demographic information (age, gender, BMI), and lifestyle factors (screen time, physical activity, year in school, dorm status).
    *   **Food Insecurity Metabolome:** Metabolomic data showing various metabolites detected in samples (amino acids, organic acids, vitamins, fatty acids, etc.).

---

## 📈 Analytical Workflow & Questions Explored
Using PartyRock's AI assistant (Whiskers), I interrogated the matching spreadsheets with a structured three-part questioning framework designed to bridge lifestyle metadata with biological metabolome metrics:

1.  **Nutritional-Metabolome Bridge (Question 1):** *Looking across both files, how do the profiles of key energy metabolites (like amino acids and fatty acids) in the metabolome file vary or correlate based on a student's actual caloric and macronutrient intake recorded in the metadata file?*
2.  **Lifestyle Variance Matrix (Question 2):** *Within the metadata file, what visible trends or patterns emerge when analyzing nutritional intake (macro/micronutrients) alongside lifestyle factors like screen time, physical activity levels, and dorm residency status?*
3.  **Physiological Categorization (Question 3):** *How do distinct physiological categories (such as specific BMI brackets, age, and gender) map against the recorded variances of organic acids and amino acid chains found in the cohort's metabolomic profiles?*

---

## 🎛️ Analysis Artifacts Generated
*   **AI-Generated Analysis Table:** Commanded the assistant to build a structured matrix synthesizing complex row data, clearly mapping nutrient variables and lifestyle habits against demographic subsets.
*   **Verification Strategy:** Evaluated the AI's conclusions against the dataset's actual values to test whether the foundational transformer model accurately flagged significant data correlations (like specific metabolite variances matching physical activity scores) without experiencing mathematical hallucinations.

## 🧠 AI Practitioner Skills Demonstrated
*   **Complex Data Ingestion:** Utilized AI workflows to distill highly technical scientific measurements (macronutrients and mass spectrometry metabolome outputs) into accessible summaries.
*   **Analytical Evaluation:** Evaluated generated matrices to ensure the AI maintained structural integrity, mapping the correct biological metrics to the correct student demographic metrics.
*   **Responsible AI Guardrails:** Practiced working with anonymized health and demographic datasets, focusing on identifying broad statistical health trends while protecting data integrity.

