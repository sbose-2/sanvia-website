# Sanvia Website - Render Deployment Guide

## Step-by-Step Deployment to Render

### 1. Prepare Your Repository

First, make sure all your files are committed to GitHub:

```bash
# Initialize git repository (if not already done)
git init

# Add all files
git add .

# Commit changes
git commit -m "Initial commit: Sanvia website ready for Render deployment"

# Add remote repository (replace with your GitHub repo URL)
git remote add origin https://github.com/yourusername/sanvia-website.git

# Push to GitHub
git push -u origin main
```

### 2. Deploy to Render

1. **Go to Render Dashboard**
   - Visit: https://dashboard.render.com
   - Sign in with GitHub (recommended)

2. **Create New Static Site**
   - Click "New +" button
   - Select "Static Site"
   - Choose "Connect a repository"
   - Find and select your `sanvia-website` repository

3. **Configure Deployment Settings**
   ```
   Name: sanvia-website
   Branch: main
   Build Command: (leave empty)
   Publish Directory: .
   ```

4. **Advanced Settings (Optional)**
   - Auto Deploy: ✅ Enabled
   - PR Previews: ✅ Enabled (for testing)

### 3. Custom Domain Setup

#### Option A: Using GoDaddy DNS (Recommended)

1. **In Render Dashboard:**
   - Go to your deployed site
   - Click "Settings" → "Custom Domains"
   - Add both domains:
     - `sanvia.co`
     - `www.sanvia.co`

2. **In GoDaddy DNS Management:**
   ```
   Type    Name    Value                           TTL
   CNAME   www     sanvia-website.onrender.com     1 Hour
   A       @       216.24.57.1                     1 Hour
   ```
   
   *Note: Replace `sanvia-website.onrender.com` with your actual Render URL*
   *Render will provide the exact A record IP in your dashboard*

#### Option B: Using Render DNS (Alternative)

1. In GoDaddy, change nameservers to Render's nameservers
2. Manage DNS entirely through Render dashboard

### 4. Verification & Testing

1. **Check Deployment Status**
   - Monitor build logs in Render dashboard
   - Ensure "Deploy successful" status

2. **Test Your Site**
   - Visit temporary Render URL: `https://sanvia-website.onrender.com`
   - Test all sections and animations
   - Verify mobile responsiveness
   - Check form functionality

3. **Verify Custom Domain**
   - Once DNS propagates (5-60 minutes), visit `https://sanvia.co`
   - SSL certificate automatically provisioned
   - Redirects from HTTP to HTTPS

### 5. Performance Optimization

Your site is already optimized with:
- ✅ SVG assets for fast loading
- ✅ Minified CSS and JavaScript
- ✅ Proper cache headers (configured in `render.yaml`)
- ✅ CDN distribution worldwide
- ✅ Automatic Gzip compression

### 6. Monitoring & Updates

1. **Auto-Deploy Setup**
   - Any push to `main` branch automatically deploys
   - Check deployment status in Render dashboard

2. **Performance Monitoring**
   - Render provides basic analytics
   - Consider adding Google Analytics for detailed insights

3. **SSL Certificate**
   - Automatically provisioned and renewed
   - No manual intervention needed

### 7. Environment-Specific Configuration

For different environments, you can use Render's branch deploys:

```yaml
# render.yaml (already included)
services:
  - type: web
    name: sanvia-website
    env: static
    buildCommand: ""
    staticPublishPath: .
```

### 8. Troubleshooting Common Issues

#### DNS Not Propagating
- Use `nslookup sanvia.co` to check DNS
- Allow up to 48 hours for full propagation
- Use online DNS checkers for verification

#### Build Failures
- Check build logs in Render dashboard
- Ensure all files are properly committed
- Verify `render.yaml` syntax

#### 404 Errors
- Confirm `index.html` is in root directory
- Check rewrite rules in `render.yaml`

### 9. Post-Deployment Checklist

- [ ] Site loads at `https://sanvia.co`
- [ ] All animations and interactions work
- [ ] Mobile responsiveness verified
- [ ] Contact forms function properly
- [ ] SSL certificate is active
- [ ] All internal links work
- [ ] SEO meta tags are present
- [ ] Social media preview cards display correctly

### 10. Future Updates

To update your website:
1. Make changes locally
2. Test changes locally: `python -m http.server 8000`
3. Commit and push to GitHub: `git push origin main`
4. Render automatically deploys changes
5. Verify updates at `https://sanvia.co`

## Support Resources

- **Render Documentation:** https://render.com/docs/static-sites
- **Render Status Page:** https://status.render.com
- **Render Community:** https://community.render.com

Your Sanvia website is now ready for professional deployment! 🚀