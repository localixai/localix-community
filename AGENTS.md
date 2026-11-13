# AGENTS.md

Instructions for AI coding agents working on this repository.

This repository holds no code. It is two lists of what other people publish in their own
repositories: `.localix-mini-app/marketplace.json` (mini apps) and `.claude-plugin/marketplace.json`
(plugins). [README.md](README.md) says what Localix does with them, and
[CONTRIBUTING.md](CONTRIBUTING.md) is the rule for an entry.

## Rules

- **One entry per change**, in alphabetical order by `name`.
- **A mini app's entry names its author's marketplace**: `source` is `github` (the repository whose
  latest release publishes it) or `url`. `name` is the app's name in its own `mini-app.json`.
- **A plugin's entry is pinned to a commit** of the repository it lives in.
- **No curation here.** `featured`, `installByDefault`, `suggestFor` and `collections` are refused:
  Localix vouches for nothing in these lists and takes no curation from them.
- **Never copy an author's code into this repository**: an entry only names where it lives.
- Each change to the mini app list is released, signed, by the workflows in `.github/workflows/`.
  Never tag or push unasked.

## Checking an entry

`mini-app marketplace validate --fetch` (the CLI of the `mini-app-authoring` plugin) checks the mini
app list; `claude plugin validate .` checks the plugin list. The same checks run on a pull request.
