# WAT Rooms documentation

The docs for WAT Rooms, the meeting-room booking app for the WAT community. Built on [Mintlify](https://mintlify.com): pages are MDX with YAML frontmatter, configured in `docs.json`. Run `mint dev` to preview, `mint broken-links` to check links.

## What this documents

- The web app at `https://wat-app.vercel.app`.
- The `wat` CLI (repo `WATbeta/wat-cli`, package `@wat/wat`, command `wat`).
- The `wat` skills plugin (repo `WATbeta/wat-plugin`) for AI coding agents.

The CLI and the skills are the source of truth for commands and flags. When they change, update `cli.mdx` and `plugin.mdx` to match.

## Hard rules

- **Never put the WAT signup code value in the docs.** It is secret. Say "ask a WAT admin for it".
- Do not document `npm install -g @wat/wat`: it is not published to public npm. The verified install is clone, then `npm install && npm run build && npm link`.
- Do not document the staging URL as a user URL; reference it only via `--env dev`.

## Style

- Active voice, second person ("you"), sentence case headings.
- Bold for UI elements (Click **Settings**), code formatting for commands, paths, file names.
- Do not use " - " or " — " as separators in sentences. Use commas, colons, or restructure.
