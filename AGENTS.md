# sam-plugins

- This repo is the Claude Code marketplace `sam-plugins` (sanghoooo's plugins). `.claude-plugin/marketplace.json`
  lists them; `README.md` (in Korean) has the install commands and a table of the plugins. Keep the two in step.
- A plugin with a repo of its own (an app, tests or releases, like sam-ui) is listed with a `git-subdir` source at
  its plugin folder on that repo's default branch, so its releases reach installs without a change here. A small
  plugin goes in `plugins/<name>/` here with a relative source.
- Installs are `<plugin>@sam-plugins` and projects record that id; renaming the marketplace or a plugin breaks
  them.
- Run `claude plugin validate .` after changing the marketplace.
