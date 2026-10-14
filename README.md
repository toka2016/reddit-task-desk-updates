# Reddit Task Desk updates

Windows application downloads and the signed update feed for Reddit Task Desk.

## Download

[Download RedditTaskDesk-1.9.0.0.exe](https://raw.githubusercontent.com/toka2016/reddit-task-desk-updates/main/RedditTaskDesk-1.9.0.0.exe)

Close your previous copy, keep the application in a writable folder, then run the executable. Windows with .NET Framework 4.7.2 or later is required. Existing settings, profiles, tasks and reports stay in the same data folder. If you use a custom `--data-dir`, continue using that argument.

## Instruction visibility and control in 1.9.0

**Settings > Agent Rules** remains the shared participation guidance editor. **Settings > Workflow instructions** now exposes editable General workflow, Prompt planning, Adaptive browsing and Comment publication guidance, plus five Prompt planning defaults. An empty section stays empty. Changes apply to new sessions; queued sessions and pending drafts retain their saved instructions.

**Preview instructions** shows app-generated developer instructions, the task prompt and tool definitions without connecting or running a model. The publication reference uses explicit placeholders. **Tasks > Instructions** previews the saved task/settings; the Settings preview can include unsaved drafts. **Sessions & reports > Recorded instructions** shows the recorded request payloads and dispatch state for the selected session, including accepted-plan and publication phases. Session reports save the same trace. Historical payloads that were not recorded are not invented. Secret-like values are redacted in saved/viewed copies.

**Settings > App controls** explains the fixed execution checks, supported bounds and their reasons. Account identity, saved action limits, exact-text authorization, disclosure and uncertain-action protection remain enforced. This view covers Reddit Task Desk's assembled instructions; it does not expose or override OpenAI service/model instructions or externally configured Codex instructions.

## Home, Popular and All

In Fields mode choose the browsing scope **Home**, **Popular**, **All**, or selected **Communities**. In Prompt mode name the feed you want. Home uses the actual signed-in Reddit homepage at `/`, not Popular. A feed task can open posts observed in that feed and read those posts' real community rules; it does not invent rules for r/popular or grant unrestricted community browsing. Search is disabled for feed-only tasks. Returning to the feed and scrolling may reveal more posts while retaining the shared action ceilings.

Observed post provenance is saved in the session report. The app still requires reading the selected post before an action, checks the account and limits, and records only verified results as confirmed.

## Manual-intervention pauses

The 1.8.1 correction remains: ordinary loading, network, model and known no-click errors do not disable future tasks. A run can fail or complete with recoverable errors. Persistent red pauses require manual intervention, such as CAPTCHA, required sign-in/account verification, account mismatch, access restriction, uncertain submitted action, or critical history/storage/callback problems. Use **Retry after fix** after addressing a manual issue. Unknown actions are never replayed automatically.

## Automatic updates

In **Settings > Updates**, keep **Automatic updates** enabled. The default feed is:

`https://raw.githubusercontent.com/toka2016/reddit-task-desk-updates/main/latest.json`

The app checks while idle at startup and approximately every six hours while running. It waits for no active or queued sessions, unsaved edits, owned dialogs or imminent scheduled task before replacement and restart. Existing disabled update settings and custom sources stay unchanged.

An RSA-SHA256 signed manifest is verified using the embedded public key, followed by executable size, SHA-256, product and version checks. This application update signature is separate from Windows Authenticode; the executable is not Authenticode-signed. The private signing key and application data are never stored in this public repository.

## Validation limits

Builds target Microsoft .NET Framework 4.7.2 references. Tests use offline controller/browser peers, DOM fixtures and a Mono/Xvfb UI harness. Native Windows UI, actual Windows update replacement/restart and live AdsPower/Reddit/model execution remain unverified in this environment. No live social actions or paid inference are used for release verification.
