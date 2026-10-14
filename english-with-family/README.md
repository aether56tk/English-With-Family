# English With Family

A free, beginner-friendly English practice app with Malayalam meanings.

## Features
- Friendly eight-question placement check with a suggested starting level
- 100 themed lessons with English phrases and Malayalam meanings (336+ everyday phrases)
- Browser text-to-speech, including a test button for “Good morning!”
- Conversation practice for home, shopping, meeting people and clinic visits; 20 lesson topics cover family, routines, food, school, phone calls, weather, restaurants, travel, work, plans, health and polite requests
- Quiz and revision practice
- Daily streaks, last-seven-day activity calendar, weekly goal and achievement badges
- Multiple local learner profiles (up to eight)
- Local progress stored in the browser (no cloud sync)
- Installable web app manifest and app-shell caching for supported browsers

## Publish with GitHub Pages
1. Open Settings → Pages.
2. Select **Deploy from a branch**, choose `main` and `/(root)`, then save.
3. Wait for GitHub Pages to publish the site.
4. Open the repository's GitHub Pages URL. The root page redirects to `/english-with-family/`.
5. On Android, open the website in Chrome and choose **Install app** or **Add to Home screen** when offered.

## Run locally
From the `english-with-family` directory, run `python -m http.server 8000`, then open `http://localhost:8000`. Install and service-worker features generally require localhost or HTTPS.

## Privacy, terms and ownership
- Read `privacy.html` and `terms.html` before using the app.
- No root `LICENSE` file is provided, so do not assume this repository is open-source or that third-party assets/content may be reused. Confirm ownership and permissions before distributing or commercializing it.
- The privacy and terms pages are starter notices, not legal advice or a guarantee of compliance. Obtain qualified legal review before commercial launch, collecting personal data, or targeting children.

## Important limitations
- The level check is a simple knowledge check, not a full assessment of speaking, listening, or pronunciation.
- The app focuses on useful everyday phrases rather than grammar-heavy lessons; it does not provide certification or guarantee fluency.
- Profiles and progress are stored in local browser storage on one device and do not automatically sync across phones.
- Text-to-speech voice selection depends on device/browser availability.
- Any speaking feedback should be treated as practice support, not a reliable pronunciation score.
- The app shell may work offline after caching, but speech features can depend on the browser and device.


## Android APK

An Android WebView wrapper is included in the repository under `android/`. It packages the web app as local assets so the lessons can open without a browser address bar.

To build a test APK:
1. Open the repository on GitHub and select **Actions**.
2. Select **Build Android APK**.
3. Click **Run workflow** and confirm.
4. When the run succeeds, open the run summary and download **English-With-Family-debug-apk** from the Artifacts section.
5. Extract the downloaded ZIP and install `app-debug.apk` on your Android phone. You may need to allow installs from your browser or file manager.

The workflow creates a debug APK for testing, not a Play Store release. The APK has not been built or device-tested in this commit yet. Some browser-dependent features, especially speech recognition, may behave differently inside Android WebView.
