# Classic City Band Website

Modern Jekyll website for classiccityband.org hosted on GitHub Pages.

## Quick Start - Getting This Live in 5 Days

### Step 1: Upload Files to GitHub

1. Go to your repository: https://github.com/webmasterCCB/CCBwebsite
2. **IMPORTANT:** Make sure your repo is PUBLIC (GitHub Pages requires this on free accounts)
   - Go to Settings > General > scroll to bottom
   - Click "Change visibility" > Make public
3. Click "Add file" > "Upload files"
4. Drag ALL the files from this folder into GitHub
5. Commit the files

### Step 2: Enable GitHub Pages

1. In your repo, go to **Settings**
2. Click **Pages** in the left sidebar
3. Under **Source**, select:
   - Branch: **main**
   - Folder: **/ (root)**
4. Click **Save**
5. Wait 2-5 minutes - your site will be live at: `https://webmastercCB.github.io/CCBwebsite/`

### Step 3: Point Your Domain

1. In your Bluehost/domain registrar:
   - Find DNS settings
   - Add a CNAME record:
     - Name: `www`
     - Value: `webmasterCCB.github.io`
   - Add A records pointing to:
     - 185.199.108.153
     - 185.199.109.153
     - 185.199.110.153
     - 185.199.111.153

2. Back in GitHub Pages settings:
   - Enter your custom domain: `classiccityband.org`
   - Check "Enforce HTTPS" (wait 24 hours first)

Domain changes can take up to 48 hours to propagate.

---

## Customization Checklist

### Immediate Priorities

- [ ] **Edit _config.yml** - Update email, social media URLs
- [ ] **Replace placeholder images** on homepage (in index.html)
- [ ] **Add Google Calendar** to concerts.md and index.html
- [ ] **Set up donation buttons** in carnegie-hall.md (PayPal, Stripe, etc.)
- [ ] **Fill in missing info** in about.md (history, conductor bio, etc.)
- [ ] **Add rehearsal details** in join.md (day, time, location)
- [ ] **Add contact phone numbers** where marked
- [ ] **Update Carnegie Hall progress** in carnegie-hall.md as donations come in

### Photos to Add

Replace the placeholder images with real photos:
- Hero section on homepage
- Event cards on homepage  
- Carnegie Hall page header
- Performance photos throughout

Save photos to `/assets/images/` and update the image paths in the HTML/Markdown files.

### Google Calendar Setup

1. Create a Google Calendar for CCB events (or use existing)
2. Go to Calendar Settings > Integrate calendar
3. Copy the embed code
4. Paste into:
   - `index.html` (in the calendar-container section)
   - `concerts.md` (in the calendar-container section)

### Payment Integration

For Carnegie Hall fundraising, choose a payment processor:

**PayPal** (Easiest):
1. Go to paypal.com/donate
2. Create a donation button
3. Copy the button code
4. Paste into carnegie-hall.md

**Stripe**:
1. Create a Stripe account
2. Use Stripe Checkout or Payment Links
3. Add the link/button to carnegie-hall.md

**Multiple options**: Add both so donors can choose!

---

## Editing the Site

### Simple Text Changes

Most pages are in Markdown (.md files). Edit them like a text document:

```markdown
## This is a heading

This is regular text.

[This is a link](https://example.com)
```

### Updating the Homepage

Edit `index.html` to change:
- Hero text
- Carnegie Hall banner
- Event cards

### Changing Colors

Edit `assets/css/style.css`:
- `--primary-red` 
- `--primary-navy`
- `--accent-gold`

### Adding New Pages

1. Create a new .md file (e.g., `media.md`)
2. Add this header:
```
---
layout: page
title: Your Page Title
---

Your content here
```
3. Add link to `_includes/header.html` navigation

---

## Updating Content

### Via GitHub Website (Easiest)

1. Go to your repo
2. Click on the file you want to edit
3. Click the pencil icon (Edit)
4. Make changes
5. Scroll down and click "Commit changes"
6. Wait 1-2 minutes, refresh your site

### Via Git (If you're comfortable with command line)

```bash
git clone https://github.com/webmasterCCB/CCBwebsite.git
cd CCBwebsite
# Make your changes
git add .
git commit -m "Update content"
git push
```

---

## Carnegie Hall Progress Updates

To update the fundraising thermometer:

1. Edit `carnegie-hall.md`
2. Find the progress-bar section
3. Update two things:
   - `width: 0%` → change to percentage raised (e.g., `width: 20%`)
   - `$0 raised` → change to actual amount (e.g., `$10,000 raised`)

Example:
```html
<div class="progress-bar" style="width: 35%;">
  $17,500 raised of $50,000
</div>
```

---

## Members-Only Section (Future)

When ready to add password-protected pages:

1. Create a new page: `members.md`
2. Add this JavaScript at the top:
```html
<script>
var password = "your-password-here";
var input = prompt("Enter password:");
if (input !== password) {
  window.location.href = "/";
}
</script>
```

This is basic protection - good enough for rehearsal schedules and internal docs.

---

## Troubleshooting

**Site not showing up?**
- Wait 5-10 minutes after committing
- Check Settings > Pages shows "Your site is live at..."
- Make sure repo is public

**Changes not appearing?**
- Wait 1-2 minutes
- Hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
- Check if file was actually committed

**Domain not working?**
- DNS changes take 24-48 hours
- Check if site works at github.io URL first
- Verify DNS settings in domain registrar

**Styling looks broken?**
- Check if style.css uploaded correctly
- Look for typos in file paths

---

## Support

Jekyll documentation: https://jekyllrb.com/docs/  
GitHub Pages docs: https://docs.github.com/en/pages

---

## Current Status

- ✅ Site structure complete
- ✅ Carnegie Hall fundraising page ready
- ✅ Modern responsive design
- ✅ Red/Navy color scheme
- ⏳ Needs real content/photos
- ⏳ Needs Google Calendar
- ⏳ Needs payment integration

**Target: Live in 5 days!**
