# Android release security checklist

The debug APK is for testing only. Never sell or describe it as a production release.

## Before release
1. Generate a long-lived Android release keystore on a trusted device. Keep the key and passwords private and make a secure offline backup; losing the key can prevent future upgrades.
2. Never commit signing files or passwords. Keep local signing files out of Git and out of build logs.
3. Create a protected GitHub Environment named `production-release`, restrict it to the protected main branch, and require approval if available.
4. Store the keystore and signing values as environment secrets, not ordinary repository secrets.
5. Run the signed release workflow manually from main. If signing values are missing, no release APK should be produced.
6. Verify the APK signature and confirm that the Android manifest reports `debuggable=false`. Check that the certificate fingerprint is the expected one.
7. Install on a clean Android device and test upgrade over a previous build signed with the same key.
8. Test lessons, Malayalam text, navigation, offline use, saved progress/reset, text-to-speech and typing. Test voice input separately in supported browsers; the Android wrapper does not request native microphone access, so do not promise speech recognition in the APK.
9. Review CodeQL results and dependency/security alerts. Test supported Android versions and obtain legal review of the privacy notice before selling, especially for use by children.
10. Increase `versionCode` for every Android update. Publish only the verified signed build.

## Workflow and user safety
- Keep GitHub Actions permissions minimal and pin actions to reviewed immutable commit SHAs.
- Review dependency update PRs before merging them.
- A successful build or scan is not proof that the app is vulnerability-free.
- Never disable Play Protect or tell users to bypass Android or WhatsApp security warnings. Investigate warnings and resolve them through legitimate signing, distribution and security review.
