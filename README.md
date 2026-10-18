# Weekend Projects — setup

One main site, one repo per project. The main site reads your GitHub repos and lists any tagged as weekend projects, so you never have to edit it when you add something new.

## How it fits together

```
github.com/YOU/YOU.github.io      → https://YOU.github.io             (main site, this index.html)
github.com/YOU/pixel-garden       → https://YOU.github.io/pixel-garden/
github.com/YOU/budget-cli         → (no demo — just links to the code)
```

GitHub Pages serves every project repo under your main domain automatically, so it all feels like one website even though each project is its own repo.

## One-time setup (≈5 minutes)

1. Create a new **public** repo named exactly `YOUR-USERNAME.github.io`.
2. Add `index.html` from here and change `GITHUB_USER` at the top of the script to your username.
3. In the repo: **Settings → Pages → Source: Deploy from a branch → `main` / root**.
4. After a minute your site is live at `https://YOUR-USERNAME.github.io`.

## Every weekend

1. Create a new repo for the project (e.g. `pixel-garden`).
2. On the repo page, click the ⚙️ next to **About** and add the topic **`weekend-project`**.
   - Add a short description too — it shows up on the main site.
3. If it has a web demo: **Settings → Pages → Deploy from `main`**. It'll appear at `YOUR-USERNAME.github.io/pixel-garden/` and the main site will link to it as "Live".
   - Hosted somewhere else (Vercel, Netlify, etc.)? Put that URL in the About → **Website** field instead; it takes priority.
4. Add a thumbnail: put an image called **`preview.png`** in the root of the project repo. A 1200×900 screenshot (4:3) works best; portfolio tiles crop it to 16:9, so keep the important bit in the middle. No image? The tile gets a colourful initials card instead.
5. Proud of it? Add the topic **`portfolio`** as well. Its tile becomes double-width with a ★ sticker.

The whole tile opens the project's own page (its GitHub Pages site or Website link), so each project stays self-contained. The small "code ↗" link goes to the repo.

**Preview before setup:** while `GITHUB_USER` is still the placeholder, the page shows sample projects so you can see the design. Open `index.html` in your browser to try it.

Removing a topic takes it off the site — nothing gets deleted.

## Tips

- **Project template:** make one repo with your usual README skeleton (goal, what I built, what I learned, next time) and tick **Settings → Template repository**. Then every new weekend project starts from "Use this template".
- **Weekend dates** come from when the repo was created. A repo started on a Monday counts toward the previous weekend.
- **Private repos** never appear, so you can keep unfinished experiments private and flip them public when ready.
- **Custom domain:** add it under Settings → Pages on the main repo; project sites follow it automatically (e.g. `yourdomain.com/pixel-garden/`).
- The GitHub API allows 60 unauthenticated requests per hour per visitor, which is plenty for a personal site.
