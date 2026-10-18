# Reddit Task Desk updates

Current release: **1.17.3.0**.

The signed updater feed is `latest.json`. The existing app verifies the publisher signature, executable hash, size and version. Automatic installation waits for an idle state and keeps the existing data folder.

The configured reasoning model now starts before browser/account preparation. It calls `prepare_session`, receives readiness diagnostics, and chooses cancellable waits and retries within the same session time and token budget. No fixed two-attempt quota applies. Plan acceptance, browsing and actions remain unavailable until the expected account is verified. Repeated preparation after success reuses that binding.

Native startup can try one guarded real Windows click on a verified exposed title-bar point of the exact AdsPower window after the initial foreground request fails. No uncertain click is repeated. An unavailable desktop can be rechecked during preparation only when the native error proves no input may have been sent; the app does not unlock Windows or bypass desktop restrictions. Confirmed profile cleanup ownership survives same-profile preparation retries.

The Tasks panel now identifies saved profile/task issues and their original session separately from the latest outcome. Historical blockers and unknown actions remain preserved. Inspect prior uncertain input before using Retry after fix; creating a task does not clear an old profile issue.

Built against Microsoft .NET Framework 4.7.2. Focused offline regressions passed. The unchanged shipped 1.16.7 updater accepted the signed package using the original pinned key. **Actual Windows/RDP operation, installed upgrading, AdsPower native input and live Reddit remain unverified here.** Native mouse and keyboard require an unlocked interactive desktop. Recovery does not guarantee every goal will complete.
