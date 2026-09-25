---
name: pr-descriptions
description: Write or update a pull request description. Use when opening a pull request or editing its body.
---

# Pull request descriptions

The reader is a maintainer deciding whether the contribution is in the
right place and safe to merge, and later someone browsing for what it
added.

- What it adds or changes, and where, in a sentence or two. Not how it
  works; that is in the README or the code.
- Anything a maintainer needs to decide goes first, as a short list: an
  unclear folder, a file that might be too large.
- A change to someone else's contribution mentions its author.
- No commit list. No testing section; where the code was run goes in the
  README.
- Link the issue that gives context, with a closing keyword if the pull
  request fixes it.
- One contribution per pull request.

## Calibration

This repository has no history to measure yet. Take the rule of thumb
from [polaris], a larger repository with the same maintainer: 27 words at
the median, 45 to 62 at the seventy-fifth percentile, 103 to 110 at the
ninetieth, 354 at the longest. A new contribution needs fewer, since its
README does the explaining.

[polaris]: https://github.com/E3SM-Project/polaris

## Enough

A new contribution (constructed):

> Adds cloud/read-from-source-coop/, a short notebook that opens ISMIP7
> output on source.coop with xarray without downloading it.

A question for the maintainer, then the change (constructed):

> **Not sure:** this only handles the AIS grids for now, so I put it in
> AIS/. It should move to general/ if someone adds GrIS.
>
> Adds AIS/thickness-change-maps/, which plots the change in ice
> thickness between two years of a simulation.

A fix to someone else's contribution (constructed):

> Fixes GrIS/surface-mass-balance-maps/ for models on the 1 km grid; the
> notebook assumed 5 km. Fixes #12.
>
> @author, you're listed in the README. Does this look right to you?

## Too much

An agent-written description (constructed) restated the README under
"Overview", listed every function under "Changes", and ended with a
"Testing" section and a list of six commits. None of it helped a
maintainer decide whether the notebook belonged in cloud/, which was the
one question worth asking.
