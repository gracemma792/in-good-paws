# 🐾 In Good Paws — Dog Walking Website

A beautiful Astro website for the In Good Paws dog walking business, built for deployment on GitHub Pages.

## Tech Stack
- **Framework**: [Astro](https://astro.build) v4
- **Hosting**: GitHub Pages (static)
- **CI/CD**: GitHub Actions

## Setup & Deployment

### 1. Edit `astro.config.mjs`
Update the `site` and `base` fields:
```js
export default defineConfig({
  site: 'https://YOUR-GITHUB-USERNAME.github.io',
  base: '/in-good-paws',  // or '/' if this is your root repo
});
```

### 2. Push to GitHub
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/in-good-paws.git
git push -u origin main
```

### 3. Enable GitHub Pages
- Go to your repo → **Settings** → **Pages**
- Under **Source**, select **GitHub Actions**

That's it! GitHub Actions will automatically build and deploy on every push to `main`.

## Local Development
```bash
npm install
npm run dev
```

## Customise

### Update your contact info
Edit `src/components/Contact.astro`:
- Phone number
- Email address
- Service area

### Update your pricing
Edit `src/components/Services.astro` — change the `price` field on each service.

### Update testimonials
Edit `src/components/Testimonials.astro` — swap in real client reviews.

### Update the `astro.config.mjs`
If your repo is named something else, update `base` to match.

## Project Structure
```
in-good-paws/
├── .github/workflows/deploy.yml   # GitHub Actions CI/CD
├── src/
│   ├── layouts/Layout.astro       # Base HTML layout + global CSS
│   ├── pages/index.astro          # Main page
│   └── components/
│       ├── Nav.astro
│       ├── Hero.astro
│       ├── Services.astro
│       ├── About.astro
│       ├── Testimonials.astro
│       ├── Contact.astro
│       └── Footer.astro
├── public/
│   └── favicon.svg
├── astro.config.mjs
└── package.json
```
