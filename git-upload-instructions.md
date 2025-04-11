# Uploading Your Website to GitHub Pages Using Git Command Line

This guide will walk you through the process of uploading your website files to your GitHub Pages repository using Git command line.

## Prerequisites

1. Git installed on your computer
2. A GitHub account
3. A repository named `yourusername.github.io` already created on GitHub

## Step-by-Step Instructions

### Step 1: Clone Your GitHub Repository

First, you need to clone your empty GitHub repository to your local machine:

```bash
# Replace 'yourusername' with your actual GitHub username
git clone https://github.com/yourusername/yourusername.github.io.git
```

This will create a new directory named `yourusername.github.io` on your computer.

### Step 2: Copy Your Website Files

Copy all your website files from the current directory to the cloned repository directory:

```bash
# Navigate to your current website directory if you're not already there
# cd /path/to/your/website

# Copy all files to the cloned repository
# Replace 'yourusername' with your actual GitHub username
cp -R * /path/to/yourusername.github.io/
```

Alternatively, you can manually copy all files from your current directory to the cloned repository directory using your file explorer.

### Step 3: Navigate to the Repository Directory

```bash
# Replace 'yourusername' with your actual GitHub username
cd /path/to/yourusername.github.io
```

### Step 4: Add All Files to Git

```bash
# Add all files to git
git add .
```

### Step 5: Commit Your Changes

```bash
# Commit with a descriptive message
git commit -m "Initial website commit"
```

### Step 6: Push to GitHub

```bash
# Push to the main branch
git push origin main
```

If your default branch is named "master" instead of "main", use:

```bash
git push origin master
```

### Step 7: Verify Your Website

After pushing your files, GitHub Pages will automatically build and deploy your website. This usually takes a few minutes.

Visit `https://yourusername.github.io` in your browser to see your live website.

## Troubleshooting

### Authentication Issues

If you encounter authentication issues, you may need to:

1. Use a personal access token instead of your password
2. Set up SSH keys for GitHub

### Branch Issues

If your repository uses a different default branch:

```bash
# Check which branches exist
git branch -a

# Push to the correct branch
git push origin your-branch-name
```

### Custom Domain

If you're using a custom domain:

1. Make sure your CNAME file is properly set up with your domain
2. Configure your DNS settings as described in custom-domain-setup.md
3. In your GitHub repository settings, add your custom domain in the GitHub Pages section

## Updating Your Website in the Future

To update your website in the future:

1. Navigate to your local repository
2. Make your changes
3. Add, commit, and push:

```bash
git add .
git commit -m "Description of your changes"
git push origin main
```

Your website will automatically update after pushing your changes.