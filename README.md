# Reddit Task Desk updates

Current published release: **1.17.18.0**.

[Download the current application](RedditTaskDesk-1.17.18.0.exe). The signed automatic-update feed is [latest.json](latest.json). The app verifies the original publisher signature, executable hash, size and version. Installation waits for an idle state and keeps the existing data folder.

Version 1.17.18 adds the saved **Start with one clean tab (70% direct Reddit / 30% Google)** option. When enabled, startup creates a verified work tab in the configured AdsPower profile and closes that profile's recorded pre-existing page tabs, including unsaved drafts. Cookies and sign-in state remain. Each new session chooses its startup route once; preparation retries retain the route and completed cleanup. The startup Google query grants no task search permission. Google challenge, consent or login barriers stop the current run without declaring the Reddit account blocked.

Startup verifies the expected Reddit account without avatar input before native readiness, issue recovery or task planning. Bounded ordinary Windows activation does not depend on querying another foreground application's GUI thread. Strict checks still apply before title-bar pointer placement or click. Established foreground loss, Escape and uncertain input remain stopping conditions; no browser-input fallback or challenge bypass is introduced.

## Next release candidate

**1.17.22.0 is built and locally validated, but is not yet published to the automatic-update feed.** Publication requires the original publisher signing key.

Adds **Instructions → Always use direct Reddit entry**. When saved, a new clean session opens Reddit Home directly, then performs the same account verification, native readiness and finite-plan checks. The setting is frozen into the session, instruction preview and report. Unchecked or missing values retain the earlier 70% direct Reddit / 30% Google choice. Preparation retries keep the selected route.

Read-only inspection of a failed startup found a visible Reddit result whose actual Google anchor was an opaque `/goto` URL. Its displayed citation did not establish the destination before a click. These rendered opaque result links now end the session with **GOOGLE_RESULT_DESTINATION_UNVERIFIED**, a compatibility explanation and guidance to save direct startup for a new session. They are not clicked or guessed. No automatic direct fallback, new persistent profile/task pause, Reddit account-access block or task authority is introduced.

Validation passed: **128 focused offline groups, 49 browser DOM groups and eight Windows settings UI groups**, including the direct choice overriding a Google draw, frozen settings, historical behavior, opaque-link no-replay, unknown-action preservation and minimum-size layout. The opaque-link regression failed against the prior payload and passed against the candidate. Live Google DOM was inspected read-only; no live native Reddit task or full three-post completion is claimed.

The candidate retains known-listing history returns, foreground-loss diagnostics, the startup focus handoff, bounded page observations and clean-tab startup. Earlier foreground interruptions and native screenshot limitations are separate and remain unresolved. Established focus loss and uncertain input still stop native input; historical issues remain preserved.

Built for Microsoft .NET Framework 4.7.2. The local Desktop shortcut opens the candidate after it is reopened. The current signed automatic-update release remains **1.17.18.0**.
