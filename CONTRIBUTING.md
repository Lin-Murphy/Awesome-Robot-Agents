# Contributing

For a suggestion, you only need three things:

1. The original project, paper, code, demo, or author-post link.
2. One or two sentences explaining how an LLM/VLM or embodied agent participates in **robot-arm manipulation**.
3. Any useful evidence label: real robot, simulation, code available, author-reported, or visual replay.

For a correction, point to the entry and explain what is wrong. The [Issue forms](.github/ISSUE_TEMPLATE/submit-project.yml) are optional guides; a free-form Issue or a README edit is also welcome. Unknown details are fine.

## Editorial checks

The maintainer checks the primary source and writes the model's **decision**, the arm's execution interface or controller, **environment** (physical arm or physics simulation), access status, and one important prerequisite or limitation. Pure VLA policies, unrelated robot tasks, and visual replays without an arm-agent loop are outside the main collection. Unknown details stay unknown. A public repository does not automatically carry an open-source license or a runnable setup.

Results remain `Author-reported` until a documented maintainer rerun links the revision, configuration, procedure, and observed logs. Source reading or a mock run is insufficient. Link original media with credit rather than copying it. Disclose a relationship to the project when relevant.

```markdown
### [Project name](https://original-source.example)

One sentence about the task.

- **Model / role:** Model and its output; name the controller or policy that executes it.
- **Setting:** Real arm or physics simulation; robot and stack.
- **Available:** Direct primary-source link, code/guide/demo status, license and asset access.
- **Limit:** Prerequisite, failure, or evidence boundary; include sample size for metrics.
```

Keep one canonical entry per project in the [README](README.md). When the page becomes too long, move details to category pages and retain one or two homepage examples. Update [UPDATES](UPDATES.md) for substantive changes. Original text here uses [MIT](LICENSE); third-party terms remain with their authors, as described in the README's attribution section.
