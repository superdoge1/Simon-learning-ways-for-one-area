# Simon Learning Ways for One Area

`learn-domain-simon` is a Codex skill for building structured learning plans for any specific field. It uses the Simon learning method to turn a broad learning goal into a knowledge map, small learning chunks, layered quizzes, deliverable-based practice, one-page reviews, and high-value GitHub resources.

## What It Does

When invoked, the skill first asks which language you want the learning plan to use. Then it asks what field you want to learn and, when needed, collects a lightweight learner profile:

- Current level or background
- Desired outcome or use case
- Weekly time budget
- Preferred learning style: theory-first, practice-first, or balanced

It then generates a learning plan in the selected language with:

- A core concept knowledge map
- A dependency-aware learning sequence
- Fine-grained learning chunks
- Short explanations for each chunk
- Layered quiz questions: recall, explanation, transfer, and counterexample
- Deliverable-based practice tasks
- A final synthesis project
- Weekly and monthly one-page review templates
- Categorized GitHub learning resources

## Resource Categories

The skill ranks GitHub repositories by learning value and groups them into categories such as:

- Roadmaps
- Courses
- Project-based learning
- Awesome lists
- Official implementations
- Reference tools

It prioritizes authority, maintenance, documentation quality, runnable examples, learning path clarity, community validation, and fit with the learner's goal.

## Project Structure

```text
learn-domain-simon/
+-- SKILL.md
+-- agents/
|   +-- openai.yaml
+-- references/
    +-- github-resource-rubric.md
    +-- learning-framework.md
```

## How To Use

Install the `learn-domain-simon` folder into your Codex skills directory, then invoke it with:

```text
Use $learn-domain-simon to build a Simon-method learning plan for a field I choose.
```

Example fields:

- Large language model application development
- Quantitative trading
- Product management
- Distributed systems
- Psychology

The skill will ask for the output language and the specific field before producing the learning plan.

## Notes

The skill asks for the desired output language before generating the plan. If no language is provided after asking, it defaults to Chinese and states that assumption.

The original design also references this source when available:

```text
http://xhslink.com/o/9AYTyZ13uox
```

If the link content is inaccessible, the skill follows the Simon-method workflow captured in this repository.
