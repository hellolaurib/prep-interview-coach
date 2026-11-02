# PREP Interview Coach

A single-page tool to practice job interviews in English with the PREP method (Point, Reason, Example, Point).

## Flow
1. Paste a job offer, Claude generates 6 likely interview questions.
2. Pick a question or write a custom one (the question stays editable). Write the answer in 4 PREP boxes; each has 4 clickable sentence-starter labels.
3. Check grammar: Claude returns a score, corrections per section with explanations, PREP feedback and a polished answer.

## Tech
- Everything lives in `index.html`: plain HTML, CSS and vanilla JS. No build step.
- Calls the Anthropic Messages API directly from the browser (`anthropic-dangerous-direct-browser-access` header). The API key is entered in the page and saved in localStorage.
- Model is set in the `MODEL` constant at the top of the script.
- Design tokens (pink palette, fonts) are CSS variables in `:root`.

## Style rules
- UI copy in English.
- Never use the em dash character in UI text or prompts.
- Keep the pink look: hot pink `#D6246E`, plum ink `#2B1020`, blush background `#FFF0F5`, Bricolage Grotesque for headings, Inter for body.

## Run
Open `index.html` in a browser, or serve the folder: `npx serve .`
