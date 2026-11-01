# Fruit Frenzy — Mini Game

A lightweight, original HTML5 fruit-slicing arcade game built with plain HTML, CSS and JavaScript. It has no backend, build step, paid API, or third-party game assets.

## Play locally

**Option 1 — simplest:** open `index.html` in a modern browser.

**Option 2 — local web server (recommended):**
```bash
cd fruit-slice-arcade
python3 -m http.server 8080
```
Then visit [http://localhost:8080](http://localhost:8080).

## Controls

- Mouse: click and drag through fruit.
- Touch: swipe across the play area.
- `Space`: start / pause / resume.
- `R`: restart.
- `Esc`: pause.
- Use the speaker button to toggle sound.

Slice fruit to earn points. Consecutive slices within the combo window multiply your points. Avoid bombs: three bomb hits end the round. Your best score is stored in your browser using `localStorage`.

## Deploy to Vercel

This is a static site; no build command is needed.

### Git-based deployment
1. Create a Git repository and add the files in this folder.
2. Push the repository to GitHub, GitLab, or Bitbucket.
3. In Vercel, choose **Add New → Project** and import the repository.
4. Set **Framework Preset** to **Other**.
5. Leave **Build Command** blank and set **Output Directory** to `.` (or leave the default if Vercel detects the static site).
6. Click **Deploy**.

### Vercel CLI
Install the Vercel CLI, sign in, then run from this project directory:
```bash
vercel
```
For a production deployment:
```bash
vercel --prod
```

## Project files

- `index.html` — semantic page structure and game UI.
- `styles.css` — responsive styling and overlays.
- `game.js` — game loop, pointer input, collisions, scoring, audio and effects.

## Notes

- The game uses emoji fruit as lightweight system-rendered artwork and original canvas effects.
- Sound is synthesized with Web Audio after the player interacts with the page; it can be muted at any time.
- The game is designed to work on current desktop and mobile browsers.
