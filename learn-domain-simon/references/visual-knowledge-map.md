# Visual Knowledge Map

Use this reference when creating the core concept map.

## Goal

Create an interactive learning map inspired by wide software-engineering roadmap diagrams: concept nodes sit on a large canvas, resources appear as thumbnails or cards near the relevant node, and hovering or focusing a node shows the recommended materials for that concept.

## Preferred Artifact

When file creation is available, create an interactive HTML file using `assets/interactive-knowledge-map-template.html` as the base.

Do not require JPG export. Use static images only as optional screenshots or previews if the user explicitly asks for them.

## Visual Rules

- Use a wide canvas, preferably dark or neutral, so colored nodes and resource covers stand out.
- Place concepts by learning sequence from left to right or top to bottom.
- Use clear stage colors:
  - prerequisite
  - core
  - practice
  - advanced
  - synthesis project
- Draw visible dependency edges between nodes.
- Avoid overlapping nodes, labels, and resource cards.
- Keep node labels short. Put details in hover cards.
- Attach resource thumbnails close to the related node with dashed or subtle connector lines.
- Provide a legend for stages and resource types.

## Resource Cards

Each node can have zero or more resources. For every resource, store:

- title
- type: code, docs, video, book, course, paper, tool, or checklist
- url, when verified
- thumbnail or cover URL, when available and allowed
- reason
- suggested study action
- week

On hover or keyboard focus, show a panel with the node summary and resource cards. If thumbnails are unavailable, use compact text cards with type badges.

## Data Shape

Use this data shape when producing an artifact or a map specification:

```json
{
  "nodes": [
    {
      "id": "git-basics",
      "label": "Git / GitHub",
      "stage": "prerequisite",
      "week": 1,
      "summary": "Version control foundation for AI-assisted coding.",
      "resources": [
        {
          "title": "GitHub Skills",
          "type": "course",
          "url": "https://skills.github.com/",
          "thumbnail": "",
          "reason": "Hands-on GitHub practice.",
          "action": "Complete one beginner module."
        }
      ]
    }
  ],
  "edges": [
    { "from": "git-basics", "to": "agent-workflow", "label": "enables" }
  ]
}
```

## Fallback

If an interactive artifact cannot be created, output a table with:

- node
- stage
- week
- depends on
- resources
- hover-card content
