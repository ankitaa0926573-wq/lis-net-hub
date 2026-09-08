# Putting the LIS NET Hub online (free, ~5 minutes, once)

Everything in this folder is the website. Upload these **6 files** and you get a permanent
`https://` link that opens on your phone anytime — laptop off, no Claude needed.

    index.html                 <- the hub itself (2 MB)
    manifest.webmanifest       <- lets Android install it as an app
    sw.js                      <- makes it work offline
    icon-192.png
    icon-512.png
    icon-512-maskable.png

Do NOT rename `index.html` — that exact name is what makes the site load.

---

## Option A — GitHub Pages (recommended: permanent, free forever)

1. Go to **github.com** and sign up (free). Skip if you already have an account.
2. Click **+** (top right) -> **New repository**.
   - Repository name: `lis-net-hub`
   - Set it to **Public**  (Pages needs Public on the free plan)
   - Tick **Add a README file**
   - Click **Create repository**
3. On the repo page click **Add file** -> **Upload files**.
4. Drag in all 6 files from this folder. Click **Commit changes**.
5. Go to **Settings** (top of repo) -> **Pages** (left sidebar).
6. Under "Build and deployment", set **Source: Deploy from a branch**,
   **Branch: main**, folder **/ (root)**. Click **Save**.
7. Wait 1-2 minutes, then refresh that page. Your link appears at the top:

       https://<your-username>.github.io/lis-net-hub/

That link is permanent. Open it on your phone.

### To add it to your Android home screen
Open the link in Chrome -> tap the **⋮** menu -> **Add to Home screen** / **Install app**.
It then opens full-screen like a normal app, and works with no signal.

### To update it later (when new sets are added)
Repo -> **Add file** -> **Upload files** -> drag the new `index.html` -> Commit.
Also open `sw.js`, change the `CACHE` line (e.g. `lisnet-2026-09-20`), and commit that too,
otherwise phones keep showing the old cached copy.

---

## Option B — Netlify (fastest to a first link)

1. Go to **app.netlify.com/drop**.
2. Drag this whole folder onto the page. You get a live URL within seconds.
3. Sign up (free) when prompted to **claim the site**, or the link is temporary.
4. Site settings -> **Change site name** to something memorable.

Updating means dragging the folder on again from your site's Deploys tab.

---

## Notes

- The site is fully self-contained. No database, no server, nothing to maintain.
- It is a **public** URL. Anyone with the link can read it. There is nothing private in it
  (practice questions and notes), but do not add anything personal to this folder.
- Both services are free at this size. 2 MB is far below either limit.
