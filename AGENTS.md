> This file is now customized for the DojiFunded docs project. Keep updating it as the product and docs strategy evolve.
> For Mintlify product knowledge, install the Mintlify skill: `npx skills add https://mintlify.com/docs`

# Documentation project instructions

## About this project

- This is a Mintlify documentation site for DojiFunded
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Run `mint dev` to preview locally
- Run `mint broken-links` to check links
- The current product source of truth for behavior and UI is `doji-interface`
- When product docs and the frontend conflict, inspect the frontend before writing

## Product summary

- DojiFunded is an on-chain funded trading protocol
- The product evaluates traders under predefined risk rules, then grants access to funded accounts
- The platform is built for discretionary traders and autonomous strategies
- Key product themes are transparency, on-chain verification, institutional execution, embedded wallets, and AI-native tooling

## Primary doc sections

- Getting started
  Covers introduction, how it works, and account types
- Onboarding
  Covers account creation, wallet funding, lifecycle, and future autonomous strategy funding
- Platform
  Covers overview, terminal, dashboard, AI backtesting engine, AI copilot, and payouts
- Resources
  Covers markets, venues, fees, rules, partners, and bug reports
- Legal
  Covers terms of use and privacy policy

## Terminology

- Use `DojiFunded` as the canonical product name
- Use `Doji` only when the content is intentionally more conversational or when referring to the product shorthand
- Use `funded account` for accounts that have passed evaluation and can earn payouts
- Use `evaluation` for the qualification phase before funding
- Use `account type` for Degen, 1-Step, 2-Step Elite, and 2-Step Classic
- Use `execution venue` or `execution partner` for the underlying trading venue or protocol
- Use `embedded wallet` or `Doji wallet` for the wallet created for each user
- Use `trading identity` for the user's username and public profile
- Use `connected wallet` when referring to the user wallet used for execution, verification, or payouts
- Use `payout` instead of `withdrawal` unless the product UI specifically uses `withdrawal`
- Use `on-chain` when describing settlement, verification, payouts, NFTs, or execution-backed infrastructure
- Use `autonomous strategies` instead of vague phrases like `AI bots`
- Use `risk parameters` or `trading rules` instead of generic `restrictions`

## Product facts to preserve

- Users can sign up with email or wallet connection
- The platform creates an embedded wallet during signup
- Users choose an account type and an execution venue before payment
- Payment methods include crypto and card
- Trading uses a virtual allocation for evaluation and funded account accounting
- Off-platform trading is not permitted
- Position, PnL, and drawdown monitoring happen in real time
- Trade positions are recorded on-chain as NFTs
- Eligible payouts are requested from the dashboard and settled on-chain
- There are no recurring fees for evaluations in the current source material

## Current account types

- `Degen (Instant Funding)`
- `1-Step`
- `2-Step Elite`
- `2-Step Classic`

When writing about account types:

- Keep the comparison factual
- Preserve distinctions around profit targets, drawdown model, daily drawdown, leverage, risk per trade, minimum trade duration, and payout conditions
- Do not invent rules that are not confirmed in source material

## Current add-ons

- `80% / 90% Profit Split`
- `Remove 1% Risk Per Trade Limit`
- `Enable Hedging on the Same Currency`

When writing about add-ons:

- Present them as optional account customizations
- Do not assume every add-on is available for every account type unless confirmed

## Style preferences

- Use active voice and second person
- Keep sentences concise
- Keep one idea per sentence
- Use sentence case for headings
- Bold UI labels: Click **Settings**
- Use code formatting for file names, commands, paths, route names, environment variables, and code references
- Lead with what the user is doing or trying to achieve
- Prefer concrete product language over marketing language
- Keep product claims grounded in platform behavior
- When describing flows, write steps in the order users experience them
- Always include a `Next steps` section at the end of procedural or onboarding pages when it helps users move forward

## Voice and messaging

- Sound clear, direct, and product-literate
- Explain funded trading in plain language
- Emphasize transparency, verifiability, and on-chain settlement where relevant
- Emphasize that DojiFunded supports both traders and autonomous strategies
- Avoid hype words such as `revolutionary`, `game-changing`, `best-in-class`, or `seamless`
- Avoid filler like `simply`, `just`, `easy`, or `obviously`
- Avoid vague claims about performance, profits, or outcomes

## Page-writing guidance

- Introduction pages should explain what DojiFunded is, who it is for, and how funded trading works on the platform
- Account pages should compare account types with scannable tables and explicit rule summaries
- Onboarding pages should explain signup, identity setup, venue selection, funding, and payment clearly
- Lifecycle pages should explain how a user moves from landing page to funded trading and payouts
- Platform pages should explain the terminal, dashboard, AI tools, payouts, and wallet model without drifting into backend internals
- Resource pages should be practical and referenceable
- Legal pages should stay precise and avoid interpretive rewrites unless requested

## Frontend-informed writing notes

- The main product surface is the trading app in `doji-interface`
- The default user destination is the trading terminal, not a marketing homepage
- Major product surfaces visible in the frontend include `trade`, `dashboard`, `leaderboard`, `profile`, `affiliate`, `agents`, and `backtesting`
- The visual language is dark-first, dense, terminal-like, and trading-oriented
- If a doc page describes a UI flow, verify labels and route behavior against the frontend first

## Content boundaries

- Do document funded trading concepts, account types, onboarding, execution venues, payouts, rules, and user-facing platform flows
- Do document embedded wallet behavior at the user level
- Do document AI-native features only at the level users can access or understand
- Do not document internal admin tooling
- Do not document hidden anti-abuse systems in implementation detail
- Do not document raw environment variables, internal service URLs, or backend architecture unless the page is explicitly internal
- Do not promise features that are marked as coming soon
- Treat `Funding Autonomous Agents Strategies` as future-facing unless the product surface is live and confirmed

## Accuracy rules

- Prefer the shared product brief and the `doji-interface` codebase over assumptions
- If account rules, payouts, or venue behavior are time-sensitive, verify them before publishing
- If the docs source and frontend disagree, flag the mismatch instead of blending them silently
- Preserve meaningful distinctions between evaluation accounts, funded accounts, and instant funding

## Useful local checks

- Run `mint dev` for local preview
- Run `mint broken-links` before finalizing nav or link changes
- Review `docs.json` before creating or moving pages
