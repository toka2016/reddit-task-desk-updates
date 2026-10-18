# Reddit Task Desk updates

Current release: **1.17.2.0**.

The signed updater feed is `latest.json`. The app verifies publisher signature, executable hash, size and version before installation. Use the existing application with automatic updates enabled; installation waits for an idle state. Settings and action history stay in their existing data folder.

1.17.2 improves native Windows foreground and pointer readiness using bounded observations after one activation/placement request. Known readiness failures before click/key/wheel dispatch are recoverable without new permanent pauses. During reasoning, recovery uses fresh inspection within existing task limits. Unknown or possibly submitted actions are never automatically repeated; historical manual-intervention blockers remain preserved.

Profile import retries eligible unclassified plain-text responses on the same page at most twice, without importing partial lists. Known subscription or permission failures remain distinct. The editable Workflow guide explains bounded recovery; only the exact previous bundled default is migrated, preserving custom and empty guidance.

Built against Microsoft .NET Framework 4.7.2. Focused offline regression suites passed. The unchanged original 1.16.7 updater accepted the signed 1.17.2 package using the original pinned key. **Actual Windows/RDP, AdsPower native input, live Reddit and installed upgrading remain unverified here.** Native mouse and keyboard still need an unlocked interactive desktop; this release cannot guarantee foreground access or completion of every task.
