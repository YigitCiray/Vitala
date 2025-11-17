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

### 5. Custom Domain Setup (www.vitalaco.com and vitalaco.com)

The `CNAME` file has been created with `www.vitalaco.com`. To complete the setup:

1. **Push the CNAME file to GitHub** (it's already in the repository)

2. **In GitHub Pages Settings:**
   - Go to Settings → Pages
   - Under "Custom domain", enter: `www.vitalaco.com`
   - Check "Enforce HTTPS" (will be available after DNS is configured)
   - Click Save
   - **Note**: GitHub will automatically detect and configure the root domain (vitalaco.com) once DNS is set up correctly

3. **Configure DNS with your domain provider** (where you bought vitalaco.com):
   
   **For www.vitalaco.com - Add a CNAME record:**
   - **Type**: `CNAME`
   - **Name/Host**: `www`
   - **Value/Target**: `yigitalpciray.github.io` (or `yigitalpciray.github.io.` if your provider requires trailing dot)
   - **TTL**: 3600 (or default)
   
   **For root domain (vitalaco.com) - Add FOUR A records:**
   You need to create 4 separate A records, each with one of these IP addresses:
   
   **A Record 1:**
   - **Type**: `A`
   - **Name/Host**: `@` (or leave blank, or `vitalaco.com`)
   - **Value**: `185.199.108.153`
   - **TTL**: 3600
   
   **A Record 2:**
   - **Type**: `A`
   - **Name/Host**: `@` (or leave blank, or `vitalaco.com`)
   - **Value**: `185.199.109.153`
   - **TTL**: 3600
   
   **A Record 3:**
   - **Type**: `A`
   - **Name/Host**: `@` (or leave blank, or `vitalaco.com`)
   - **Value**: `185.199.110.153`
   - **TTL**: 3600
   
   **A Record 4:**
   - **Type**: `A`
   - **Name/Host**: `@` (or leave blank, or `vitalaco.com`)
   - **Value**: `185.199.111.153`
   - **TTL**: 3600
   
   **Important**: 
   - The root domain (vitalaco.com) MUST use A records (not CNAME)
   - You need all 4 A records for redundancy
   - Some DNS providers allow you to add multiple IPs in one record, others require separate records

4. **Wait for DNS propagation** (can take a few minutes to 48 hours)

5. **Verify**: Once DNS propagates, GitHub will show a green checkmark next to your custom domain in Pages settings

Your site will be accessible at:
- `https://www.vitalaco.com`
- `https://yigitalpciray.github.io/Vitala` (still works as backup)

## File Structure

```
Vitala/
├── index.html          # Main landing page
├── privacy.html        # Privacy policy page
├── terms.html          # Terms of conditions page
├── styles.css          # Main stylesheet
├── CNAME              # Custom domain configuration
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

