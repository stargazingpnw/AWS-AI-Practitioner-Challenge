# Project 2: Analyze Data Using AI with PartyRock

## Project Objective

Use PartyRock's Analyze Data feature (Whiskers) to upload a dataset, ask analytical questions, generate an AI-built analysis table, and critically evaluate the accuracy and usefulness of the resulting insights.

## Dataset

**Association of Food Insecurity on Gut Microbiome and Metabolome Profiles in a Diverse College-Based Sample**
Source: [Mendeley Data, Arizona State University (Mohr et al., 2022)](https://data.mendeley.com/datasets/s4ydf6kb8y/1)

The dataset compares fecal microbiome and metabolome profiles of racially and ethnically diverse first-year college students experiencing different levels of food access. Two files were used: a metadata file (demographics, lifestyle factors, nutritional intake) and a metabolome file (amino acids, organic acids, fatty acids, and energy metabolites).

## Questions Asked

**1. How do profiles of key energy metabolites (amino acids and fatty acids) vary or correlate with students' actual caloric and macronutrient intake?**

Findings showed weak overall correlations between dietary intake and metabolite levels. Acetylcarnitine showed the strongest relationship with total calories (r = 0.30) and total fat (r = 0.26). Branched-chain amino acids showed near-zero correlation with protein intake (r = -0.09 to 0.01), despite being dietary amino acids. This suggests metabolic regulation and individual variation dominate over short-term dietary tracking, and that metabolite levels likely reflect longer-term metabolic patterns rather than recent intake.

**2. What trends emerge when analyzing nutritional intake alongside lifestyle factors like screen time, physical activity, and dorm residency?**

Dorm 2 students showed healthier patterns across the board: higher caloric and protein intake, more physical activity, and less screen time than Dorm 1. High screen time correlated with higher sugar intake (r = 0.19) and higher BMI (r = 0.22), but had no relationship with physical activity (r = -0.007). The most notable finding was a paradoxical inverse relationship between caloric intake and BMI (r = -0.17): underweight students consumed the most calories but had the least activity and most screen time, while normal-weight students showed the best balance of moderate intake, high activity, and low screen time. This points to lifestyle context mattering more than raw caloric intake alone, and raises the possibility of underreporting bias among higher-BMI students.

**3. How do physiological categories like BMI bracket, age, and gender map against variances in organic acids and amino acid metabolites?**

Female students showed significantly elevated lactate (+128%), pyroglutamate (+29%), and BCAAs (+7%) compared to male students, despite having 9% lower average BMI, suggesting more efficient metabolic processing. Underweight students showed signs of protein catabolism (highest BCAAs, highest lactate) alongside impaired TCA cycle function (lowest organic acids), while overweight students showed signs of oxidative stress (highest pyroglutamate and tryptophan). BMI correlated negatively with phenylalanine (r = -0.21) and BCAAs (r = -0.14), which runs counter to typical obesity research where BCAAs are usually elevated, suggesting this younger, more active cohort behaves differently than sedentary populations typically studied.

## Generated Analysis Table

Whiskers produced a combined table integrating demographics, lifestyle factors, nutritional intake, and full metabolomic profiles per student, sorted by BMI then age and gender. This allowed cross-referencing of physiological and lifestyle variables against metabolite abundance in a single view.

## Evaluation of AI-Generated Insights

The AI's statistical outputs (correlation coefficients, percentage differences) were internally consistent and the interpretations offered plausible, evidence-grounded explanations rather than overstating causation. Notably, the AI appropriately flagged its own paradoxical findings (the inverse BMI-calorie relationship, the inverse BMI-BCAA relationship) rather than glossing over results that contradicted expectations, and offered reasonable alternative explanations such as underreporting bias and cohort-specific metabolic dynamics.

The most valuable aspect of this exercise was using the AI as a hypothesis-generation tool: the correlations and patterns it surfaced are not conclusions on their own, but they identify exactly where a real researcher would want to dig deeper, such as the unexpected inverse relationship between BCAAs and BMI in this cohort.

## Key Insights

1. **The body tightly regulates branched-chain amino acid (BCAA) levels regardless of protein intake.** Despite BCAAs being dietary amino acids, they showed near-zero correlation with protein consumption, suggesting metabolic regulation dominates over short-term dietary tracking.
2. **Higher screen time correlates with higher sugar intake**, possibly influenced by emotional states tied to screen content or by passive snacking behavior during screen use.
3. **Dorm 2 students showed both higher protein intake and higher physical activity**, which the AI interpreted as a likely sign of better dining or recreational options in that dorm, an inference that goes beyond raw statistics into plausible real-world reasoning.

## Evaluation of AI Reasoning

Beyond reporting correlations, the AI's analysis showed an ability to apply real-world logic to its findings rather than only restating the numbers. For example, when it noticed Dorm 2 students had both higher protein intake and higher activity levels, it proposed that Dorm 2 likely has healthier food options available, a reasonable inferential leap rather than a simple statistical restatement. This kind of grounded reasoning, drawing a plausible causal hypothesis from a correlation, is what distinguishes a useful analysis from a purely mechanical one, and it's a meaningfully more reliable output than what a general-purpose LLM would produce without structured data to reason from directly.

## Key Takeaway

Lifestyle context (activity level, screen time, dorm environment) appeared to matter more than absolute caloric intake alone in determining health outcomes in this cohort, and metabolomic profiles reflect longer-term physiological regulation more than they reflect any single day's dietary intake.
