# canada-nyc-2026

This is a PUBLIC repo whose only purpose is to host the StatiCrypt-encrypted family trip 2026 site (`index.html`, NYC & Canada aurora trip) via GitHub Pages.

## Rules

- Only `index.html` (the encrypted page), this file, and the README belong here. Nothing else should ever be committed: no unencrypted itinerary, no loose images, no ticket PDFs, no personal data. The passphrase must never appear in this repo either.
- There is NO stored unencrypted master: `index.html` (encrypted) is the only copy of the site. The content is recoverable only with the passphrase, so losing the passphrase means losing the site.
- To update the site, use the decrypt-edit-re-encrypt cycle (ask Pablo or Saebom for the passphrase, never write it to disk):
  1. Decrypt to a temp folder OUTSIDE this repo (e.g. a scratchpad dir): `npx staticrypt index.html -p <passphrase> --decrypt --salt ae63b6d13da99d5595d35d3d61cde3e9 -d <tempdir>`
  2. Edit the decrypted HTML there.
  3. Re-encrypt with the SAME salt so viewers' remember-me keeps working: `npx staticrypt <tempdir>/index.html -p <passphrase> --salt ae63b6d13da99d5595d35d3d61cde3e9 -d <tempdir>/encrypted --remember 30 --short`, then copy the result back here as `index.html`. (The salt is not secret; it is visible in the published page. Without `--salt`, StatiCrypt silently uses a random salt and decryption fails.)
  4. Delete the temp folder and any `.staticrypt.json` it produced, verify `git status` shows only `index.html` changed, then commit and push. Never commit an unencrypted version.
- Never use em dashes in any output, filename, or title.
