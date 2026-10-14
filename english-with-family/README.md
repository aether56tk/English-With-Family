# English With Family

A free, beginner-friendly English practice app with Malayalam meanings.

## Features
- Friendly eight-question placement check with a suggested starting level
- Step-by-step everyday lessons with English phrases and Malayalam meanings
- Browser text-to-speech, including a test button for “Good morning!”
- Conversation practice for home, shopping, meeting people and clinic visits
- Quiz and revision practice
- Daily streaks, last-seven-day activity calendar, weekly goal and achievement badges
- Multiple local learner profiles (up to eight)
- Progress export as JSON
- Installable web app manifest and app-shell caching for supported browsers

## Publish with GitHub Pages
1. Open Settings → Pages.
2. Select **Deploy from a branch**, choose `main` and `/(root)`, then save.
3. Wait for GitHub Pages to publish the site.
4. Open the repository's GitHub Pages URL. The root page redirects to `/english-with-family/`.
5. On Android, open the website in Chrome and choose **Install app** or **Add to Home screen** when offered.

## Run locally
From the `english-with-family` directory, run `python -m http.server 8000`, then open `http://localhost:8000`. Install and service-worker features generally require localhost or HTTPS.

## Important limitations
- The level check is a simple knowledge check, not a full assessment of speaking, listening, or pronunciation.
- The app focuses on useful everyday phrases rather than grammar-heavy lessons; it does not provide certification or guarantee fluency.
- Profiles and progress are stored in local browser storage on one device and do not automatically sync across phones.
- Text-to-speech voice selection depends on device/browser availability.
- Any speaking feedback should be treated as practice support, not a reliable pronunciation score.
- The app shell may work offline after caching, but speech features can depend on the browser and device.
