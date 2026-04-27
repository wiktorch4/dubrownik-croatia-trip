# 🚀 GitHub Deployment Instructions

## Step 1: Create GitHub Repository

1. Go to [GitHub.com](https://github.com) and log in
2. Click the **"+"** icon in the top right → **"New repository"**
3. Fill in:
   - **Repository name**: `split-croatia-trip` (or any name you prefer)
   - **Description**: "Interactive trip planner for Split, Croatia 🇭🇷"
   - **Public** or **Private** (Public needed for free GitHub Pages)
   - **DON'T** initialize with README (we already have one)
4. Click **"Create repository"**

## Step 2: Push Your Code

Copy the commands from GitHub's "…or push an existing repository from the command line" section.

They'll look like this (replace YOUR_USERNAME with your actual GitHub username):

```bash
cd /home/claude/split-croatia-trip
git remote add origin https://github.com/YOUR_USERNAME/split-croatia-trip.git
git branch -M main
git push -u origin main
```

**OR if you're using SSH:**

```bash
cd /home/claude/split-croatia-trip
git remote add origin git@github.com:YOUR_USERNAME/split-croatia-trip.git
git branch -M main
git push -u origin main
```

## Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **"Settings"** tab
3. Scroll down to **"Pages"** in the left sidebar
4. Under **"Source"**, select:
   - Branch: **main**
   - Folder: **/ (root)**
5. Click **"Save"**

## Step 4: Wait & Access Your Site

- GitHub Pages will build your site (takes 1-2 minutes)
- Your site will be live at: `https://YOUR_USERNAME.github.io/split-croatia-trip/`
- You can find the exact URL in the Pages settings

## 🎉 That's It!

Your Split Croatia trip planner is now live on the internet!

### Share with Friends:
Just send them the GitHub Pages URL. They can:
- View the interactive map
- Click locations to open in Google Maps
- Add their own custom places (saved locally)
- Switch between map views

## 📱 Make it a Mobile App (PWA - Optional)

Want it to work like a mobile app? Add these files:

### Create `manifest.json`:
```json
{
  "name": "Split Croatia Trip",
  "short_name": "Split Trip",
  "description": "Interactive trip planner for Split, Croatia",
  "start_url": "/",
  "display": "standalone",
  "background_color": "#0077BE",
  "theme_color": "#0077BE",
  "icons": [
    {
      "src": "icon-192.png",
      "sizes": "192x192",
      "type": "image/png"
    },
    {
      "src": "icon-512.png",
      "sizes": "512x512",
      "type": "image/png"
    }
  ]
}
```

Add to `<head>` in index.html:
```html
<link rel="manifest" href="manifest.json">
<meta name="theme-color" content="#0077BE">
<meta name="apple-mobile-web-app-capable" content="yes">
```

Then commit and push:
```bash
git add .
git commit -m "Add PWA support"
git push
```

Now users can "Add to Home Screen" on mobile! 📱

## 🔄 Future Updates

Whenever you make changes:

```bash
cd /home/claude/split-croatia-trip
git add .
git commit -m "Your update message"
git push
```

GitHub Pages will automatically update your live site!

---

**Need Help?** Check [GitHub Pages documentation](https://docs.github.com/en/pages)
