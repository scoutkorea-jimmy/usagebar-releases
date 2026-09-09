# Jimmy Assist — AI Fuel Gauge

Formerly UsageBar. A small macOS menu-bar app for tracking AI subscription usage. Apple Silicon, macOS 13 or later.

- Used / remaining display, reset countdown and refresh timestamps
- Claude subscription usage, including server-reported Fable limits, via your own sign-in session
- ChatGPT subscription Codex limits via the official local Codex app-server and your existing login
- Configurable refresh intervals and low-remaining notifications
- In-app signed updates powered by Sparkle, including delta patches when available

The ChatGPT meter shows Codex subscription limits. Regular-chat message counts are not supported. ChatGPT desktop or a supported local Codex CLI installation is required for this connection. No account sessions or user preferences are included in this repository or in the release files.

This repository contains public release files and the signed update feed. It does not contain signing private keys. The app currently uses a local ad-hoc code signature; Apple Developer ID signing and notarization are not available for this build.

Download an initial installation from [Releases](https://github.com/scoutkorea-jimmy/usagebar-releases/releases). Afterwards, use the app's update button or automatic updates; manual reinstalls are not required.

Updates use HTTPS and Ed25519 signatures for both the feed and payloads. The app checks automatically every six hours when enabled. Downloaded automatic updates install at app exit; you can also install immediately from the update dialog.


Version 0.4.0 adds a distinct Control Room, pause/resume, network-aware polling, helper timeouts and redacted connection diagnostics. Codex reset coupons display their available count and earliest expiry; redemption requires explicit confirmation and preserves an idempotency key across uncertain requests and restarts. There is no automatic redemption or purchase. Claude promotions are accessed through its official usage screen.

The internal bundle identifier and UsageBar.app install path remain unchanged for update and account compatibility.


Version 0.5.0 redesigns the overview and Control Room around information hierarchy, progressive disclosure, consistency and accessibility. It adds a shared light/dark palette, large text, descriptive labels and keyboard shortcuts while retaining existing usage, notification and coupon behavior.
