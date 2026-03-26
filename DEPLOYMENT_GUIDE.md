# Farm Fresh Connect - GitHub & Vercel Deployment Guide

## Step 1: Create GitHub Repository

1. Go to [GitHub.com](https://github.com)
2. Click **New Repository**
3. Enter repository name: `farm-fresh-connect`
4. Add description: `Farm Fresh Connect - Agricultural e-commerce platform`
5. Choose **Public** (for Vercel integration)
6. Click **Create repository**
7. **DO NOT** initialize with README (we already have one)

## Step 2: Push Code to GitHub

After creating the repository on GitHub, run these commands:

```bash
cd c:\Users\brand\Downloads\farm-fresh-connect-33d860d7-main\farm-fresh-connect-33d860d7-main

# Set the remote URL (replace YOUR_USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/farm-fresh-connect.git

# Rename branch to main
git branch -M main

# Push to GitHub
git push -u origin main
```

## Step 3: Configure Vercel Deployment

### Option A: Using Vercel CLI (Recommended)

```bash
# Install Vercel CLI globally
npm install -g vercel

# Deploy from project directory
cd c:\Users\brand\Downloads\farm-fresh-connect-33d860d7-main\farm-fresh-connect-33d860d7-main
vercel

# Follow prompts to:
# - Link to GitHub account
# - Select the farm-fresh-connect repository
# - Configure build settings (Vite will be detected)
```

### Option B: Using Vercel Web Dashboard

1. Go to [vercel.com](https://vercel.com)
2. Sign in with GitHub
3. Click **Add New** → **Project**
4. Select `farm-fresh-connect` repository
5. Configure:
   - **Framework**: Vite
   - **Build Command**: `npm run build`
   - **Output Directory**: `dist`
6. Add Environment Variables:
   ```
   VITE_PAYPAL_CLIENT_ID=<your_paypal_client_id>
   VITE_YOCO_SECRET_KEY=<your_yoco_secret_key>
   VITE_SUPABASE_URL=<your_supabase_url>
   VITE_SUPABASE_ANON_KEY=<your_supabase_anon_key>
   ```
7. Click **Deploy**

## Current Git Status

✅ Repository initialized  
✅ Files staged and committed  
✅ Ready for GitHub push  

## Next Steps

1. Create repository on GitHub (if not done)
2. Run git commands above to push
3. Deploy to Vercel
4. Your app will be live at: `farm-fresh-connect.vercel.app`

