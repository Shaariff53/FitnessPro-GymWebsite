# Deployment Guidelines

Complete guide for deploying FitnessPro to production.

## 📋 Table of Contents

1. [Pre-Deployment Checklist](#pre-deployment-checklist)
2. [Deployment Options](#deployment-options)
3. [Hosting Providers](#hosting-providers)
4. [Domain Configuration](#domain-configuration)
5. [SSL/HTTPS Setup](#ssltls-setup)
6. [Performance Optimization](#performance-optimization)
7. [Monitoring and Maintenance](#monitoring-and-maintenance)
8. [Troubleshooting](#troubleshooting)

## Pre-Deployment Checklist

Before deploying, ensure:

### Code Quality
- [ ] All code is tested and working
- [ ] No console errors or warnings
- [ ] All links are verified
- [ ] Images load correctly
- [ ] CSS is properly applied
- [ ] Mobile responsiveness tested

### Documentation
- [ ] README.md is complete and accurate
- [ ] All features documented
- [ ] Setup instructions are clear
- [ ] CONTRIBUTING.md is in place

### Performance
- [ ] Images are optimized for web
- [ ] CSS files are minified (optional)
- [ ] JavaScript is minified (optional)
- [ ] No broken links
- [ ] Page load times are acceptable

### Security
- [ ] No hardcoded sensitive data
- [ ] Forms use HTTPS (if processing data)
- [ ] No credentials in repository
- [ ] Security headers configured

### Browser Testing
- [ ] Tested on Chrome
- [ ] Tested on Firefox
- [ ] Tested on Safari
- [ ] Tested on Edge
- [ ] Mobile testing done

## Deployment Options

### Option 1: GitHub Pages (Free)

GitHub Pages is the easiest and free hosting option for static websites.

#### Steps

1. **Push to GitHub** (if not already done)
   ```bash
   git add .
   git commit -m "Deploy to GitHub Pages"
   git push origin main
   ```

2. **Enable GitHub Pages**
   - Go to your repository on GitHub
   - Click Settings
   - Scroll to "GitHub Pages"
   - Select source: `main` branch
   - Select folder: `/(root)` or `/docs` (optional)
   - Click "Save"

3. **Access Your Site**
   - Your site will be available at: `https://yourusername.github.io/gym-website`
   - Or if using custom domain: your custom domain

#### Create index.html at Root (Optional)

To make GitHub Pages serve correctly:

```html
<!DOCTYPE html>
<html>
<head>
    <meta http-equiv="refresh" content="0; url=./src/pages/homepage.html">
</head>
</html>
```

Save as `index.html` in the root directory.

### Option 2: Netlify (Free)

Netlify offers easy deployment with automatic HTTPS.

#### Steps

1. **Sign up** on [netlify.com](https://www.netlify.com)

2. **Connect GitHub**
   - Click "New site from Git"
   - Select GitHub
   - Authorize Netlify
   - Choose repository

3. **Configure Build**
   - Build command: (leave empty - it's static)
   - Publish directory: `src` or `src/pages`

4. **Deploy**
   - Click "Deploy site"
   - Your site is live immediately

#### Deploy Updates

After pushing to GitHub:
1. Netlify automatically detects changes
2. Rebuilds and redeploys automatically
3. Updates live within minutes

### Option 3: Vercel (Free)

Similar to Netlify, offers easy deployment.

#### Steps

1. **Sign up** on [vercel.com](https://vercel.com)

2. **Import Project**
   - Click "Import Project"
   - Select GitHub
   - Choose repository

3. **Configure**
   - Framework: Static site
   - Root directory: `./` or `./src`

4. **Deploy**
   - Click "Deploy"
   - Site is live

### Option 4: Traditional Web Hosting

For traditional shared hosting or VPS:

#### FTP/SFTP Upload

```bash
# Install FTP client (FileZilla, WinSCP, etc.)
# Connect to your hosting server
# Upload files from src/ folder to public_html/ directory
```

#### Directory Structure on Server

```
public_html/
├── pages/
│   ├── homepage.html
│   ├── aboutus.html
│   └── [other pages]
├── css/
│   ├── homepage.css
│   └── [other CSS]
└── assets/
    └── images/
        └── [all images]
```

#### SSH Upload

```bash
# Create tarball
tar -czf gym-website.tar.gz src/

# Upload to server
scp gym-website.tar.gz user@server.com:/home/user/

# Extract on server
ssh user@server.com
tar -xzf gym-website.tar.gz -C /var/www/html/
```

## Hosting Providers

### Recommended Free/Paid Options

| Provider | Type | Price | Benefits |
|----------|------|-------|----------|
| GitHub Pages | Static | Free | Simple, integrated with Git |
| Netlify | Static | Free/Paid | Auto-deploy, free SSL, good CMS |
| Vercel | Static | Free/Paid | Fast, auto-deploy, great UI |
| Cloudflare | CDN | Free/Paid | Fast, security, DDoS protection |
| AWS S3 | Storage | Paid (cheap) | Scalable, reliable |
| Google Firebase | Platform | Free/Paid | Realtime, good performance |
| Heroku | Platform | Paid | Easy deployment, auto-scaling |

## Domain Configuration

### Using Custom Domain with GitHub Pages

1. **Purchase Domain**
   - Buy domain from GoDaddy, Namecheap, Google Domains, etc.

2. **Add CNAME File**
   ```bash
   # Create CNAME file in repository root
   echo "yourdomain.com" > CNAME
   git add CNAME
   git commit -m "Add custom domain"
   git push
   ```

3. **Configure DNS** (at your domain provider)
   ```
   CNAME record: yourdomain.com -> yourusername.github.io
   ```

4. **Enable HTTPS**
   - GitHub Pages > Settings
   - Check "Enforce HTTPS"

### Using Custom Domain with Netlify

1. **Add Domain**
   - Netlify dashboard > Domain settings
   - Click "Add custom domain"
   - Enter domain name

2. **Update DNS** (at domain provider)
   - Follow Netlify's instructions
   - Usually: NS records pointing to Netlify

3. **HTTPS**
   - Automatically enabled with Let's Encrypt

## SSL/TLS Setup

### HTTPS Configuration

All modern hosting provides free HTTPS:

- ✅ GitHub Pages - Auto HTTPS
- ✅ Netlify - Let's Encrypt (free)
- ✅ Vercel - Let's Encrypt (free)
- ✅ Cloudflare - Free SSL

### Redirect HTTP to HTTPS

For traditional hosting, add to `.htaccess`:

```apache
<IfModule mod_rewrite.c>
    RewriteEngine On
    RewriteCond %{HTTPS} off
    RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]
</IfModule>
```

## Performance Optimization

### Image Optimization

1. **Compress Images**
   ```bash
   # Using ImageMagick
   mogrify -quality 85 -resize 1920x1080 src/assets/images/*.jpg
   ```

2. **Use Web Formats**
   - Convert to WebP for modern browsers
   - Keep JPG as fallback

### CSS/JS Minification

```bash
# Using online tools or:
# CSS Minifier
# JavaScript Minifier
```

### Caching Headers

Add to `.htaccess` for traditional hosting:

```apache
# Cache static assets
<FilesMatch "\.(jpg|jpeg|png|gif|ico|css|js)$">
    Header set Cache-Control "max-age=2592000, public"
</FilesMatch>
```

### CDN Setup

For faster content delivery globally:
- Cloudflare (recommended)
- CloudFront
- MaxCDN

## Monitoring and Maintenance

### Regular Checks

- ✅ Weekly: Check links and functionality
- ✅ Monthly: Review analytics
- ✅ Monthly: Check for SSL certificate renewal
- ✅ Quarterly: Security audit
- ✅ Quarterly: Performance review

### Analytics

Set up Google Analytics:

```html
<!-- Add to homepage.html -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_ID');
</script>
```

### Uptime Monitoring

- Uptime Robot (free)
- Pingdom
- StatusCake

### Backups

GitHub serves as automatic backup. For additional safety:
1. Regular local backups
2. Database backups (if applicable)
3. Archive important versions

## Troubleshooting

### Images Not Showing

**Problem**: Images return 404 after deployment

**Solution**:
- Check file paths on server match local paths
- Ensure images are uploaded to correct directory
- Verify image file names (case-sensitive on Linux)
- Check image permissions (755)

### Links Not Working

**Problem**: Navigation broken after deployment

**Solution**:
- Verify all .html files are uploaded
- Check relative paths match new structure
- Test all internal links
- Check console for 404 errors

### Slow Performance

**Problem**: Website loads slowly

**Solution**:
- Enable gzip compression
- Optimize images
- Use CDN
- Reduce HTTP requests
- Check hosting server status

### HTTPS Not Working

**Problem**: Mixed content or SSL errors

**Solution**:
- Update all external links to HTTPS
- Check Google Fonts CDN uses HTTPS
- Verify certificate is valid
- Check browser console for mixed content warnings

### Forms Not Submitting

**Problem**: Contact form not working

**Solution**:
- If using form service (Netlify forms), configure properly
- Ensure backend is set up if needed
- Check form action URL
- Test on different browsers

### GitHub Pages Not Updating

**Problem**: Changes not reflecting after push

**Solution**:
- Clear browser cache (Ctrl+Shift+Delete)
- Wait 1-2 minutes for deployment
- Check GitHub Actions for build errors
- Verify main branch is selected
- Hard refresh (Ctrl+F5)

---

## Post-Deployment

After successful deployment:

1. ✅ Test all features thoroughly
2. ✅ Share with team and get feedback
3. ✅ Monitor for errors
4. ✅ Set up analytics
5. ✅ Plan for maintenance
6. ✅ Document deployment process
7. ✅ Train team on updates

## Support & Help

- GitHub Docs: https://docs.github.com
- Netlify Docs: https://docs.netlify.com
- Vercel Docs: https://vercel.com/docs

---

**Need help?** Open an issue or contact the development team.

Happy deploying! 🚀
