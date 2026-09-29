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
| **GitHub Copilot** | Subscription value and premium-request quota | Your local Copilot CLI login. No key. |
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

The latest release is **2.0.16** (19 September 2026). Highlights from the 2.0 line:

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

<!--
CLAIM VERIFICATION LOG (drafted 2026-09-28). Remove before publishing, or keep as a maintainer note.

Sources abbreviated:
  SITE    = https://www.tokens4breakfast.app (fetched 2026-09-28)
  SC      = T4B Website origin/main (c00df3c, 2026-09-19) src/lib/site-content.ts
  PROV    = T4B Website origin/main src/lib/providers.ts
  PRICE   = T4B Website origin/main src/lib/price-change.ts
  REG     = .worktrees/t4b-v2-premium-upgrade/Tokens 4 Breakfast/Core/Providers/ProviderRegistry.swift (+ ProviderID.swift)
  CL      = .worktrees/t4b-v2-premium-upgrade/CHANGELOG.md
  PBX     = .worktrees/t4b-v2-premium-upgrade/Tokens 4 Breakfast.xcodeproj/project.pbxproj
  STUDIO  = https://www.onekapisch.com (fetched 2026-09-28, raw HTML)
  REPO    = gh api repos/onekapisch/Tokens-4-Breakfast (contents listing)

Header / badges
- Tagline "AI spend and limits in the Mac menu bar." -> STUDIO (T4B card tagline)
- 11 providers, names and order -> PROV TRACKED_PROVIDERS; SITE lists the same 11 + "Gemini (coming soon)"; REG has the same 11 available + Gemini .unavailable
- Pro $14.99 one-time, no subscription -> PRICE (standardPrice after 2026-08-31) + SITE ("$14.99 one-time purchase"); SC pricingPlans "one-time payment"
- Free = 1 provider, no time limit -> SC pricingPlans ("$0 — forever", "1 provider of your choice"), FAQ "no time limit"; app DataCollectionManager.freeProviderLimit = 1
- No account -> SC trustBadges / privacyBadges; SITE
- macOS 14.6+, Apple Silicon & Intel -> SC ctaHardwareNote; PBX MACOSX_DEPLOYMENT_TARGET = 14.6
- Telemetry none -> SC privacyBadges "No telemetry"; SITE; grep of app source found no analytics/crash SDK (TelemetryDeck, PostHog, Sentry, Firebase, Mixpanel, Amplitude, Crashlytics, Aptabase)
- Stars badge / all repo links -> repo full_name confirmed as onekapisch/Tokens-4-Breakfast via gh api; issue templates exist at .github/ISSUE_TEMPLATE (bug_report.yml, feature_request.yml) so /issues/new/choose works
- Download link -> https://www.tokens4breakfast.app/download?source=github_readme returns 302 to /downloads/Tokens%204%20Breakfast.zip (checked 2026-09-28)
- Screenshots docs/menubar.png and docs/insights.png -> exist in REPO docs/ (only two files there). Alt text describes what the images actually show (viewed). NOTE: both images date from 2026-06-20 (v1.x UI, pre-2.0); consider refreshing them. Old alt text claimed "Usage Insights ... weekly limit usage", kept in spirit.

What you get
- Menu bar metric options (provider cost, all-provider spend, subscription total, Claude 5h/weekly cap, Codex and Grok) -> SC screenshotShowcaseItems "display"; CL 2.0.3 (Codex metric), 2.0.6/2.0.7 (Grok metric), 2.0.13 (pin weekly cap)
- Up to two extra metrics -> CL 2.0.15 "Multi-metric menu bar"
- API-equivalent valuation at published rates; unpriced models shown as unpriced -> SC featurePillars "Your usage, in real money"; SC whatsNewRelease 2.0.16 "Honest by default"; CL 2.0.1 ("unknown models are stored as 'pricing unknown' instead of $0")
- Claude 5h/weekly/per-model limits, Codex limits, Grok weekly, reset times, forecast, alerts -> REG (Claude Web, Codex, Grok capabilities); CL 2.0.14 (per-limit burn-rate forecast line), 2.0.15 (weekly-limit alerts), 2.0.9 (Codex per-model limits), 2.0.6 (Grok)
- Subscription tracking incl. Grok -> SC featurePillars "AI Subscription Tracking"; CL 2.0.8 (Grok as a subscription, ChatGPT plan refresh)
- Focus Mode, warns at 80% and 100% -> SC FAQ "What is Focus Mode?"; CL 2.0.14 (Focus sessions restored)
- Usage Intelligence lenses + tabs, Pro -> SC proFeatures + pricingPlans PRO; CL 2.0 (Overview, Limit Runway, Efficiency, Plan Value; Timeline, Provider, Model, Project, Session tabs); CL 2.0.1 (dashboard gated to Pro)
- Budgets, CSV export, weekly summary, Pro -> SC pricingPlans PRO bullets
- Token Card, Pro -> SC proFeatures "Shareable Token Card"; CL 2.0 ("Free users could reach the Token Card" fixed = Pro-gated)
- Currency setting (EUR, GBP, more; user-set rate) -> CL 2.0.9 "Spend in your currency"
- Privacy Audit Log logs every outbound request with host, reason, time -> SC FAQ "How can I verify what the app is doing?"; CL 2.0 (audit log records every provider request before it is sent)

Supported providers
- "11 connect, 8 report real spend, rest limits or balance" -> PROV providerCoverageSentence / spendProviderCount; SC FAQ "What providers are supported?"
- Per-provider "what it reports" and "how it connects" -> REG descriptors (description, connectionMethod, capabilities). Codex = limits + spend; Copilot = spend + quota ("Copilot subscription value and premium-request quota"); OpenRouter = spend + balance + models ("spend, model mix, and remaining credits"); DeepSeek = balance only; Anthropic API/OpenAI/Mistral = admin keys
- Gemini "coming soon / not collecting" -> PROV COMING_SOON_PROVIDERS; REG availability .unavailable; SITE "Gemini (coming soon)"
- Admin-key caveat -> SC setupSteps "Connect"; PROV needsAdminKey
- Keychain storage, sent only to that provider -> REG guide steps; SC FAQ "What credentials does the app store"

Free vs Pro
- Every row -> SC pricingPlans FREE/PRO bullets and tierSnapshotCards (7-day vs 30-day history also in app UI/LaunchPriceEndingView.swift "free keeps 7 days"); Token Card row -> SC proFeatures
- Future updates included -> SC tierSnapshotCards "Lifetime updates"; SC FAQ "including all future updates"
- Per-Mac license -> SC FAQ "Can I use it on multiple Macs?"
- 14-day money-back -> SC pricingPlans PRO note; SC FAQ refund
- $7.99 launch buyers keep everything incl. future updates -> CL 2.0.12 "The launch price is ending"

Privacy and security
- SQLite on Mac, no cloud backend -> SC trustBadges + FAQ "Is my data sent to any server?"
- Only usage metadata kept, prompts never stored/sent -> SC FAQ "Does the app read my conversations or prompts?"
- Network calls = providers + license activation + update check -> SC FAQ "Is my data sent to any server?"
- Signed, hardened runtime, notarized -> SC FAQ "How can I verify what the app is doing?"
- Built in Germany -> SC privacyBadges + FAQ
- SECURITY.md link -> exists in REPO (see note below about its content)

Install
- Zip, drag to Applications -> SC setupSteps "Download"
- Sparkle auto-update; app asks when a version is ready -> app Info.plist SUFeedURL + Core/Utils/SparkleUpdater.swift; CL 2.0.12 "Updates actually install now"
- Data path ~/Library/Application Support/Tokens4Breakfast -> app Core/Storage/StorageManager.swift appSupportDirectory() appends "Tokens4Breakfast" (file data.db); PBX ENABLE_APP_SANDBOX = NO so the path is not containerized. CORRECTS the old README, which said "Tokens 4 Breakfast" with spaces.
- Keychain service com.onekapisch.tokensforbreakfast -> app Core/Utils/KeychainHelper.swift
- Requirements -> see header

Recent releases
- 2.0.16 latest, 19 Sep 2026 -> live appcast https://tokens4breakfast.app/appcast.xml top item "Version 2.0.16", pubDate Fri, 19 Sep 2026; SC whatsNewRelease
- Each highlight -> CL entries for 2.0.16, 2.0.15, 2.0.14, 2.0.10, 2.0.9, 2.0.6
- "What's New sheet" -> CL 2.0.6 / 2.0.15 reference the in-app What's New sheet

How it compares
- ccusage and CodexBar descriptions -> T4B Website origin/main src/lib/seo/comparison-pages.ts (slugs ccusage-gui, codexbar-alternative: "ccusage is a widely used command-line tool for analyzing local agent usage and costs"; "CodexBar is a strong free open-source menu bar tracker for coding-provider usage windows"). Pages return HTTP 200, as does /alternatives.

Roadmap
- "Many recent features started as requests" -> CL credits requesters in 2.0.5, 2.0.9, 2.0.10, 2.0.13, 2.0.14, 2.0.15

FAQ
- Gemini reason -> REG Gemini availability reason ("Google does not currently expose the authoritative account usage data T4B requires")
- Others -> as cited above

More from OneKapisch
- Taglines verbatim from STUDIO: Mac 4 Breakfast "Your one battery app that does it all."; LUMEL "Brighter than macOS allows. Darker than its minimum."; Clip 4 Breakfast "The clipboard manager that never slows your Mac down."; Chime 4 Breakfast "Run-completion alerts"; Easy Write "On-device writing tools"; SkyLocation "Know where you are. Without internet or signal."
- Links: STUDIO card links (mac4breakfast.app, getlumel.app, clip4breakfast.app, skylocation.app); GitHub repos per request, both confirmed public via gh api (onekapisch/chime-4-breakfast, onekapisch/easy-write). "Open source" = public repos (Easy Write repo description says open-source).

DELIBERATELY LEFT OUT (unverifiable, stale, or risky)
- "T4B users routinely find $40+/month they forgot" (old README) and the site's "$47/month" pull quote: no data source.
- Site testimonials (Alex M., Priya K., James T.): not verifiable.
- Old competitor table (e.g. "CodexBar / ClaudeBar: single provider", checkmark grid): not supported; CodexBar is multi-provider per the site's own comparison page. Replaced with the site's own one-line framings.
- Download size: SITE says "~10 MB", old README "~12 MB", live zip Content-Length is 11,111,933 bytes. Omitted, since it changes each release.
- "Under 2 minutes to set up": marketing claim, no measurement.
- "Plan Value can save $80-$180 per month" (SC FAQ): no source.
- "Typically < 30 MB RAM" (SC FAQ): not re-measured for 2.0.x.
- Claude Web connection details: sources disagree (SC FAQ says paste a sessionKey cookie; SC featurePillars says one tap via the Claude Code login; REG says "guided local session flow"). Draft uses REG's neutral wording.
- Morning digest, notch reset celebration, multi-machine rollup (roadmap), Pro Max: left out. Reset celebrations became Pro in 2.0.5, but the changelog says that was deliberately not announced publicly.
- Anything from 2.0.17 (Opus 5.5 pricing, fast-mode pricing): unreleased per CL / appcast.
- Version badge: repo has no GitHub Releases, so a dynamic release badge would show nothing.
- WiFi 4 Breakfast (on STUDIO but not in the requested list).

ISSUES FOUND OUTSIDE THIS README (not edited)
- REPO SECURITY.md is stale: data path "~/Library/Application Support/Tokens 4 Breakfast" (actual folder: Tokens4Breakfast), provider list includes Gemini as queried and omits Codex/Claude Web/Grok/Anthropic API, and the contact is kapisch@icloud.com while the app now uses support@onekapisch.com (CL 2.0.13).
- REPO CHANGELOG.md stops at 1.1.1 (June 2026), so the draft no longer points readers at it.
- REPO description still says "across 8 providers ... Cursor, Copilot, Gemini ...".
- T4B Website site-config.ts DEFAULT_GITHUB_URL still points to Tokens4Breakfast-daily.
- SC FAQ "Is my data sent to any server?" gives the legacy DB path ~/.tokensforbreakfast/data.db; the app migrated it to Application Support (StorageManager.swift).
- SC FAQ ClaudeMeter/SessionWatcher answers use stale counts ("7 additional providers", "6 additional providers").
-->
