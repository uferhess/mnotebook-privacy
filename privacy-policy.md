# Privacy Policy — M Notebook

**Last updated: 10 October 2026**

M Notebook (package `com.mnotebook.app`, "the app") is a personal note-taking app.
This policy explains what data the app handles and what it does not.

## What the app stores

- **Your notes and images.** Notes are saved on your device in a local
  database (offline-first). If you sign in with Google and enable sync, note
  files (JSON) and attached images are uploaded to **your own Google Drive**,
  into a folder named **"M Notebook"** in your Drive root. The app uses the
  `drive.file` scope, which means it can only see and manage files **it
  created itself** — it cannot read any other files in your Drive.
- **Google account identity.** Signing in stores your email address, display
  name, and profile photo on the device, used only to label your sync account
  and to isolate each account's notes (`owner_uid`). There is no Firebase —
  sign-in is direct Google Sign-In and Drive API.
- **Your PIN (if you set one).** The PIN is stored **only on the device** as a
  salted, iterated SHA-256 hash. The PIN itself never leaves your phone and is
  never sent to Google or anyone else.

## What the app does NOT do

- **No analytics, no crash reporting, no ads, no trackers.** The app ships no
  Firebase, no advertising SDKs, and no third-party analytics.
- **No contacts, location, microphone, or camera access beyond what you choose.**
  Images come only from photos you pick or attach yourself.
- **No selling or sharing.** We do not sell, rent, or share your data with any
  third party. Data sent to Google Drive is covered by Google's own privacy
  policy (https://policies.google.com/privacy).

## Your control

- **Sign out** in the app to stop syncing; your notes stay on the device.
- **Delete the "M Notebook" folder** in Google Drive to remove the cloud copy.
- **Uninstall the app** to remove the local database and settings from the
  device.

## Children

The app is not directed at children under 13 and does not knowingly collect
their data.

## Changes

If this policy changes, the updated version will be published with the app
release it applies to.

## Contact

Questions about this policy: contact the app developer through the app's
support channel.

---

_Source-grounded from the v42 build (sha256 `455fe515…14205f`):
`driveService.folderName = 'M Notebook'`, scope `https://www.googleapis.com/auth/drive.file`,
`auth_service.dart` stores email/displayName/photoUrl + owner_uid isolation,
`pin_controller.dart` salted iterated SHA-256 in SharedPreferences,
`pubspec.yaml` has no firebase/analytics/crashlytics deps, comments in
`oauth_config.dart`/`drive_service.dart` confirm "no Firebase anywhere"._
