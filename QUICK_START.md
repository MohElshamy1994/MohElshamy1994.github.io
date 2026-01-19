# Quick Start Guide - Deploy in 5 Minutes! ⚡

## Prerequisites
- GitHub account (you already have: MohElshamy1994)
- Git installed on your computer

## Step-by-Step Deployment

### 1️⃣ Create GitHub Repository (2 minutes)

1. Go to: https://github.com/new
2. Repository name: **MohElshamy1994.github.io** (EXACTLY this name!)
3. Make it **Public**
4. **DO NOT** check any boxes (no README, no .gitignore, no license)
5. Click **Create repository**

### 2️⃣ Push Your Code (1 minute)

Open PowerShell in this folder and run these commands:

```powershell
# Remove the existing remote (from the template)
git remote remove origin

# Add YOUR GitHub repository
git remote add origin https://github.com/MohElshamy1994/MohElshamy1994.github.io.git

# Stage all your customizations
git add .

# Commit your changes
git commit -m "Customize portfolio for Mohamed Elshamy"

# Push to GitHub
git push -u origin main
```

### 3️⃣ Enable GitHub Actions (30 seconds)

1. Go to: https://github.com/MohElshamy1994/MohElshamy1994.github.io/settings/actions
2. Scroll to **Workflow permissions**
3. Select **Read and write permissions**
4. Click **Save**

### 4️⃣ Wait for Build (4 minutes)

1. Go to: https://github.com/MohElshamy1994/MohElshamy1994.github.io/actions
2. Watch the "Deploy" action run (takes ~4 minutes)
3. Wait until it shows a green checkmark ✅

### 5️⃣ Configure GitHub Pages (30 seconds)

1. Go to: https://github.com/MohElshamy1994/MohElshamy1994.github.io/settings/pages
2. Under **Source**: Select "Deploy from a branch"
3. Under **Branch**: Select **gh-pages** (NOT main!)
4. Click **Save**

### 6️⃣ Visit Your Site! (1 minute)

Wait ~1 minute, then visit:
**https://MohElshamy1994.github.io**

🎉 **Your portfolio is now live!**

---

## ⚠️ Troubleshooting

### "Deploy" action failed?
- Check that you enabled "Read and write permissions" in Step 3
- Re-run the action from the Actions tab

### Site shows 404?
- Make sure you selected **gh-pages** branch (not main)
- Wait a few more minutes for GitHub Pages to deploy

### Site shows default content?
- Make sure you committed and pushed your changes in Step 2
- Check that the files were actually modified (run `git status`)

---

## 🎨 Before You Deploy (Optional but Recommended)

### Add Your Photo
Replace `assets/img/prof_pic.jpg` with your professional headshot.

### Add Project Images
Add images to `assets/img/` and update project files:
- `_projects/1_project.md` → change `img: assets/img/your-image.jpg`
- Repeat for all projects

---

## 📱 After Deployment

### Share Your Portfolio
- Add to your LinkedIn profile
- Include in your email signature
- Share on your CV/resume
- Add to your GitHub profile README

### Keep It Updated
- Add new projects as you complete them
- Update your CV regularly
- Add blog posts about your work
- Keep publications current

---

**Need detailed instructions?** See `SETUP_INSTRUCTIONS.md`

**Questions?** Check `CUSTOMIZATION_SUMMARY.md` for what's been configured.

