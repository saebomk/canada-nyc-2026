# canada-nyc-2026

This is a PUBLIC repo whose only purpose is to host the StatiCrypt-encrypted family trip 2026 site (`index.html`, NYC & Canada aurora trip) via GitHub Pages.

## Rules

- Only `index.html` (the encrypted page), this file, and the README belong here. Nothing else should ever be committed: no unencrypted itinerary, no loose images, no ticket PDFs, no personal data. The passphrase must never appear in this repo either.
- The editable master (`family-trip-2026.html`) lives in the private repo `saebomk/kwon-garcia-travel-2026` (locally `/Users/pablo/repos/kwon-garcia-travel-2026`).
- To update the site: from the master repo, encrypt `family-trip-2026.html` with StatiCrypt (AES-256, remember-me 30 days: `npx staticrypt family-trip-2026.html -p <passphrase> -d encrypted --remember 30 --short`), copy the result here as `index.html`, commit, push.
- Never use em dashes in any output, filename, or title.
