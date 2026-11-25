# check-before-dispatching-work

**Version:** v0.1.0 · **Last updated:** 2026-11-25

A small skill for anyone who coordinates work across agents, workers, or teammates: **check the status before you dispatch, so the same task is never sent twice.**

## Use when

- Before you dispatch work to another agent, worker, or teammate.
- When several agents or people run in parallel and share one account or one work stream.
- Before you start a browser task that uses an account someone else might be using at the same time.

## The problem

When several agents or people work in parallel, the same task gets dispatched twice: two workers produce two versions of the same deliverable, two browser tasks fight over one account, or a finished task gets re-sent because nobody checked the log. The cost is wasted effort, conflicting outputs, and time spent untangling which copy is real.

## The fix

Three habits, in order:

1. **Read the status first.** Check the work stream's status file and any running tasks before you dispatch anything.
2. **Confirm nothing identical is already running.** Compare the task name, target, and account against running and recently finished items. Dispatch only unclaimed work.
3. **Record the dispatch and verify the return.** Write down what you sent, to whom, and what file should come back — then read the return back and check it before marking the task done.

## Example

Before dispatching a task, the coordinator reads the work stream's status file and checks the running tasks. The status file shows the same task is already in progress, so the coordinator skips the dispatch and notes the reason in the status file instead of sending a second copy.

## Install

Run the commands below from the root of the cloned repository.

**Claude Code** (personal skills, available in every project on this machine):

```sh
mkdir -p ~/.claude/skills/
cp -r check-before-dispatching-work ~/.claude/skills/
```

Claude Code watches this directory, so the skill is available without a restart. If this is the first time you created the top-level skills directory, run `/reload-skills` once.

**Codex** (where Codex's own installer puts skills):

```sh
mkdir -p ~/.codex/skills/
cp -r check-before-dispatching-work ~/.codex/skills/
```

OpenAI's docs also list `~/.agents/skills/` as the user skills folder for Codex; Codex reads the installer folder above too. Check that it loaded with `/skills` in a Codex session.

**Other tools:** copy the `check-before-dispatching-work` folder into your tool's skills directory — confirm the exact path in your tool's own documentation first. No skills directory path could be verified for Muse, so no path is given here.

## Contents

- `check-before-dispatching-work/SKILL.md` — the skill itself.

## Scope

- For: coordinating work across several agents, workers, or teammates, especially when they share accounts or a work stream.
- Not for: a single person working on a single task, or work with no status file to check.

## Origin

Distilled from practical lessons in preventing duplicate task dispatches when coordinating multiple agents or workers.

## Feedback

Issues and suggestions are welcome — open an issue on this repository.

## License

MIT — see the `LICENSE` file.
