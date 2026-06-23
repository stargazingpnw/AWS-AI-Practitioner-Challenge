# NutriWellness Personal Health Coach

An interactive, AI-powered morning alignment coach built on **Amazon PartyRock** (leveraging Amazon Bedrock foundational models) for the **AWS AI & ML Scholars / AI Practitioner Challenge**.

## 📌 Project Overview
**NutriWellness Personal Health Coach** is a high-utility, single-session application designed to eliminate health-related information overload and decision fatigue. 

Instead of acting as a traditional, overwhelming historical tracker, this app is designed to be used **first thing in the morning**. It takes a user's objective physical baselines, yesterday's behaviors (meals and steps), and today's subjective mood to generate hyper-focused, bite-sized, and immediately executable targets for the next 24 hours.

## 💡 The Problem & The Pivot (Architecture Insights)
### ❌ The Core Challenge: Platform Constraints
The original vision for this project was a full-scale tracking app requiring user authentication, database persistence for long-term progress logs, multi-page flows, and external database API lookups. 

However, **Amazon PartyRock is built for single-session generative workflows** and does not support user logins, data persistence, multi-page routing, or external APIs. 

### 💡 The Solution: The "Morning Routine" Framework
Instead of scrapping the project, I pivoted the app's entire architecture to match PartyRock's core strengths:
1. **From Tracking to Coaching:** Swapped long-term data tracking for a hyper-focused "Morning Evaluation" framework. 
2. **Combating Information Overload:** Merged redundant widgets (Nutrition Plan + Food Analysis) into a single unified workspace. Ruthlessly constrained all AI outputs to **2–3 actionable bullets** so users can execute tasks without cognitive fatigue.
3. **Cross-Widget Consistency:** Fine-tuned prompts to prevent data friction (such as ensuring step counts match perfectly between fitness and progress modules).

---

## 🛠️ How It Works & Core Widgets

### 1. User Input Panel
*   **Body Metrics:** Height (Inches) and Current Weight (Lbs) number inputs for manual entry, plus age and gender baselines.
*   **Detailed Metrics:** Specific inputs for neck, chest, bicep, waist, hips, thigh, and calf measurements.
*   **Behavioral Recaps (Yesterday):** Text fields capturing exact ingredients/measurements eaten yesterday, along with yesterday's precise step count.
*   **Subjective State:** Single-select dropdown for current morning mood (9 distinct states including anxious, stressed, happy, sad, etc.).
*   **Safety Filters:** A multi-tier dietary preference selector (6 categories: *Carnivore, Carnivore-minus red meat, Pescatarian, Ovo-lacto vegetarian, Vegetarian, Vegan*) coupled with an open-text **Food Allergies** input.

### 2. Streamlined AI Output Modules (Amazon Bedrock)
*   **BMI Analysis:** Calculates exact BMI with visible step-by-step math, maps health status, and gives one motivating insight.
*   **Unified Nutrition Analysis & Plan:** Explicitly scores yesterday's food log (1-10 scale), bridges how those foods affected today's mood, defines today's exact macro/calorie targets, and outlines 3 simple meal suggestions.
*   **Fitness Plan for Today:** Prescribes 3-4 highly specific exercises, sets a daily step goal synchronized with your progress tracker, and offers one recovery tip.
*   **Mood Support for Today:** Validates morning emotional energy, naming exactly 3 mood-regulating foods and 1 lifestyle action.
*   **Progress Guidance for Today:** Delivers exactly 3 core metrics to watch, 3 priority actions for the day, and one closing motivational sign-off.

---

## 🧠 AWS AI & Prompt Engineering Concepts Demonstrated
*   **Strict Guardrail Logic & Safety Alignment:** Implemented highly rigid prompt constraint blocks across all nutrition, mood, and progress widgets to prevent severe AI hallucinations—such as suggesting chicken to vegetarians or dairy to users with listed allergies.
*   **Output Length Optimization:** Leveraged custom row-bounding and character limits within the prompt templates to optimize token efficiency and guarantee clear, text-walled UI boundaries.
*   **Multi-Modal Synthesis:** Showcases how foundational models can dynamically merge qualitative user feelings (mood strings) with quantitative data (inches, pounds, steps) into logical, daily directives.

---

## 🔗 Try It Out
[👉 Click Here to Run NutriWellness Personal Health Coach on PartyRock]([https://partyrock.aws/u/stargazingpnw/D5G7gOBly/NutriWellness-Personal-Health-Coach])

*Note: Because PartyRock does not save session states, you can safely paste your metrics, screenshot your daily plan, or copy/paste your customized targets to your personal notes app daily!*
