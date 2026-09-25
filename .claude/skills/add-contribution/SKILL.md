---
name: add-contribution
description: Add a script, notebook or snippet to the repository, or change one already here. Use when helping someone contribute, when moving a contribution, or when writing or revising a contribution's README.
---

# Adding a contribution

The person you are helping has code that works for them and wants others
to be able to use it. The reader is an ISMIP7 scientist browsing for
something that saves them a day. They decide from the README in under a
minute, and English may not be their first language.

CONTRIBUTING.md has the folder layout and the checklist. This skill is
how to apply them.

## Where it goes

- A contribution goes under AIS/ or GrIS/ if it only makes sense for that
  ice sheet, even if it runs in the cloud.
- cloud/ is for the platforms themselves: getting data out of source.coop,
  setting up an environment on CryoCloud.
- Everything else goes in general/.
- Each contribution is its own folder, named for what it does, in
  lowercase with hyphens: `cloud/read-from-source-coop/`, not
  `cloud/smith-snippet/` or `cloud/test2/`.

A notebook that reads ISMIP7 output from source.coop on CryoCloud goes in
cloud/, even if its example file is Antarctic: it would work the same on
a Greenland file. A notebook that maps basal melt under each Antarctic ice
shelf goes in AIS/, even though it reads from source.coop.

If it is not clear, ask the user, and put the question at the top of the
pull request description.

## Preparing the code

Change as little as possible. The contributor's working code is the
point, and they need to recognize it when someone asks them a question
about it.

- Do not restructure, reformat, rename, add a command-line interface, add
  tests or type hints, or turn it into a package.
- Do move hard-coded paths, especially ones with a username in them, into
  one clearly marked variable near the top.
- Do remove credentials: tokens, passwords, access keys, `.netrc`
  contents. Read them from the environment or a file outside the
  repository instead, and say in the README how to set them. If a
  credential was ever committed, stop and tell the user: it must be
  revoked, and the branch rewritten before it is pushed. A later commit
  that deletes it is not enough; the pull request shows every commit.
- Do not add data. Link to where the data lives: source.coop, Globus,
  Zenodo. A small figure the README shows is fine.
- Keep notebook outputs that show the result, such as a plot. Clear the
  ones that are large or that show usernames, hostnames or paths.

## The README

Every contribution has a README.md in its folder. For a snippet it can be
five lines. It says, in this order:

1. What the code does, in one or two sentences, and for which ice sheet
   or data.
2. What it needs: the input data, with a link to where to get it, and the
   packages to install.
3. How to run it: the command, or which notebook to open, then what the
   reader will see.
4. Who wrote it, as a GitHub handle, and where and when it was last run.

- Show a path or a file name as it is, not as a template with field
  names in braces.
- Backticks are for what the reader types: commands, package names to
  install, values to set. File names and variable names go in plain text.
- Say what the code does, not why it was written that way.
- Do not explain ISMIP7 conventions the reader already works with. Link
  to the protocol or a maintained tool's documentation where it matters.

## Opening the pull request

- Commit on a new branch, push it to the user's fork, and open the pull
  request against `main` on ismip/ismip7-community.
- One contribution per pull request.
- Write the description with the `pr-descriptions` skill.

## Enough

A README for a short snippet (constructed):

> # Read from source.coop
>
> Opens ISMIP7 model output on source.coop with xarray, without
> downloading it first. Works for AIS and GrIS files.
>
> Needs `xarray` and `s3fs`. Open read_from_source_coop.ipynb and run all
> cells; the last cell plots ice thickness for the first time step.
>
> By @contributor. Last run on CryoCloud, September 2026.

## Too much

A 15-line snippet arrived as a package (constructed): pyproject.toml, a
src/ layout, a command-line interface with six options, a test file and a
400-word README explaining the design. The contributor could not answer
questions about it, and the next person to use it had to read all of that
to find the three lines that open the file. The snippet, a variable for
the path, and the README above would have done.
