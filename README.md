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

## Weekly Practice Updates (Excel, Python, AI)

This project includes a weekly GitHub Actions workflow at `.github/workflows/weekly-practice.yml`.

### One-time setup
1. Upload the **contents** of this folder to your existing GitHub repository (keep `.github/workflows/weekly-practice.yml` and `scripts/update_practice.py` in their folders).
2. In the repository, open **Settings → Pages → Build and deployment → Source**, and select **GitHub Actions**. The weekly workflow deploys the site after generating the updated `practice.json` file.
3. To generate AI-written questions, open **Settings → Secrets and variables → Actions → New repository secret**. Name it `API key` and paste an API key from your OpenAI API account. Never put the key in `index.html`, `app.js`, or any public file.
4. Open **Actions → Update Skill Lab practice → Run workflow** to run the first update. Check the workflow log and then open the deployed site → **Weekly Practice**.

### What happens each week
- Runs on Mondays at 08:30 India time (03:00 UTC).
- Collects recent discovery links through Google News RSS for Excel, Python, and AI topics.
- If `API key` is configured, asks the OpenAI API to create a small set of original practice questions with answers and links back to supplied sources.
- Deploys the refreshed site and `practice.json` to GitHub Pages.

### Cost and accuracy notes
- GitHub Actions and GitHub Pages may be available at no additional charge within the applicable plan limits; check your repository/account plan.
- OpenAI API usage is billed separately and is not automatically included with a ChatGPT subscription. Keep usage limits enabled and monitor API usage.
- Without `API key`, the workflow can collect resource links but will not generate AI questions.
- RSS discovery results may be duplicated or imperfect. Questions are study aids; verify answers and follow source links. This workflow does not scrape paywalled article bodies.
- GitHub Pages is static hosting. The API key is used only in the GitHub Actions environment, not in the browser.
