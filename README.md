# Reddit Task Desk updates

Current release: **1.16.9.0**.

The signed updater feed is `latest.json`. The app verifies the publisher signature, executable hash, size and version before installation.

Version 1.16.9 preserves coherent cumulative token usage through cancellation, serializes Codex shutdown, and improves private-detail-free startup access-denied diagnostics. It includes the 1.16.8 retry-reason, profile-list error, startup identity and browser observation fixes. Existing task settings, custom instructions and action history remain compatible.

The executable was cross-built and locally checked with focused regression suites and the shipped 1.16.7 updater verifier. Native 1.16.9 Windows/live AdsPower execution and installation were not rerun. Windows permission failures and AdsPower subscription restrictions are not claimed resolved.
