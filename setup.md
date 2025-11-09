# GitHub Pages Setup Instructions

## Quick Setup Guide

### Step 1: Create GitHub Repository

1. Go to GitHub.com and create a new repository
2. Name it (e.g., `capcut-download` or use your username for `username.github.io`)
3. Make it **Public** (required for free GitHub Pages)

### Step 2: Upload Files

1. Upload all files to your repository:
   - `index.html`
   - `thankyou.html`
   - `404.html`
   - `_config.yml`
   - `images.png`
   - `README.md`
   - All other files

### Step 3: Enable GitHub Pages

**Option A: Using Repository Settings (Recommended)**

1. Go to your repository on GitHub
2. Click **Settings** tab
3. Scroll down to **Pages** section (left sidebar)
4. Under **Source**, select:
   - Branch: `main` (or `master`)
   - Folder: `/ (root)`
5. Click **Save**
6. Wait 1-2 minutes for GitHub to build your site

**Option B: Using GitHub Actions (Advanced)**

- The `.github/workflows/pages.yml` file will automatically deploy when you push to main branch

### Step 4: Access Your Site

Your site will be available at:

- `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`
- Or if repository is named `YOUR-USERNAME.github.io`: `https://YOUR-USERNAME.github.io/`

### Step 5: Test URLs

- Home: `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/` or `/index.html`
- Thank You: `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/thankyou` or `/thankyou.html`

## Troubleshooting

### Error: "There isn't a GitHub Pages site here"

**Solution 1: Check Repository Settings**

1. Make sure GitHub Pages is enabled in Settings > Pages
2. Select the correct branch (`main` or `master`)
3. Wait 2-5 minutes after enabling (GitHub needs time to build)

**Solution 2: Check Repository Name**

- If your URL is `username.github.io/repository-name`, make sure the repository name matches
- Repository must be **Public** (or you need GitHub Pro for private repos)

**Solution 3: Check File Structure**

- All files should be in the root of the repository (or in `/docs` folder if using that option)
- Make sure `index.html` exists in the root

**Solution 4: Force Rebuild**

1. Go to Settings > Pages
2. Change the source branch to something else, save
3. Change it back to `main`, save
4. Wait for rebuild

### Clean URLs Not Working

If `/thankyou` doesn't work but `/thankyou.html` does:

1. **Check \_config.yml exists** - This file is needed for Jekyll
2. **Wait for Jekyll to process** - GitHub Pages uses Jekyll, wait 1-2 minutes after pushing files
3. **Use direct links** - You can always use `/thankyou.html` directly in your links

### Alternative: Disable Jekyll

If you want to disable Jekyll completely:

1. Create a file named `.nojekyll` in the root
2. This will serve files as-is without Jekyll processing
3. You'll need to use `.html` extensions in URLs

## File Checklist

Make sure these files are in your repository:

- ✅ `index.html`
- ✅ `thankyou.html`
- ✅ `404.html`
- ✅ `_config.yml`
- ✅ `images.png`
- ✅ `README.md`
- ✅ `.github/workflows/pages.yml` (optional)

## Custom Domain (Optional)

To use a custom domain:

1. Add a `CNAME` file with your domain name
2. Configure DNS settings as per GitHub instructions
3. Update domain in repository Settings > Pages

## Need Help?

- Check GitHub Pages documentation: https://docs.github.com/en/pages
- GitHub Pages status: https://www.githubstatus.com/
- Repository settings: Settings > Pages
