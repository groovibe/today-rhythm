# Android source bundle for CI

The GitHub Actions debug build downloads the complete Stage 2.3 Android source bundle from the Groovibe Google Drive folder, verifies its SHA-256 checksum, extracts it into the runner workspace, and builds the APK.

- Google Drive file ID: `196QeTYDYxk6FskZHrcHoS-UBgFs6mC_u`
- File name: `today-rhythm-github-upload.zip`
- SHA-256: `bdb97532b359d4df948e623d134e74a9dfbb1c770d59fea25dda061a13e72b6c`
- Android project path after extraction: `android/TodayRhythmAndroid`

The root `index.html` remains the GitHub Pages web app and is not replaced by this bundle.

When the Android source changes, upload the new ZIP to Drive and update both the file ID and SHA-256 in `.github/workflows/android-debug.yml` and this document.
