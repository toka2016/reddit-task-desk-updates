# Reddit Task Desk updates

Current release: **1.17.1.0**.

The signed updater feed is `latest.json`. The app verifies publisher signature, executable hash, size and version before installation.

1.17.1 improves native Windows input startup compatibility. It waits briefly for the exact AdsPower window marker and initial foreground/page focus; it sends no repeated activation. Cursor movement uses one position request and bounded read-only settling, then retains exact target/foreground checks before clicks. Calibration avoids expecting a new event from zero movement. Numeric pointer diagnostics do not assume human interference.

Profile-import connection failures now identify the local connect stage. The reported generic RPC -32603 root cause is not established or claimed fixed. Existing settings, prompts, profiles, action permissions and history remain preserved. Native Windows input remains enabled when saved; no silent browser-input fallback is added.

Built against Microsoft .NET Framework 4.7.2. Focused driver, DOM, integration, connection, identity and instruction tests passed offline. The shipped original 1.16.7 updater accepted the signed package. **Actual Windows/RDP, AdsPower native input and installed upgrade remain unverified here.** No VPS connection or live Reddit action was performed.
