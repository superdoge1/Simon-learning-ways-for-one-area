---
name: learn-domain-simon
description: Build learning plans for any specific field using the Simon learning method: first ask the user what output language they want, then ask what domain they want to learn and capture their learner profile, then create an interactive dependency-aware knowledge map with hover resource cards, chunked learning path, layered quiz practice, deliverable-based projects, weekly/monthly one-page compression reviews, and week-by-week learning resources. Use when the user wants to learn a domain systematically, build a study roadmap, decompose knowledge into small chunks, make a visual learning map, or find staged GitHub/video/book/course resources for a learning topic.
---

# Learn Domain Simon

## Workflow

Always collect the output language before producing the plan. Then collect the learning field and learner profile.

1. Ask: "你希望学习方案使用什么语言输出？例如：中文、English、日本語、双语。"
2. Ask: "你想学习的具体领域是什么？例如：大模型应用开发、量化交易、产品经理、分布式系统、心理学。"
3. Collect a lightweight learner profile before planning when it is missing:
   - Current level or background.
   - Desired outcome or use case.
   - Weekly time budget.
   - Preferred style: theory-first, practice-first, or balanced.
4. If the field is too broad, ask one narrowing question before planning. Broad examples include "AI", "编程", "商业", "数学", and "设计".
5. If the user already supplied enough context in the same request, do not ask again; state reasonable assumptions instead.
6. Output the complete plan in the selected language. If no language is provided after asking, default to Chinese and state that assumption.
7. Read `references/learning-framework.md` before designing the learning flow.
8. Read `references/visual-knowledge-map.md` before designing the visual map.
9. Read `references/github-resource-rubric.md` before selecting learning resources.

## Required Output

Produce a structured learning plan with these sections:

1. `学习目标与边界`
   - State the selected output language, learner profile, expected outcome, prerequisites, weekly time budget, learning style, and what is intentionally out of scope.
   - If prerequisites are unknown, assume a motivated beginner and state that assumption.

2. `交互式核心概念知识地图`
   - Prefer an interactive HTML/SVG knowledge map rather than Mermaid mindmap.
   - Use `assets/interactive-knowledge-map-template.html` as the starting point when creating an artifact.
   - Use a wide dark canvas, color-coded stage nodes, visible dependency edges, resource cover thumbnails, and hover/focus resource cards, following `references/visual-knowledge-map.md`.
   - Attach recommended code repositories, official docs, videos, books, or courses to the relevant concept node.
   - If file creation is not appropriate, output a structured map specification with nodes, edges, stage labels, weekly order, and per-node resources.
   - Do not require JPG export.

3. `组块化学习路径`
   - Split the field into small chunks.
   - For each chunk, include:
     - `周次`: the week or sequence slot for this chunk.
     - `知识传授`: the key idea in concise teaching language.
     - `分层测验`: recall, explanation, transfer, and counterexample questions.
     - `可交付实践`: one concrete artifact such as a notebook, demo, case analysis, code repository, decision memo, reading card, diagram, or mini-project.
     - `本周资源`: staged resources matched to this chunk, including repositories, documentation, videos, books, or courses when verified.
     - `完成标准`: observable evidence that the chunk is learned and the artifact is usable.

4. `综合项目`
   - Design one final project that combines the most important chunks.
   - Include required deliverables, evaluation criteria, and optional stretch goals.

5. `周复盘：一页纸压缩`
   - Provide a reusable weekly one-page template.
   - Include concepts, examples, mistakes, questions, deliverables, and next actions.

6. `月复盘：组块打包`
   - Provide a monthly synthesis template that compresses learned chunks into higher-level modules.
   - Include "可复用模型", "个人知识地图变化", and "下月迁移练习".

7. `按周学习资源索引`
   - Search GitHub and the web for current resources relevant to each week.
   - Include code repositories, official documentation, videos, books, courses, and reference tools when verified.
   - Group resources by week and by map node, not only in a final undifferentiated list.
   - For each resource, include link, type, why it is valuable, best learning stage, how to study it, and the deliverable it supports.
   - If live search is unavailable, say so and provide executable search queries for each week.

## Resource Search Requirement

Prefer current, source-attributed results. Use available web/search tools when possible. Query patterns:

- `site:github.com <field> roadmap`
- `site:github.com <field> awesome`
- `site:github.com <field> tutorial`
- `site:github.com <field> examples`
- `site:github.com <field> course`
- `<field> official docs`
- `<field> beginner course video`
- `<field> recommended books`

Do not invent repository, video, book, or course URLs. If a URL cannot be verified, present it as a search query rather than a link.

## Link Reference

The user requested that the method also consider this source where possible:

`http://xhslink.com/o/9AYTyZ13uox`

If the source content is available from user-provided text, screenshots, or accessible browsing, incorporate the relevant learning-process details. If it is inaccessible, state briefly that the plan follows the user-provided Simon-method requirements instead.
