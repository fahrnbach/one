---
title: "Getting Started with SparkDocs"
description: "Instructions for GPTs and humans alike to understand the SparkDocs vision, workflow, and prerequisites."
tags: ["meta", "workflow", "onboarding", "sparkdocs", "gpt", "process"]
---
# Overview

This document is a foundational primer for anyone — GPT or human — aiming to contribute to the SparkDocs knowledge system. It explains the broader vision, lays out our structured documentation process, and details the specific formatting and intent behind each entry. Think of it as your onboarding pass into the **fahrnbach.one universe** — an interconnected system of public documentation, project blueprints, and digital storytelling.

Whether you're here to generate content, provide feedback, or build tools based on this architecture, this file ensures we’re speaking the same language and following the same rhythms.

[[[
  
Intent: To establish a consistent onboarding experience for contributors to the SparkDocs ecosystem, particularly GPT agents being prompted to generate new or updated articles.

Process:
1. **Understand the Mission**: SparkDocs isn't just documentation. It's a **manifesto**, a **blueprint**, and a **living archive**. It supports the development and ideation of the entire *fahrnbach.one* system — from AI concepts and creative tooling to infrastructure and outreach.

2. **Use the Standard Format**: Every SparkDoc entry follows a strict markdown format with structured frontmatter and an `Overview` heading, followed by an embedded **meta-process block** (this block), which lives between triple square brackets. Never include `[[[` or `]]]` in output outside the process section. The format should always be respected to ensure compatibility and clarity.

3. **Follow the Meta-Process**:
   - **PreCog**: Chat with a GPT to identify the knowledge domain, gaps, or design goals behind a new document.
   - **Generate**: Draft the initial document using this template.
   - **Score**: The user assigns an **Alignment** (how well this matches intent) and **Confidence** (how technically or conceptually solid it feels) score manually.
   - **MetaCog**: Revisit articles, refine language, and improve structure.
   - **Repeat**: Each document may undergo several iterations. Increment the `Iteration` number after each major change.

4. **Tag Thoughtfully**: Tags should be short, lowercase, and describe key concepts in the doc (e.g., `"ai"`, `"graphQL"`, `"meta"`, `"project-management"`). These support better filtering and future features like tag-based search or cross-linking.

5. **Prerequisites for GPTs**:
   - Must be capable of interpreting markdown and YAML-style frontmatter.
   - Must understand and maintain structural consistency in all output.
   - Must refrain from “summarizing” or adding commentary outside the markdown block unless asked.
   - Must use `"double quotes"` for frontmatter items, and comma-separated arrays for tags.
   - Must not escape characters or wrap in triple backticks unless formatting for markdown is requested.

6. **Prompting GPT**:
   - To trigger the template automatically, use the reserved keyword:  
     `<<<sparkdoc>>>`
   - GPT should respond with a complete `.md` file using the format above and generate all missing content (title, tags, description, overview, meta-process, and initial scores).

7. **Human Involvement**: This system is designed to **augment**, not replace, human judgment. Final scores, project relevance, and cross-document linking are determined by the human overseer.

8. **Storage & Use**: All documents are stored under the `spark-docs` project and auto-linked via the sidebar config. The content may eventually serve as:
   - Source-of-truth documentation
   - Seed material for future AI assistants
   - Content for a public knowledgebase

]]]

For more information on WHY these docs exist, visit `/meta/overview/overview`.

Iteration: 0  
Alignment: 10  
Confidence: 10
