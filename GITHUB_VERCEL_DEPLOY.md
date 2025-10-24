# 🚀 Quick Deploy to Vercel via GitHub

## Fastest Method: Push to GitHub → Deploy on Vercel

### Step 1: Initialize Git (if not already done)
```bash
cd /Users/abhinavsuri/Downloads/prescripto-full-stack
git init
git add .
git commit -m "Initial commit - Prescripto Full Stack"
```

### Step 2: Create GitHub Repository
1. Go to **https://github.com/new**
2. Repository name: `prescripto-full-stack`
3. Keep it **Public** or **Private**
4. Don't initialize with README (we already have files)
5. Click **"Create repository"**

### Step 3: Push to GitHub
```bash
# Replace YOUR_USERNAME with your GitHub username
git remote add origin https://github.com/YOUR_USERNAME/prescripto-full-stack.git
git branch -M main
git push -u origin main
```

---

## 🌐 Deploy on Vercel

### Step 4: Import on Vercel
1. Go to **https://vercel.com**
2. Click **"Add New"** → **"Project"**
3. Click **"Import Git Repository"**
4. Select your `prescripto-full-stack` repository
5. You'll need to deploy **3 separate projects**:

---

## 📁 Deploy Each Part

### 1️⃣ Deploy Frontend
- **Project Name**: `prescripto-frontend`
- **Framework Preset**: Vite
- **Root Directory**: `frontend`
- **Build Command**: `npm run build`
- **Output Directory**: `dist`
- **Environment Variables**:
  ```
  VITE_BACKEND_URL = (we'll add this after backend is deployed)
  ```

### 2️⃣ Deploy Backend (Next)
- **Project Name**: `prescripto-backend`
- **Framework Preset**: Other
- **Root Directory**: `backend`
- **Build Command**: (leave empty)
- **Environment Variables**: (all your .env variables)

### 3️⃣ Deploy Admin (Next)
- **Project Name**: `prescripto-admin`
- **Framework Preset**: Vite
- **Root Directory**: `admin`
- **Build Command**: `npm run build`
- **Output Directory**: `dist`

---

## ⚡ Alternative: Just Deploy Frontend First

If you want to deploy frontend only right now:

1. **Go to Vercel.com** → New Project
2. **Import your GitHub repo**
3. **Configure:**
   - Root Directory: `frontend`
   - Framework: Vite
   - Build: `npm run build`
   - Output: `dist`
4. **Add Environment Variable:**
   - `VITE_BACKEND_URL` = `http://localhost:4000` (temporary)
5. **Click Deploy**

---

## 📋 Your Links After Deployment

- **Frontend**: `https://prescripto-frontend.vercel.app`
- **Backend**: (deploy on Render/Railway - I'll help next)
- **Admin**: `https://prescripto-admin.vercel.app`

---

## 🔥 Super Quick Option: Use Vercel CLI

If you're already logged in to Vercel in browser, you can also:

```bash
cd frontend
npx vercel --prod
```

Follow the prompts, and you'll get a link instantly!

---

**Which method do you prefer? Let me know and I'll help you proceed! 🚀**
