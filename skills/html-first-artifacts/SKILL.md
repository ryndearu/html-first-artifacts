---
name: html-first-artifacts
description: 'Create standalone HTML-first artifacts for planning, code review, prototyping, reports, research, learning, and throwaway editing tools. Use when asked to generate a rich single-file HTML document with embedded CSS/JS, interactive controls, export loops, visual diagrams, or visually dense shareable reports.'
---

# Agent Skill: HTML-First Artifacts

**Objective:** Replace standard Markdown outputs with highly readable, visually dense, interactive, and shareable single-file HTML documents.

## Core Operating Principles

When invoked to plan, review code, prototype, report, or build interfaces, you will bypass standard Markdown and generate a comprehensive HTML file.

* **Maximize Information Density:** Use standard HTML tags, CSS for styling, SVG for illustrations, and JavaScript for interactions.
* **Ensure Visual Clarity:** Organize documents logically using tabs, visual hierarchies, and responsive layouts for cross-device readability.
* **Enable Portability:** Produce standalone HTML files (embedding CSS and JS directly) so the user can easily share them via a simple link or file drop.
* **Contextual Ingestion:** Utilize all available context (file systems, git history, codebase) to inform the content of the HTML artifact.

## Implementation Protocols by Use Case

Execute the following patterns based on the user's request:

### 1. Specs, Planning, and Exploration
* **Action:** Create a rich canvas for brainstorming and planning.
* **Format:** Grid layouts for side-by-side comparisons of different approaches.
* **Content:** Include visual mockups, CSS-styled data flow diagrams, and embedded code snippets. Explicitly label the tradeoffs for each option.

### 2. Code Review and Understanding
* **Action:** Build visual aides for Pull Requests or complex codebase topics.
* **Format:** Render visual diffs with inline margin annotations.
* **Content:** Color-code findings by severity (e.g., red for critical, yellow for warnings). Use SVGs to draw system flowcharts (like streaming or backpressure logic) to explain complex code.

### 3. Design and Prototypes
* **Action:** Generate interactive, functional sketches of UI components.
* **Format:** Working HTML/CSS/JS prototypes (e.g., a checkout button with a play animation).
* **Content:** Include interactive UI controls (sliders, knobs, toggles) so the user can tune parameters (like animation timing or colors).
* **Required Element:** Include a "Copy Parameters" button to easily extract the user's tweaked settings.

### 4. Reports, Research, and Learning
* **Action:** Synthesize broad context into accessible explainers.
* **Format:** Long-form HTML documents, interactive explainers, or presentation decks.
* **Content:** Use SVGs for technical diagrams (e.g., token-bucket flows). Annotate 3–4 key code snippets, and always conclude with a styled "Gotchas" or "Summary" section optimized for a single read-through.

### 5. Custom Editing Interfaces (Throwaway Editors)
* **Action:** Build single-use, purpose-built HTML tools for specific data tasks (e.g., triaging tickets, editing feature flags, tuning prompts).
* **Format:** Interactive dashboards with features like drag-and-drop columns (Now/Next/Later), form-based editors with dependency warnings, or side-by-side prompt preview windows.
* **Required Element (The Export Loop):** You **must** include an export function. Add a functional button (e.g., "Copy as JSON", "Copy as Markdown", or "Copy Diff") that serializes the user's UI actions back into a text format they can paste back into their workflow.

## Technical Constraints for HTML Generation
* **No ASCII/Unicode Art:** Never use ASCII or Unicode characters for diagrams or color estimations. Always use SVGs and CSS background colors.
* **Single-File Output:** Embed all CSS within `<style>` tags and JavaScript within `<script>` tags to ensure the file can be shared and opened without missing assets.
* **Readability Over Brevity:** Do not artificially limit token usage if it sacrifices the visual layout. A long, well-structured HTML file is strictly preferred over a dense, unreadable Markdown file.
