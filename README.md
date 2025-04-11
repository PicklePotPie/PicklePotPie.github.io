# The Calm Blue Sea - Official Website

This is the official website for the post-rock band "The Calm Blue Sea". The site is designed to be hosted using GitHub Pages.

## Project Structure
- `index.html` - Main landing page
- `css/style.css` - Styling with dark/moody yet peaceful aesthetic
- `images/` - Band photos and other images
- `website-plan.md` - Detailed plan for the website

## Features
- Responsive design that works on desktop, tablet, and mobile devices
- Dark/moody aesthetic with blue accents inspired by the band name
- Social media links to Instagram, Bandcamp, Spotify, Facebook, and Twitter
- Simple, elegant layout focusing on the band's identity

## Deploying to GitHub Pages

### Step 1: Create a GitHub Account
If you don't already have one, create a GitHub account at [github.com](https://github.com).

### Step 2: Create a New Repository
1. Click the "+" icon in the top right corner of GitHub and select "New repository"
2. Name your repository `yourusername.github.io` (replace 'yourusername' with your actual GitHub username)
3. Make the repository public
4. Click "Create repository"

### Step 3: Upload Your Website Files
Option 1: Using Git (Command Line)
```bash
# Clone the repository to your computer
git clone https://github.com/yourusername/yourusername.github.io.git

# Copy all website files into the cloned directory
# Then add, commit, and push the files
git add .
git commit -m "Initial website commit"
git push origin main
```

Option 2: Using GitHub Web Interface
1. Navigate to your new repository on GitHub
2. Click "Add file" > "Upload files"
3. Drag and drop all your website files or use the file selector
4. Add a commit message like "Initial website commit"
5. Click "Commit changes"

### Step 4: Enable GitHub Pages
1. Go to your repository on GitHub
2. Click "Settings" > "Pages" (in the left sidebar)
3. Under "Source", select "main" branch
4. Click "Save"
5. Wait a few minutes for your site to be published

### Step 5: Access Your Website
Your website will be available at `https://yourusername.github.io`

## Setting Up a Custom Domain

If you have your own domain name, you can use it with your GitHub Pages site while keeping your domain visible in the browser URL.

### Step 1: Configure DNS Settings at Your Domain Registrar

#### For Apex Domain (example.com)
Add these A records:
- Type: A
- Name: @ (or leave blank)
- Value: 185.199.108.153
- Value: 185.199.109.153
- Value: 185.199.110.153
- Value: 185.199.111.153
- TTL: 3600 (or default)

#### For www Subdomain (www.example.com)
Add this CNAME record:
- Type: CNAME
- Name: www
- Value: yourusername.github.io (replace with your GitHub username)
- TTL: 3600 (or default)

For best results, set up both the apex domain and www subdomain.

### Step 2: Configure GitHub Repository Settings

1. Go to your repository on GitHub
2. Click "Settings" > "Pages" (in the left sidebar)
3. Under "Custom domain", enter your domain name (e.g., example.com)
4. Click "Save"
5. Check "Enforce HTTPS" for secure connections (recommended)

### Step 3: Add a CNAME File to Your Repository

A CNAME file tells GitHub Pages which domain to use:

1. Create a file named `CNAME` (all uppercase, no file extension) in the root of your repository
2. Add your domain name as the only content (e.g., `example.com`)
3. Save the file

Example CNAME file content:
```
example.com
```

### Step 4: Wait for DNS Propagation

DNS changes can take anywhere from a few minutes to 48 hours to propagate. During this time, your domain might not work correctly with GitHub Pages.

### Step 5: Verify Setup

After DNS propagation:
1. Visit your domain in a browser
2. Verify that your website loads correctly
3. Check that the URL remains your custom domain
4. Verify that HTTPS works if you enabled it

## Customization
- Replace the placeholder in `images/` with your actual band photo
- Update the social media links in `index.html` with your actual profiles
- Modify the band description in `index.html` to match your band's style

## Contact
For any questions or issues with the website, please reach out through our social media channels.