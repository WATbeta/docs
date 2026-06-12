# WAT Rooms documentation

The docs for WAT Rooms, the meeting-room booking app for the WAT community. Built on [Mintlify](https://mintlify.com): pages are MDX with YAML frontmatter, configured in `docs.json`. Run `mint dev` to preview, `mint broken-links` to check links.

## What this documents

- The web app at `https://app.wat.com`.
- The `wat` CLI (repo `WATbeta/wat-cli`, package `@wat-toolbox/wat`, command `wat`).
- The `wat` skills plugin (repo `WATbeta/wat-plugin`) for AI coding agents.

The CLI and the skills are the source of truth for commands and flags. When they change, update `cli.mdx` and `plugin.mdx` to match.

## Hard rules

- **Enrollment is allowlist-gated, not code-gated.** First login self-enrolls when the email's domain (or the exact address) is on the admin-managed resident list (web app, Admin → Users & Access). Never document a signup code — that mechanism was removed in 2026-06. A resident-list miss automatically files an **access request** with the admins (v1.10): say "you'll receive an email if your request is approved", not "ask a WAT admin to add you".
- The CLI is published to npm as `@wat-toolbox/wat`. Document install as `npm install -g @wat-toolbox/wat` (global, needed for the skills plugin which calls `wat`) or `npx @wat-toolbox/wat …` for one-off commands. Do NOT document a clone/build/link from-source flow.
- Do not document the staging URL as a user URL; reference it only via `--env dev`.

## Style

- Active voice, second person ("you"), sentence case headings.
- Bold for UI elements (Click **Settings**), code formatting for commands, paths, file names.
- Do not use " - " or " — " as separators in sentences. Use commas, colons, or restructure.
