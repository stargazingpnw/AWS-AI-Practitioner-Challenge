# Project 1: NutriWellness Personal Health Coach

An AI-powered morning wellness coach built on Amazon PartyRock for the AWS AI Practitioner Challenge (Udacity).

## Project Overview

NutriWellness is a single-session application designed to reduce health-related information overload and decision fatigue. Rather than acting as a traditional historical tracker, the app is meant to be used first thing in the morning: it takes a user's physical baselines, yesterday's behavior (meals and steps), and today's mood, and generates focused, immediately executable guidance for the next 24 hours.

## The Problem and the Pivot

**The original vision** called for a full tracking app with user authentication, persistent historical logs, multi-page conditional flows, and external nutrition database lookups.

**The constraint:** PartyRock is built for single-session generative workflows. It does not support user logins, data persistence, multi-page routing, or external API access.

**The pivot:** Rather than abandoning the project, I redesigned it around PartyRock's actual strengths.

1. **From tracking to coaching** — Swapped long-term historical tracking for a focused "morning evaluation" framework: reflect on yesterday, plan today.
2. **Reducing information overload** — Merged two overlapping widgets (a forward-looking nutrition plan and a separate yesterday's-food analysis) into one unified widget, and constrained every AI output to two to three actionable items rather than long-form explanations.
3. **Cross-widget consistency** — Refined prompts to keep outputs aligned across widgets, for example ensuring the step count referenced in the fitness widget matched the step goal referenced in the progress widget.

## How It Works

### User Input Panel

- **Body metrics:** Height (inches), current weight (lbs), age, gender
- **Detailed measurements:** Neck, chest, bicep, waist, hips, thigh, calf
- **Yesterday's behavior:** Food log (ingredients and measurements) and step count
- **Current state:** Morning mood, selected from nine emotional states
- **Safety inputs:** Dietary category (six types, from carnivore to vegan) and an open-text food allergies field

### AI Output Widgets

- **BMI Analysis** — BMI calculation with visible math, health category, and one motivating insight
- **Nutrition Analysis and Plan** — Scores yesterday's food log (1–10), connects it to today's mood, sets today's calorie and macro targets, and suggests three simple meals
- **Fitness Plan for Today** — Three to four specific exercises, a step goal calibrated to yesterday's activity, and one recovery tip
- **Mood Support for Today** — Acknowledges the user's current mood and names three mood-supportive foods plus one non-food strategy
- **Progress Guidance for Today** — Three metrics to track, three priority actions, and one motivating closing line

## What This Demonstrates

- **Guardrail design for safety-critical accuracy** — Added explicit dietary and allergy enforcement across every food-related widget after catching the AI suggest a non-compliant food (chicken to a vegetarian user) during testing. This required reinforcing the constraint in each widget individually, since each one generates independently.
- **Output constraint engineering** — Deliberately limited every widget's output length to reduce cognitive overwhelm, prioritizing a small number of genuinely actionable items over comprehensive but unusable detail.
- **Architecture pivoting under real constraints** — Redesigned the entire app concept around what the platform could actually do, rather than forcing an incompatible vision onto an incompatible tool.
- **Structured input over open-ended conversation** — Unlike a general chatbot, which can lead a user down unfocused tangents, the app uses targeted data intake to produce consistent, actionable output every time.

## Try It

[Run NutriWellness Personal Health Coach on PartyRock](https://partyrock.aws/u/stargazingpnw/D5G7gOBly/NutriWellness-Personal-Health-Coach)

Note: PartyRock does not save session state. Copy, screenshot, or paste your results into your own notes if you want to keep them.
