# footprint-audit (plugin)

A Claude Code skill to audit and clean up **your own** digital footprint, with a removal workflow based on EU rights (GDPR) and country modules (Italy included). Full documentation is in the [repository README](https://github.com/giuseppe-falco/footprint-audit).

## What the skill runs, fetches and stores

The plugin contains only Markdown instructions: no hooks, no MCP servers, no scripts. When the skill is used, the agent may:

- **Run web searches and fetch public pages** with Claude Code's own tools. The queries contain the identifiers the user provides (name, email addresses, usernames, phone number).
- **Install and run [Sherlock](https://github.com/sherlock-project/sherlock)**, an open-source username checker, with `uv tool install sherlock-project` or `pipx install sherlock-project`. Sherlock sends HTTP requests to public profile URLs on about 400 sites. The user approves the install like any other command.
- **Query public APIs anonymously:** Gravatar (an md5 hash of an email address, computed locally), the GitHub REST API (commits by author email), and the archive.org CDX API.
- **Open a visible browser window** (for example with Playwright), only if one is available, to read public pages or the user's own session. The user logs in by hand; the agent never types, asks for or stores passwords, 2FA codes or cookies.
- **Use the `gh` and `git` CLIs on the user's own repositories**, for example to change visibility or rewrite commit emails, only after explicit confirmation for each action. A mirror backup is made first.

No data is sent to any other service. The audit inventory is written to a private local folder (`~/.local/share/footprint/`, mode 700) and is never uploaded.

## Scope

Only for the user, or for someone who has given explicit consent. The skill refuses to profile third parties and does not create fake accounts. It is not legal advice.

## License

MIT
