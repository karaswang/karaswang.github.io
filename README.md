# karaswang.github.io — deploy artifact, do not edit directly

This repo is the **published copy** of Kara Wang's personal site, served by
GitHub Pages at **https://karaswang.github.io**. It is generated output, not
a place to make edits.

## Do not edit files here

All source edits (HTML, CSS, images, content, etc.) happen in the separate
**`karaswang-site`** working repo. This repo's contents are overwritten
(`rsync --delete`) from there every time `deploy.sh` runs — any change made
directly in this repo will be silently wiped out on the next deploy.

Treat this repo as read-only / build output:

1. Make edits in `karaswang-site`.
2. Run `./deploy.sh` from `karaswang-site` to copy the changes here.
3. Review the diff it prints, then commit and push **from this repo**:
   ```bash
   git add -A
   git commit -m "Update site"
   git push
   ```

## About this file

This file itself is `deploy.sh`-managed: it's written in `karaswang-site` as
`README-FOR-GITHUB-PAGE.md`, and `deploy.sh` copies it here as `README.md`
on every run (it's excluded from the regular rsync so it doesn't end up
duplicated under its source name). **Edit `README-FOR-GITHUB-PAGE.md` in
`karaswang-site`, not this file** — direct edits here will be overwritten
the next time `./deploy.sh` runs.

See `karaswang-site`'s `README.md` and `HOW_TO_EDIT.txt` for the full
editing guide and publishing workflow.
