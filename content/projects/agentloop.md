---
title: "AgentLoop — Real Estate Deal Communication & AI Summary Platform"
short_title: "AgentLoop"
short_desc: "A centralized client portal for real estate agents with live listing activity and automated AI weekly deal summaries."
date: 2026-08-25
draft: false
tags: ["Real Estate Tech", "AI Agent", "Client Portal", "Human-in-the-Loop", "UX Design"]
categories: ["AI & Web Applications"]
icon: "images/agentloop-icon.svg"
appUrl: "https://weijia-ren.github.io/agentloop-realestate/"
githubUrl: "https://github.com/weijia-ren/agentloop-realestate"
status: "Prototype"
weight: 3
summary: "A shared web platform for real estate agents and clients that centralizes active listing status, organizes milestone communication, and drafts weekly AI deal summaries for agent review."
---

<div class="project-hero-card">
  <div class="project-hero-badges">
    <span class="badge badge-live">Interactive Prototype</span>
    <span class="badge">Human-in-the-Loop AI</span>
    <span class="badge">Real Estate SaaS</span>
  </div>
  <p class="project-tagline"><strong>Stay in the loop on every deal.</strong></p>
  <div class="project-actions">
    <a href="https://weijia-ren.github.io/agentloop-realestate/" target="_blank" rel="noopener" class="btn btn-primary">Launch Live Prototype ↗</a>
    <a href="https://github.com/weijia-ren/agentloop-realestate" target="_blank" rel="noopener" class="btn btn-secondary">GitHub Repo ↗</a>
  </div>
</div>

## The Problem

Real estate transactions are stressful, multi-week negotiations where communication quickly degrades:
- **Scattered Communication**: Agents and clients exchange fragmented updates across texts, emails, phone calls, and messaging apps (WeChat, WhatsApp).
- **Client Anxiety**: Buyers and sellers frequently wonder: *"What is happening with my listing right now, and what comes next?"*
- **Agent Burden**: Top-performing agents spend hours each week manually drafting repetitive status updates instead of closing deals.

## The Solution

**AgentLoop** is a shared web application designed to eliminate transaction friction by providing a single source of truth for every active listing:

1. **Centralized Deal Dashboard**: Tracks showings, open house attendance, offers, appraisal status, and inspection contingencies in one live timeline.
2. **AI-Drafted Weekly Client Briefings**: An automated agent analyzes the past week’s MLS events, feedback logs, and price movements to generate a clear, professional client briefing.
3. **Human-in-the-Loop Approval**: The agent reviews, edits, and approves the AI-drafted report with one tap before it delivers to the client.

## Core Features

- **Active Listing Hub**: Real-time status indicators across key milestones (Active, Under Contract, Pending, Closed).
- **Multi-Channel Activity Logging**: Quick-entry forms for buyer feedback, agent private notes, and showing counts.
- **Weekly Summary Generator**: LLM-assisted report generation formatted for rapid client comprehension.
- **Client Portal View**: Clean, branded client-facing dashboard accessible without complex account hurdles.

## Product Thinking & Architecture

- **Information Hierarchy**: Prioritizes *"Current Status"* and *"Next Steps"* at the very top of the client view to immediately alleviate buyer/seller anxiety.
- **Agent Safeguards**: By enforcing an explicit agent review gate, AgentLoop avoids "hallucinated" or unauthorized client notifications common with unconstrained AI bots.
- **Tech Stack**: Lightweight frontend wireframe architecture deployed via GitHub Pages and modern static site generation.

---

<div class="project-footer-cta">
  <h3>Explore the Prototype</h3>
  <p>Test the interactive wireframe and review the full listing management flow.</p>
  <a href="https://weijia-ren.github.io/agentloop-realestate/" target="_blank" rel="noopener" class="btn btn-primary">Open AgentLoop Wireframe ↗</a>
</div>
