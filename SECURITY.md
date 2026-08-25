# Security & Privacy

LUMEL is built to be private *by architecture*, not by promise.

## What LUMEL collects

**Nothing.** No analytics, no telemetry, no crash reporting, no accounts, no ads, no identifiers.

## Data flow

- LUMEL runs in Apple's **App Sandbox** and ships **without any network entitlement**, so it has no ability to open a network connection, so it cannot send data off your Mac even in principle.
- Your preferences (boost level, mode, per-display settings, onboarding state) are stored locally in macOS `UserDefaults` on your device. Nothing syncs to a server, because there is no server.
- The optional **LUMEL Pro** purchase is processed entirely by the **App Store (StoreKit)**. LUMEL never sees or handles payment details, and the transaction does not route through any LUMEL backend.

## Permissions

LUMEL requests **no special permissions**:

- ❌ **No Accessibility permission.** The global shortcut (⌃⌥⌘B) uses Carbon's `RegisterEventHotKey`, which needs no permission and never reads or stores keystrokes.
- ❌ No screen recording, camera, microphone, location, or contacts access.
- ❌ No network access.

## Display safety

LUMEL renders through Apple's public Extended Dynamic Range path. Your Mac's display firmware enforces its own thermal limits, so LUMEL cannot drive a panel beyond what the hardware already permits. The mini-LED / LCD displays it supports do not suffer OLED-style burn-in. Sustained boost runs warmer, which is why LUMEL is built for bursts and includes an optional auto-off timer plus battery-aware safeguards.

## Reporting a vulnerability

Found a security issue? Please **email [support@onekapisch.com](mailto:support@onekapisch.com)** with details and steps to reproduce. Please don't open a public issue for security reports. We aim to acknowledge within a few days, and we're happy to credit you once it's resolved.
