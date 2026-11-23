# Personal website

A single-page static site: plain HTML and CSS, no frameworks, no build step.

```
personal-website/
  index.html
  styles.css
  vercel.json
  assets/
    background.jpg
    background-retro.jpg
    portrait.png
    favicon.png
    fonts/
      Exo2-VariableFont_wght.woff
  README.md
```

## Before you deploy

Open `index.html` and replace the items marked `TODO`:

1. `Your Name` in the `<title>`, the meta description and the `<h1>`.
2. The LinkedIn and GitHub URLs in the footer.

To preview locally, open `index.html` in your browser.

## Deploy with GitHub and Vercel

### 1. Create a GitHub repository
1. Sign in at [github.com](https://github.com) and click **New repository**.
2. Name it (for example `personal-website`), leave it empty (no README or .gitignore) and click **Create repository**.

### 2. Upload or push the project
**Easiest (browser upload):** on the new repository page click **uploading an existing file**, drag in everything inside the `personal-website` folder (including the `assets` folder), then click **Commit changes**.

**Or with Git:**
```bash
cd personal-website
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/personal-website.git
git push -u origin main
```

### 3. Import the repository into Vercel
1. Sign in at [vercel.com](https://vercel.com) with your GitHub account.
2. Click **Add New... > Project**, find your repository and click **Import**.

### 4. Deploy
1. Leave **Framework Preset** as **Other**. Leave Build Command and Output Directory empty.
2. Click **Deploy**. After a few seconds you get a live `.vercel.app` URL.
3. Future changes pushed to `main` redeploy automatically.

### 5. Connect your custom domain
1. In Vercel open your project, then **Settings > Domains**, enter your domain and click **Add**.
2. Vercel shows the DNS records to set at your domain registrar. Typically:
   - **Apex domain** (`example.com`): an `A` record pointing to the IP Vercel displays.
   - **Subdomain** (`www.example.com`): a `CNAME` record pointing to the value Vercel displays.
3. Use the exact values Vercel shows for your project, as they can change. Wait for DNS to propagate (minutes to a few hours); Vercel issues the HTTPS certificate automatically.
