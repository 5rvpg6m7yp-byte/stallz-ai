# STALLZ AI — GitHub Actions Android project

This ZIP is a source project designed for a GitHub Actions APK build. It contains:
- Native Android wrapper (Java + Android manifest + Gradle)
- App interface (HTML, CSS, JavaScript)
- Optional Python/Flask chat backend scaffold
- GitHub Actions workflow to build and upload a debug APK artifact

## Upload to GitHub

1. Extract this ZIP.
2. Open your GitHub repository.
3. Upload the **contents inside `STALLZ_AI_FINAL`** into the repository root (not an extra nested folder). The root must contain `settings.gradle`, `build.gradle`, `app/`, `backend/`, and `.github/`.
4. Commit the files to the `main` branch.
5. Open the repository's **Actions** tab.
6. Select **Build STALLZ AI APK** and choose **Run workflow**. A push to `main` also triggers the workflow.
7. Wait for a green successful run. Open the run and download the artifact named **STALLZ-AI-debug-APK**. Extract the downloaded artifact ZIP to find `app-debug.apk`.

## What is and isn't complete

The UI and Android project source are included. The workflow is configured but has **not been run from this environment**, so no APK has been verified yet.

The chat currently shows a clear demo message unless you configure and deploy the Python backend and set `API_BASE` in `app/src/main/assets/app.js` to its HTTPS address. The backend can call a compatible AI provider if its credentials are configured as environment secrets on the backend host. The image/video creation, 8-second video rendering, accounts, cloud history, and payments are not implemented as working services yet; they require separate provider/backend integrations. Plan cards are previews only.

Use only free tiers/open-source options where practical, and check each provider's usage limits. Never commit API keys or secrets to GitHub.
