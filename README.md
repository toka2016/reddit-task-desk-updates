# Reddit Task Desk updates

Windows application downloads and the signed update feed for Reddit Task Desk.

## Download

[Download RedditTaskDesk-1.11.1.0.exe](https://raw.githubusercontent.com/toka2016/reddit-task-desk-updates/main/RedditTaskDesk-1.11.1.0.exe)

Close your previous copy, keep the application in a writable folder, then run the executable. Windows with .NET Framework 4.7.2 or later is required. Existing settings, profiles, tasks and reports stay in the same data folder. If you use a custom `--data-dir`, continue using that argument.

## One clear launch file and an app icon in 1.11.1

Continue opening the same **Reddit Task Desk** shortcut or the current executable. Updates replace that file in place. New update candidates and retained recovery backups are stored in a private hidden subfolder on the same drive, keeping them out of the main application-folder view. **Settings > Launch app** shows the current executable and provides **Organize update files** for older updater-owned backups.

Completed older backups are moved only when their private update plan, successful startup marker and file hashes establish that they belong to this app and the old helper has finished. Recovery copies remain available. Unrecognized files and manually downloaded versioned executables are preserved; filenames alone never authorize moving them. Profiles, tasks, reports and the active data folder stay unchanged.

The executable now contains an original navy-and-coral task icon in multiple resolutions. The app window, taskbar, notification-area icon and app shortcuts use it. There is no loose icon file to keep beside the executable.

## Automatic AdsPower profile import in 1.11.0

Open AdsPower with Local API enabled and save its connection in the app. **Profiles** automatically imports the available profiles at startup and after connection changes, using the saved MCP connection. **Refresh from AdsPower** runs it manually; **Cancel sync** stops an active import. The automatic option is visible and can be disabled.

The import reads profile IDs and names without opening profile browsers or requesting model generation. It adds new IDs once and preserves existing custom names, expected Reddit usernames, task bindings and reports. Profiles absent from a later response are not deleted. Profiles removed in this app stay excluded until **Restore hidden profiles** is selected.

A valid, unambiguous Reddit username in explicit AdsPower Reddit-platform metadata can prefill the expected account. Otherwise the profile shows **Account not set**: edit it once to enter the expected Reddit username before creating tasks. Metadata does not establish which account is signed in; session identity checks remain in place.

All pages must be fetched successfully before settings change. Errors leave existing data intact and appear in Profiles and Activity. Automatic import yields to active, queued and imminent scheduled sessions. Private response fields such as account passwords, cookies and proxy credentials are not saved or sent to a model.

## A clear app shortcut in 1.10.1

Use **Reddit Task Desk** on your desktop or in the Windows Start menu to reopen the app after an update. The first supported Windows launch attempts to create these per-user shortcuts; shortcut errors remain visible without preventing the app from starting. **Settings > Launch app** shows the actual executable location, individual shortcut results, **Create / repair shortcuts**, and **Open app folder**. Shortcuts preserve the active data folder. They do not enable startup with Windows.

The updater continues replacing the running executable in place, so its filename may retain an older version number. The shortcut remains the launch entry. New update handoffs use `.tmp` candidates and `.bak` recovery backups instead of additional launchable `.exe` copies beside the app. Upgrades from older versions still accept their exact legacy handoff paths; old recovery files are not silently deleted. Keep the executable in its folder, or repair the shortcuts after moving it. Conflicting unrelated shortcuts are preserved and reported.

## Calmer browsing in 1.10.0

Open **Settings > Browsing pace** to set a minimum time on each readable page, an interval between supported browser actions, and a pause after scrolling. The initial settings are **12 seconds**, **3 seconds**, and **2 seconds**. These are minimums: time already spent reading or reasoning counts, so the app waits only for the remaining time. Set a value to zero to disable that added wait, use **Calm defaults** to restore the initial pace, or **No added waits** to clear all three delays. Click **Save browsing pace** to apply changes to new sessions.

**Reuse the current page** checks the browser's actual URL and readable state before avoiding a redundant reload. The app can start from an already open supported Reddit page instead of resetting it to Home. Identity checks, actual task scope and observed feed provenance still apply. No close-browser operation is added; browser lifetime also depends on the external AdsPower connector.

Waits run locally without model requests, cancel with Stop and remain inside the existing session duration. That duration is an upper bound, not a target to fill. Reports show the saved pace and actual added wait time; waiting is not reported as human reading. Queued sessions and later approvals retain their recorded pace. Historical sessions without a pace snapshot keep the previous behavior for later approvals. Unsaved pace edits delay automatic update installation.

A manual challenge appearing during a wait is checked before navigation or action. An external page change during a wait cannot authorize a click on an unrelated discussion. Post-submission verification is not artificially delayed; uncertain submitted actions still require manual inspection.

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
