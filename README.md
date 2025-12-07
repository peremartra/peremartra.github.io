# Pere Martra - Personal Site

Clean, professional landing page with photo, social links, and two-column service layout.

## Quick Setup (5 minutes)

### 1. Add Your Photo
Place your profile photo: `assets/images/profile.jpg`
- Format: JPG or PNG
- Recommended: 400x400px minimum
- Will display as 160px circle

### 2. Update Personal Info
Edit `_config.yml`:
```yaml
author:
  email: your-actual-email@example.com

github_username: peremartra
linkedin_username: your-linkedin
twitter_username: your-twitter  # optional, remove if you don't have one
```

### 3. Review Content
Check `index.md` for the About section and Current Work.

Training and Consulting content is in `_layouts/home.html` (lines 49-86).
To edit services, see "Editing Services Content" below.

### 4. Upload to GitHub

**Via Web:**
1. Create repo: `peremartra.github.io`
2. Drag all files
3. Commit

**Via Terminal:**
```bash
cd peremartra-final
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/peremartra/peremartra.github.io.git
git push -u origin main
```

### 5. Enable GitHub Pages
Settings → Pages → Source: `main` → Folder: `/ (root)` → Save

Wait 2 minutes → https://peremartra.github.io

---

## Site Structure

```
┌─────────────────────────────────────┐
│  [PHOTO]  PERE MARTRA               │
│           GitHub LinkedIn X          │
├─────────────────────────────────────┤
│  About & Current Work               │
├──────────────────┬──────────────────┤
│ TRAINING         │ CONSULTING       │
│ - Workshops      │ - LLM Opt        │
│ - Small teams    │ - Agent Migrate  │
└──────────────────┴──────────────────┘
│ Selected Work (Books + Repos)       │
├─────────────────────────────────────┤
│ Contact                             │
└─────────────────────────────────────┘
```

---

## Editing Content

### About Section
Edit `index.md` - everything after `---`

### Services (Training & Consulting)
Edit `_layouts/home.html` lines 49-86

**Training section (lines 49-63):**
- Service intro
- What I Offer
- Format
- Availability

**Consulting section (lines 65-79):**
- LLM Optimization
- Agent Migration
- Availability

### Credentials (Books & Repos)
Edit `_layouts/home.html` lines 82-96

### Styling
Edit `assets/css/style.css`:
- Main accent color: `#2563eb` (blue, used throughout)
- Background: `#fafbfc` (service boxes)
- Text: `#2c3e50` (main), `#4a5568` (secondary)

---

## File Descriptions

### Core Files
- `index.md` - About section content
- `_layouts/home.html` - Page structure and services content
- `assets/css/style.css` - All styling
- `_config.yml` - Site configuration and personal info

### Assets
- `assets/images/profile.jpg` - Your photo (ADD THIS)
- `assets/css/style.css` - Styling

### Configuration
- `Gemfile` - Ruby dependencies
- `.gitignore` - Files to ignore
- `_config.yml` - Jekyll config

---

## Key Features

✅ Clean hero with circular photo  
✅ Professional two-column layout  
✅ Credentials section below services  
✅ Mobile responsive  
✅ Font Awesome icons for social links  
✅ No JavaScript (fast & simple)  
✅ Easy to edit  

---

## Customization

### Change Colors
Edit `style.css`:
- Find `#2563eb` (blue accent) - replace with your preferred color
- Find `#fafbfc` (service box background) - adjust if needed

### Change Layout
- Adjust column widths: `.services` grid (line 106)
- Adjust spacing: padding/margin values throughout

### Add/Remove Social Links
Edit `_config.yml`:
- Add username (no @ symbol)
- To remove: delete or comment out the line
- Icons update automatically

---

## Local Preview (Optional)

```bash
bundle install
bundle exec jekyll serve
# Visit http://localhost:4000
```

Not required - you can edit directly on GitHub.

---

## Custom Domain (Later)

Settings → Pages → Custom domain → `peremartra.com`

Then configure DNS at your domain provider.

---

## Content Guidelines

**Keep it concise:**
- About: 2-3 paragraphs max
- Services: Brief descriptions
- Credentials: Highlights only

**What to emphasize:**
- Your unique expertise
- Concrete deliverables
- Limited availability (creates value)

**What to avoid:**
- Long paragraphs
- Too much technical jargon
- Overwhelming detail

---

## Troubleshooting

**Photo not showing:**
- Check file is at `assets/images/profile.jpg`
- Case-sensitive on Linux servers

**Services not updating:**
- Edit `_layouts/home.html`, not `index.md`
- Wait 2-3 minutes after push

**Social icons missing:**
- Font Awesome loads from CDN
- Check internet connection
- Verify usernames in `_config.yml`

**Columns look weird:**
- On mobile, columns stack (this is normal)
- On desktop, should be side-by-side

---

## Next Steps

1. [ ] Add profile.jpg
2. [ ] Update _config.yml
3. [ ] Review index.md
4. [ ] Upload to GitHub
5. [ ] Enable Pages
6. [ ] Test on mobile
7. [ ] Share link

---

## Philosophy

This site prioritizes:
- **Immediate impact** (photo + name)
- **Clear structure** (hero → about → services)
- **Minimal content** (people scan, don't read)
- **Easy maintenance** (few files to edit)

Less content, more clarity.

---

## Support

- Jekyll docs: https://jekyllrb.com
- GitHub Pages: https://pages.github.com
- Font Awesome: https://fontawesome.com

For questions about the structure, review the comments in `_layouts/home.html` and `style.css`.
