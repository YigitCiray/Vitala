# Vitala Website

One-page flyer website for Vitala - a health mobile application company launching an iOS app.

## GitHub Pages Setup

To host this website on GitHub Pages, follow these steps:

### 1. Create a GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Name your repository (e.g., `vitala-website` or `vitala`)
5. Make sure it's set to **Public** (required for free GitHub Pages)
6. **Do NOT** initialize with README, .gitignore, or license (we already have files)
7. Click "Create repository"

### 2. Initialize Git and Push Your Code

Open your terminal in the project directory and run:

```bash
# Initialize git repository
git init

# Add all files
git add .

# Create initial commit
git commit -m "Initial commit: Vitala website"

# Add your GitHub repository as remote (replace USERNAME and REPO-NAME)
git remote add origin https://github.com/USERNAME/REPO-NAME.git

# Push to GitHub
git branch -M main
git push -u origin main
```

**Replace `USERNAME` with your GitHub username and `REPO-NAME` with your repository name.**

### 3. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on **Settings** (top menu)
3. Scroll down to **Pages** in the left sidebar
4. Under **Source**, select:
   - **Branch**: `main`
   - **Folder**: `/ (root)`
5. Click **Save**

### 4. Access Your Site

Your website will be available at:
```
https://USERNAME.github.io/REPO-NAME
```

**Note:** It may take a few minutes for the site to be available after enabling GitHub Pages.

### 5. Custom Domain (Optional)

If you have a custom domain (e.g., `vitalaco.com`):

1. In the GitHub Pages settings, enter your custom domain
2. Add a `CNAME` file in your repository root with your domain name
3. Configure DNS records with your domain provider:
   - Type: `CNAME`
   - Name: `www` (or `@` for root domain)
   - Value: `USERNAME.github.io`

## File Structure

```
Vitala/
├── index.html          # Main landing page
├── privacy.html        # Privacy policy page
├── terms.html          # Terms of conditions page
├── styles.css          # Main stylesheet
└── README.md          # This file
```

## Local Development

To view the website locally:

1. Simply open `index.html` in your web browser
2. Or use a local server:
   ```bash
   # Python 3
   python -m http.server 8000
   
   # Node.js (with http-server)
   npx http-server
   ```
3. Visit `http://localhost:8000` in your browser

## Updating the Site

After making changes:

```bash
git add .
git commit -m "Description of changes"
git push
```

Changes will be live on GitHub Pages within a few minutes.

