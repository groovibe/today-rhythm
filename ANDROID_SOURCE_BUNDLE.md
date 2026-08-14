# Android CI source bundle

GitHub Actions reconstructs the Today Rhythm Android Stage 2.3 source from verified Base64 text chunks stored under:

`ci/source-text-v5/`

Concatenation order:

1. `part00`
2. `part01`
3. `part02`
4. `part03a`
5. `part03b`
6. `part04`
7. `part05`
8. `part06`
9. `part07`

Decoded ZIP SHA-256:

`ec07add294a1dacfbe7ab96778e726edcf82a108b21bd69e42d4d5efe0563316`

The workflow verifies this checksum before extraction. Web fonts are downloaded from the official Google Fonts repository during CI, subset to the characters used by `index-android.html`, and packaged as local WOFF2 assets. The installed Android app remains fully offline and does not receive the INTERNET permission.

The root `index.html` remains the GitHub Pages web app and is not replaced by the Android build process.
