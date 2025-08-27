# Stanz Clips — Static Site for TikTok Developer App

> This repo hosts a minimal public website with Terms & Privacy, suitable for TikTok Developer **URL verification** and **Content Posting API** app requirements.

**URL:** https://vedvart.github.io/stanz-clips/

## Files
- `index.html` — landing page with visible links to Terms & Privacy
- `terms.html` — plain‑English Terms of Service
- `privacy.html` — plain‑English Privacy Policy (no cookies, no analytics, no forms)
- `robots.txt` — minimal
- `.nojekyll` — prevents Jekyll processing (optional)
- `PLACEHOLDER_TIKTOK_VERIFICATION.txt` — replace with the exact file TikTok gives you when verifying a URL property (see below).

> ⚠️ This is not legal advice. These pages are simple, generic templates tailored to your details.

## Publish to GitHub Pages (Project site)
You’ll end up at: **https://vedvart.github.io/stanz-clips/**

### One‑time setup with Git (no GitHub CLI required)
```bash
# 1) Unzip the bundle and cd into it
unzip stanzclips_site_bundle.zip -d stanzclips_site
cd stanzclips_site

# 2) Initialize repo
git init
git add .
git commit -m "Initial site"

# 3) Create remote repo (via browser UI) named stanz-clips under vedvart
#    https://github.com/new  (Owner: vedvart, Repository name: stanz-clips, Public)
#    Then add the remote and push:
git remote add origin https://github.com/vedvart/stanz-clips.git
git branch -M main
git push -u origin main
```

### Enable Pages (GUI)
- Go to **Settings → Pages**  
- **Build and deployment** → Source: **Deploy from a branch**  
- Branch: **main**, Folder: **/** (root) → **Save**  
- Wait a minute; the site will appear at **https://vedvart.github.io/stanz-clips/**

### (Alternative) Using GitHub CLI
```bash
# Requires: https://cli.github.com/  (run 'gh auth login' once)
unzip stanzclips_site_bundle.zip -d stanzclips_site
cd stanzclips_site
git init && git add . && git commit -m "Initial site"
gh repo create vedvart/stanz-clips --public --source=. --remote=origin --push
# Enable Pages from branch root:
gh api -X PUT repos/vedvart/stanz-clips/pages -f source[branch]=main -f source[path]=/
```

## TikTok URL Verification (when prompted in the TikTok console)
1. On your TikTok app page, open **URL properties** → **Verify** → choose **URL prefix** (recommended for GitHub Pages).
2. TikTok will give you **a file name and file contents** (or a path).  
3. Replace `PLACEHOLDER_TIKTOK_VERIFICATION.txt` with *exactly* the file TikTok provides (name and contents), at the repo root.  
4. Commit & push. Verify the file is visible at:  
   `https://vedvart.github.io/stanz-clips/FILENAME_FROM_TIKTOK.txt`  
5. Click **Verify** back in the TikTok console.

## Maintenance
- Update terms/privacy in this repo as needed and push to `main`.
- Email: stanzclips@gmail.com
- Jurisdiction: USA, Pennsylvania
- Owner: Stanz Clips

