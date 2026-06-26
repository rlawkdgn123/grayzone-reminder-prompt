# GrayZone Reminder Prompt

Daily Todo Reminder is a reusable prompt package for generating an evidence-based daily todo list and a local HTML dashboard.

The prompt is written in Korean because the original workflow is Korean-first. It is designed to be copied into Codex, ChatGPT, Claude, or another agent runner that can read local project files.

## What It Does

- Reads configured work logs, daily summaries, work records, task lists, and repository status.
- Produces today's todo text from explicit evidence only.
- Creates or updates `TodoList (YYYY-MM-DD).html`.
- Provides a local HTTP preview link when the runner supports serving local files.
- Runs a first-run setup flow before creating files or registering automation.

## What It Does Not Do

- It does not edit source work logs, task lists, project documents, code, assets, scenes, Notion pages, or version-control state.
- It does not invent tasks when there is no evidence.
- It does not assume missing paths or permissions.

## Files

- `prompt.md`: the transfer prompt to paste into your agent or automation.
- `Templates/PROGRAMMER_DAILY_TODO_TEMPLATE.html`: default programmer-oriented HTML template.
- `Templates/ART_DAILY_TODO_TEMPLATE.html`: art-pipeline-oriented HTML template.
- `Templates/README.md`: template notes.

## Quick Start

1. Open `prompt.md`.
2. Fill the environment block near the top.
3. Set paths you do not use to `없음`.
4. Paste the prompt into your agent or scheduled automation.
5. On the first run, answer the setup questions one at a time.

The prompt intentionally asks for confirmation before writing setup state, creating folders, starting a local server, or registering recurring automation.

## Suggested Output Layout

```text
your-workspace/
  Daily Todo/
    TodoList (2026-06-26).html
    onboarding-state.json
```

You can choose any output path during first-run setup.

## Version

This repository starts from the V1.4 package.

## License

MIT License.

