---
name: learn-domain-simon
description: Build learning plans for any specific field using the Simon learning method: first ask the user what output language they want, then ask what domain they want to learn and capture their learner profile, then create a dependency-aware knowledge map, chunked learning path, layered quiz practice, deliverable-based projects, weekly/monthly one-page compression reviews, and categorized high-value GitHub learning resources. Use when the user wants to learn a domain systematically, build a study roadmap, decompose knowledge into small chunks, or find strong GitHub repositories for a learning topic.
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
8. Read `references/github-resource-rubric.md` before selecting GitHub resources.

## Required Output

Produce a structured learning plan with these sections:

1. `学习目标与边界`
   - State the selected output language, learner profile, expected outcome, prerequisites, weekly time budget, learning style, and what is intentionally out of scope.
   - If prerequisites are unknown, assume a motivated beginner and state that assumption.

2. `核心概念知识地图`
   - Use Mermaid `mindmap` when the interface can render Mermaid.
   - Use an indented tree if Mermaid is unsuitable.
   - Show 3-6 first-level branches and enough second-level concepts to make the domain navigable.
   - Add recommended learning order and prerequisite links between major branches.
   - Mark concepts as `先修`, `核心`, or `进阶` when useful.

3. `组块化学习路径`
   - Split the field into small chunks.
   - For each chunk, include:
     - `知识传授`: the key idea in concise teaching language.
     - `分层测验`: recall, explanation, transfer, and counterexample questions.
     - `可交付实践`: one concrete artifact such as a notebook, demo, case analysis, code repository, decision memo, reading card, diagram, or mini-project.
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

7. `GitHub 高价值学习资源`
   - Search GitHub or the web for current repositories relevant to the field.
   - Categorize resources as `路线图类`, `课程类`, `项目实战类`, `awesome 清单类`, `官方实现类`, or `参考工具类`.
   - Rank links inside each category by learning value, not only popularity.
   - For each resource, include link, why it is valuable, best learning stage, and how to study it.
   - If live search is unavailable, say so and provide executable GitHub search queries.

## GitHub Search Requirement

Prefer current, source-attributed results. Use available web/search tools when possible. Query patterns:

- `site:github.com <field> roadmap`
- `site:github.com <field> awesome`
- `site:github.com <field> tutorial`
- `site:github.com <field> examples`
- `site:github.com <field> course`

Do not invent repository URLs. If a URL cannot be verified, present it as a search query rather than a link.

## Link Reference

The user requested that the method also consider this source where possible:

`http://xhslink.com/o/9AYTyZ13uox`

If the source content is available from user-provided text, screenshots, or accessible browsing, incorporate the relevant learning-process details. If it is inaccessible, state briefly that the plan follows the user-provided Simon-method requirements instead.
