---
name: plan-documents
description: Write a plan for work not yet started, for a colleague or the user to approve before implementation begins.
---

# Plan documents

The reader is deciding whether to let you proceed.

- Open questions and anything needing a decision go at the top.
- The steps, in order, one line each.
- Do not justify each step. Do not list the files you will touch. Do not
  restate the repository back.
- If a step needs a paragraph to explain, it belongs in an issue, not in
  the plan.

## Enough

Plans are approved in conversation rather than committed, so there is no
colleague-written example to copy. The following is constructed.

> **Open:** should notebooks be labeled by their language as well as
> `notebook`, or only as `notebook`?
>
> 1. Add a labeler config: AIS/ and GrIS/ by path, `notebook`, `Python`
>    and `MATLAB` by file extension.
> 2. Run it on `pull_request_target`, which never checks out the pull
>    request's code.
> 3. Open a test pull request from a fork and check the labels.
