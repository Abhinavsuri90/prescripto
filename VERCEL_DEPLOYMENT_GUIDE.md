# 🚀 Vercel Deployment Guide - Frontend

## ✅ Build Complete!
The frontend has been successfully built and is ready for deployment.

---

## 📋 Manual Deployment Steps on Vercel

### Step 1: Go to Vercel
1. Open your browser and go to: **https://vercel.com**
2. Click **"Log in"** or **"Sign Up"** if you don't have an account
3. Sign in with GitHub, GitLab, or Bitbucket

### Step 2: Deploy New Project
1. Click on **"Add New..."** button (top right)
2. Select **"Project"**

### Step 3: Two Options for Deployment

#### **Option A: Import from GitHub (Recommended)**
1. If your code is on GitHub:
   - Click **"Import Git Repository"**
   - Select your repository
   - Select the **frontend** folder as root directory
   - Click **"Deploy"**

#### **Option B: Deploy from Local (Quick)**
1. In the terminal, run:
   ```bash
   cd frontend
   vercel login
   ```
2. Follow the login prompts (check your email)
3. Then run:
   ```bash
   vercel --prod
   ```

---

## ⚙️ Environment Variables to Add on Vercel

After importing/deploying, you need to add environment variables:

### Go to Project Settings → Environment Variables

Add this variable:

**Key:** `VITE_BACKEND_URL`  
**Value:** `YOUR_BACKEND_URL_HERE` (we'll deploy backend next)

For now, you can use: `http://localhost:4000` or deploy backend first.

---

## 🎯 Your Frontend Links Will Be:

After deployment, Vercel will give you URLs like:
- **Production**: `https://your-project-name.vercel.app`
- **Preview**: `https://your-project-name-git-main.vercel.app`

---

## 📝 Quick Terminal Deployment (After Login)

If you want to use terminal:

```bash
cd /Users/abhinavsuri/Downloads/prescripto-full-stack/frontend

# Login to Vercel (do this once)
vercel login

# Deploy to production
vercel --prod
```

The CLI will ask you:
1. **Set up and deploy?** → Yes
2. **Which scope?** → Select your account
3. **Link to existing project?** → No (first time)
4. **Project name?** → prescripto-frontend (or your choice)
5. **Directory?** → ./ (just press Enter)
6. **Override settings?** → No

---

## 🔄 After You Get the Frontend URL

1. Copy your frontend URL from Vercel
2. We'll use it when deploying the backend
3. Update backend CORS to allow your frontend URL

---

## 📱 Project Configuration (Already Done)

✅ `vercel.json` is already configured  
✅ Build output is in `dist/` folder  
✅ All dependencies are installed  
✅ Production build is complete

---

## 🚨 Important Notes

1. **Backend URL**: After deployment, update `VITE_BACKEND_URL` in Vercel dashboard
2. **CORS**: Backend needs to allow your Vercel frontend URL
3. **Environment**: The `.env` file is NOT uploaded to Vercel (that's good for security)
4. **Re-deployment**: Any push to GitHub will auto-deploy if connected

---

## 🎉 What Happens After Deployment

1. You'll get a live URL like: `https://prescripto-frontend.vercel.app`
2. Share this link for your submission
3. Users can access your frontend worldwide
4. Next, we'll deploy the backend to Render/Railway

---

**Ready to deploy? Go to https://vercel.com and start! 🚀**
