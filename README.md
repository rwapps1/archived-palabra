# Palabra — Spanish Vocab Quiz

A single-page vocab quiz. It loads a Spanish–English word list straight from this repo, quizzes you on 20 words at a time (mixed randomly between Spanish→English and English→Spanish), and scores you out of 20 at the end.

## Files

- `spanish-quiz-repo.html` — the quiz page
- `words.xlsx` — your word list (add this yourself — see format below)

## Setup

1. Add both files to the same folder in this repo (root is simplest).
2. In **Settings → Pages**, set the source to deploy from the branch/folder these files live in.
3. Visit the Pages URL GitHub gives you.

If you'd rather the quiz be the site's homepage, rename `spanish-quiz-repo.html` to `index.html`.

## Word list format

| Column A (Spanish) | Column B (English) |
|---|---|
| perro | dog |
| grande | big / large |

- Column A: Spanish, Column B: English.
- A header row is optional — there's a toggle on the page to skip it.
- Put more than one accepted answer in a cell separated by `/`, `,`, or `;` — any of them will be marked correct.
- Accents are optional when typing an answer (`como` counts for `cómo`).

## Updating the list

Edit `words.xlsx`, commit, and push. Reload the page or hit **New list** to pull the latest version.

## A couple of things to know

- The page fetches `words.xlsx` on load, so it needs to be **served** (GitHub Pages, or any local server) — opening the HTML file directly on your computer won't work, since browsers block that kind of file access. If it can't load the file, the page falls back to a manual upload button automatically.
- If you rename `words.xlsx` to something else, update the `WORDS_FILE` constant near the top of the `<script>` in the HTML file to match.
