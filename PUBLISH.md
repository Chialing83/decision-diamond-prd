# Publish this PRD canvas to GitHub Pages

The folder is already a git repo with an initial commit. You just need to push it to a new GitHub repo and turn on Pages.

---

## Step 1 · Create an empty GitHub repo

1. Open <https://github.com/new>
2. **Repository name**: `decision-diamond-prd` (or any name you want; the URL uses this)
3. **Public** (required for free GitHub Pages)
4. **DO NOT** check any of "Add a README", "Add .gitignore", or "Choose a license" — this repo already has files
5. Click **Create repository**

You'll land on a page with a URL like `https://github.com/beaver1109/decision-diamond-prd`.

---

## Step 2 · Push the folder from Terminal

Open Terminal. If you don't know the path to this folder, drag the folder from Finder into the Terminal window — the path will appear.

```bash
cd "PATH_TO_THIS_FOLDER"     # replace with the actual path (or use the drag trick)
git remote add origin https://github.com/beaver1109/decision-diamond-prd.git
git push -u origin main
```

If prompted for credentials, use your GitHub username and a **personal access token** as the password (not your account password). You can create a token at <https://github.com/settings/tokens> → Generate new token (classic) → check the `repo` scope.

If you've pushed to GitHub before with the `gh` CLI or SSH, that will handle auth automatically and you can skip the token step.

---

## Step 3 · Turn on GitHub Pages

1. Back on your GitHub repo page, click **Settings** (top nav)
2. In the left sidebar, click **Pages**
3. Under **Build and deployment → Source**, select **Deploy from a branch**
4. Under **Branch**, pick `main` and folder `/ (root)`, then click **Save**

Wait ~30–60 seconds for the first deploy. GitHub shows a green banner with the live URL when it's ready.

---

## Step 4 · Your public link

If you named the repo `decision-diamond-prd` and your GitHub username is `beaver1109`:

**Live URL:** https://beaver1109.github.io/decision-diamond-prd/

Share that link with the design team. Any time you update the files locally and `git push` again, GitHub Pages will rebuild automatically in ~30 seconds.

---

## Updating later (from your local copy)

```bash
cd "PATH_TO_THIS_FOLDER"
git add -A
git commit -m "describe what changed"
git push
```

That's it. The live URL always points at the latest commit on `main`.

---

## If you'd rather not use GitHub

Any static hosting service works. The whole folder is self-contained — HTML + images + a README. You can drag it into:

- **Netlify Drop** (<https://app.netlify.com/drop>) — literally drag the folder onto the page, get a URL in seconds, no account needed
- **Vercel** (<https://vercel.com/new>) — import the folder as a static project
- **Cloudflare Pages** — similar drag-and-drop or Git-connected deploy

Netlify Drop is the fastest if you just want a shareable link with zero setup.
