# LovoCus — Privacy Policy

**Effective date:** 26 Apr 2026
**Last updated:** _<same as effective date initially>_
**App name:** LovoCus
**Developer:** Mikmon-Studio
**Contact:** mikmonnovastudio@gmail.com

---

## 1. Summary in one paragraph

LovoCus is an offline-first focus and productivity timer. **We do not collect, transmit, sell, or share any personal data.** All session data, settings, and preferences are stored locally on your device and never leave it. The app does not require an account, does not include analytics, advertising, or tracking SDKs, and does not request internet permission.

---

## 2. What data LovoCus stores **locally on your device**

The app stores the following information **only on your device** (using Android `SharedPreferences` and a local SQLite-style database). None of this data is transmitted to us or any third party.

- **Session history** — start time, end time, duration, mode (Soft / Strict), whether the session was completed or cancelled, number of pauses, and number of foreground app interruptions detected during Strict sessions.
- **App preferences** — your chosen focus duration, break duration, selected focus and break soundtracks, focus intensity, and whether app blocking is enabled.
- **Block-list selections** — the package names of apps you have personally chosen to block during focus sessions.
- **Daily aggregates** — the per-day summaries LovoCus computes from the above (used to render the Dashboard charts).

You can delete all of this data at any time by clearing the app's storage in Android Settings → Apps → LovoCus → Storage → Clear Data, or by uninstalling the app.

---

## 3. What data we **do not** collect

LovoCus does **not** collect, transmit, or store remotely:

- Your name, email address, phone number, or any account identifier.
- Your device identifiers (advertising ID, Android ID, IMEI, MAC address, etc.).
- Your location (precise or approximate).
- Your contacts, calendar, photos, microphone audio, camera images, or files outside the app.
- Crash logs, analytics, telemetry, or usage metrics.
- Any of the local data described in section 2.

We have no servers, no backend, and no cloud infrastructure associated with LovoCus.

---

## 4. Permissions LovoCus requests, and why

| Permission | Why it is needed | Data leaves the device? |
| --- | --- | --- |
| `FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_MEDIA_PLAYBACK` | Keeps your focus timer and soundtrack running reliably while the screen is locked or the app is backgrounded. | No |
| `POST_NOTIFICATIONS` | Shows the ongoing-session notification (timer + cancel button) and session-complete cues. | No |
| `ACCESS_NOTIFICATION_POLICY` | Lets LovoCus enable Do Not Disturb mode automatically during a focus session, so notifications don't break your concentration. Phone calls are not silenced. | No |
| `BIND_ACCESSIBILITY_SERVICE` *(only active if you enable App Blocking in Settings)* | Detects when a blocked app comes to the foreground during an active focus session and returns you to your home screen. The service reads the package name of the foregrounded app **only**, compares it against the block-list you chose, and discards the value immediately. It does not read window content, screen text, passwords, or any other accessibility metadata. | No |

You can revoke any of these permissions at any time from Android system Settings.

---

## 5. About the Accessibility service

LovoCus's Accessibility service is **strictly opt-in**. It is disabled by default. To enable it, you must:

1. Turn on "Block distracting apps" in LovoCus Settings, **and**
2. Manually grant Accessibility access in Android system Settings.

When active, the service:

- Operates only while a focus session is in progress.
- Listens for `TYPE_WINDOW_STATE_CHANGED` events to read the package name of the app that just came to the foreground, and for `TYPE_VIEW_CLICKED` events to count screen interactions during Strict sessions for the in-app statistics shown on your Dashboard.
- Has `canRetrieveWindowContent="false"` declared in its configuration, meaning it cannot read on-screen text, form fields, passwords, or any accessibility metadata beyond a package name and an event type.
- Does not log, store, or transmit any data outside the device.

You can disable it at any time by turning off App Blocking in LovoCus Settings, or by revoking Accessibility access in Android Settings.

You are always in control of this feature:

- You choose which apps to block.
- You can turn blocking off at any time.
- You can revoke Accessibility permission at any time.

LovoCus is intended for focus and productivity support only.

---

## 6. Children's privacy

LovoCus is intended for general audiences and is not directed at children under the age of 13. We do not knowingly collect any data from anyone, including children. The app does not require an account.

---

## 7. Third parties

LovoCus does not integrate any third-party SDKs, analytics libraries, advertising networks, or tracking tools. The only third-party assets included are:

- A small set of public-domain or commercially-licensed ambient audio tracks bundled into the app for use as focus/break soundtracks.
- The Android Jetpack and AndroidX system libraries, which are standard parts of every Android app and do not transmit data on LovoCus's behalf.

---

## 8. Data security

Because LovoCus does not transmit your data anywhere, the only relevant security boundary is your device itself. Data is stored using Android's standard app-private storage, which is sandboxed from other apps. Use a device PIN, password, or biometric lock to protect your device.

---

## 9. Your rights

Because LovoCus does not collect or store your data on any server, there is nothing for us to access, export, or delete on your behalf. You retain full control:

- **Access / export:** view your session history at any time on the Dashboard tab.
- **Delete:** clear all data via Android Settings → Apps → LovoCus → Storage → Clear Data, or uninstall the app.
- **Withdraw consent:** revoke any permission via Android system Settings, or uninstall the app.

These options give you the equivalent of GDPR (EU/UK), CCPA/CPRA (California), and similar privacy-law rights, without us having to mediate the request.

---

## 10. Changes to this policy

If we ever change how the app handles data — for example, if a future version adds optional cloud backup or analytics — we will update this policy, change the "Last updated" date at the top, and prompt you in-app before any new data handling begins. You will always be given a chance to decline before any new collection occurs.

---

## 11. Contact

Questions, concerns, or requests about this policy?

**Email:** mikmonnovastudio@gmail.com
**Developer:** Mikmon-Studio

---

## 12. Terms of use

Use of LovoCus is also governed by the Terms of Use:

- `TERMS_OF_USE.md`

---

*This policy applies to the LovoCus Android application distributed on Google Play. It does not cover any third-party website that may link to it.*
