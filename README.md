# Reddit Task Desk updates

Current published release: **1.17.18.0**.

[Download the current application](RedditTaskDesk-1.17.18.0.exe). The signed automatic-update feed is [latest.json](latest.json). The app verifies the original publisher signature, executable hash, size and version. Installation waits for an idle state and keeps the existing data folder.

Version 1.17.18 adds the saved **Start with one clean tab (70% direct Reddit / 30% Google)** option. When enabled, startup creates a verified work tab in the configured AdsPower profile and closes that profile's recorded pre-existing page tabs, including unsaved drafts. Cookies and sign-in state remain. Each new session chooses its startup route once; preparation retries retain the route and completed cleanup. The startup Google query grants no task search permission. Google challenge, consent or login barriers stop the current run without declaring the Reddit account blocked.

Startup verifies the expected Reddit account without avatar input before native readiness, issue recovery or task planning. Bounded ordinary Windows activation does not depend on querying another foreground application's GUI thread. Strict checks still apply before title-bar pointer placement or click. Established foreground loss, Escape and uncertain input remain stopping conditions; no browser-input fallback or challenge bypass is introduced.

## Next release candidate

**1.17.20.0 is built and locally validated, but is not yet published to the automatic-update feed.** Publication requires the original publisher signing key.

Adds **Focus browser for startup** in the Tasks toolbar after a known no-input initial activation failure. While the app is foreground, the owner can request ordinary Windows activation of the exact pinned profile window. Fresh preparation still verifies the account and native readiness before any plan or task browsing. The control cannot reactivate an already prepared session, reacquire established lost focus, repeat uncertain input, reset automatic activation limits or target another session/profile. Windows may still decline activation; no foreground restriction is bypassed.

The candidate also retains the 1.17.19 account/readiness diagnostics and bounded missing-page observation fixes, along with the 1.17.18 clean startup features.

Validation passed: 143 focused offline groups and seven Windows toolbar UI groups, including minimum-size layout. A scoped native test used the compiled candidate and exact marked browser; real Windows activation was accepted and the bound browser was observed foreground. Only the waiting state in a standalone driver instance was simulated. No native mouse/keyboard input or Reddit task was run. This does not establish full live task completion, and the reported earlier access-denied condition was not reproduced in current read-only checks.

Built for Microsoft .NET Framework 4.7.2. Historical blockers and unknown actions remain preserved; inspect uncertain input before retrying.
