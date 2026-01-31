# Classic City Band Website - Admin Guide

## Welcome!

This guide will help you manage the Classic City Band website. No technical expertise required - if you can edit a document, you can update this site!

## Quick Facts

- **Website:** classiccityband.org
- **Hosting:** GitHub Pages (FREE - no monthly fees!)
- **Repository:** https://github.com/webmasterCCB/CCBwebsite
- **No plugins to update, no security vulnerabilities, no monthly costs**

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Common Tasks](#common-tasks)
3. [Updating Pages](#updating-pages)
4. [Adding Images](#adding-images)
5. [Managing Calendars](#managing-calendars)
6. [Emergency Contacts](#emergency-contacts)

---

## Getting Started

### What You Need
- GitHub account with access to the CCBwebsite repository
- Basic text editing skills
- That's it!

### How the Site Works
- Files are stored on GitHub
- When you edit a file and save ("commit"), GitHub automatically rebuilds the site
- Changes appear live in 2-3 minutes
- No software to install - everything is done in your web browser

---

## Common Tasks

### Task 1: Update Concert Information

**File to edit:** `concerts.md`

1. Go to: https://github.com/webmasterCCB/CCBwebsite
2. Click on `concerts.md`
3. Click the pencil icon (top right) to edit
4. Make your changes
5. Scroll down, add a commit message like "Updated spring concert info"
6. Click "Commit changes"
7. Wait 2-3 minutes and refresh the website to see changes

### Task 2: Update Contact Email

**File to edit:** `_config.yml`

1. Go to: https://github.com/webmasterCCB/CCBwebsite
2. Click on `_config.yml`
3. Click the pencil icon
4. Find the line: `email: info@classiccityband.org`
5. Change the email address
6. Commit changes
7. This updates the email everywhere on the site automatically!

### Task 3: Add/Change Photos

**Folder:** `assets/images/`

1. Go to: https://github.com/webmasterCCB/CCBwebsite/tree/main/assets/images
2. Click "Add file" → "Upload files"
3. Drag your photo(s) into the upload area
4. Click "Commit changes"
5. Photos should be:
   - JPG format for photos
   - PNG format for logos/graphics with transparency
   - Under 500KB each (compress large photos first)
   - Reasonable dimensions (1920px wide max for hero images, 800px for content photos)

**To use your uploaded photo in a page:**
- Edit the page file (like `about.md`)
- Add this line where you want the photo:
  ```
  ![Description of photo](/CCBwebsite/assets/images/your-photo-name.jpg)
  ```

### Task 4: Update Navigation Menu

**File to edit:** `_includes/header.html`

1. Go to: https://github.com/webmasterCCB/CCBwebsite/tree/main/_includes
2. Click `header.html`
3. Click the pencil icon
4. Find the `<nav>` section with the menu items
5. To change text: Edit between `>` and `</a>`
6. To add a new link: Copy an existing `<li><a>...</a></li>` line and modify it
7. Commit changes

### Task 5: Update Home Page Text

**File to edit:** `index.html`

1. Go to: https://github.com/webmasterCCB/CCBwebsite
2. Click `index.html`
3. Click the pencil icon
4. Find the section you want to change (hero text is near the top)
5. Edit carefully - don't change things in `< >` brackets unless you know what you're doing
6. Commit changes

---

## Updating Pages

### Main Pages and Their Files

| Page | Filename | Purpose |
|------|----------|---------|
| Home | `index.html` | Landing page with hero image and quick links |
| Performances | `concerts.md` | Concert calendar |
| About | `about.md` | Band history and information |
| Join Us | `join.md` | Membership information and form |
| Support | `support.md` | Donation options |
| Carnegie Hall | `carnegie-hall.md` | Carnegie Hall trip information |
| Big Band Athens | `bigband-athens.md` | Big Band Athens ensemble page |
| German Polka Band | `polka/polka.md` | Polka band page |

### How to Edit Any Page

1. Navigate to the file on GitHub
2. Click the pencil icon
3. Make changes:
   - Regular text: Just type normally
   - **Bold text:** Use `**bold text**` or `<strong>bold text</strong>`
   - *Italic text:* Use `*italic*` or `<em>italic</em>`
   - Headings: Use `##` for main headings, `###` for subheadings
   - Links: Use `[link text](URL)` or `<a href="URL">link text</a>`
4. Scroll down and commit changes

### Tips for Editing
- Always add a clear commit message explaining what you changed
- Preview changes if possible (some files show a Preview tab)
- Don't delete lines you don't understand - they might be needed for formatting
- If you break something, you can always revert to a previous version (see "Emergency Help" below)

---

## Adding Images

### Image Specifications

**Hero Image (top of homepage):**
- Dimensions: 1920px wide × 800-1000px tall
- Format: JPG
- File size: Under 500KB
- Current file: `assets/images/Michael_conducts_audience_singalong.jpg`

**Quick Links Button Images:**
- Dimensions: 400px × 190px (for main buttons)
- Format: PNG with transparency
- Current files: `performances-bg.png`, `support-bg.png`, `join-bg.png`, etc.

**Content Images:**
- Dimensions: 800-1200px wide recommended
- Format: JPG
- File size: Under 300KB

### How to Replace the Hero Image

1. Create your new image (1920×800px)
2. Upload to `assets/images/` (name it something descriptive)
3. Edit `assets/css/style.css`
4. Find the line: `background: url('../images/Michael_conducts_audience_singalong.jpg')`
5. Change the filename to your new image name
6. Commit changes

### How to Add Images to Pages

**Simple method (in .md files):**
```markdown
![Image description](/CCBwebsite/assets/images/your-image.jpg)
```

**With more control:**
```html
<img src="/CCBwebsite/assets/images/your-image.jpg" 
     alt="Image description" 
     style="max-width: 100%; height: auto;">
```

---

## Managing Calendars

### The calendars are Google Calendars - update them directly in Google!

**Current Calendars:**
1. Classic City Band Performances
2. Big Band Athens Performances

**To update events:**
1. Log into the CCB Google account
2. Open Google Calendar
3. Add, edit, or delete events
4. Changes appear on the website automatically (no need to touch GitHub!)

**To change calendar settings:**
- The embed codes are in `concerts.md`
- Only change these if you need to show a different calendar
- The current setup shows events in "Agenda" (list) view

### Calendar Embed Code Location
File: `concerts.md`
Look for lines starting with `<iframe src="https://calendar.google.com/..."`

---

## Site Colors

The site uses these colors (defined in `assets/css/style.css`):

- **Primary Red:** #c41e3a (CCB red)
- **Primary Navy:** #003366 (CCB navy)
- **Accent Gold:** #d4af37 (for highlights)
- **Light Gray:** #f4f4f4 (backgrounds)
- **Dark Gray:** #333 (text)
- **White:** #ffffff

To change site colors, edit the `:root` section at the top of `style.css`

---

## Fonts

The site uses:
- **Headings:** Merriweather (serif, bold)
- **Body text:** Open Sans (sans-serif)

These are loaded from Google Fonts and don't need to be downloaded.

---

## Making the Site Live / Changing Domain

**Current setup:**
- Domain: classiccityband.org
- Hosting: GitHub Pages (free)
- Domain registrar: Bluehost

**If you need to change domain settings:**

1. In GitHub: Repository Settings → Pages → Custom domain
2. At domain registrar: Update DNS A records to point to GitHub Pages
3. GitHub Pages IP addresses:
   - 185.199.108.153
   - 185.199.109.153
   - 185.199.110.153
   - 185.199.111.153

**Annual cost:** $15/year for domain only (hosting is free!)

---

## Common Problems and Solutions

### Problem: Changes aren't showing up

**Solution:**
1. Wait 2-3 minutes after committing (GitHub needs time to rebuild)
2. Hard refresh your browser: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
3. Try viewing in incognito/private mode
4. Check that your commit actually saved (look for green checkmark on GitHub)

### Problem: Site looks broken

**Solution:**
1. Check what you changed in the last commit
2. Look for missing closing tags (every `<div>` needs `</div>`, etc.)
3. Revert to previous version (see below)

### Problem: I need to undo a change

**Solution:**
1. Go to the file on GitHub
2. Click "History" (top right)
3. Find the version before your change
4. Click "..." → "View file"
5. Copy the old content
6. Go back to current file, click edit, paste old content
7. Commit with message "Reverted to previous version"

### Problem: Image isn't showing

**Solution:**
1. Check filename matches exactly (case-sensitive!)
2. Verify file uploaded to `assets/images/` folder
3. Check path in code: `/CCBwebsite/assets/images/filename.jpg`
4. Make sure image is JPG or PNG format

### Problem: Calendar not updating

**Solution:**
- Calendars update automatically from Google
- If events aren't showing, check Google Calendar settings
- Calendar must be set to "Public" in Google Calendar settings

---

## Emergency Contacts

**For website help:**
- GitHub username of original developer: webmasterCCB
- Contact: [Add current webmaster email here]

**For domain/DNS issues:**
- Domain registrar: Bluehost
- Account access: [Add account info location]

**For emergency site restoration:**
- All previous versions are saved in GitHub history
- Contact someone with GitHub experience to help revert changes
- Website backup: Entire site is backed up automatically by GitHub

---

## File Structure Reference

```
CCBwebsite/
├── _includes/
│   ├── header.html          (Navigation menu)
│   └── footer.html          (Footer content)
├── _layouts/
│   ├── default.html         (Main page template)
│   └── page.html           (Content page template)
├── assets/
│   ├── css/
│   │   └── style.css       (All site styling - colors, fonts, layout)
│   ├── images/             (All photos and graphics)
│   └── documents/          (PDFs like Form 1023, Letter 947)
├── polka/
│   └── polka.md            (German Polka Band page)
├── _config.yml             (Site settings - email, title, URLs)
├── index.html              (Homepage)
├── about.md                (About page)
├── concerts.md             (Performances/calendar page)
├── join.md                 (Join Us page)
├── support.md              (Support/donations page)
├── carnegie-hall.md        (Carnegie Hall info)
├── bigband-athens.md       (Big Band Athens page)
├── donate-general.md       (General donations)
├── donate-carnegie.md      (Carnegie Hall donations)
├── members-payment.md      (Members-only payment portal)
└── README.md               (This file!)
```

---

## Pro Tips

1. **Always add clear commit messages** - "Updated spring concert date" is better than "changes"
2. **Preview before committing** when possible
3. **Make one change at a time** - easier to undo if something breaks
4. **Keep image files small** - compress before uploading
5. **Don't delete files you don't understand** - they might be needed
6. **Bookmark frequently used pages** on GitHub for quick access
7. **Ask for help** - the GitHub community is very helpful

---

## Resources

**Learning More:**
- Markdown guide: https://www.markdownguide.org/basic-syntax/
- GitHub basics: https://guides.github.com/
- HTML basics: https://www.w3schools.com/html/

**Image Tools:**
- Free image compression: https://tinypng.com/
- Favicon generator: https://favicon.io/
- Free stock photos: https://unsplash.com/

**Testing:**
- HTML validator: https://validator.w3.org/
- Mobile-friendly test: https://search.google.com/test/mobile-friendly

---

## Version History

- **January 2026:** Site rebuilt on GitHub Pages by David
- **Previous:** WordPress site on Bluehost (retired due to security issues)

---

**Questions?** Contact the current webmaster or consult GitHub's documentation.

**Remember:** You can't permanently break anything - every version is saved and can be restored!
