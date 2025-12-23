# Downloads Folder

Place your APK and IPA files here.

## Android APK

After building your Android app:

1. Build the signed APK in Android Studio
2. Copy `android/app/build/outputs/apk/release/app-release.apk`
3. Rename it to `faculty-quest.apk`
4. Place it in this folder

The download link in `index.html` points to: `downloads/faculty-quest.apk`

## iOS IPA (Optional)

If you have an iOS app:

1. Build and archive in Xcode
2. Export the IPA file
3. Place it here as `faculty-quest.ipa`
4. Update the link in `index.html`

## File Size

Keep file sizes reasonable:
- APK: Usually 20-30 MB
- IPA: Usually 25-35 MB

## Note

The `.apk` and `.ipa` files are not included in git (see `.gitignore`).
You need to build and add them manually before deploying.
