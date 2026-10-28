# Skill Lab

A mobile-friendly, beginner-oriented learning and practice PWA for Excel, Python and AI.

## Included
- Three learning tracks with 22 Excel lessons, 25 Python lessons and 21 AI lessons
- Lesson completion and local progress tracking
- Practice challenge with hint, solution and answer checking
- Quick quizzes and XP points
- Project briefs and downloadable fictional CSV datasets
- Responsive layout and PWA manifest/service worker
- GitHub Pages-friendly static files

## Run locally (Windows 11)
1. Extract the ZIP into a folder.
2. Open `index.html` in Chrome or Edge.
3. Lessons and basic practice work locally. PWA installation/offline caching requires serving over HTTPS or localhost (GitHub Pages provides HTTPS).
4. Progress is saved in that browser's local storage. It does not sync between devices.

## Publish on GitHub Pages
1. Create a repository, e.g. `skill-lab`.
2. Upload the contents of this folder to the repository root (not the ZIP itself).
3. Open Settings → Pages.
4. Under Build and deployment, select `Deploy from a branch`.
5. Choose branch `main` and folder `/(root)`, then Save.
6. Wait for the deployment and open the URL shown by GitHub Pages.

## Important limitations in this starter
- Excel practice is concept and formula practice, not a full Excel spreadsheet engine.
- Python challenges teach core concepts and predict output; this starter does not execute arbitrary Python code in the browser.
- AI Lab teaches AI concepts and prompt writing; it does not connect to an AI API or send user data to an AI service.
- No account or cloud sync; progress is local to the current browser.
- Google Fonts are optional; the app uses system fallbacks if unavailable.
