# Reddit Task Desk updates

Current release: **1.15.0**.

This repository serves the signed update feed for Reddit Task Desk. Use the existing application shortcut and its automatic updater.

Version 1.15.0 adds prompt-controlled community joining through the attached AdsPower browser. A separate maximum of 0–20 new joins is recorded in the accepted plan. The app verifies the exact community and account, clicks Join once, and checks membership. Already-present memberships and uncertain outcomes remain distinct in reports. Existing task prompts and historical snapshots are preserved. No browser extension is required.

Local synthetic validation does not guarantee compatibility with every live Reddit layout. No live Reddit actions were used to prepare this release.

The signed manifest is latest.json. Executables use immutable versioned filenames; the updater verifies their signature, size and SHA-256 before replacement. This repository contains no credentials or user account data.
