# footprint-audit

A Claude Code skill to **audit and clean up your own digital footprint**, with a removal workflow based on EU rights (GDPR) and country modules (Italy included).

Most footprint and OSINT skills are built for investigating other people, or only cover US data brokers and the CCPA. This one is the opposite: it is a self-audit, read-only by default, and it ends with concrete EU removal steps.

## What it does

1. **Collects your identifiers:** name, city, phone, current and old email addresses, historical usernames.
2. **Runs parallel reconnaissance** with subagents:
   - name, city and phone;
   - email addresses: Gravatar, public GitHub commits, archive.org;
   - usernames, with [Sherlock](https://github.com/sherlock-project/sherlock) and a list of known false positives;
   - search operators run in a local-language browser.
3. **Checks platforms behind a login** from three points of view:
   - as a stranger, with the platform's "view as" or public-profile feature, or a logged-out browser;
   - in your own session: you log in by hand in a visible browser window, and the agent never sees or stores your password;
   - as the platform sees you, with its data export or a GDPR art. 15 access request.
4. **Builds an inventory** with a confidence grade (A–D) and a proposed action for each exposure. The inventory is kept in a private local folder.
5. **Cleans up:**
   - checklists for your own accounts;
   - GitHub hygiene: making old repos private, rewriting commit emails to the noreply address, email-privacy settings;
   - GDPR art. 17 erasure requests and complaints to the data protection authority;
   - Google and Bing delisting;
   - archive.org removal.
6. **Suggests a re-check** every 3–6 months.

## Safety rules built in

- Only for yourself, or for someone who has given explicit consent. It refuses to build profiles of third parties.
- Reconnaissance is read-only. The agent does not log in by itself, submit forms, use paid services or run third-party scrapers. The only logged-in view is your own session, where you log in by hand.
- Deleting, sending and filling in forms is done by you. Destructive actions (visibility changes, force pushes) need explicit confirmation, and a mirror backup is made first.
- Your data never goes into the skill files or into synced folders: the inventory stays in `~/.local/share/footprint/`.

## Install

As a Claude Code plugin:

```
/plugin marketplace add giuseppe-falco/footprint-audit
/plugin install footprint-audit@footprint-audit
```

Or copy `plugins/footprint-audit/skills/footprint-audit/` into `~/.claude/skills/`. The skill follows the `SKILL.md` format, so it can be adapted to other agents that support skills.

Then ask, for example: *"Audit my digital footprint"* or *"Check what's online about me and help me remove it"*.

## Platform cards

`references/platforms/` has one card per platform: Facebook, Instagram, LinkedIn, X, Google, TikTok, Snapchat, Discord, Telegram, Truecaller and ask.fm. Each card covers:
- how to see yourself as a stranger;
- what to check while logged in;
- which settings to tighten;
- how to export your data;
- the EU controller and its privacy contact;
- how to delete the account and remove content.

Items still marked "(to verify)" could not be confirmed on an official page. Corrections are welcome.

The skill does not create fake or "demo" accounts to look at you from outside. It breaks the platforms' terms, and the stranger view gives the same answer.

## Country modules

`references/countries/it.md` covers Italian directories, public lists (*albo pretorio*, *graduatorie*), classified-ad sites, the Garante and an erasure letter in Italian. Contributions for other countries are welcome: follow the same structure (local sources, supervisory authority, letter in the local language).

## Disclaimer

This is not legal advice. Removal forms and URLs change often: the skill asks the agent to check them before proposing them.

## License

MIT
