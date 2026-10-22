---
title: "Duplicate Tab Closer — Chrome Extension"
short_title: "Duplicate Tab Closer"
short_desc: "A lightweight Chrome extension that automatically detects and closes duplicate tabs to save RAM and streamline workflows."
date: 2026-10-10
draft: false
tags: ["Chrome Extension", "Productivity", "Manifest V3", "Browser Tool", "JavaScript"]
categories: ["Browser Extensions"]
icon: "images/duplicate-tab-closer-icon.svg"
driveUrl: "https://drive.google.com/drive/folders/1oC6DV8RKJDyfto1l9Wi1tOZInnJrI3Iz"
status: "Extension"
weight: 3
summary: "A productivity-focused Chrome extension designed to combat tab overload. It intelligently identifies duplicate URLs across open browser windows in real time, automatically closing redundant tabs to reduce memory consumption and cognitive fatigue."
---

<div class="project-hero-card">
  <div class="project-hero-badges">
    <span class="badge badge-live">Chrome Extension</span>
    <span class="badge">Manifest V3</span>
    <span class="badge">Local & Private</span>
  </div>
  <p class="project-tagline"><strong>Never drown in duplicate tabs again. Clean, fast, and automated.</strong></p>
  <div class="project-actions">
    <a href="https://drive.google.com/drive/folders/1oC6DV8RKJDyfto1l9Wi1tOZInnJrI3Iz" target="_blank" rel="noopener" class="btn btn-primary">Download from Google Drive ↗</a>
  </div>
</div>

## The Problem

Knowledge workers, researchers, and developers constantly suffer from **tab overload**:
1. **Accidental Duplicate Sprawl**: Clicking repeated links from Slack, emails, research documents, or search engines frequently opens 4–5 identical copies of the same article, ticket, or dashboard without realizing it.
2. **Browser Performance Degradation**: Every open duplicate tab silently consumes substantial RAM and CPU overhead, draining battery life and slowing down multitasking.
3. **Cognitive Overload**: Searching through a sea of tiny, unreadable tab headers wastes mental energy and disrupts deep focus.

## The Solution

**Duplicate Tab Closer** is an unobtrusive, background Chrome extension that automatically keeps your browser organized:

- **Instant Duplicate Detection**: Monitors newly opened or refreshed tabs via Chrome's reactive tab listeners.
- **Smart URL Normalization**: Compares URLs intelligently by stripping superficial query parameters (e.g., Google tracking tags, UTM codes, session fragments) so duplicate pages with slightly different query strings are correctly identified.
- **Preserves Active & Pinned Tabs**: Protects currently focused tabs, pinned tabs, and forms in progress, ensuring zero accidental loss of work.
- **One-Click Manual Clean-Up**: Provides a quick popup action to scan and deduplicate all open tabs across every browser window on demand.

## Architecture & Privacy

Like all tools in this portfolio, **Duplicate Tab Closer** is architected with strict privacy guarantees:

| Pillar | Implementation Details |
| :--- | :--- |
| **Permissions** | Strictly confined to `tabs` and `storage` APIs required for tab management. |
| **Local-Only Execution** | All tab evaluations happen 100% inside your local Chrome runtime. |
| **Zero Telemetry** | No analytics SDKs, no external network requests, and zero tracking scripts. |
| **Manifest V3 Compliant** | Built using Chrome's modern, power-efficient background service worker standard. |

## How to Install (Developer Mode)

1. Download the extension files from the [Google Drive folder](https://drive.google.com/drive/folders/1oC6DV8RKJDyfto1l9Wi1tOZInnJrI3Iz).
2. Open Google Chrome and navigate to `chrome://extensions/` in your address bar.
3. Toggle on **Developer mode** in the top right corner.
4. Click **Load unpacked** and select the unzipped `Dedup_tab` folder.
5. The extension is now active and will automatically keep your browsing sessions clean!

---

<div class="project-footer-cta">
  <h3>Get the Extension</h3>
  <p>Access the source files and package directly via Google Drive.</p>
  <a href="https://drive.google.com/drive/folders/1oC6DV8RKJDyfto1l9Wi1tOZInnJrI3Iz" target="_blank" rel="noopener" class="btn btn-primary">Open Google Drive Folder ↗</a>
</div>
