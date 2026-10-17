# Reddit Task Desk updates

Current release: **1.16.5**.

This repository hosts the signed Windows update feed and versioned executable for Reddit Task Desk. The app verifies the signed manifest and executable hash before installing an update.

## Release 1.16.5

When the account-menu control changes before clicking, the adapter can discard the stale reference and bind the current eligible control again at most twice. Each attempt stays on the original page and account, rechecks current identity and the control, and stops on persistent instability. Dispatched or uncertain opener clicks are never repeated.

Fixed diagnostics identify changed nodes, markers, metadata, ancestry, page, account or expiry, and report the refresh count. User profiles, tasks, schedules, custom instructions and action history are preserved.

Verification uses offline DOM and MCP fixtures. The user's exact live Reddit layout was not reproduced, and no live Reddit action was performed.

Use the app's **Settings → Updates** or the versioned executable referenced in `latest.json`.
