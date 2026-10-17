# Reddit Task Desk updates

Current release: **1.16.6.0**.

The signed updater feed is `latest.json`. The app verifies the publisher signature, executable hash, size and version before installation.

Version 1.16.6 verifies the signed-in Reddit account once at session start. Browsing and actions then reuse that session binding without reopening or rescanning the account menu. New sessions verify again. Visible CAPTCHA, login and access-block detection remains active. Existing tasks, custom instructions and action history are preserved.
