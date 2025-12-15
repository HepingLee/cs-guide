# Copilot Instructions for PPT Project

## Project Overview
This project is a single-page, interactive HTML presentation titled "CS Major Level Up Guide" (CS专业打怪升级指南). It uses a gamified theme to guide Computer Science students through their studies.

## Tech Stack
- **Core**: HTML5, Vanilla JavaScript.
- **Styling**: Tailwind CSS (via CDN: `https://cdn.tailwindcss.com`).
- **Visualization**: Chart.js (via CDN: `https://cdnjs.cloudflare.com/ajax/libs/Chart.js/3.9.1/chart.min.js`).
- **Fonts**: Google Fonts (Noto Sans SC, Fira Code).

## Architecture & Patterns
- **Single File Structure**: All code (HTML, CSS, JS) resides in `ppt.html`.
- **CDN Dependency**: Libraries are loaded via `<script src="...">` in `<head>`. No local `node_modules` or build steps.
- **Design System**:
  - **Theme**: Solarized Light (Modified).
  - **Colors**: 
    - Background: `#fdf6e3` (Base)
    - Text: `#586e75` (Primary), `#93a1a1` (Secondary)
    - Accents: `#2aa198` (Cyan), `#d33682` (Magenta), `#268bd2` (Blue), `#dc322f` (Red/Warning), `#859900` (Green/Success).
  - **Typography**: `Noto Sans SC` for body text, `Fira Code` for code blocks.

## Development Workflow
- **Editing**: Edit `ppt.html` directly.
- **Preview**: Open `ppt.html` in a browser. **Note**: Requires active internet connection to load CDNs.
- **Debugging**: Use browser developer tools (Console/Network).

## Coding Conventions
- **HTML Structure**: 
  - Use semantic tags (`<section id="...">`, `<nav>`, `<footer>`).
  - Sections are linked via ID (e.g., `#profile`, `#skills`).
- **Styling**: 
  - Prefer Tailwind utility classes for layout and spacing.
  - Use `<style>` block only for specific overrides (scrollbars, chart containers, font imports).
- **JavaScript**: 
  - Keep logic simple and contained within the `<script>` tag at the bottom of `<body>`.
  - Use `document.addEventListener('DOMContentLoaded', ...)` for initialization.
- **Content Tone**: 
  - Maintain the "Gamification" metaphor (Level Up, Boss, XP, Inventory, Save Point).
  - Target Audience: CS Freshmen (friendly, encouraging, practical).

## Key Components
- **Charts**: 
  - `mathChart`: Radar chart showing subject relevance.
  - `examChart`: Horizontal bar chart for study prioritization.
  - **Constraint**: Chart containers must have explicit height/width styles for responsiveness.
- **Interactive Elements**: 
  - `fixBugBtn`: Toggles code block content and styles.
  - `scrollToSection`: Smooth scrolling navigation.
