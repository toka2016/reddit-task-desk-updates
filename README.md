# Reddit Task Desk updates

Current release: **1.17.0.0**.

The signed updater feed is `latest.json`. The app verifies the publisher signature, executable hash, size and version before installation.

Version 1.17.0 adds **Use Windows desktop mouse and keyboard**, enabled by default for new sessions. Native movement, clicks, wheel scrolling and text/key input use Windows itself; browser observations locate the exact controls and verify outcomes. The bound AdsPower window needs an unlocked active Windows desktop. Hold Escape or switch foreground to stop input. Unsupported or unavailable native input does not silently fall back to DOM or browser-only clicks.

Instructions save/revert, previews, per-session snapshots and reports include the mode. Desktop counters are distinct from confirmed Reddit actions. Existing prompts, guides, profiles, schedules, history and historical session input modes remain preserved. An explicit checkbox opt-out selects the prior browser adapter for new sessions.

The executable was cross-built against Microsoft .NET Framework 4.7.2 and checked with focused synthetic driver, DOM, settings/UI and lifecycle tests. The original shipped 1.16.7 updater accepted the signed 1.17.0 package. **Native Windows, RDP/DPI cursor calibration, AdsPower UI Automation, live Reddit actions and installed upgrading remain unverified here.** Offline tests do not certify those paths. Windows permission failures and AdsPower subscription restrictions are not claimed resolved.
