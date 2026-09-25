# Contributing

Anyone in the ISMIP7 community can add a script, notebook or snippet here.
It does not need to be polished. A maintainer checks that it is in the
right place, has a README, and looks safe, then merges it. Nobody checks
that it is correct, so say in your README what you have used it for.

## Check the maintained tools first

Some processing is already done by the
[maintained ISMIP7 tools](README.md#maintained-tools), which are tested
and documented. If one of them nearly does what you need, open an issue
there. If your
code should become part of one, open an issue there too, and share it
here in the meantime.

## Questions and ideas

Ask in the [ISMIP discussions](https://github.com/orgs/ismip/discussions);
this repository does not have its own. If you are starting something
others may need too, ask there first, in case someone already has it.
Once your contribution is merged, **Show and tell** is a good place to
announce it.

## Where it goes

Each contribution is its own folder, with a README.md, in one of four
places:

```
AIS/        only makes sense for Antarctica
GrIS/       only makes sense for Greenland
cloud/      about a platform: getting data from source.coop, setting up CryoCloud
general/    everything else
```

The ice sheet comes first. A notebook that maps melt under Antarctic ice
shelves goes in AIS/, even if it runs on CryoCloud. A notebook that shows
how to read any ISMIP7 file from source.coop goes in cloud/, even if its
example file is Antarctic.

Name the folder for what the code does, in lowercase with hyphens, for
example cloud/read-from-source-coop/.

## What a contribution needs

- **A README.md in its folder.** It can be five lines. Say what the code
  does, what data and packages it needs, how to run it, who you are (your
  GitHub handle), and where and when you last ran it.
- **No data.** Link to where the data lives instead: source.coop, Globus,
  Zenodo. A small figure your README shows is fine.
- **No passwords, tokens or keys**, in the code or in notebook outputs.
  Read them from an environment variable, and say in the README which
  one.
- **No personal paths.** Put paths like /glade/u/home/yourname/... in one
  variable near the top, so others can change it.
- **Code you are allowed to share.** Everything here is under the
  [MIT License](LICENSE). If you adapted code from somewhere else, say
  where.

## How to submit

You submit through a fork: your own copy of this repository on GitHub.
You make your changes there, then open a pull request asking for them to
be added here. Only maintainers can change this repository directly.

Fork into your personal GitHub account, not an organization's. With a
personal fork, maintainers can help with small fixes if you ask them to.

### In the browser

1. Click **Fork** at the top of this page.
2. In your fork, open the folder your contribution goes in, for example
   cloud/.
3. Click **Add file**, then **Create new file**. Type
   `read-from-source-coop/README.md` as the name; the slash makes the
   folder. Write the README.
4. Choose **Create a new branch for this commit**, then **Propose
   changes**. GitHub shows a pull request form. Check that it goes from
   your branch to `main` on ismip/ismip7-community, and create it.
5. In your fork, switch to your branch, open your new folder, and add
   your code with **Add file**, then **Upload files**. Commit to the same
   branch; the pull request updates by itself.

### On the command line

With the [GitHub CLI](https://cli.github.com/):

```bash
gh repo fork ismip/ismip7-community --clone
cd ismip7-community
git switch -c add-read-from-source-coop
# add your folder, then:
git add cloud/read-from-source-coop
git commit -m "Add a notebook that reads ISMIP7 output from source.coop"
git push -u origin add-read-from-source-coop
```

`git push` prints a link that opens the pull request.

## What happens next

A maintainer reads your pull request, usually without running the code.
If something needs changing, they comment on the line, often with a
suggested fix you can accept with one click. For bigger changes, such as
moving the folder, they may offer to do it on your branch. They only do
that if you say yes.

Maintainers also add labels, for the ice sheet, platform, language and
topic, so others can find your contribution.

## Changing someone else's contribution

Open a pull request as above, and mention the author named in the
README, for example @their-handle. The maintainer waits for them to
agree.

## Using an AI agent

Many of us use AI coding agents. Their instructions for this repository
are in [CLAUDE.md](CLAUDE.md), and [AGENTS.md](AGENTS.md) points agents
other than Claude to it. Pull request text an agent wrote says so at the
end. You are responsible for what you submit, whoever wrote it.
