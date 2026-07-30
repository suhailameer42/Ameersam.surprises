# Deploying sam.html to GitHub Pages with a custom domain

## Goal
Make `http://Ameer.com/sam.html` open directly and allow the QR code to work from any network.

## What is needed
1. You must own or control the `Ameer.com` domain.
2. The domain must be configured to point at a public host.
3. `sam.html` must be uploaded to that host.

## Recommended setup: GitHub Pages

### 1. Create a GitHub repository
- Create a new public repository on GitHub, for example `ameer-surprise`.
- Clone it locally or upload your files using the GitHub web UI.

### 2. Add your files
Copy these files into the repo:
- `sam.html`
- `index.html` (if needed)
- `images/` folder and any other assets
- `share-qr.png`
- `heart-qr.png` / other QR images
- `CNAME` (already created in this workspace)

The `CNAME` file should contain exactly:
```
Ameer.com
```

### 3. Enable GitHub Pages
- In the GitHub repo, go to `Settings` → `Pages`.
- Set the source branch to `main` (or `master`) and folder `/ (root)`.
- Save.

### 4. Update DNS for `Ameer.com`
Use your domain provider to add these records:
- `A` record to `185.199.108.153`
- `A` record to `185.199.109.153`
- `A` record to `185.199.110.153`
- `A` record to `185.199.111.153`

Or if GitHub Pages asks, add a `CNAME` record to `username.github.io`.

### 5. Wait for DNS propagation
It can take some minutes to hours for the domain to start resolving to GitHub Pages.

### 6. Test
Open:
- `http://Ameer.com/sam.html`

If it loads, the QR code you generated will work on any network.

## If you do not own `Ameer.com`
Then this link cannot be made to work globally unless the owner configures the domain for you.

## Note
A QR image that encodes `http://Ameer.com/sam.html` is already generated in `share-qr.png`, but the domain must point to your hosted page for it to work.
