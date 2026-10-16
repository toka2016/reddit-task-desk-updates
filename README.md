# Reddit Task Desk updates

Current release: **1.16.3**.

This repository hosts the signed Windows update feed and versioned executable for Reddit Task Desk. The app verifies the signed manifest and executable hash before installing an update.

## Release 1.16.3

Browser history return now uses a guarded Back operation with actual arrival verification. Visible Reddit search filters and community sorting menus have additional supported forms. When a requested search filter is unavailable, readable same-query results can be returned with their actual filters and an explicit incomplete status.

User task/profile data and custom instructions remain unchanged. Profile import's unclassified plain-text error is not claimed fixed; it needs the actual underlying error for diagnosis.

The release was checked with offline DOM and MCP fixtures; those checks do not guarantee every live Reddit layout. No live Reddit action or user profile was used for verification.

Use the app's **Settings → Updates** or the versioned executable referenced in `latest.json`.
