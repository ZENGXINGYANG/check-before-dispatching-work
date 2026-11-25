---
name: check-before-dispatching-work
description: Check the status before dispatching work, so the same task is never sent twice.
---

# Check before dispatching work

A small skill for anyone who coordinates work across agents, workers, or teammates: check the status before you dispatch, so the same task is never sent twice.

Distilled from practical lessons in preventing duplicate task dispatches. The fix is boring on purpose: read first, compare, record, verify.

## Read the status before you dispatch

- Read the top entries of the status file for the work stream before you dispatch anything. A status file needs at minimum: task name, owner, status, and the expected output file.
- Check open browser windows before you dispatch a browser task.
- Treat a worker report that contradicts the status file as unconfirmed until you re-read the source files directly.
- Skip the dispatch and note the reason in the status file when the status is unclear and no fresh read can settle it.

## Confirm nothing identical is already running

- Compare the task name, target, and account with every running and recently finished item before you dispatch.
- Dispatch only work that is unclaimed and not already in progress; when no conflicting task is running, take the next unclaimed item from the queue.
- Never dispatch two tasks that use the same account in parallel when that account allows only one task at a time.
- Never instruct a worker to overwrite a draft, working file, or task package that another worker is still using, and give every new output a new file name.

## Record the dispatch and verify the return

- Record the task ID, the worker, the start time and the expected output file in the status file right after you dispatch.
- Read back the returned file and check its size and content against the report before you mark the task done.
- Record a duplicate dispatch in the status file at once, with what was sent twice and what you did to stop the second copy.
- Check the status file again on the next check instead of dispatching a waiting task early when it depends on a task that is still running.

## Alternatives for better results

- Hold a task until an active scheduled run finishes when sending it now would duplicate work that run already covers.
- Ask the worker to report the file size and a short content check with every return so a silent overwrite is easy to spot.
