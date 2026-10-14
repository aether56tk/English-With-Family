# Android release signing and security checklist

The GitHub Actions APK artifact is a debug-signed testing build. Do not sell or distribute it as the production release.

## Before producing a customer release

1. Configure a release signing key locally or as protected GitHub Actions secrets. Never commit a keystore, passwords, or signing key to Git.
2. Configure the Gradle release build type to use that signing configuration and set isDebuggable to false.
3. Build a release APK/AAB and verify its certificate with Android SDK apksigner verify --print-certs.
4. Test install, upgrade, offline lessons, local progress, speech features, and supported Android versions/devices.
5. Keep the signing key backed up securely. Losing it may prevent upgrades for customers.
6. Keep a clear privacy policy describing local progress storage and any browser/device speech-recognition processing.
7. Review CodeQL results and secret-scanning alerts before release.

Do not disable Android Play Protect or instruct users to bypass security warnings. A successful build is not a malware-free certification.
