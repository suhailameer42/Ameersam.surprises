# Ameer Surprise Page

This project contains the `sam.html` surprise page and the generated QR code assets.

## Push to your GitHub account

Use your GitHub URL and create a repository, for example:
- `https://github.com/suhailameer42/ameer-surprise`

Then run these commands from `c:\Users\suhai\OneDrive\Desktop\m`:

```bash
git init
git add .
git commit -m "Deploy surprise page"
git branch -M main
git remote add origin https://github.com/suhailameer42/ameer-surprise.git
git push -u origin main
```

## Enable GitHub Pages

1. Open the repo on GitHub.
2. Go to `Settings` → `Pages`.
3. Set source to `main` branch and folder `/ (root)`.
4. Save.

## Custom domain

The `CNAME` file already includes:

```
Ameer.com
```

Make sure your domain DNS is pointed to GitHub Pages if you want `http://Ameer.com/sam.html` to work.
