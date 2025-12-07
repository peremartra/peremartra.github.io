# Pere Martra - Personal Site

Minimal Jekyll site for GitHub Pages. No problematic plugins, works out of the box.

## Quick Setup

### 1. Create GitHub Repository

1. Go to GitHub and create a new repository named `peremartra.github.io`
2. Make it public
3. Don't initialize with README (we have this one)

### 2. Upload Files

**Option A: Via GitHub Web Interface**
1. Go to your new repository
2. Click "uploading an existing file"
3. Drag and drop ALL files from this folder
4. Commit with message: "Initial site setup"

**Option B: Via Git Command Line**
```bash
cd /path/to/this/folder
git init
git add .
git commit -m "Initial site setup"
git branch -M main
git remote add origin https://github.com/peremartra/peremartra.github.io.git
git push -u origin main
```

### 3. Enable GitHub Pages

1. Go to your repository settings
2. Navigate to "Pages" in the left sidebar
3. Under "Source", select "Deploy from a branch"
4. Select branch: `main` and folder: `/ (root)`
5. Click "Save"

### 4. Wait for Deployment

GitHub will build your site automatically. This takes 1-2 minutes.

Your site will be live at: `https://peremartra.github.io`

## Customization

### Essential Edits (Before Publishing)

Edit `_config.yml`:
```yaml
email: your-actual-email@example.com
# Uncomment and add your social links:
github_username: peremartra
linkedin_username: your-linkedin
```

Edit `contact.md`:
- Replace "your-email@example.com" with your actual email
- Update GitHub and LinkedIn links

### Content Updates

All content is in Markdown files. Edit directly on GitHub or locally:

- `index.md` - Home page / Hero section
- `research.md` - Publications and projects
- `training.md` - Training programs
- `contact.md` - Contact information

### Local Development (Optional)

If you want to preview changes locally before pushing:

```bash
# Install dependencies (first time only)
bundle install

# Run local server
bundle exec jekyll serve

# View at http://localhost:4000
```

## Adding Your Custom Domain (Later)

1. In repository settings → Pages → Custom domain
2. Enter: `peremartra.com`
3. Check "Enforce HTTPS" (after DNS propagates)
4. Update your domain's DNS:
   - Add CNAME record: `www` → `peremartra.github.io`
   - Add A records for apex domain (see [GitHub docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site))

## Troubleshooting

**Site not appearing after 5 minutes?**
- Check GitHub Actions tab in your repo for build errors
- Ensure repository is public
- Verify GitHub Pages is enabled in settings

**Build failing?**
- This setup uses only GitHub Pages compatible gems
- Should work without any configuration changes
- Check the Actions tab for specific error messages

**Need to make quick fixes?**
- Edit files directly on GitHub
- Changes deploy automatically within 1-2 minutes

## Structure

```
.
├── _config.yml          # Site configuration
├── index.md             # Home page
├── research.md          # Research & publications
├── training.md          # Training programs
├── contact.md           # Contact page
├── Gemfile              # Ruby dependencies
└── README.md            # This file
```

## Next Steps

1. [ ] Replace placeholder email addresses
2. [ ] Add your actual GitHub/LinkedIn/Twitter links
3. [ ] Update contact page with preferred contact method
4. [ ] Optional: Add a profile photo
5. [ ] Optional: Customize colors/styling
6. [ ] Test all links after deployment

## Support

Jekyll documentation: https://jekyllrb.com/docs/  
GitHub Pages docs: https://docs.github.com/en/pages

---

**Note**: This is a minimal setup using only GitHub Pages native features. No external plugins = no deployment headaches.
