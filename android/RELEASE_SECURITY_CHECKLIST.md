# Android release security checklist

The debug APK is for testing only. Do not sell it as a production release.

Before release, configure a protected signing key, verify the APK certificate, confirm debuggable=false, test the app on Android devices, and review CodeQL and Dependabot results. Never commit signing material or tell users to bypass Play Protect or WhatsApp warnings.
