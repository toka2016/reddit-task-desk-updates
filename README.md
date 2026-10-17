# Reddit Task Desk updates

Current release: **1.16.4**.

This repository hosts the signed Windows update feed and versioned executable for Reddit Task Desk. The app verifies the signed manifest and executable hash before installing an update.

## Release 1.16.4

Account verification uses native browser pointer input for the observed account control when supported, rechecks the control before clicking, and confirms the account from fresh UI evidence. A click acknowledgement is not proof of identity. An uncertain click is not repeated. Older compatible servers retain one validated DOM fallback, and account-menu failures include a fixed activation diagnostic.

User task/profile data and custom instructions remain unchanged. The separate profile-import plain-text error is not claimed fixed.

Verification used offline DOM and MCP fixtures. The user's exact live Reddit layout was not reproduced, and no live Reddit actions were performed.

Use the app's **Settings → Updates** or the versioned executable referenced in `latest.json`.
