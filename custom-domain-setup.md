# Setting Up Your Custom Domain with GitHub Pages

This guide provides step-by-step instructions for setting up your custom domain with your GitHub Pages website.

## Quick Setup Checklist

1. ✅ Update the CNAME file with your actual domain name
2. ⬜ Configure DNS settings at your domain registrar
3. ⬜ Configure GitHub repository settings
4. ⬜ Wait for DNS propagation
5. ⬜ Verify your setup

## Step 1: Update the CNAME File

1. Open the `CNAME` file in this repository
2. Replace `example.com` with your actual domain name (e.g., `thecalmbluesea.com`)
3. Save the file

## Step 2: Configure DNS Settings at Your Domain Registrar

Log in to your domain registrar (where you purchased your domain) and add the following DNS records:

### For Apex Domain (thecalmbluesea.com)

Add these A records:

- Type: A
- Name: @ (or leave blank)
- Value: 185.199.108.153
- Value: 185.199.109.153
- Value: 185.199.110.153
- Value: 185.199.111.153
- TTL: 3600 (or default)

### For www Subdomain (<www.thecalmbluesea.com>)

Add this CNAME record:

- Type: CNAME
- Name: www
- Value: yourusername.github.io (replace with your GitHub username)
- TTL: 3600 (or default)

## Step 3: Configure GitHub Repository Settings

1. Go to your repository on GitHub
2. Click "Settings" > "Pages" (in the left sidebar)
3. Under "Custom domain", enter your domain name (e.g., thecalmbluesea.com)
4. Click "Save"
5. Check "Enforce HTTPS" for secure connections (recommended)

## Step 4: Wait for DNS Propagation

DNS changes can take anywhere from a few minutes to 48 hours to propagate. During this time, your domain might not work correctly with GitHub Pages.

## Step 5: Verify Setup

After DNS propagation:

1. Visit your domain in a browser
2. Verify that your website loads correctly
3. Check that the URL remains your custom domain
4. Verify that HTTPS works if you enabled it

## Troubleshooting

If your domain isn't working after 48 hours:

- Verify DNS settings at your registrar
- Check the CNAME file in your repository
- Ensure your GitHub Pages site is publishing from the correct branch
- Look for any error messages in the GitHub Pages section of your repository settings

For more detailed information, refer to the [GitHub Pages documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).