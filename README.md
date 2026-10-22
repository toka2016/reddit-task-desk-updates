# Reddit Task Desk updates

Current published release: **1.17.18.0**.

[Download the current application](RedditTaskDesk-1.17.18.0.exe). The signed automatic-update feed is [latest.json](latest.json). The app verifies the original publisher signature, executable hash, size and version. Installation waits for an idle state and keeps the existing data folder.

Version 1.17.18 adds the saved **Start with one clean tab (70% direct Reddit / 30% Google)** option. When enabled, startup creates a verified work tab in the configured AdsPower profile and closes that profile's recorded pre-existing page tabs, including unsaved drafts. Cookies and sign-in state remain. Each new session chooses its startup route once; preparation retries retain the route and completed cleanup. The startup Google query grants no task search permission. Google challenge, consent or login barriers stop the current run without declaring the Reddit account blocked.

Startup verifies the expected Reddit account without avatar input before native readiness, issue recovery or task planning. Bounded ordinary Windows activation does not depend on querying another foreground application's GUI thread. Strict checks still apply before title-bar pointer placement or click. Established foreground loss, Escape and uncertain input remain stopping conditions; no browser-input fallback or challenge bypass is introduced.

## Next release candidate

**1.17.19.0 is built and locally validated, but is not yet published to the automatic-update feed.** Publication requires the original publisher signing key.

The candidate separates account verification from desktop readiness, preserves the current session's verified account through desktop-only preparation retries, and retries only missing page observations within bounded read-only limits. It preserves the 1.17.18 startup features and historical uncertainty protections.

Validation passed: 307 focused offline/loopback groups, 175 synthetic DOM checks, and 29 Windows settings UI assertions. The UI fixture's expected native save-error dialog was acknowledged separately. These checks do not establish live AdsPower/Google/Reddit operation, actual browser input, or an installed upgrade. No real Reddit task or social action was run for these checks.

Built for Microsoft .NET Framework 4.7.2. Historical blockers and unknown actions remain preserved; inspect uncertain input before retrying.
