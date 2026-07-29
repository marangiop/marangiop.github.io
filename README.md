# Setup instructions

This is a minimal Jekyll blog, ready for GitHub Pages. GitHub builds the site
for you automatically every time you push — no build step to run yourself.

## 1. Create the repository

Go to github.com and create a **new repository** named exactly:

```
marangiop.github.io
```

(replace `your-username` with your actual GitHub username — this exact name is
what makes GitHub auto-host it at `https://your-username.github.io`, no config
needed).

Leave it public, don't initialize with a README (we already have one).

## 2. Push this folder to it

From inside this `blog-site` folder:

```bash
git init
git add .
git commit -m "Initial blog setup"
git branch -M main
git remote add origin https://github.com/your-username/your-username.github.io.git
git push -u origin main
```

## 3. Enable Pages (usually automatic)

Go to your repo → **Settings → Pages**. Since the repo is named
`your-username.github.io`, GitHub Pages is usually enabled automatically with
source set to "Deploy from branch: main / root". If not, just set that
manually and save.

## 4. Wait a minute, then visit

```
https://your-username.github.io
```

First build can take 1-2 minutes. You'll see a green checkmark under the
**Actions** tab when it's done.

---

## Adding a new post

Every post is one markdown file inside `_posts/`, named:

```
YYYY-MM-DD-some-title.md
```

with this at the top of the file:

```markdown
---
layout: post
title: "Your Title Here"
date: YYYY-MM-DD
---

Your content, in normal markdown, starts here.
```

Drop your other documents in there the same way you'd add any file — copy the
markdown content in below the front matter, rename the file with today's date,
`git add`, `commit`, `push`. It'll appear on the homepage automatically, newest
first.

## Editing the look

- `_config.yml` — site title, description, dark/light skin, social links.
- The theme used here is `minima`, which ships with GitHub Pages by default —
  no need to install anything for it to work online.
- To preview changes locally before pushing (optional, needs Ruby installed):

  ```bash
  bundle install
  bundle exec jekyll serve
  ```

  then open `http://localhost:4000`.

## Notes

- Don't rename `_posts` or `_config.yml` — Jekyll looks for these exact names.
- Any `.md` file placed directly in the repo root (like `index.md`) becomes a
  page; anything in `_posts/` becomes a dated blog post.
