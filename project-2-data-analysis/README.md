# Project 2: Gut Microbiome & Food Insecurity Analysis (PartyRock Data Analysis)

An empirical data investigation executed as part of the **AWS AI Practitioner Challenge**, exploring the capabilities of Large Language Models to process, clean, and summarize high-density biological spreadsheet data via PartyRock's *Analyze Data* feature.

## 📌 Project Objective
The goal of this project was to leverage PartyRock's data sandbox to upload raw records, perform targeted multi-turn data mining, generate cross-tabulated insights tables, and evaluate the analytical precision of the AI's data synthesis.

## 📊 The Dataset Environment
*   **Target Source:** Derived from the peer-reviewed Mendeley Data repository: [*"Association of food insecurity on gut microbiome and metabolome profiles in a diverse college-based sample"*](https://data.mendeley.com/datasets/s4ydf6kb8y/1) (Mohr et al., 2022).
*   **Data Format:** Two `.xlsx` spreadsheets mapping raw biological and demographic metrics for a cohort of 60 first-year college students.
*   **Core Variables:** 
    *   Food Security Status (Food Secure [FS] vs. Food Insecure [FI])
    *   Microbial Abundance & Diversity (e.g., Enterobacteriaceae, Eisenbergiella, Megasphaera, Holdemanella)
    *   Metabolomic Profiles (e.g., picolinic acid, phosphocreatine, 2-pyrrolidinone)

---

## 📈 Analytical Workflow & Questions Explored
Using PartyRock's AI assistant (Whiskers), I interrogated the spreadsheets with a structured three-part questioning framework:

1.  **Cohort Comparison (Question 1):** *What are the primary differences in gut microbial abundance (specifically Enterobacteriaceae vs. Megasphaera) between the food secure (FS) and food insecure (FI) student cohorts?*
2.  **Metabolomic Trends (Question 2):** *Which specific metabolites related to energy transfer and gut-brain-axis communication show the highest variation between the two groups?*
3.  **Pattern Recognition (Question 3):** *What overall patterns emerge when correlating a student's 30-day food access security tier with their recorded biological diversity?*

---

## 🎛️ Analysis Artifacts Generated
*   **AI-Generated Analysis Table:** Commanded the assistant to build a structured matrix synthesizing complex row data, clearly splitting microbial markers by food security status for fast comparison.
*   **Verification Strategy:** Evaluated the AI's conclusions against the dataset's baseline scientific findings to test whether the foundational transformer model accurately flagged significant data points (like elevated picolinic acid) without experiencing mathematical hallucinations.

## 🧠 AI Practitioner Skills Demonstrated
*   **Complex Data Ingestion:** Successfully utilized AI workflows to distill highly technical scientific measurements (16S rRNA sequencing and mass spectrometry outputs) into accessible summaries.
*   **Analytical Evaluation:** Evaluated generated matrices to ensure the AI maintained structural integrity, mapping the correct biological metrics to the correct student groupings.
*   **Responsible AI Guardrails:** Practiced working with anonymized health and demographic datasets, focusing on identifying broad statistical health trends while protecting data integrity.
