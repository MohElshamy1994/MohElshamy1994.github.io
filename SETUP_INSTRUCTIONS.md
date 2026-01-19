# Mohamed Elshamy - Hardware Design Portfolio

This is your personal portfolio website built with the al-folio Jekyll theme, customized for showcasing your hardware design and embedded systems expertise.

## ✅ What's Been Configured

### 1. Personal Information
- **Name**: Mohamed Elshamy
- **Email**: elshamy@nmsu.edu
- **GitHub**: MohElshamy1994
- **LinkedIn**: moh-elshamy
- **Google Scholar**: OIW1wDYAAAAJ
- **ResearchGate**: Mohamed-Elshamy-6

### 2. About Page
- Professional summary highlighting 8+ years of hardware design experience
- Research focus on SoC power and thermal modeling
- Technical proficiency overview
- Professional background

### 3. CV Section
Complete CV with:
- Education (PhD, MSc x2, BSc)
- Work Experience (Research Assistant, Senior Hardware Design, etc.)
- Technical Skills (Programming, EDA Tools, MCUs, Protocols)
- Academic Honors
- Certifications
- Relevant Coursework

### 4. Projects Showcase
Created 7 hardware design projects:
1. **Automotive Telematics Device** - Vehicle tracking and diagnostics
2. **Solar MPPT Controller** - High-efficiency solar charge controller
3. **IoT Smart Home Controller** - Multi-protocol home automation
4. **Industrial Data Logger** - Multi-channel data acquisition
5. **Battery Management System** - Intelligent BMS for Li-ion packs
6. **Multi-Layer PCB Laboratory** - PCB fabrication facility management
7. **SoC Power & Thermal Modeling** - PhD research project

### 5. News/Announcements
- PhD program start
- Completion of UAE position
- NMSU Data Mining Contest achievement

## 🚀 Next Steps to Deploy on GitHub

### Step 1: Create GitHub Repository

1. Go to GitHub and create a new repository named: `MohElshamy1994.github.io`
   - **Important**: The repository name MUST be exactly `<your-username>.github.io`
   - Make it **Public**
   - Do NOT initialize with README, .gitignore, or license

### Step 2: Push Your Code

Open PowerShell in your workspace and run:

```powershell
# Initialize git repository
git init

# Add all files
git add .

# Commit the changes
git commit -m "Initial commit: Mohamed Elshamy Hardware Design Portfolio"

# Add your GitHub repository as remote
git remote add origin https://github.com/MohElshamy1994/MohElshamy1994.github.io.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Actions

1. Go to your repository on GitHub
2. Click on **Settings** → **Actions** → **General**
3. Under "Workflow permissions", select **Read and write permissions**
4. Click **Save**

### Step 4: Wait for Deployment

1. Go to the **Actions** tab in your repository
2. Wait for the "Deploy" workflow to complete (~4 minutes)
3. Once complete, you'll see a new `gh-pages` branch

### Step 5: Configure GitHub Pages

1. Go to **Settings** → **Pages**
2. Under "Build and deployment":
   - **Source**: Deploy from a branch
   - **Branch**: Select `gh-pages` (NOT main)
   - **Folder**: / (root)
3. Click **Save**

### Step 6: View Your Site

After ~1 minute, your site will be live at:
**https://MohElshamy1994.github.io**

## 🎨 Customization Tips

### Add Your Profile Picture
1. Replace `assets/img/prof_pic.jpg` with your professional photo
2. Recommended size: 400x400 pixels or larger
3. Format: JPG or PNG

### Add Project Images
- Add images to `assets/img/` folder
- Update the `img:` field in each project's front matter
- Use descriptive names (e.g., `telematics_board.jpg`)

### Update Publications
Edit `_bibliography/papers.bib` to add your publications in BibTeX format.

### Customize Colors
Edit `_sass/_themes.scss` to change the theme color from purple to your preference.

### Add Blog Posts (Optional)
Create new files in `_posts/` folder following the naming convention:
`YYYY-MM-DD-title.md`

## 📝 Important Files

- **`_config.yml`** - Main site configuration
- **`_pages/about.md`** - Your homepage/bio
- **`_data/cv.yml`** - Your CV data
- **`_data/socials.yml`** - Social media links
- **`_projects/*.md`** - Your project descriptions
- **`_bibliography/papers.bib`** - Your publications

## 🔧 Local Testing (Optional)

To test locally before deploying:

### Using Docker (Recommended for Windows)

1. Install [Docker Desktop for Windows](https://www.docker.com/products/docker-desktop)
2. Open PowerShell in your workspace
3. Run:
```powershell
docker compose up
```
4. Open browser to `http://localhost:8080`

### Using WSL (Windows Subsystem for Linux)

Follow the instructions in `INSTALL.md` for WSL setup.

## 📚 Documentation

- **Installation Guide**: See `INSTALL.md`
- **Customization Guide**: See `CUSTOMIZE.md`
- **FAQ**: See `FAQ.md`
- **Original Theme**: [al-folio GitHub](https://github.com/alshedivat/al-folio)

## 🆘 Need Help?

- Check the [al-folio FAQ](FAQ.md)
- Visit the [al-folio discussions](https://github.com/alshedivat/al-folio/discussions)
- Review the [al-folio wiki](https://github.com/alshedivat/al-folio/wiki)

## 📧 Contact

If you need assistance with your portfolio, feel free to reach out:
- Email: elshamy@nmsu.edu
- LinkedIn: [moh-elshamy](https://www.linkedin.com/in/moh-elshamy/)

---

**Good luck with your portfolio! 🎉**

