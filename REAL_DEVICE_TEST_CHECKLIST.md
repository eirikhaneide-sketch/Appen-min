# DESTIM V1.13 – Real-device test checklist

Use this checklist on a physical Android phone before treating the launcher flow as release-ready.

## 1. First run
- [ ] Fresh install shows the privacy disclosure before Usage Access.
- [ ] “Continue without usage data” still opens the app.
- [ ] Granting Usage Access works.
- [ ] Restarting DESTIM does not repeatedly show the disclosure.

## 2. Usage data
- [ ] Screen time roughly matches Android Digital Wellbeing.
- [ ] App openings are plausible.
- [ ] Evening use is plausible.
- [ ] Score details expose the actual inputs.
- [ ] No crash when Usage Access is denied.

## 3. Dumb Phone
- [ ] App list contains normal launchable apps.
- [ ] Essential profile selects useful basics.
- [ ] Minimal profile reduces the selection.
- [ ] Custom selection persists.
- [ ] 30-minute session starts.
- [ ] 1-hour session starts.
- [ ] 2-hour session starts.
- [ ] Until-morning session calculates the next morning correctly.
- [ ] Countdown updates every second.
- [ ] Selected apps launch correctly.
- [ ] Unselected apps are not shown in the DESTIM Dumb Phone screen.
- [ ] END SESSION works.
- [ ] Restarting DESTIM during an active session restores the session.
- [ ] Pressing Home while DESTIM is the default launcher returns to the intended DESTIM surface.

## 4. Launcher
- [ ] Android allows DESTIM to be selected as Home.
- [ ] Home opens the DESTIM launcher.
- [ ] Normal launcher can be restored through Android settings.
- [ ] No accidental launcher loop.
- [ ] Back behavior is understandable.
- [ ] App launch/return behavior is stable.
- [ ] Lock/unlock does not break the session.

## 5. Focus / Sleep
- [ ] Focus opens the monochrome mode.
- [ ] Sleep opens the monochrome mode.
- [ ] End Mode returns to DESTIM.
- [ ] Restart behavior is acceptable.

## 6. OEM checks
Test at least one non-Pixel Android device if possible.
- [ ] Samsung/One UI
- [ ] OnePlus/OxygenOS
- [ ] Xiaomi/HyperOS or another OEM

## 7. Release blockers
Do not move toward Play release if any of these occur:
- Crash during active Dumb Phone
- Session unexpectedly disappears
- User becomes unable to return to a normal launcher
- Usage data is clearly inaccurate
- App requests unnecessary sensitive permissions
- Unexpected data leaves the device
