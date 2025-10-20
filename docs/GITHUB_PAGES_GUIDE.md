# GitHub Pages Setup Guide

How to turn your repository into a live website

---

## What Is GitHub Pages?

GitHub Pages turns your repository into a public website. Instead of people navigating markdown files on GitHub, they can read your content on a clean, formatted website.

**Your future website URL will be:**
`https://michalvalco.github.io/postmodern-sage/`

---

## Setup Steps

### Step 1: Enable GitHub Pages

1. Go to your repository: https://github.com/michalvalco/postmodern-sage
2. Click **Settings** (top menu)
3. Scroll down to **Pages** (left sidebar under "Code and automation")
4. Under "Build and deployment":
   - **Source:** Select "Deploy from a branch"
   - **Branch:** Select "main" and "/root" (or "/ (root)")
   - Click **Save**

### Step 2: Wait for Deployment (2-5 minutes)

GitHub will build your site. You'll see:
- "Your site is being built from the main branch"
- Then: "Your site is live at https://michalvalco.github.io/postmodern-sage/"

### Step 3: Visit Your Site

After deployment completes, visit:
`https://michalvalco.github.io/postmodern-sage/`

---

## What Gets Displayed?

**Default behavior:**
- GitHub Pages looks for `README.md` in your root directory
- Converts it to HTML automatically
- Uses a basic GitHub theme

**Your current setup will show:**
- Your main README.md as the homepage
- All markdown files are accessible via their paths
- Example: `https://michalvalco.github.io/postmodern-sage/wisdom-library/README.md`

---

## Customization Options

### Option A: Use Jekyll Theme (Simple)

GitHub Pages uses Jekyll by default. You can choose a theme:

1. Go to Settings → Pages
2. Under "Theme Chooser," click "Choose a theme"
3. Select one (e.g., Minimal, Cayman, Slate)
4. GitHub will add a `_config.yml` file to your repository

**Recommended for you:** "Minimal" or "Cayman" theme
- Clean, readable
- Works well for text-heavy content
- Professional appearance

### Option B: Create Custom Jekyll Site (Advanced)

Create a `_config.yml` file in your root directory:

```yaml
title: A Postmodern Sage
description: Wisdom for 21st-century seekers
theme: minima
baseurl: "/postmodern-sage"
url: "https://michalvalco.github.io"

# Navigation
header_pages:
  - wisdom-library/README.md
  - contemporary-challenges/README.md
  - practical-guides/README.md
  - recommended-resources/README.md

# Social links
github_username: michalvalco
```

### Option C: Use Custom Domain (Professional)

If you own a domain (e.g., `postmodernsage.com`):

1. Go to Settings → Pages
2. Under "Custom domain," enter your domain
3. Follow instructions to configure DNS
4. Your site becomes: `https://postmodernsage.com`

---

## Making Your Site Look Better

### 1. Add a Custom Index Page

Create `index.md` in your root directory (GitHub will prioritize this over README.md):

```markdown
---
layout: default
title: Home
---

# Welcome to A Postmodern Sage

Wisdom for navigating 21st-century challenges.

[Explore the Wisdom Library →](wisdom-library/)
[Contemporary Challenges →](contemporary-challenges/)
[Practical Guides →](practical-guides/)
```

### 2. Improve Navigation

Add front matter to your markdown files:

```markdown
---
layout: default
title: Ethics in Practice
---

# Ethics in Practice

Your content here...
```

### 3. Add Custom CSS (Optional)

Create `assets/css/style.scss`:

```scss
---
---

@import "{{ site.theme }}";

// Custom styles
body {
  font-family: Georgia, serif;
  line-height: 1.8;
}

h1, h2, h3 {
  color: #2c3e50;
}
```

---

## Current vs. Enhanced Setup

### What You Have Now (Basic)

✅ Repository content is accessible  
✅ Markdown renders as HTML  
✅ Basic GitHub styling  
⚠️ No custom navigation  
⚠️ Basic visual design  

### What You Could Have (Enhanced)

✅ Custom theme  
✅ Professional navigation menu  
✅ Custom homepage  
✅ Better typography  
✅ Social sharing  
✅ Custom domain (optional)  

---

## Recommended Next Steps

### For Quick Launch (5 minutes)

1. **Choose a theme** in Settings → Pages → Theme Chooser
2. **Test your site** at https://michalvalco.github.io/postmodern-sage/
3. **Done!** Your content is now live

### For Professional Setup (30 minutes)

1. **Choose theme** (Minimal or Cayman recommended)
2. **Create `_config.yml`** with the configuration above
3. **Create custom `index.md`** for homepage
4. **Add navigation** to key sections
5. **Test and refine**

### For Advanced Setup (2-3 hours)

1. All of the above, plus:
2. **Custom CSS** for brand styling
3. **Blog functionality** for regular updates
4. **Search functionality** (Jekyll plugin)
5. **Analytics integration** (Google Analytics)
6. **Custom domain** setup

---

## Testing Your Site

After any changes:

1. **Commit and push** changes to GitHub
2. **Wait 2-5 minutes** for GitHub to rebuild
3. **Refresh your browser** (hard refresh: Ctrl+Shift+R or Cmd+Shift+R)
4. **Check for errors** in Settings → Pages

---

## Troubleshooting

**Site not building?**
- Check Settings → Pages for error messages
- Verify `_config.yml` syntax if you created one
- Ensure branch is set to "main"

**Changes not showing?**
- GitHub Pages caching can take 5-10 minutes
- Try hard refresh in browser
- Clear browser cache

**404 errors?**
- Check file paths (case-sensitive)
- Ensure files have `.md` extension
- Verify links use correct relative paths

---

## Resources

**GitHub Pages Documentation:**
https://docs.github.com/en/pages

**Jekyll Themes:**
https://pages.github.com/themes/

**Jekyll Documentation:**
https://jekyllrb.com/docs/

---

## My Recommendation for You

**Start simple:**

1. ✅ Enable GitHub Pages (you've done this)
2. Choose "Minimal" theme in Theme Chooser
3. Test at https://michalvalco.github.io/postmodern-sage/
4. See how it looks
5. Decide if you want more customization

**Your content is already well-structured.** A basic theme will make it look professional immediately.

**Later, if you want:** Custom domain, advanced styling, blog features

---

**Current Status:** ✅ GitHub Pages is enabled  
**Next Step:** Choose a theme in Settings → Pages → Theme Chooser  
**Test URL:** https://michalvalco.github.io/postmodern-sage/

Let me know when you've chosen a theme and I'll help you customize further!
