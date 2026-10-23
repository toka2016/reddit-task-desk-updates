# Reddit Task Desk updates

Current published release: **1.17.18.0**.

[Download the current application](RedditTaskDesk-1.17.18.0.exe). The signed automatic-update feed is [latest.json](latest.json). The app verifies the original publisher signature, executable hash, size and version. Installation waits for an idle state and keeps the existing data folder.

Version 1.17.18 adds the saved **Start with one clean tab (70% direct Reddit / 30% Google)** option. When enabled, startup creates a verified work tab in the configured AdsPower profile and closes that profile's recorded pre-existing page tabs, including unsaved drafts. Cookies and sign-in state remain. Each new session chooses its startup route once; preparation retries retain the route and completed cleanup. The startup Google query grants no task search permission. Google challenge, consent or login barriers stop the current run without declaring the Reddit account blocked.

Startup verifies the expected Reddit account without avatar input before native readiness, issue recovery or task planning. Bounded ordinary Windows activation does not depend on querying another foreground application's GUI thread. Strict checks still apply before title-bar pointer placement or click. Established foreground loss, Escape and uncertain input remain stopping conditions; no browser-input fallback or challenge bypass is introduced.

## Next release candidate

**1.17.21.0 is built and locally validated, but is not yet published to the automatic-update feed.** Publication requires the original publisher signing key.

Known returns to an observed community listing or feed now prefer the app's bounded, verified browser history path before a header link can reload the listing or fail outside the viewport. Post navigation still requires a currently visible eligible link. One-pixel clipped links are rejected before native pointer placement.

Foreground-loss diagnostics now describe the already-observed window/process relation: this app, the bound browser process, another process, or no foreground window. They include no window titles or page text. Diagnostics send no input, do not reacquire focus and cannot mask the stopping condition.

The reported run passed account verification, native readiness and read-only plan acceptance, opened one post, then later lost foreground while verifying a wheel event. The old log cannot identify which window took focus. The separate native screenshot limitation remains unresolved; it did not stop text browsing. This candidate does not claim a remedy for the external focus change or full live task completion. Established focus loss and uncertain input still stop further native input.

Validation passed: 187 focused offline groups and 50 browser DOM groups, including explicit and post-to-post community returns, lost-focus diagnostics, input failure policy, unknown-action preservation and screenshot authority boundaries. The listing-return regression failed before the fix and passed afterward. No live Reddit task, native Windows input or screenshot test was run for 1.17.21.

The candidate retains the earlier startup focus handoff, account/readiness diagnostics, bounded missing-page observation fixes and clean startup features. Built for Microsoft .NET Framework 4.7.2. Historical blockers and unknown actions remain preserved; inspect uncertain input before retrying.

The local Desktop shortcut opens the candidate after the older app is closed and the shortcut is reopened. The current signed automatic-update release remains **1.17.18.0**.
