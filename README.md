# Reddit Task Desk updates

Windows application downloads and the signed update feed for Reddit Task Desk.

## Download

[Download RedditTaskDesk-1.8.0.0.exe](https://raw.githubusercontent.com/toka2016/reddit-task-desk-updates/main/RedditTaskDesk-1.8.0.0.exe)

Close your previous copy, keep the application in a writable folder, then run the downloaded executable. Windows with .NET Framework 4.7.2 or later is required. Existing settings, profiles, tasks and reports stay in the same data folder. If you use a custom `--data-dir`, continue using that same argument.

## Red blocked tasks and repair in 1.8.0

Technical problems stop affected sessions as **Blocked**, with red task/profile indicators and a panel showing the reason, diagnostic code and repair steps. Normal runs and schedules stay paused until the issue is repaired. Profile-level issues pause other tasks sharing the same profile. Saved schedules are preserved, and pause records survive restarting the application.

After fixing the reported problem, choose **Retry after fix**. It starts a fresh session using the current task settings and keeps the barrier active until that session succeeds. Failed or interrupted retries stay blocked. Reports retain original outcomes and retry history; uncertain submissions are never replayed. **View issue report** opens the source session. The app checks supported visible CAPTCHA/login/access screens and provides a model report_issue tool for technical blockers. CAPTCHA is completed manually; unsupported future site layouts may require the agent or user to identify the issue.

## Profile tasks and organized reports in 1.7.0

In **Tasks**, select a profile in the left panel to see its tasks, or choose **All profiles**. New tasks preselect the current profile. **Profiles > View tasks** and **Tasks > View task reports** provide direct navigation.

**Sessions & reports** now groups history by **profile > task**, with the newest sessions first. **Open task report** opens a saved aggregate containing confirmed actions, pending/unknown outcomes, token totals, errors and links to every session report. Tasks without sessions have an empty state; deleted or reassigned tasks remain accessible in historical groups under their original profile. Existing session files and daily reports stay in their original locations, and grouping uses stable identities rather than display names.

## Automatic comments in 1.6.1

Open **Tasks > Edit > Task & limits > Comment publication** and enable **Publish comments automatically**. This option works in Fields and Prompt modes and remains off by default for existing and new tasks. Enabled tasks can publish eligible comments without a separate confirmation, within saved community/action limits and the remaining session time/token budget. Comments are verified before they count as confirmed, and reports record whether authorization came from the task setting or a later human approval.

Explicit requests to prepare drafts for review remain in the approval queue; remove such wording from your task prompt when you want automatic publication. Changing the checkbox does not publish old pending drafts. Unsent automatic comments cancel on stop or restart, and uncertain submissions are never retried automatically. All community, account and duplicate protections remain active.

## Prompt mode

Open **Tasks > Edit > Task setup > Prompt** and enter the full task in **Task prompt**. Saved community selections and comment, upvote, review, search and scroll fields are disabled and ignored. The model creates a finite session plan from the prompt before browsing; actual limits and chosen communities appear in the session report. Communities can be different from those saved in Fields mode.

The chosen profile, model, session duration, token threshold and schedule remain controlled by the app. Comment publication follows the task checkbox; explicit review drafts still require approval. If an action is not requested, it stays disabled. If comments or upvotes are explicitly requested without a count, default ceilings are 3 comments or 5 upvotes; these are maxima, not activity targets.

Community candidates are selected before browsing, then checked for relevance and applicable participation rules. This release does not add a site-wide discovery search. Existing tasks keep Fields mode until you choose Prompt.

## Automatic updates

Version 1.5.1 includes this update source by default:

`https://raw.githubusercontent.com/toka2016/reddit-task-desk-updates/main/latest.json`

In **Settings > Updates**, keep **Automatic updates** enabled. The application checks while idle at startup and approximately every six hours while running. It downloads a newer release and waits until the app is idle, with no queued sessions, unsaved settings or imminent scheduled task, before replacement and restart. Previously disabled automatic updates and custom update sources remain unchanged.

The updater authenticates an RSA-SHA256 signed manifest using its embedded public key, then checks the executable size, SHA-256, product identity and version before installation. This is an application update signature; the executable does not have a Windows Authenticode signature.

The private signing key and application data are not stored in this repository. This repository contains only public release binaries, the signed feed and this documentation. Future updates become available when a newer signed release is published here.

## Validation limits

The build and offline update/migration tests were run against Microsoft .NET Framework 4.7.2 reference assemblies. Native Windows GUI operation and the Windows replacement/restart process still require validation on Windows.
