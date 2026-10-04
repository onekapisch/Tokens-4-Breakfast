<div align="center">

# Tokens 4 Breakfast

### AI spend and limits in the Mac menu bar.

Track **token usage, spend, subscriptions, and rate limits** across **11 AI providers** from one private Mac menu bar app: Claude Code, Claude Web, Cursor, Codex, GitHub Copilot, Anthropic API, OpenAI, Grok, DeepSeek, Mistral, and OpenRouter. **Runs locally. No account. Free plan, or Pro for a one-time $14.99.**

![macOS 14.6+](https://img.shields.io/badge/macOS-14.6%2B-000000?logo=apple&logoColor=white)
![Apple Silicon & Intel](https://img.shields.io/badge/Apple%20Silicon%20%26%20Intel-%E2%9C%93-555)
![Providers](https://img.shields.io/badge/providers-11-2563eb)
![Free plan](https://img.shields.io/badge/Free-1%20provider-1ca86a)
![Pro](https://img.shields.io/badge/Pro-%2414.99%20one--time-F59E0B)
![No telemetry](https://img.shields.io/badge/telemetry-none-1ca86a)
[![Website](https://img.shields.io/badge/website-tokens4breakfast.app-2563eb)](https://www.tokens4breakfast.app)
[![Stars](https://img.shields.io/github/stars/onekapisch/Tokens-4-Breakfast?style=social)](https://github.com/onekapisch/Tokens-4-Breakfast/stargazers)

### [Download free for macOS](https://www.tokens4breakfast.app/download?source=github_readme) · [Website](https://www.tokens4breakfast.app) · [Report a bug / request a feature](https://github.com/onekapisch/Tokens-4-Breakfast/issues/new/choose)

<img src="docs/menubar.png" alt="Tokens 4 Breakfast menu bar popover showing today's spend across Claude and OpenRouter, OpenRouter credits left, Claude Web session and weekly limits, and a subscriptions total" width="360">
&nbsp;&nbsp;
<img src="docs/insights.png" alt="Tokens 4 Breakfast usage dashboard showing 30-day tokens by project, share of tokens by model, weekly limit used, and a cheaper-model suggestion" width="560">

</div>

---

> [!NOTE]
> **Tokens 4 Breakfast is a commercial, closed-source macOS app.** This repository hosts the public **docs and issue tracker**, not the app's source code. Bug reports and feature requests are welcome in [Issues](https://github.com/onekapisch/Tokens-4-Breakfast/issues).

## Why

If you build with AI, your spend and your limits are spread across a handful of tools, and you usually find out about either one too late:

- **The bill.** Claude, ChatGPT, Cursor, Copilot, and a few API keys each bill separately, and nothing adds them up until the invoices arrive.
- **The limit.** You hit a Claude or Codex window halfway through an agent run, with no warning.

Tokens 4 Breakfast keeps both numbers in your menu bar while you work: what your usage costs, what your subscriptions cost, and how much of each limit you have left.

## What you get

- **Live numbers in the menu bar.** Pick what the menu bar shows: a provider's cost, all-provider spend, a subscription total, a Claude 5-hour or weekly cap, or Codex and Grok usage. Up to two extra compact metrics can sit beside it.
- **Usage in real money.** Claude Code and Codex usage is valued at each model's published API rate, so a flat subscription still shows what the same tokens would have cost. Models without a public rate are marked unpriced, never guessed.
- **Limits before you hit them.** Claude 5-hour, weekly, and per-model limits, Codex limits, and the Grok weekly limit, each with a reset time and a burn-rate forecast. Claude limits also send alerts as you approach the cap.
- **Subscription tracking.** Add Claude, ChatGPT, Cursor, Copilot, Grok, and other plans, and see them next to your usage-based spend.
- **Focus Mode.** Set a dollar budget for a work session and get warned at 80% and 100%.
- **Usage Intelligence (Pro).** A dashboard with Limit Runway (when you will hit each cap at your current pace), Efficiency (where a cheaper model would do the job), and Plan Value (whether your plan pays for itself), plus breakdowns by provider, model, project, and session.
- **Budgets and exports (Pro).** Per-provider daily and weekly budgets with alerts, CSV export, and a weekly summary.
- **Token Card (Pro).** A shareable image of your token count or its API-equivalent value, generated from your own data.
- **Your currency.** Show spend in EUR, GBP, and more, at a conversion rate you set.
- **Privacy Audit Log.** Every outbound request the app makes is logged in Settings, with host, reason, and time.

## Supported providers

11 providers connect. 8 of them report real spend; Claude Web and Grok report live rate limits only, and DeepSeek reports account balance, so the app shows no dollar figure for those three.

| Provider | What it reports | How it connects |
|---|---|---|
| **Claude Code** | Spend (API-equivalent), projects, models, sessions | Local session files. No key. |
| **Claude Web** | Claude 5-hour, weekly, and per-model limits | Your claude.ai session, via a guided connect in Settings |
| **Cursor** | Spend, projects, models, sessions | Local Cursor data. No key. |
| **Codex** | Spend and plan limits | Local Codex CLI sessions. No key. |
| **GitHub Copilot** | Subscription value and monthly quota (AI credits or premium requests, as GitHub reports it) | Your local Copilot CLI login. No key. |
| **Grok** | SuperGrok weekly limit | Your local Grok CLI login. No key. |
| **Anthropic API** | Organization API spend | Anthropic Admin API key (organizations only) |
| **OpenAI** | Organization API spend | OpenAI organization Admin API key |
| **Mistral** | Organization API spend | Mistral Enterprise Admin API key |
| **OpenRouter** | Spend, model mix, remaining credits | OpenRouter API key |
| **DeepSeek** | Account balance | DeepSeek API key |
| **Gemini** | Coming soon | Not collecting yet |

OpenAI, Anthropic API, and Mistral need an organization admin key; a personal key cannot read their usage endpoints. Keys are stored in the macOS Keychain and sent only to that provider's API.

## Free vs Pro

| | Free | Pro |
|---|---|---|
| Price | $0, no time limit | **$14.99 one-time**, no subscription |
| Providers | 1 of your choice | All 11 |
| History | Today and 7 days | 30 days |
| Menu bar spend, Claude Code 5-hour timer | ✓ | ✓ |
| Focus Mode session budgets | ✓ | ✓ |
| AI subscription tracking | ✓ | ✓ |
| Privacy Audit Log | ✓ | ✓ |
| Usage Intelligence (Limit Runway, Efficiency, Plan Value) | | ✓ |
| Per-provider daily and weekly budgets | | ✓ |
| CSV export and weekly summary | | ✓ |
| Sessions tab with cost breakdown | | ✓ |
| Token Card | | ✓ |
| Priority email support | | ✓ |

Pro includes future updates. It is licensed per Mac and comes with a 14-day money-back guarantee. If you bought Pro at the $7.99 launch price, you keep everything, including future updates.

## Privacy and security

- **Local storage.** Usage lives in a SQLite database on your Mac. There is no Tokens 4 Breakfast account and no cloud backend.
- **No prompts, ever.** From Claude Code's logs the app keeps usage metadata only (token counts, model, timestamp, cost). Your prompts and responses are not stored or sent anywhere.
- **No telemetry.** The only network calls go to the providers you connect, a license check when you activate Pro, and the update check. Each one appears in the Privacy Audit Log.
- **Credentials in the Keychain.** API keys and sessions are stored in the macOS Keychain and sent only to the matching provider.
- **Signed and notarized** by Apple, with the hardened runtime. Built in Germany.

See [SECURITY.md](SECURITY.md) for how to report a vulnerability.

## Install

1. **[Download the latest release](https://www.tokens4breakfast.app/download?source=github_readme).**
2. Open the .zip and drag **Tokens 4 Breakfast** to `/Applications`.
3. Launch it, click the menu bar icon, and connect a provider in Settings.

**Updating:** built-in auto-update (Sparkle). The app tells you when a new version is ready to install.
**Uninstalling:** quit the app and move it to the Trash. Your data is in `~/Library/Application Support/Tokens4Breakfast`; saved keys are in your login Keychain under `com.onekapisch.tokensforbreakfast`.
**Requirements:** macOS 14.6 Sonoma or later, Apple Silicon or Intel.

## Recent releases

The latest release is **2.0.17** (4 October 2026). Highlights from the 2.0 line:

- **2.0.17:** a pace marker on every 5-hour and weekly limit, a Codex credits watch, value per 1% of your limit (Pro), and Claude Opus 5.5 / Sonnet 5.5 and GPT-6.1 Sol priced.
- **2.0.16:** GPT-6 and Claude Fable 5.1 priced; every model rate re-checked against the providers' official pricing pages.
- **2.0.15:** extra metrics in the menu bar, weekly-limit alerts at 80/95/100%, and a selectable period for the popover's headline figure.
- **2.0.14:** Focus sessions back in the popover, a burn-rate forecast per limit, and early-reset tracking.
- **2.0.10:** Anthropic API organization spend.
- **2.0.9:** spend in your own currency, support for the standalone Copilot CLI, and Codex per-model limits.
- **2.0.6:** Grok / SuperGrok weekly limit.

Full notes for each version appear in the app's What's New sheet.

## How it compares

[ccusage](https://www.tokens4breakfast.app/alternatives/ccusage-gui) is a command-line tool for local agent usage and costs; Tokens 4 Breakfast puts that kind of visibility in a native menu bar app and adds subscriptions, budgets, and more providers. [CodexBar](https://www.tokens4breakfast.app/alternatives/codexbar-alternative) is a free, open-source menu bar tracker for coding-provider limits; Tokens 4 Breakfast also tracks spend, subscriptions, and budgets around those limits. More side-by-side pages: [tokens4breakfast.app/alternatives](https://www.tokens4breakfast.app/alternatives).

## Roadmap and feedback

The roadmap follows what users ask for. Want a provider or a feature? **[Open an issue](https://github.com/onekapisch/Tokens-4-Breakfast/issues/new/choose).** Many recent features started as requests here and by email.

## FAQ

**Is it open source?** No, it is a commercial app. This repo holds docs and the issue tracker. <br>
**Does it read my prompts?** No. It keeps token counts, model names, timestamps, and cost, never conversation content. <br>
**Does it send my data anywhere?** No telemetry. It only calls the providers you connect, plus the Pro license check and the update check. <br>
**Why is there no dollar figure for Claude Web, Grok, or DeepSeek?** Those providers report limits or a balance, not spend, and the app does not invent one. <br>
**What about Gemini?** Google does not currently expose the account usage data the app needs, so Gemini stays disabled until it does. <br>
**Can I use Pro on more than one Mac?** Pro is licensed per Mac. The free plan has no device limit. <br>
More: **[full FAQ](https://www.tokens4breakfast.app/faq)**

## More from OneKapisch

Other apps from the same studio ([onekapisch.com](https://www.onekapisch.com)):

- **[Mac 4 Breakfast](https://www.mac4breakfast.app/)**: Your one battery app that does it all.
- **[LUMEL](https://getlumel.app/)**: Brighter than macOS allows. Darker than its minimum.
- **[Clip 4 Breakfast](https://clip4breakfast.app/)**: The clipboard manager that never slows your Mac down.
- **[Chime 4 Breakfast](https://github.com/onekapisch/chime-4-breakfast)**: Run-completion alerts. Open source.
- **[Easy Write](https://github.com/onekapisch/easy-write)**: On-device writing tools. Open source.
- **[SkyLocation](https://www.skylocation.app/)**: Know where you are. Without internet or signal.

---

<div align="center">

**If Tokens 4 Breakfast is useful to you, a star helps other builders find it.**

[Website](https://www.tokens4breakfast.app) · [Download](https://www.tokens4breakfast.app/download?source=github_readme) · [FAQ](https://www.tokens4breakfast.app/faq) · [Privacy](https://www.tokens4breakfast.app/privacy)

</div>
