# Setup Notes

Most of this README works the moment you commit it — the stats cards, streak card,
trophies, activity graph, and LeetCode card are all hosted services that just need
your username in the URL (already done). Two things need one extra step:

## 1. ASCII portrait (`assets/ascii-portrait.svg`)
This is a real file, not a hosted link — commit the `assets/` folder alongside
`README.md` in your `Rohan-Gautam/Rohan-Gautam` repo, in the same relative
location. It animates on its own (each row fades in) the moment the page loads,
no Action required.

## 2. Snake animation
This one **does** need a GitHub Action, since the snake SVG is generated from
your real contribution graph on a schedule:

1. Commit `.github/workflows/snake.yml` to your `Rohan-Gautam/Rohan-Gautam` repo.
2. Go to the repo's **Settings → Actions → General** and make sure Actions are
   enabled (they are by default for public repos).
3. Either wait for the daily cron, or trigger it manually: **Actions tab →
   "Generate Snake Animation" → Run workflow**.
4. After the first run, it creates an `output` branch with the SVG files —
   the README already points at
   `.../Rohan-Gautam/output/github-contribution-grid-snake-dark.svg`, so once
   that branch exists the image will just start showing up.

That's it — everything else is live immediately on push.
