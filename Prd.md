# AURA — Personality Audit Game
### Product Requirements Document (PRD)
> **Status:** Trial / Exploratory · **Version:** v1.0 · **Date:** June 2026

---

## Overview

| Field | Detail |
|---|---|
| **Product Name** | AURA |
| **Type** | Web-based Single-Page Application (SPA) |
| **Target Users** | Indian college students, ages 18–23 |
| **Primary Platform** | Mobile browser |
| **Secondary Platform** | Desktop browser |
| **Tech Stack** | HTML · CSS · Vanilla JS — single file, no backend |

---

## Problem Statement

College students are highly self-curious, but existing personality tools (MBTI, 16Personalities) feel **foreign, clinical, and unrelatable**. There is no personality or self-awareness product built specifically for the **Indian college experience** — with relevant scenarios and a result format that feels worth sharing.

---

## Goal

Build a **gamified self-awareness quiz** that:
- Feels fun and quick to answer
- Produces a meaningful, personalised result
- Is **highly shareable** within college communities — starting with Sentra's network

---

## User Flow

```
Intro Screen → Name Input → 100 Questions (5 categories × 20) → Score Calculation → Results Reveal → Share / Retake
```

---

## Screen Breakdown

### 1. Intro Screen
- AURA logo + tagline
- Animated background
- Single CTA button: **Start**

---

### 2. Name Screen
- Free-text input for the user's name
- Name is used for personalisation on the results screen (e.g. *"Aashay, your AURA score is…"*)
- **Continue** button to proceed

---

### 3. Question Screen
- Progress bar showing current question (e.g. *1 of 100*)
- Subtle category label (optional display)
- Short, scenario-based question text
- **4 tappable answer options**
- Auto-advances after selection with a highlight animation
- **No back button** — intentional design choice to reduce overthinking

---

### 4. Results Screen

| Element | Description |
|---|---|
| **Personalised heading** | Name-based (e.g. *"Aashay, your AURA score is…"*) |
| **AURA Score** | 0–100, shown with a count-up animation |
| **Personality Type** | Label + 2-line description |
| **5 Dimension Bars** | Animated fill for each category score |
| **Strengths & Blind Spot** | 2 strengths + 1 blind spot |
| **Share Card** | Auto-generated shareable card |
| **Retake Button** | Resets and restarts the quiz |

---

## Scoring Logic

| Step | Formula |
|---|---|
| Per answer | Gives **0–4 points** to its category |
| Category score | `(sum of answers / 80) × 100` |
| AURA Score | Average of all 5 category scores |
| Personality label | Determined by the **top 2 highest-scoring** categories |

> **5 Categories × 20 Questions = 100 Questions total**
> Max points per category = 20 questions × 4 points = **80 points**

---

## Design System

| Token | Value |
|---|---|
| **Background** | `#0a0a0a` |
| **Primary Accent** | `#7C3AED` (purple) or `#00F5FF` (cyan) |
| **Primary Text** | `#FFFFFF` |
| **Secondary Text** | `#888888` |
| **Card Background** | `#111111` |
| **Font** | Inter or system sans-serif |
| **Animations** | Fade + slide · 300ms transitions |
| **Layout** | Mobile-first · max-width 430px |

---

## Success Metrics

| Metric | Target |
|---|---|
| Completion rate | > 60% |
| Share rate | > 30% |
| Average session time | 8–12 minutes |
| Organic distribution | WhatsApp groups & Instagram Stories |

---

## Out of Scope — v1

The following features are **explicitly excluded** from the first version:

- ❌ No login or user accounts
- ❌ No data storage or backend
- ❌ No leaderboard *(planned for v2)*
- ❌ No AI-generated personalised analysis *(planned for v2)*

---

## Notes

> This is a **trial / exploratory PRD** for the initial version of AURA. The product is intended to validate the core concept — a relatable, gamified personality quiz for Indian college students — before investing in more advanced features in subsequent versions.
