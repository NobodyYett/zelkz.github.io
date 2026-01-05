# Zelkz Legal Pages - GitHub Pages Setup

This folder contains legal documents for Zelkz apps, ready to deploy to GitHub Pages.

## File Structure

```
/
├── index.html              ← Landing page (zelkz.github.io)
└── bloom/
    ├── privacy.html        ← Privacy Policy (zelkz.github.io/bloom/privacy.html)
    └── terms.html          ← Terms of Service (zelkz.github.io/bloom/terms.html)
```

## Deployment Steps

### Step 1: Create GitHub Repository

1. Go to [github.com/new](https://github.com/new)
2. Name the repository: **`zelkz.github.io`** (must match your GitHub username)
3. Make it **Public**
4. Click **Create repository**

### Step 2: Upload Files

**Option A: GitHub Web Interface (Easiest)**

1. In your new repo, click **"Add file"** → **"Upload files"**
2. Drag and drop all files maintaining the folder structure:
   - `index.html`
   - `bloom/privacy.html`
   - `bloom/terms.html`
3. Click **"Commit changes"**

**Option B: Command Line**

```bash
# Clone the empty repo
git clone https://github.com/YOUR_USERNAME/zelkz.github.io.git
cd zelkz.github.io

# Copy the files (adjust path as needed)
cp -r /path/to/github-pages/* .

# Push to GitHub
git add .
git commit -m "Add legal pages for Bloom"
git push origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repo on GitHub
2. Click **Settings** → **Pages** (in left sidebar)
3. Under "Source", select **Deploy from a branch**
4. Select **main** branch and **/ (root)**
5. Click **Save**
6. Wait 1-2 minutes for deployment

### Step 4: Verify

Your pages will be live at:

| Page | URL |
|------|-----|
| Landing | `https://zelkz.github.io` |
| Privacy Policy | `https://zelkz.github.io/bloom/privacy.html` |
| Terms of Service | `https://zelkz.github.io/bloom/terms.html` |

## Custom Domain (Optional)

If you buy `zelkz.com`, you can connect it:

1. In repo Settings → Pages → Custom domain
2. Enter `zelkz.com`
3. Add DNS records at your domain registrar:
   - Type: `A` → `185.199.108.153`
   - Type: `A` → `185.199.109.153`
   - Type: `A` → `185.199.110.153`
   - Type: `A` → `185.199.111.153`
   - Type: `CNAME` for `www` → `zelkz.github.io`

## Adding Future Apps

To add legal pages for another app:

1. Create a new folder (e.g., `new-app/`)
2. Add `privacy.html` and `terms.html`
3. Update `index.html` to include a new app section
4. Commit and push

## URLs for App Store Connect

Use these URLs when submitting to App Store:

- **Privacy Policy URL:** `https://zelkz.github.io/bloom/privacy.html`
- **Terms of Service URL:** `https://zelkz.github.io/bloom/terms.html`

## Support

Questions? Contact support@zelkz.com
