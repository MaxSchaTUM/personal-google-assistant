# Personal Google Assistant

A minimal information website for a private, single-user Hermes assistant hosted on Hostinger. It describes two separate Google OAuth integrations: Calendar (`calendar.events`, `calendar.freebusy`) and Gmail (`gmail.modify`). It does not run the assistant or connect visitors' Google accounts.

## Website and repository

- Repository: https://github.com/MaxSchaTUM/personal-google-assistant
- Homepage: https://maxschatum.github.io/personal-google-assistant/
- Privacy policy: https://maxschatum.github.io/personal-google-assistant/privacy.html
- Terms of use: https://maxschatum.github.io/personal-google-assistant/terms.html

The hostname to try in Google Cloud Console's Authorized domains field is `maxschatum.github.io` (no scheme or path). Google may require additional ownership verification. GitHub Pages publication does not publish or verify either Google OAuth app or guarantee acceptance of these URLs or this domain.

## Files

- `index.html`: application homepage
- `privacy.html`: data access, processing, storage and revocation disclosures
- `terms.html`: brief terms of use
- `style.css`: shared, responsive styling using system fonts

There is no framework, build step, JavaScript, analytics, cookie functionality, external font or runtime dependency. Internal links are relative to work under the repository subpath. The public site and its repository must contain no assistant credentials or private operational data.

## Maintenance

1. Edit the relevant HTML or shared CSS. Keep the description accurate if the assistant's hosting, scopes, AI processing, Telegram delivery or record handling changes. Update the policy's effective date when its substance changes; preserve the creation date of 17 November 2026.
2. Preview locally with `python3 -m http.server 8000` from this directory, then visit `http://localhost:8000/`. Check all three pages, navigation, keyboard focus and a narrow mobile viewport. Stop the server with Ctrl-C.
3. Stage only the five intended files: `git add index.html privacy.html terms.html style.css README.md`. Review `git diff --cached` and `git diff --cached --name-only` before committing. Never add OAuth client files, tokens, `.env` files, credentials, calendar data, email contents or chat history.
4. Commit and push to `main`. GitHub Pages deploys from the root (`/`) of `main`, using branch-based deployment. No custom workflow is required.
5. Check deployment with `gh api repos/MaxSchaTUM/personal-google-assistant/pages` and `gh api repos/MaxSchaTUM/personal-google-assistant/pages/builds/latest`. Verify the three live URLs return HTTP 200 and all internal navigation and the stylesheet load successfully.

GitHub repository Settings → Pages shows the deployment source and status. No custom domain or paid service is configured. Keep Google Cloud settings separate: update them manually if desired. A public contact address is not included; only publish one explicitly approved by the owner. GitHub's hosting may process technical visitor information as described in the privacy policy.
