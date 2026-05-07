# DojiFunded docs

This repository contains the Mintlify documentation site for DojiFunded.

The site is no longer using the Mintlify starter content. The navigation, page set, and writing guidance have been rewritten around the DojiFunded product and the current `doji-interface` frontend.

## Current structure

The docs are organized into these main sections:

- `index.mdx`
- `how-it-works.mdx`
- `doji-accounts.mdx`
- `onboarding/`
- `platform/`
- `resources/`
- `legal/`
- `api-reference/`

Navigation and site branding live in `docs.json`.

Project-specific documentation rules live in `AGENTS.md`.

## Current status

The current pass covers:

- introduction
- funded trading flow
- account types and add-ons
- account creation
- wallet funding
- user lifecycle
- platform overview
- terminal, dashboard, and payouts at a first-pass level
- placeholder sections for AI tools, legal, and API reference

Still pending or intentionally lightweight:

- deeper terminal documentation based on the live frontend
- fuller dashboard and payout workflow detail
- venue-specific and market-specific reference content
- approved legal text
- real API endpoint documentation from the backend source of truth

## Local development

Install the Mintlify CLI:

```bash
npm i -g mint
```

Run the docs locally from the repository root:

```bash
mint dev
```

By default, Mintlify serves the site at `http://localhost:3000`.

## Validation

Check internal links before wrapping up a docs pass:

```bash
mint broken-links
```

If the CLI behaves unexpectedly, update it:

```bash
mint update
```

## Writing workflow

Before editing docs:

- read `AGENTS.md`
- inspect `docs.json`
- verify user-facing product details against `doji-interface`

Use the shared product brief and the frontend as the primary sources of truth for user-facing behavior.

Do not invent:

- API contracts
- legal language
- venue-specific details
- fee tables

unless those are confirmed in source material.

## AI-assisted writing

For Mintlify-specific authoring guidance, install the Mintlify skill:

```bash
npx skills add https://mintlify.com/docs
```

## Notes

- The site title in `docs.json` is currently set to `SomeDoc` per the latest request.
- The API reference section is intentionally preserved for future backend documentation.
- The repo has been cleaned of the old Mintlify starter pages and folders that were no longer useful.
