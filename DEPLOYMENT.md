# Deployment Guide - Excellence Graphics Account Management

## 📋 Prerequisites

Before deploying, ensure you have:
- ✅ Git installed on your computer
- ✅ A GitHub account
- ✅ A Netlify account (free tier is sufficient)

## 🚀 Step-by-Step Deployment

### Step 1: Install Dependencies

Since npm is not available on your system, you'll need to install Node.js first:

1. Download Node.js from: https://nodejs.org/
2. Install the LTS (Long Term Support) version
3. Restart your computer
4. Verify installation by opening PowerShell and running:
   ```powershell
   node --version
   npm --version
   ```

### Step 2: Install Project Dependencies

Open PowerShell in your project directory and run:

```powershell
cd "C:\Users\Aysha\Desktop\My Softwares\Ac3"
npm install
```

This will install all required dependencies (React, Vite, etc.)

### Step 3: Test Locally

Run the development server to test the application:

```powershell
npm run dev
```

Open your browser and go to `http://localhost:5173` to see your application running.

### Step 4: Create GitHub Repository

1. **Initialize Git** (if not already done):
   ```powershell
   git init
   git add .
   git commit -m "Initial commit - Excellence Graphics Account Management System"
   ```

2. **Create a new repository on GitHub**:
   - Go to https://github.com
   - Click the "+" icon → "New repository"
   - Name it: `excellence-graphics-account-management`
   - Keep it public or private (your choice)
   - Don't initialize with README (we already have one)
   - Click "Create repository"

3. **Push your code to GitHub**:
   ```powershell
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/excellence-graphics-account-management.git
   git push -u origin main
   ```
   
   Replace `YOUR_USERNAME` with your actual GitHub username.

### Step 5: Deploy to Netlify

#### Option A: Deploy via Netlify Dashboard (Recommended)

1. **Go to Netlify**:
   - Visit https://app.netlify.com
   - Sign up or log in (you can use your GitHub account)

2. **Import your project**:
   - Click "Add new site" → "Import an existing project"
   - Choose "Deploy with GitHub"
   - Authorize Netlify to access your GitHub account
   - Select your `excellence-graphics-account-management` repository

3. **Configure build settings**:
   - **Build command**: `npm run build`
   - **Publish directory**: `dist`
   - **Base directory**: (leave empty)
   
   These settings are automatically detected from `netlify.toml`

4. **Deploy**:
   - Click "Deploy site"
   - Wait 2-3 minutes for the build to complete
   - Your site will be live at a URL like: `https://random-name-12345.netlify.app`

5. **Custom Domain** (Optional):
   - Go to "Site settings" → "Domain management"
   - Click "Add custom domain"
   - Follow instructions to add your own domain

#### Option B: Deploy via Netlify CLI

If you prefer command line:

```powershell
# Install Netlify CLI
npm install -g netlify-cli

# Login to Netlify
netlify login

# Deploy
netlify deploy --prod
```

### Step 6: Verify Deployment

1. Visit your Netlify URL
2. Test all features:
   - ✅ Add a customer
   - ✅ Edit a customer
   - ✅ View customer details
   - ✅ Delete a customer
   - ✅ Filter by payment status
   - ✅ Search customers

## 🔄 Updating Your Deployed Site

Whenever you make changes to your code:

```powershell
# Save your changes
git add .
git commit -m "Description of your changes"
git push

# Netlify will automatically rebuild and deploy!
```

Netlify has **automatic deployments** enabled by default. Every time you push to GitHub, it will rebuild and deploy your site automatically.

## 📱 Features Included

- ✅ Customer CRUD operations (Create, Read, Update, Delete)
- ✅ Payment status tracking (Full/Partial/None)
- ✅ Search functionality
- ✅ Filter by payment status
- ✅ Responsive design (works on mobile, tablet, desktop)
- ✅ Data persistence using localStorage
- ✅ Modern glassmorphic UI
- ✅ Smooth animations

## 🗄️ Data Storage

**Current Setup**: The application uses **localStorage** for data persistence. This means:
- ✅ Data is saved in the browser
- ✅ No backend server needed
- ✅ Works offline
- ⚠️ Data is specific to each browser/device
- ⚠️ Clearing browser data will delete customers

**For Production with Backend** (Future Enhancement):

If you need data to sync across devices, you can integrate:
- **Supabase** (recommended - free tier available)
- **Firebase**
- **MongoDB Atlas**

Let me know if you'd like help setting up a backend!

## 🆘 Troubleshooting

### Build Fails on Netlify

If the build fails, check:
1. All files are committed to Git
2. `package.json` is in the root directory
3. Build command is `npm run build`
4. Publish directory is `dist`

### Site Loads but Looks Broken

1. Clear your browser cache
2. Check the browser console for errors (F12)
3. Verify all CSS files are loaded

### Data Not Saving

1. Check if localStorage is enabled in your browser
2. Ensure you're not in private/incognito mode
3. Check browser console for errors

## 📞 Support

If you encounter any issues:
1. Check the browser console (F12) for error messages
2. Verify all files are properly uploaded to GitHub
3. Check Netlify build logs for deployment errors

---

**Congratulations!** 🎉 Your Excellence Graphics Account Management System is now live!

Share your Netlify URL with your team to start managing customers.
