# Google Drive Sync Setup Guide

Your habit tracker now has **auto-sync with Google Drive**! Follow these steps to enable it.

---

## 🎯 What You'll Get

✅ **Auto-save** — Every change syncs to Google Drive automatically  
✅ **Cross-device** — Access your data on phone, laptop, tablet  
✅ **Cloud backup** — Never lose your data  
✅ **Privacy** — Only YOU can access your data  

---

## 📋 Setup Steps (Takes 5 minutes)

### Step 1: Create a Google Cloud Project

1. Go to: https://console.cloud.google.com/
2. Click **"Select a project"** → **"New Project"**
3. Name it: `Loggd Habit Tracker`
4. Click **"Create"**

### Step 2: Enable Google Drive API

1. In your new project, go to: **APIs & Services → Library**
2. Search for: `Google Drive API`
3. Click on it → Click **"Enable"**

### Step 3: Create OAuth Credentials

1. Go to: **APIs & Services → Credentials**
2. Click **"Create Credentials"** → **"OAuth client ID"**
3. If prompted, configure consent screen:
   - User Type: **External**
   - App name: `Loggd`
   - User support email: your email
   - Scopes: Skip (click Save and Continue)
   - Test users: Add your email
   - Click **"Save and Continue"** until done
4. Back to **Create OAuth client ID**:
   - Application type: **Web application**
   - Name: `Loggd Web`
   - **Authorized JavaScript origins**: Add these:
     ```
     https://your-username.github.io
     http://localhost:8000
     http://127.0.0.1:8000
     ```
     (Replace `your-username` with your actual GitHub username)
   - Click **"Create"**
5. Copy your **Client ID** (looks like: `123456789-abcdef.apps.googleusercontent.com`)

### Step 4: Create API Key

1. Still in **Credentials**, click **"Create Credentials"** → **"API Key"**
2. Click **"Restrict Key"** (recommended):
   - Application restrictions: **HTTP referrers**
   - Website restrictions: Add `https://your-username.github.io/*`
   - API restrictions: Select **Google Drive API**
3. Click **"Save"**
4. Copy your **API Key**

### Step 5: Add Credentials to Your App

1. Open `index.html` in a text editor
2. Find this section (around line 1200):
   ```javascript
   const DRIVE_CONFIG = {
     CLIENT_ID: 'YOUR_GOOGLE_CLIENT_ID_HERE.apps.googleusercontent.com',
     API_KEY: 'YOUR_API_KEY_HERE',
   ```
3. Replace:
   - `YOUR_GOOGLE_CLIENT_ID_HERE` with your Client ID
   - `YOUR_API_KEY_HERE` with your API Key
4. Save the file

### Step 6: Deploy to GitHub Pages

1. Go to your GitHub repository
2. Upload the modified `index.html`
3. Wait 1 minute for GitHub Pages to update
4. Visit your site: `https://your-username.github.io/your-repo/`

### Step 7: Connect Google Drive

1. Open your deployed app
2. You'll see a banner: **"Sync across all your devices!"**
3. Click **"Connect Google Drive"**
4. Sign in with your Google account
5. Click **"Allow"** when prompted
6. Done! ✨

---

## 🔄 How It Works

- **Auto-save**: Every time you complete a habit, check a task, or make any change → auto-saves to Google Drive after 2 seconds
- **Auto-load**: When you open the app on a new device → automatically loads your data from Google Drive
- **Always in sync**: Background sync every 30 seconds keeps all devices updated

---

## 📱 Using on Multiple Devices

### On your phone:
1. Open Safari/Chrome
2. Go to: `https://your-username.github.io/your-repo/`
3. Click **"Connect Google Drive"**
4. Sign in
5. All your data appears!

### On your laptop:
1. Same URL
2. Same Google account
3. Same data ✓

---

## 🔧 Troubleshooting

### "Auth failed" error
- Make sure you added your site URL to **Authorized JavaScript origins** in Google Cloud Console
- Try clearing browser cache and reconnecting

### "Sync failed" error
- Check that Google Drive API is enabled
- Make sure your API Key restrictions allow your website

### Data not syncing
- Check the sync status indicator (top-right corner)
- Click "Settings" → "Force sync now"
- Check your internet connection

### Starting fresh
Want to disconnect and start over?
1. Click the sync status indicator → "Settings"
2. Click "Disconnect Google Drive"
3. Your local data stays safe
4. Reconnect whenever you want

---

## 🔒 Privacy & Security

- Your data is stored in YOUR Google Drive (not on any third-party server)
- Only YOU can access it (not even the app developer can see it)
- All communication is encrypted (HTTPS)
- You can disconnect anytime

---

## 💡 Pro Tips

1. **Bookmark the app** on your phone's home screen (like a native app!)
2. **Check sync status** — Green dot = all good ✅
3. **Manual export** — Still export your data weekly as extra backup (see README.md)

---

## 📞 Need Help?

If you get stuck:
1. Check the JavaScript console for error messages (F12 → Console)
2. Double-check your Client ID and API Key are correct
3. Make sure your GitHub Pages URL matches what you put in Google Cloud Console

---

## 🎉 You're All Set!

Once connected, your habit tracker will:
- ✅ Sync automatically across all devices
- ✅ Back up to Google Drive every 30 seconds  
- ✅ Never lose your data again

Enjoy tracking your life! 🚀
