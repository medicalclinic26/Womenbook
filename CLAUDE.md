# Women's Health Patient Education Handbook (medicalclinic26.github.io/Womenbook)

Static site: `index.html` (HTML + CSS + vanilla JS, no build step) plus pictures in `images/` (named by block id, e.g. `A-04a.jpg` for block A-04).
Hosted on GitHub Pages from the `main` branch of `medicalclinic26/Womenbook`. It goes live about a minute after a push.

## Account
- This repo belongs to the **medicalclinic26** GitHub account, not archuthan97. The remote uses the SSH alias `github-medicalclinic26` (in `~/.ssh/config`, key `~/.ssh/id_ed25519_medicalclinic26`). Keep it that way; do not switch the remote to plain `git@github.com:`.
- Commits here use the repo-local identity `medicalclinic26 <medicalclinic26@users.noreply.github.com>`.

## Structure
- Chapters: `chap-D` diabetes, `chap-H` high blood pressure, `chap-T` thyroid, `chap-A` asthma, `chap-O` obesity, plus front matter (`F-xx` blocks, `fm-card`).
- Each block is `.blk` with `.blk-id` (e.g. `D-03`), `.blk-head` (`.bh-si`, `.bh-ta`, `.bh-en`), `.blk-body` and `.blk-images`.
- Text is written three times: `.lang.lang-si`, `.lang.lang-ta`, `.lang.lang-en`. The language switch sets `body[data-lang]` to `all`, `si`, `ta` or `en`. Any change to the content must be made in all three languages, kept in step with each other.
- Sidebar nav: `.nav-link`, `.nav-sublink`. Colours are CSS tokens on `:root` (--ink, --bg, --card, --accent, --sidebar-*); reuse them.
- Fonts: Noto Sans Sinhala and Noto Sans Tamil. Keep them.

## Rules
- Use targeted edits to `index.html`; never rewrite the whole file. Some lines (around 291–295) are very long; edit inside them carefully.
- This is patient-facing medical content. Fix spelling, grammar and layout freely, but do not change medical meaning (doses, numbers, warning signs) without asking the user first. Point out anything that looks clinically wrong instead of silently fixing it.
- Keep the Sinhala and Tamil plain and patient-friendly (as the translators wrote it). For spelling fixes in Sinhala/Tamil, list each change for the user to check.
- Mobile first: check at 390px width with no horizontal scroll, and also check the print view if one is touched.

## Workflow
Make the change, check it in a browser at phone width (open `index.html` locally), commit to `main` with a clear message, push. GitHub Pages deploys automatically.
