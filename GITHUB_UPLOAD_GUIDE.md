# How to Upload Files to GitHub - Step by Step Guide

## 📋 Prerequisites

Before starting, you need:
1. ✅ A GitHub account (create one at https://github.com if you don't have one)
2. ✅ Git installed on your computer

## 🔧 Step 1: Install Git (If Not Already Installed)

1. Download Git from: https://git-scm.com/download/win
2. Run the installer
3. Use default settings (just keep clicking "Next")
4. Restart your computer after installation

### Verify Git is Installed:
Open PowerShell and type:
```powershell
git --version
```
You should see something like: `git version 2.x.x`

## 🌐 Step 2: Create a GitHub Repository

1. Go to https://github.com
2. Log in to your account
3. Click the **"+"** icon in the top-right corner
4. Select **"New repository"**
5. Fill in the details:
   - **Repository name**: `excellence-graphics-account-management`
   - **Description**: `Customer account management system for Excellence Graphics`
   - **Visibility**: Choose "Public" or "Private"
   - **DO NOT** check "Initialize this repository with a README" (we already have files)
6. Click **"Create repository"**

## 💻 Step 3: Upload Files Using PowerShell

### Method A: Using Git Commands (Recommended)

1. **Open PowerShell** in your project folder:
   - Navigate to: `C:\Users\Aysha\Desktop\My Softwares\Ac3`
   - Hold `Shift` + Right-click in the folder
   - Select "Open PowerShell window here"

2. **Initialize Git** (first time only):
   ```powershell
   git init
   ```

3. **Configure Git** (first time only - use your GitHub email and name):
   ```powershell
   git config --global user.email "your-email@example.com"
   git config --global user.name "Your Name"
   ```

4. **Add all files**:
   ```powershell
   git add .
   ```

5. **Commit the files**:
   ```powershell
   git commit -m "Initial commit - Excellence Graphics Account Management System"
   ```

6. **Connect to GitHub** (replace YOUR_USERNAME with your GitHub username):
   ```powershell
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/excellence-graphics-account-management.git
   ```

7. **Push to GitHub**:
   ```powershell
   git push -u origin main
   ```

8. **Enter credentials** when prompted:
   - Username: Your GitHub username
   - Password: Use a **Personal Access Token** (not your password)

### How to Create a Personal Access Token:

1. Go to GitHub.com → Click your profile picture → **Settings**
2. Scroll down to **Developer settings** (bottom left)
3. Click **Personal access tokens** → **Tokens (classic)**
4. Click **Generate new token** → **Generate new token (classic)**
5. Give it a name: "Excellence Graphics Upload"
6. Check the **"repo"** checkbox
7. Click **Generate token**
8. **COPY THE TOKEN** (you won't see it again!)
9. Use this token as your password when pushing to GitHub

---

### Method B: Using GitHub Desktop (Easier for Beginners)

1. **Download GitHub Desktop**: https://desktop.github.com/
2. Install and sign in with your GitHub account
3. Click **"Add"** → **"Add existing repository"**
4. Browse to: `C:\Users\Aysha\Desktop\My Softwares\Ac3`
5. Click **"Add repository"**
6. Click **"Publish repository"**
7. Choose name and visibility
8. Click **"Publish repository"**
9. Done! ✅

---

### Method C: Upload via GitHub Website (Simplest but Limited)

1. Go to your new repository on GitHub
2. Click **"uploading an existing file"** link
3. Drag and drop all your files
4. Add commit message: "Initial commit"
5. Click **"Commit changes"**

⚠️ **Note**: This method has file size limits and is slower for many files.

## ✅ Step 4: Verify Upload

1. Go to your GitHub repository URL
2. You should see all your files listed
3. Check that `standalone.html`, `README.md`, and other files are there

## 🚀 Step 5: Deploy to Netlify (Optional)

Now that your files are on GitHub, you can deploy to Netlify:

1. Go to https://netlify.com
2. Sign up/Login (you can use your GitHub account)
3. Click **"Add new site"** → **"Import an existing project"**
4. Click **"Deploy with GitHub"**
5. Authorize Netlify to access your GitHub
6. Select your repository: `excellence-graphics-account-management`
7. **Build settings**:
   - **Build command**: Leave empty (or use `npm run build` if using the React version)
   - **Publish directory**: Leave empty (or use `dist` if using React version)
   - **Base directory**: Leave empty
8. Click **"Deploy site"**
9. Wait 2-3 minutes
10. Your site is live! 🎉

### For Standalone Version on Netlify:

If you want to deploy just the `standalone.html`:
1. Rename `standalone.html` to `index.html` in your repository
2. Follow the Netlify steps above
3. Your site will be live immediately!

## 🔄 Updating Your Files Later

When you make changes to your files:

```powershell
# Navigate to your project folder
cd "C:\Users\Aysha\Desktop\My Softwares\Ac3"

# Add changed files
git add .

# Commit with a message
git commit -m "Description of what you changed"

# Push to GitHub
git push
```

If you're using GitHub Desktop:
1. Open GitHub Desktop
2. You'll see your changes listed
3. Add a commit message
4. Click **"Commit to main"**
5. Click **"Push origin"**

## 🆘 Troubleshooting

### "Git is not recognized"
- Git is not installed or not in PATH
- Install Git from https://git-scm.com/download/win
- Restart PowerShell after installation

### "Permission denied"
- You're using your password instead of a Personal Access Token
- Create a token following the steps above
- Use the token as your password

### "Repository not found"
- Check the repository URL is correct
- Make sure you replaced YOUR_USERNAME with your actual username
- Verify the repository exists on GitHub

### "Failed to push"
- Check your internet connection
- Verify you have permission to push to the repository
- Try: `git pull origin main` first, then `git push`

## 📝 Quick Reference

```powershell
# First time setup
git init
git config --global user.email "your-email@example.com"
git config --global user.name "Your Name"
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git
git push -u origin main

# Updating later
git add .
git commit -m "Your message"
git push
```

## 🎯 Recommended Approach

**For beginners**: Use **GitHub Desktop** (Method B) - it's the easiest!

**For developers**: Use **Git commands** (Method A) - more powerful and flexible

**For quick uploads**: Use **GitHub website** (Method C) - but limited functionality

---

**Need help?** Feel free to ask if you encounter any issues! 🚀
