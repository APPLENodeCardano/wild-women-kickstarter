# Hosting Guide

This document outlines three hosting options for the Indiegogo pre-launch site, all of which support GitHub integration.

---

## Option 1: GitHub Pages (Free)

GitHub Pages serves your site directly from this repository — no external service needed.

### Setup Steps

1. Push this repository to GitHub (see below).
2. Go to your repository on GitHub.
3. Click **Settings** → **Pages** (left sidebar).
4. Under **Source**, select **Deploy from a branch**.
5. Choose **main** branch and **/ (root)** folder.
6. Click **Save**.
7. Your site will be live at: `https://YOUR_USERNAME.github.io/wild-women-indiegogo/`

### Pros
- Completely free
- No third-party account needed beyond GitHub
- Automatic deploys on every `git push`
- Custom domain support (add a `CNAME` file)

### Cons
- Public repositories only (on free GitHub plan)
- No server-side logic (fine for this static site)

---

## Option 2: Netlify (Free Tier)

Netlify offers a generous free tier with instant Git-connected deployments, form handling, and a CDN.

### Setup Steps

1. Go to [netlify.com](https://netlify.com) and sign up (free).
2. Click **Add new site** → **Import an existing project**.
3. Connect your GitHub account and select this repository.
4. Set **Build command**: *(leave blank — no build needed)*
5. Set **Publish directory**: `.` (root)
6. Click **Deploy site**.
7. Your site will be live at a Netlify subdomain (e.g., `wild-women.netlify.app`).

### Custom Domain
- In Netlify dashboard → **Domain settings** → **Add custom domain**
- Point your DNS `CNAME` to `your-site.netlify.app`

### Pros
- Free SSL certificate
- Global CDN
- Instant previews for every branch/PR
- Built-in form submissions (great for email capture)
- Easy custom domain setup

### Cons
- Requires a Netlify account

---

## Option 3: Vercel (Free Tier)

Vercel provides instant deployments with a powerful global edge network.

### Setup Steps

1. Go to [vercel.com](https://vercel.com) and sign up with GitHub (free).
2. Click **Add New Project** → **Import Git Repository**.
3. Select this repository.
4. Leave all settings as default (no build command needed).
5. Click **Deploy**.
6. Your site will be live at `https://wild-women-indiegogo.vercel.app`.

### Custom Domain
- In Vercel dashboard → **Settings** → **Domains** → **Add domain**

### Pros
- Extremely fast global edge network
- Free SSL
- Automatic deploys on every push
- Preview deployments for branches

### Cons
- Requires a Vercel account

---

## Pushing to GitHub

If you haven't already pushed this project to GitHub:

```bash
# Initialize git (if not already done)
cd wild-women-indiegogo
git init
git add .
git commit -m "Initial commit: Indiegogo pre-launch site"

# Create a new repo on GitHub, then:
git remote add origin https://github.com/YOUR_USERNAME/wild-women-indiegogo.git
git branch -M main
git push -u origin main
```

---

## Recommendation

| Use Case | Best Option |
|----------|-------------|
| Simplest setup, no extra accounts | **GitHub Pages** |
| Email capture + best free features | **Netlify** |
| Fastest global performance | **Vercel** |

For an Indiegogo pre-launch site, **Netlify** is recommended due to its built-in form handling (perfect for collecting early backer emails) and easy custom domain support.
