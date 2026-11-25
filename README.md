# check-before-dispatching-work

A small skill for anyone who coordinates work across agents, workers, or teammates: **check the status before you dispatch, so the same task is never sent twice.**

## The problem

When several agents or people work in parallel, the same task gets dispatched twice: two workers produce two versions of the same deliverable, two browser tasks fight over one account, or a finished task gets re-sent because nobody checked the log. The cost is wasted effort, conflicting outputs, and time spent untangling which copy is real.

## The fix

Three habits, in order:

1. **Read the status first.** Check the work stream's status file and any running tasks before you dispatch anything.
2. **Confirm nothing identical is already running.** Compare the task name, target, and account against running and recently finished items. Dispatch only unclaimed work.
3. **Record the dispatch and verify the return.** Write down what you sent, to whom, and what file should come back — then read the return back and check it before marking the task done.

## Contents

- `check-before-dispatching-work/SKILL.md` — the skill itself.

## Install

Copy the `check-before-dispatching-work` folder into your agent's skills directory and load it like any other skill.

## Origin

Distilled from practical lessons in preventing duplicate task dispatches when coordinating multiple agents or workers.

## License

MIT
