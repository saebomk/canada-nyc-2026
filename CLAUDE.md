# canada-nyc-2026

This is a PUBLIC repo whose only purpose is to host the StatiCrypt-encrypted family trip 2026 site (`index.html`, NYC & Canada aurora trip) via GitHub Pages.

## Rules

- Only `index.html` (the encrypted page), this file, and the README belong here. Nothing else should ever be committed: no unencrypted itinerary, no loose images, no ticket PDFs, no personal data. The passphrase must never appear in this repo either.
- The editable unencrypted master is kept locally, outside this repo, and must never be committed or pushed anywhere.
- To update the site: edit the local master, encrypt it with StatiCrypt (AES-256, remember-me 30 days: `npx staticrypt <master file> -p <passphrase> -d encrypted --remember 30 --short`), copy the result here as `index.html`, commit, push.
- Never use em dashes in any output, filename, or title.
