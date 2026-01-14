# 5-Day Launch Plan for Classic City Band Website

## Day 1: Upload & Go Live

### Step 1: Make Repository Public (REQUIRED for free GitHub Pages)
1. Go to https://github.com/webmasterCCB/CCBwebsite
2. Click **Settings**
3. Scroll to bottom to "Danger Zone"
4. Click **Change visibility**
5. Select **Make public**
6. Type the repository name to confirm
7. Click **I understand, change repository visibility**

### Step 2: Upload All Files
1. Still in your repo, click **Add file** → **Upload files**
2. Drag ALL files from the `ccb-website` folder
3. OR use "choose your files" to select all
4. Write commit message: "Initial site upload"
5. Click **Commit changes**

### Step 3: Enable GitHub Pages
1. Go to **Settings** → **Pages** (left sidebar)
2. Under **Source**:
   - Branch: select **main**
   - Folder: select **/ (root)**
3. Click **Save**
4. Wait 2-5 minutes
5. Refresh page - you'll see: "Your site is published at https://webmasterccb.github.io/CCBwebsite/"

### Step 4: Test Your Site
Click the URL from GitHub Pages settings - your site is now LIVE!

**✅ At this point, you have a working website!**

---

## Day 2: Essential Content Updates

### Priority Updates (via GitHub web interface):

1. **Edit _config.yml**
   - Click the file → Edit (pencil icon)
   - Update email address
   - Update social media URLs
   - Commit changes

2. **Edit carnegie-hall.md**
   - Add your real donation buttons (PayPal, etc.)
   - Update mailing address
   - Commit changes

3. **Edit about.md**
   - Add band history
   - Add conductor bio
   - Commit changes

4. **Edit join.md**
   - Add rehearsal day, time, location
   - Add membership fee info
   - Add contact phone
   - Commit changes

---

## Day 3: Google Calendar Integration

### Create Google Calendar
1. Go to calendar.google.com
2. Create a calendar called "CCB Concerts" (or use existing)
3. Add your upcoming concerts/events

### Get Embed Code
1. Click the three dots next to calendar name
2. Select **Settings and sharing**
3. Scroll to **Integrate calendar**
4. Click **Customize** next to embed code
5. Adjust settings (colors, size, etc.)
6. Copy the embed code

### Add to Website
1. Edit `concerts.md` on GitHub
2. Find the comment `<!-- REPLACE THIS WITH YOUR GOOGLE CALENDAR EMBED -->`
3. Delete the placeholder paragraph
4. Paste your embed code
5. Commit changes

6. Repeat for `index.html` (two calendar sections to replace)

---

## Day 4: Payment Integration & Photos

### Set Up Donations

**Option A - PayPal (Fastest)**
1. Go to paypal.com/donate
2. Create donation button for Carnegie Hall fund
3. Copy the button HTML code
4. Edit `carnegie-hall.md` on GitHub
5. Replace the placeholder donation buttons with real code
6. Commit changes

**Option B - Stripe Payment Links**
1. Create Stripe account
2. Create a Payment Link for Carnegie Hall donations
3. Copy the link
4. Edit `carnegie-hall.md`
5. Replace button href with your Stripe link
6. Commit changes

### Add Photos
1. Choose 3-5 good band photos
2. Go to repo → `assets/images/`
3. Click **Add file** → **Upload files**
4. Upload your photos (name them clearly: hero.jpg, concert1.jpg, etc.)
5. Edit pages to reference your images:
   - `index.html` - update image src paths
   - `carnegie-hall.md` - add real Carnegie Hall image if you have one

---

## Day 5: Final Polish & Domain Setup

### Point Your Domain to GitHub Pages

**In Your Domain Registrar (Bluehost, etc.):**

1. Log into your domain management
2. Find DNS settings for classiccityband.org
3. Add these DNS records:

**A Records** (for root domain):
```
Type: A
Host: @
Points to: 185.199.108.153

Type: A  
Host: @
Points to: 185.199.109.153

Type: A
Host: @
Points to: 185.199.110.153

Type: A
Host: @  
Points to: 185.199.111.153
```

**CNAME Record** (for www):
```
Type: CNAME
Host: www
Points to: webmasterccb.github.io
```

4. Save DNS changes
5. **Wait 24-48 hours for DNS to propagate**

**In GitHub:**
1. Go to Settings → Pages
2. Under "Custom domain" enter: `classiccityband.org`
3. Click **Save**
4. Wait 24 hours, then check **Enforce HTTPS**

### Final Content Check
- [ ] All placeholder text replaced
- [ ] Social media links work
- [ ] Donation buttons work
- [ ] Calendar displays correctly
- [ ] All page links work
- [ ] Mobile view looks good (test on phone)
- [ ] Contact information is correct

---

## Post-Launch Maintenance

### Update Carnegie Hall Progress
Every week, update the fundraising thermometer:

1. Edit `carnegie-hall.md`
2. Change progress bar width and amount:
```html
<div class="progress-bar" style="width: 25%;">
  $12,500 raised of $50,000
</div>
```
3. Commit changes

### Share on Social Media
- Announce new website on Facebook, Instagram
- Post direct link to Carnegie Hall campaign
- Tag local Athens businesses and groups

### Track Donations
- Check PayPal/Stripe regularly
- Thank donors promptly
- Update progress bar weekly

---

## Quick Reference

### Common File Locations
- Homepage: `index.html`
- Carnegie Hall page: `carnegie-hall.md`
- About page: `about.md`
- Concert calendar: `concerts.md`
- Join page: `join.md`
- Support page: `support.md`
- Site settings: `_config.yml`
- Styles: `assets/css/style.css`
- Logo/images: `assets/images/`

### How to Edit Any File
1. Go to file in GitHub repo
2. Click pencil icon (Edit)
3. Make changes
4. Scroll down
5. Add commit message
6. Click "Commit changes"
7. Wait 1-2 minutes
8. Refresh website

### Emergency Contact
If something breaks:
1. Check recent commits in GitHub
2. Click on commit to see what changed
3. Edit the file to fix
4. Or: revert the commit

---

## Success Metrics

Track these over the next 5 months:
- Website visitors (use Google Analytics - free)
- Carnegie Hall donations
- Social media engagement
- New member inquiries
- Concert attendance

---

## You've Got This!

Remember:
- ✅ Simple is better than perfect
- ✅ Launch now, polish later
- ✅ The Carnegie Hall deadline is what matters
- ✅ You can update anytime via GitHub

Questions? Refer back to the README.md file for more details.

**Now go make this happen! 🎺**
