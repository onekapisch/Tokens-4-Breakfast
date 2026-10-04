# Security & Privacy

Tokens 4 Breakfast is built local-first. This document explains exactly what data is handled and where it goes.

## Data flow
- **Storage:** all usage history and settings live in a local SQLite database on your Mac (`~/Library/Application Support/Tokens4Breakfast/`). Nothing is synced to a server we control. The database stores usage metadata only (models, token counts, costs, times), never prompt or response text.
- **Local sources, no key:** Claude Code and Cursor are read from local files; Codex, GitHub Copilot and Grok use your existing local CLI logins.
- **Claude Web:** your claude.ai session, connected through a guided step in Settings, is used only to read your plan limits from claude.ai.
- **API keys:** OpenAI, Anthropic API and Mistral (organization admin keys), OpenRouter and DeepSeek are queried directly from your Mac with your own keys, solely to fetch usage, cost or balance.
- **Credentials:** keys and sessions are stored in the macOS Keychain and sent only to the matching provider's official API.
- **No telemetry:** the app sends no analytics, no crash pings, and no usage data to us or any third party. The only other network calls are the Pro license check and the update check. Every outbound request appears in the in-app Privacy Audit Log.
- **No account:** there is no login and no user identifier.

## Reporting a vulnerability
Please email **support@onekapisch.com** with details and steps to reproduce. Do not open a public issue for security reports. We aim to respond within 72 hours.
