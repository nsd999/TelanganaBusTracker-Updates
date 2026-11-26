# PrajaYatri — APK updates

This public repository distributes signed Android APK updates for PrajaYatri. The application source code remains in the private PrajaYatri repository `nsd999/TelanganaBusTracker`.

## Download links used by the app

- Update manifest: `https://github.com/nsd999/TelanganaBusTracker-Updates/releases/latest/download/latest.json`
- APK: `https://github.com/nsd999/TelanganaBusTracker-Updates/releases/latest/download/app-debug.apk`

Every published release must attach both files with those exact names.

## Manifest rules

The attached `latest.json` must use schema version 1 and include:
- exact application ID: `city.nsd.telanganabustracker.debug`
- actual `versionCode` and `versionName` from the APK
- APK URL above
- SHA-256 hash of the exact APK bytes
- `mandatory: true`
- `minimumSupportedVersionCode` equal to the new APK's version code

Never upload an APK signed with a different key from the app's existing persistent signing key. Keep the keystore private and backed up securely.

The app verifies the SHA-256 digest before requesting Android's package installer. Android still requires the user to approve installing the update.
