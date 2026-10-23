# Reddit Task Desk updates

Current published release: **1.17.26.0**.

[Download the current application](RedditTaskDesk-1.17.26.0.exe). The signed update feed is [latest.json](latest.json). The app verifies the publisher signature, executable SHA-256, size and version before installation. Updates wait for an idle state and use the existing data folder.

## Instruction sources and community rules

Open **Instructions → Community rules guidance** to see and edit the application's rules-reading guidance. Choose **Save instructions** to apply it to sessions created afterward. Clearing this section removes the app's additional reading mandate; a custom task prompt or another saved guide may still request rules reading. Respecting an observed restriction and proving a page was read remain different concepts.

The default requests rules before participation, without requiring a rules-page visit for read-only tasks. Exact old bundled Agent Rules move their reading instructions into this section. Custom Agent Rules remain unchanged. Queued and historical session snapshots retain their original instruction semantics, including the older fixed tool-description wording where applicable.

Use **Instruction sources** for a map of application instruction origins, phases, edit locations and fixed technical contracts. The selected task's full effective preview is included, with later publication templates explicitly labelled. Use **Preview instructions** to inspect unsaved drafts, or **Sessions → Recorded instructions** to inspect captured session payloads. Search for `rules`, `suffix`, `startup`, or another term using the viewer's search controls. Viewing alone makes no model or browser request.

The map explains application-owned instructions. It does not reveal provider-internal instructions or pretend to reconstruct unrecorded historical requests or future tool results. Account verification, exact action targets/text, budgets, emergency release and unknown-action replay checks remain technical controls; editing guidance cannot redefine tool schemas or bypass those checks.

## Startup window recovery

Version 1.17.25 fixes dedicated-desktop preparation being permanently marked incomplete after a native window lookup failed before any application close request. A bounded, cancellable observation period tolerates delayed native window-title updates. A later preparation attempt may retry when no close request was attempted. Actual attempted closes, including refused or uncertain requests, retain their no-repeat protection.

Logs now distinguish page marker verification, absent or ambiguous native marker matches, and whether the exact window matches the foreground window. A background window can still be identified; foreground mismatch is not proof of occlusion. No guessed window, forced process termination, or save-dialog dismissal is used. Failed page-marker cleanup retains its nonce for exact cleanup before a retry.

## Editable behavior settings

Open **Instructions** to edit the comment footer, startup route probability, desktop-input options and shared guidance, then choose **Save instructions**.

- **Comment footer:** choose AI-generated, AI-assisted, Custom text, or None. The sample preview shows the application's transformation. None means no automatic suffix; any suffix supplied in the original text remains. Both comments and replies use the saved setting. The default stays AI-generated until explicitly changed.
- **Google startup percentage:** choose 0–100. Zero means direct Reddit only, 100 means Google only, and the default is 30. The value is used only with clean-tab startup. It is a probability per new session, not a required sequence of sessions. Preparation retries retain the chosen route. Startup search does not grant task-search permission.
- **Settings map:** the page identifies where to edit the task prompt, model, reasoning effort, action limits, browsing pace, scheduling, duration, token threshold, connections and automatic updates. The selected-task shortcut opens the existing task editor.
- **Additional behavior guidance:** editable instructions to the model are identified separately from actual runtime settings. Technical account/target checks, uncertain-action replay protection, emergency stop and tool-interface limits remain visible application constraints.

Shared changes apply to new sessions after saving. Already queued/running sessions and historical drafts retain their snapshots and exact stored text. Session duration and token stop threshold have a separate live editor; during native input use **F8** for its handoff. Instruction previews show saved or explicitly marked unsaved settings without starting a model or browser.

## Dedicated task desktop

The existing opt-in **Dedicated task desktop** setting prepares one work tab in the configured AdsPower profile, enters Reddit through the browser connection, verifies the account, maximizes the task window and requests normal closure of other applications while retaining AdsPower and this app. Save prompts are not dismissed and processes are not force-killed.

Task input uses the Windows pointer. **Ctrl+Alt+F8** or **Escape** restores the mouse and stops the session; the keyboard remains available. Finalization releases the mouse and attempts to close the exact task profile, including error and stop paths. Closure is only confirmed after AdsPower reports Inactive. Unknown Reddit action results remain unknown and are never replayed automatically.

## Updating and validation

The release builds on published 1.17.25.0. Default footer and startup choices preserve existing behavior. The data-folder location and publisher trust key are unchanged. This version does not incorporate unrelated unpublished 1.17.19–1.17.22 changes.

Use **Settings → Updates → Check for updates**, then confirm running version **1.17.26.0** after restart. Automatic-update availability does not prove installation on every computer. Each copy must reach the configured feed, have updates enabled and become idle. In-place replacement can retain an older executable filename.

Local application/test builds and focused offline policy/controller regression checks are recorded with the release. Native Windows rendering/input, a live AdsPower/Reddit session and an installed upgrade on the user's VPS have not been tested from this environment.
