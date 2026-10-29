# CineScope — Worldwide Movie Discovery

A responsive, installable web app that helps you search movies and TV shows, read details, and discover streaming availability by region.

## Included
- Global movie / TV / person search powered by TMDB when you configure a token
- Release dates, ratings, synopsis, genres, languages, runtime, and cast
- Region selector for provider availability
- Official-service search links for quick launch
- Local watchlist and saved preferences
- Responsive mobile layout and PWA manifest/service worker

## Quick start
1. Unzip the project.
2. Open `index.html` in a modern browser for the interface and demo titles. Some browser features and API requests work best when hosted over HTTPS.
3. For live data, create a TMDB account and request an API Read Access Token at https://www.themoviedb.org/settings/api
4. Open CineScope → Settings (gear icon) → paste the **API Read Access Token** → Save settings.
5. Search for a title. Choose a region to see provider listings where TMDB has data.

## Publish free with GitHub Pages
1. Create a GitHub repository.
2. Upload `index.html`, `styles.css`, `app.js`, `manifest.json`, `sw.js`, and `icon.svg` to the repository root.
3. In repository Settings → Pages, select deploy from the `main` branch and `/ (root)`.
4. Open the generated HTTPS site URL.

## Important notes
- TMDB data requires your own API token and is subject to TMDB terms and attribution requirements. This front-end stores the token in this browser's local storage. For a public production app, do not ship a private credential: put API requests behind a backend/proxy with rate limits and appropriate security.
- The token is used only for requests to `api.themoviedb.org`; this sample does not send it to CineScope servers.
- Provider availability is region-specific and not guaranteed complete. A provider listing does not guarantee a direct deep link to the exact title. Some links open the provider's official listing/search page and may require a subscription.
- This app does not embed streaming video or bypass provider authentication/DRM. It is an independent discovery tool, not affiliated with TMDB or any streaming service.
- Demo titles are illustrative fallbacks and do not show live availability.
- Google sign-in/cloud sync is not included in this first static build. A secure sync feature requires Firebase or another authentication/database service and configuration. The local watchlist works without an account.
- NetMirror is not integrated as a playback source. Use licensed provider links and official availability sources.

## App icon
The finalized minimalist black-and-silver CineScope icon is included as `app-icon.png` (app/PWA icon) and `icon.png` (full logo artwork). The web app manifest points to these PNG files.
