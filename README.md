# Reddit Task Desk updates

Current published release: **1.17.23.0**.

[Download the current application](RedditTaskDesk-1.17.23.0.exe). The signed automatic-update feed is [latest.json](latest.json). The application verifies the original publisher signature, executable SHA-256, size and version. Installation waits for an idle state and uses the existing data folder.

## Dedicated task desktop

Enable **Instructions → Dedicated task desktop**, then choose **Save instructions** once per installation. The saved option applies to new manual and scheduled sessions. It defaults off; publishing this update does not override an existing disabled choice or automatically close other programs.

With the option enabled, startup prepares one work tab in the exact configured AdsPower profile and enters Reddit through browser control before native mouse input. It verifies the expected account without opening the avatar menu, maximizes the retained browser window, and requests ordinary closure of other application windows. AdsPower, Reddit Task Desk, the task browser and protected Windows UI remain. AdsPower process ancestry and signed identity must be verified first. A save prompt or unconfirmed closure stops preparation without force-killing or discarding content.

After preparation, task operations use Windows mouse/keyboard input with a mouse-only reservation. Keyboard remains available. **Ctrl+Alt+F8** or **Escape** releases the mouse and stops the session. Cancellation, deadline, foreground loss and watchdog failure also release control. The native driver remains bound to its released reservation, preventing late commands from falling back to unrestricted input. Windows can remove a slow low-level hook; this implementation checks event acknowledgements and does not claim infallible exclusion.

Dedicated finalization releases the mouse and attempts to close the exact profile whose open was requested, including completion, errors, user stop, manual barriers and uncertain-input paths. Closure is only confirmed after AdsPower reports `Inactive`. Unknown actions and unresolved historical issues remain recorded; closure does not authorize replay. If AdsPower cannot confirm closure, the report states that failure.

## Compatibility and rollout

1.17.23.0 is newer than 1.17.18.0, standalone 1.17.18.1 and candidate 1.17.22.0. It is based on 1.17.18 plus the dedicated-desktop changes and does not incorporate the unpublished 1.17.19–1.17.22 enhancements. The baseline keeps its 70% direct Reddit / 30% Google entry choice. Existing data-folder location and update trust key are unchanged; compatibility with unknown fields from unpublished candidates has not been certified. Keep a data backup when switching from an unpublished candidate.

Automatic-update availability is not proof of installation on every computer. Each running copy must use this feed, have automatic updates enabled, reach its check and become idle. Use **Settings → Updates → Check for updates** to check immediately, and confirm running version **1.17.23.0** after restart. The executable filename can still contain an older number because replacement happens in place.

## Validation

The unchanged dedicated-desktop implementation passed 11 focused offline/local-protocol routes. Release application/test builds, updater compatibility and the original publisher verifier were checked before feed activation. No native Windows input, live AdsPower/Google/Reddit task, rendered Windows UI or installed-upgrade test is claimed. Windows acceptance testing remains necessary for each actual desktop environment.
