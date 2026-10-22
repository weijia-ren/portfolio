---
title: "Family Quest — Gamified Kids Task & Homework Tracker"
short_title: "Family Quest"
short_desc: "A gamified, iPad-optimized PWA for families to manage daily homework, music practice, and star rewards."
date: 2026-10-15
draft: false
tags: ["EdTech", "Behavioral Design", "Gamification", "PWA", "iPad-Optimized", "JavaScript"]
categories: ["Web Applications"]
icon: "images/family-quest-icon.svg"
appUrl: "https://family-quest-kids.netlify.app"
githubUrl: "https://github.com/weijia-ren/family-quest"
status: "Live PWA"
weight: 2
summary: "A gamified, iPad-optimized Progressive Web App designed for families to manage daily homework, music practice, routines, and star rewards. Features a 2-step review loop, reward bank, and interactive 30-day habit analytics."
---

<div class="project-hero-card">
  <div class="project-hero-badges">
    <span class="badge badge-live">Live Production App</span>
    <span class="badge">iPad & Tablet PWA</span>
    <span class="badge">Behavioral Gamification</span>
  </div>
  <p class="project-tagline"><strong>Turn daily homework and practice into an engaging family adventure.</strong></p>
  <div class="project-actions">
    <a href="https://family-quest-kids.netlify.app" target="_blank" rel="noopener" class="btn btn-primary">Launch Live App ↗</a>
    <a href="https://github.com/weijia-ren/family-quest" target="_blank" rel="noopener" class="btn btn-secondary">GitHub Repo ↗</a>
  </div>
</div>

## The Problem

Managing children's daily routines, school homework, and instrumental practice is one of the most persistent sources of daily friction for families:
1. **Nagging Fatigue**: Constant verbal reminders lead to frustration and resistance, eroding child autonomy.
2. **Disconnected Incentives**: Traditional paper sticker charts are easily forgotten, lack immediate gratification, and do not scale as children grow.
3. **Lack of Visibility**: Parents lack a consolidated view of consistency trends over time to identify which routines need structural support.

## Product Rationale & Behavioral UX

**Family Quest** is designed around positive reinforcement, behavioral commitment loops, and shared parental oversight:

- **2-Step Review Loop**:
  - *Kid Action*: The child completes an assignment or practice session and taps **"🚀 Mark Ready for Review"** with an optional note or photo.
  - *Parent Action*: The parent opens the **Parent Review Deck**, inspects the submission, and taps **"Approve & Award ⭐ Points"** (triggering celebratory confetti) or returns it with helpful guidance via **"Needs Correction 🔄"**.
- **Star Points Bank & Reward Store**:
  - Kids earn stars for verified accomplishments.
  - A customizable **Reward Store** lets children budget and redeem points for meaningful real-world privileges (e.g., choosing Friday movie night, extra outdoor play, or book purchases).
- **Streak & Consistency Mechanics**:
  - Daily streak counters (`🔥 Streak`) cultivate intrinsic motivation without punitive all-or-nothing penalties.
- **30-Day Habit & Progress Analytics**:
  - Features an interactive **30-day heatmap** in the Parent deck. Tapping any calendar block displays completed assignments, earned points, and category breakdowns across *School Homework*, *Music/Reading Practice*, and *Household Chores*.

## Architecture & Technical Highlights

| Architectural Feature | Details |
| :--- | :--- |
| **PWA & Offline Capability** | Configured with Web App Manifest and Service Worker for full-screen standalone installation on iPad and iPhone via Safari "Add to Home Screen". |
| **Touch-First Design** | High-contrast, playful UI optimized for small hands and tablet interactions with responsive touch states. |
| **Family Privacy & Security** | Local client-side storage architecture with optional 4-digit Parent PIN protection for reward settings. |
| **Edge Hosting** | Continuous automated deployment via Netlify Edge CDN. |

## Technology Stack

- **Frontend**: Semantic HTML5, CSS3 Custom Properties (responsive mobile & tablet layout), Modern ES6+ JavaScript.
- **Progressive Web App**: Custom Web App Manifest (`manifest.json`) and caching Service Worker (`service-worker.js`).
- **Hosting & CI/CD**: Netlify.

---

<div class="project-footer-cta">
  <h3>Try Family Quest</h3>
  <p>The app is live and fully functional on desktop, iPad, and mobile browsers.</p>
  <a href="https://family-quest-kids.netlify.app" target="_blank" rel="noopener" class="btn btn-primary">Open Family Quest ↗</a>
</div>
