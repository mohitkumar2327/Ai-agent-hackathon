# EduPath — Personalized Learning & Skill-Gap Agent

**Live demo:** https://claude.ai/artifact/2M6XwPSHzDG7Zn21jh11Mf

## Problem
Learners know their target role but not the exact path to it — resources are scattered and most people follow a generic curriculum regardless of what they already know.

## Solution
EduPath takes a target role and the learner's current skills (typed in, or pulled automatically from pasted resume/project text), computes the gap against that role's required skillset, and turns it into a week-by-week trail of waypoints. Each waypoint carries two curated resources and a hands-on practice task. As the learner checks items off, the route, progress bar, and stats recompute live. A natural-language panel answers questions like "what should I learn next" or "where am I on SQL" by reasoning over the learner's current state rather than canned text.

## How it maps to the brief
- **Skill/goal intake:** role selector + free-text skills + resume paste, matched against a 23-skill taxonomy across 6 roles
- **Gap analysis:** role requirements minus detected current skills
- **Structured learning objectives + resources:** each gap skill expands into resources and a task
- **Weekly plan:** gaps are auto-grouped into two-per-week waypoints
- **Dynamic tracking:** checklist state drives skill status (not started → in progress → mastered) and persists across sessions
- **Progress reporting:** live counts of acquired / in-progress / remaining skills, plus auto-generated next steps
- **Natural-language Q&A:** rule-based interpreter answers questions about gaps, current week, and specific skills

## Tech
Single self-contained HTML/CSS/JS file — no backend, no build step, no API key required. All state lives in the browser (localStorage) for the demo. In a full build, the skill taxonomy would move to a database, resume parsing would use an LLM instead of keyword matching, and the Q&A panel would call the Claude API for open-ended reasoning instead of pattern matching.

## Run it
Open `index.html` in any browser, or visit the live link above.
