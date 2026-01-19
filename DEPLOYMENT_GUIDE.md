# Deployment Guide - Replace ML Portfolio with Hardware Portfolio

## ⚠️ Important Note

Since you already have a repository named `MohElshamy1994.github.io` (your ML portfolio), you have two options:

### Option 1: Replace the Existing Repository (Recommended)

This will completely replace your ML portfolio with this hardware portfolio.

#### Steps:

1. **Add your existing repository as remote:**
```powershell
git remote add origin https://github.com/MohElshamy1994/MohElshamy1994.github.io.git
```

2. **Force push to replace the content:**
```powershell
git push -f origin main
```

⚠️ **Warning**: This will permanently delete your ML portfolio content from that repository!

3. **Enable GitHub Actions** (if not already enabled):
   - Go to: https://github.com/MohElshamy1994/MohElshamy1994.github.io/settings/actions
   - Under "Workflow permissions", select **"Read and write permissions"**
   - Click **Save**

4. **Wait for deployment** (~4 minutes):
   - Go to: https://github.com/MohElshamy1994/MohElshamy1994.github.io/actions
   - Wait for the "Deploy" action to complete ✅

5. **Configure GitHub Pages** (if needed):
   - Go to: https://github.com/MohElshamy1994/MohElshamy1994.github.io/settings/pages
   - Ensure **Source** is "Deploy from a branch"
   - Ensure **Branch** is set to **`gh-pages`** (NOT main)
   - Click **Save**

6. **Visit your site**:
   - https://MohElshamy1994.github.io

---

### Option 2: Backup ML Portfolio First

If you want to keep your ML portfolio:

1. **Rename your existing repository on GitHub:**
   - Go to: https://github.com/MohElshamy1994/MohElshamy1994.github.io/settings
   - Scroll to "Repository name"
   - Rename it to something like: `ml-portfolio` or `machine-learning-portfolio`
   - Click **Rename**

2. **Then follow Option 1 steps** to create the new hardware portfolio

---

## 🎯 Recommended Approach

Since you mentioned you want to "focus only on Hardware", I recommend **Option 1** - replacing the ML portfolio entirely with this hardware portfolio.

## 📋 Quick Command Reference

```powershell
# Navigate to your workspace
cd "F:\OneDrive - New Mexico State University\my CV\HardwareCV2026"

# Add remote (if not already added)
git remote add origin https://github.com/MohElshamy1994/MohElshamy1994.github.io.git

# Force push to replace content
git push -f origin main
```

## ✅ After Deployment

1. Wait ~5 minutes for full deployment
2. Visit: https://MohElshamy1994.github.io
3. Your hardware portfolio will be live!

## 🆘 Troubleshooting

### "Remote origin already exists"
```powershell
git remote remove origin
git remote add origin https://github.com/MohElshamy1994/MohElshamy1994.github.io.git
```

### "Failed to push"
Make sure you have the correct permissions. You may need to authenticate with GitHub.

### Site shows old ML content
- Clear your browser cache
- Wait a few more minutes
- Check that the GitHub Action completed successfully

---

**Ready to deploy?** Let me know and I'll help you with the commands!

