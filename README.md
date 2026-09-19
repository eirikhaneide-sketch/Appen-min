# DESTIM Android V1.8 — V1 Finish Foundation

Product-finish pass:
- privacy-first first-run disclosure before Usage Access
- clear explanation of local processing
- transparent score inputs
- Settings / About
- explicit "No ads. No subscriptions. No Pro version."
- discreet Support DESTIM entry point
- Usage Access settings entry
- Notification Access settings entry
- local daily history
- profile-based Dumb Phone entry
- no QUERY_ALL_PACKAGES
- no AccessibilityService

Google Play readiness still requires real-device QA, privacy-policy URL,
Data Safety declaration, store listing assets, and policy review.


## V1.9 – Functional Dumb Phone prototype

This version turns Dumb Phone from a placeholder into a working local session:
- Discovers launchable Android apps without QUERY_ALL_PACKAGES.
- Lets the user choose allowed apps.
- Includes Essential, Minimal and Custom selection flows.
- Supports 30 min, 1 hour, 2 hours and until-morning sessions.
- Persists the active session across activity recreation.
- Shows a live countdown.
- Launches only selected apps from the DESTIM Dumb Phone screen.
- Allows early exit without a penalty.
- When the session ends, DESTIM returns to its normal home screen.

Important Android limitation:
- An ordinary app cannot silently change the user's default launcher back and forth. DESTIM can act as a HOME/launcher app when the user explicitly chooses it as the default Home app in Android settings, but V1.9 does not attempt to change that setting programmatically.


## V1.10 – Monochrome distraction-free modes

The active Dumb Phone screen is now deliberately monochrome:
- Black background
- White/grey typography
- No colorful app icons
- Large clock
- Discreet countdown
- Simple text-only app list
- Minimal END SESSION / EDIT PROFILE controls

Focus and Sleep now use the same visual language:
- Black background
- Large simple typography
- Minimal information
- No decorative UI
- Persistent mode screen until the user ends it


## V1.11 – Launcher foundation

This version adds the Android launcher foundation for Dumb Phone:
- MainActivity declares itself as a HOME/DEFAULT activity.
- Android can offer DESTIM as a selectable Home app.
- HOME intents are routed to the DESTIM launcher experience.
- If Dumb Phone is active, the HOME screen opens directly into the monochrome Dumb Phone UI.
- If no Dumb Phone session is active, the Home screen opens the normal DESTIM dashboard.
- Settings includes a shortcut to Android Home settings.
- Dumb Phone includes a shortcut to Home settings.

Important:
- Android still requires the user to explicitly choose DESTIM as the default Home app.
- V1.11 does not silently change the default launcher.
- This is the foundation for a full temporary minimalist launcher experience; robust session restoration and OEM-specific behavior should be tested on physical devices before Play release.


## V1.12 – Complete launcher flow

Launcher behavior is now more coherent:
- HOME intent opens a dedicated minimalist DESTIM Home surface when no Dumb Phone session is active.
- Active Dumb Phone sessions remain on the monochrome Dumb Phone surface when HOME is pressed.
- An explicit END SESSION control remains the intentional exit path during Dumb Phone.
- Clock updates live on the minimalist Home surface.
- The launcher offers START DUMB PHONE and OPEN DESTIM actions.
- Settings explains the Home-app behavior.

This remains a user-selected Android Home app; DESTIM never silently changes the user's default launcher.


## V1.13 – Test Ready

This build is focused on real-device validation rather than new user-facing features.

Added:
- Settings test-status panel.
- Real-device test checklist covering permissions, usage data, Dumb Phone, launcher behavior, restart/recovery, Focus/Sleep and OEM testing.

The product should now move through physical-device testing before further feature expansion.
