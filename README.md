# Reddit Task Desk updates

Windows application downloads and the signed update feed for Reddit Task Desk.

## Download

[Download RedditTaskDesk-1.5.1.0.exe](https://raw.githubusercontent.com/toka2016/reddit-task-desk-updates/main/RedditTaskDesk-1.5.1.0.exe)

Close your previous copy, keep the application in a writable folder, then run the downloaded executable. Windows with .NET Framework 4.7.2 or later is required. Existing settings, profiles, tasks and reports stay in the same data folder. If you use a custom `--data-dir`, continue using that same argument.

## Automatic updates

Version 1.5.1 includes this update source by default:

`https://raw.githubusercontent.com/toka2016/reddit-task-desk-updates/main/latest.json`

In **Settings > Updates**, keep **Automatic updates** enabled. The application checks while idle at startup and approximately every six hours while running. It downloads a newer release and waits until the app is idle, with no queued sessions, unsaved settings or imminent scheduled task, before replacement and restart. Previously disabled automatic updates and custom update sources remain unchanged.

The updater authenticates an RSA-SHA256 signed manifest using its embedded public key, then checks the executable size, SHA-256, product identity and version before installation. This is an application update signature; the executable does not have a Windows Authenticode signature.

The private signing key and application data are not stored in this repository. This repository contains only public release binaries, the signed feed and this documentation. Future updates become available when a newer signed release is published here.

## Validation limits

The build and offline update/migration tests were run against Microsoft .NET Framework 4.7.2 reference assemblies. Native Windows GUI operation and the Windows replacement/restart process still require validation on Windows.
