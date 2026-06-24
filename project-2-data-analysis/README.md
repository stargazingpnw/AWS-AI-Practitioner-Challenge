# Project 2: College Cohort Nutrition & Metabolomic Profile Exploration (PartyRock Data Analysis)

An empirical data investigation executed as part of the **AWS AI Practitioner Challenge**, exploring the capabilities of Large Language Models to process, clean, and summarize high-density nutritional and biological spreadsheet data via PartyRock's *Analyze Data* feature.

## 📌 Project Objective
The goal of this project was to leverage PartyRock's data sandbox to upload raw records, perform targeted multi-turn data mining, generate cross-tabulated insights tables, and evaluate the analytical precision of the AI's data synthesis.

## 📊 The Dataset Environment
*   **Target Source:** Derived from the [peer-reviewed Mendeley Data repository](https://data.mendeley.com/datasets/s4ydf6kb8y/1) tracking metabolic metrics in a diverse college-based sample.
*   **Data Format:** Two matching `.xlsx` spreadsheets mapping raw biological and demographic metrics for a cohort of 60 first-year college students.
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

## 🔍 Empirical Findings & Data Insights

### 1. Nutritional-Metabolome Weak Correlations
*   **The Data:** Whiskers uncovered surprisingly weak direct correlations between immediate dietary consumption and active metabolite pools.
*   **Key Metrics:** Acetylcarnitine showed the strongest positive relationship to total calories ($r = 0.30$) and total fat ($r = 0.26$). Counterintuitively, branched-chain amino acids (BCAAs) showed near-zero correlation with direct protein intake ($r = -0.09$ to $0.01$).
*   **Insight:** This proves that internal metabolic regulation, high individual variations, and long-term metabolic stabilization pools dominate over immediate meal-timing intake.

### 2. Environmental & Lifestyle Impact Dynamics
*   **Dorm Variations:** Students housed in *Dorm 2* displayed significantly healthier behavioral patterns than *Dorm 1*, showing $+11\%$ higher caloric intake ($1,659$ vs $1,494$), $+26\%$ more protein, $+57\%$ more physical activity, and $-19\%$ less screen time.
*   **Screen Time Disparities:** High screen time students ($77\%$ of the cohort) consumed $+29\%$ more sugar ($79\text{g}$ vs $62\text{g}$) and had a $+4\%$ higher average BMI ($24.4$ vs $23.5$). 
*   **Reporting Bias Paradox:** Higher caloric intake mathematically correlated with a *lower* BMI ($r = -0.17$), uncovering a clear underreporting bias among higher BMI students in self-reported metrics.

### 3. Physiological Categorization & Molecular Signatures
*   **Gender-Based Variation:** Female students ($n=39$) showed $+7\%$ higher BCAAs and a staggering $+128\%$ higher lactate ($799\text{k}$ vs $350\text{k}$), pointing to higher baseline glycolytic activity despite carrying a $9\%$ lower average BMI ($23.7$ vs $26.1$).
*   **Anomalous Stress Indicators:** Underweight students (Avg BMI 17.8) showed signs of muscle catabolism and metabolic stress, tracking the highest leucine/isoleucine levels and high lactate ($1.1\text{M}$), but the lowest organic and fatty acids. Overweight students showed extreme oxidative stress signatures, tracking the highest pyroglutamate levels ($8.5\text{M}$).
*   **Literature Contradiction:** Higher BMIs inversely correlated with BCAA levels ($r = -0.14$), directly contradicting typical adult sedentary obesity research and highlighting the unique, active metabolic profiles of young student cohorts.

---

## 🎛️ Analysis Artifacts Generated
I successfully commanded Whiskers to build an integrated master analysis matrix mapping **60 individual student rows** sorting by BMI (Highest to Lowest), Age, and Gender. This consolidated layout perfectly linked:
*   **Demographics:** Student ID, Gender, Age, BMI, and Bracket.
*   **Lifestyle Filters:** Dorm location, activity levels, and minute-by-minute screen tracking.
*   **Nutritional Inputs:** Totals for calories, protein, carbs, and fats.
*   **Metabolomic Targets:** Amino acids (Isoleucine, Leucine, Valine, Phenylalanine, Tryptophan), Energy markers (Lactate, Pyroglutamate, Carnitine), Fatty acids (Palmitic, Stearic), and Organic acids (Fumarate, Alpha-KG).

## 🧠 AI Practitioner Skills Demonstrated
*   **High-Density Data Ingestion:** Utilized AI workflows to distill highly technical scientific measurements (16S rRNA sequencing and mass spectrometry metabolome outputs) into accessible summaries.
*   **Analytical Evaluation:** Evaluated generated matrices to verify model accuracy, pinpointing when the model successfully caught non-linear trends vs. self-reporting data biases.
*   **Responsible AI Guardrails:** Evaluated and manipulated complex academic medical datasets while respecting cohort anonymity and focusing strictly on high-level statistical synthesis.

