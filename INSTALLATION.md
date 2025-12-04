# Installation Guide

This guide provides detailed instructions for installing, running, and deploying the Statistical Pattern Analyzer.

## 📋 Table of Contents

- [Quick Start](#quick-start)
- [System Requirements](#system-requirements)
- [Installation Methods](#installation-methods)
- [Running Locally](#running-locally)
- [Deployment Options](#deployment-options)
- [Troubleshooting](#troubleshooting)

## ⚡ Quick Start

The fastest way to get started:

1. **Download the file**:
   ```bash
   wget https://raw.githubusercontent.com/mariorazo97/statistical-pattern-analyzer/main/statistical_pattern_analyzer.html
   ```

2. **Open in browser**:
   - Double-click the file, or
   - Right-click → Open with → Your Browser

That's it! No installation required.

## 💻 System Requirements

### Minimum Requirements

- **Browser**: Any modern web browser
  - Chrome 90+ (recommended)
  - Firefox 88+
  - Safari 14+
  - Edge 90+
- **JavaScript**: Must be enabled
- **Internet Connection**: Required only for initial load (Chart.js CDN)
- **Screen Resolution**: 1024x768 minimum (responsive design)

### Recommended

- **Browser**: Latest version of Chrome or Firefox
- **RAM**: 4GB+ for optimal performance with large datasets
- **Screen Resolution**: 1920x1080 or higher
- **Internet**: Broadband for faster CDN loading

### Not Supported

- ❌ Internet Explorer (any version)
- ❌ Browsers with JavaScript disabled
- ❌ Very old mobile browsers (pre-2020)

## 📦 Installation Methods

### Method 1: Direct Download

**Easiest method for most users**

1. Go to the [releases page](https://github.com/mariorazo97/statistical-pattern-analyzer/releases)
2. Download `statistical_pattern_analyzer.html`
3. Save it to your desired location
4. Open the file in your browser

### Method 2: Git Clone

**Best for developers**

```bash
# Clone the repository
git clone https://github.com/mariorazo97/statistical-pattern-analyzer.git

# Navigate to the directory
cd statistical-pattern-analyzer

# Open the file
open statistical_pattern_analyzer.html  # macOS
xdg-open statistical_pattern_analyzer.html  # Linux
start statistical_pattern_analyzer.html  # Windows
```

### Method 3: Download ZIP

**Alternative to Git**

1. Visit the repository: `https://github.com/mariorazo97/statistical-pattern-analyzer`
2. Click the green "Code" button
3. Select "Download ZIP"
4. Extract the ZIP file
5. Open `statistical_pattern_analyzer.html`

### Method 4: Use GitHub Pages

**No download required**

Simply visit: `https://mariorazo97.github.io/statistical-pattern-analyzer/`

## 🚀 Running Locally

### Option 1: Direct File Opening

**Simplest method:**

```bash
# macOS
open statistical_pattern_analyzer.html

# Linux
xdg-open statistical_pattern_analyzer.html

# Windows (Command Prompt)
start statistical_pattern_analyzer.html

# Windows (PowerShell)
Invoke-Item statistical_pattern_analyzer.html
```

### Option 2: Local Web Server

**Recommended for development:**

**Using Python:**
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000

# Then open: http://localhost:8000/statistical_pattern_analyzer.html
```

**Using Node.js:**
```bash
# Install http-server globally
npm install -g http-server

# Run server
http-server -p 8000

# Then open: http://localhost:8000/statistical_pattern_analyzer.html
```

**Using PHP:**
```bash
php -S localhost:8000

# Then open: http://localhost:8000/statistical_pattern_analyzer.html
```

### Option 3: Browser Extensions

**For Chrome/Edge:**
1. Install "Web Server for Chrome" extension
2. Choose folder containing the HTML file
3. Click the web server URL

## 🌐 Deployment Options

### GitHub Pages

**Free hosting by GitHub:**

1. **Fork the repository** on GitHub

2. **Enable GitHub Pages:**
   - Go to Settings → Pages
   - Source: Deploy from branch
   - Branch: main
   - Folder: / (root)
   - Click Save

3. **Access your site:**
   - Visit: `https://mariorazo97.github.io/statistical-pattern-analyzer/`
   - Note: Initial deployment may take a few minutes

4. **Automatic deployment:**
   - The included workflow will auto-deploy on push to main

### Netlify

**One-click deployment:**

1. **Fork the repository**

2. **Deploy on Netlify:**
   - Visit [Netlify](https://www.netlify.com/)
   - Click "Add new site" → "Import an existing project"
   - Connect to GitHub
   - Select your fork
   - Build settings:
     - Build command: (leave empty)
     - Publish directory: `/`
   - Click "Deploy site"

3. **Custom domain (optional):**
   - Go to Site settings → Domain management
   - Add your custom domain

### Vercel

**Fast edge deployment:**

1. **Install Vercel CLI:**
   ```bash
   npm install -g vercel
   ```

2. **Deploy:**
   ```bash
   cd statistical-pattern-analyzer
   vercel
   ```

3. **Follow prompts** to complete deployment

### Self-Hosting

**On your own server:**

1. **Copy file to server:**
   ```bash
   scp statistical_pattern_analyzer.html user@yourserver.com:/var/www/html/
   ```

2. **Configure web server:**

   **Apache (.htaccess):**
   ```apache
   <IfModule mod_headers.c>
       Header set X-Frame-Options "DENY"
       Header set X-Content-Type-Options "nosniff"
       Header set Referrer-Policy "no-referrer"
   </IfModule>
   ```

   **Nginx (nginx.conf):**
   ```nginx
   server {
       listen 80;
       server_name yourdomain.com;
       root /var/www/html;
       
       location / {
           add_header X-Frame-Options "DENY";
           add_header X-Content-Type-Options "nosniff";
           add_header Referrer-Policy "no-referrer";
       }
   }
   ```

3. **Enable HTTPS** (recommended):
   ```bash
   # Using Let's Encrypt
   sudo certbot --nginx -d yourdomain.com
   ```

### Docker Deployment

**Containerized deployment:**

1. **Create Dockerfile:**
   ```dockerfile
   FROM nginx:alpine
   COPY statistical_pattern_analyzer.html /usr/share/nginx/html/index.html
   COPY nginx.conf /etc/nginx/nginx.conf
   EXPOSE 80
   ```

2. **Build and run:**
   ```bash
   docker build -t statistical-analyzer .
   docker run -d -p 8080:80 statistical-analyzer
   ```

3. **Access:**
   - Visit: `http://localhost:8080`

## 🔧 Troubleshooting

### Common Issues

#### Issue: File won't open in browser

**Solution:**
- Make sure JavaScript is enabled
- Try a different browser
- Check file wasn't corrupted during download
- Ensure you have a modern browser

#### Issue: Charts not displaying

**Solution:**
```bash
# Check browser console for errors (F12)
# Common causes:
# - CDN blocked by firewall
# - Ad blocker interference
# - JavaScript disabled

# Fix: Download Chart.js locally
# 1. Download from: https://cdn.jsdelivr.net/npm/chart.js@4.4.0/dist/chart.umd.js
# 2. Replace CDN link in HTML with local file
```

#### Issue: Performance issues with large datasets

**Solution:**
- Use smaller dataset size (100-500 instead of 1000)
- Close other browser tabs
- Try Chrome/Edge (usually faster)
- Check RAM usage

#### Issue: CORS errors when running locally

**Solution:**
```bash
# Use a local web server instead of file://
# See "Option 2: Local Web Server" above
```

#### Issue: Mobile display issues

**Solution:**
- Rotate device to landscape
- Zoom out if needed
- Some features work better on desktop
- Try latest Chrome or Safari on mobile

### Browser-Specific Issues

#### Chrome/Edge
- Clear cache: `Ctrl+Shift+Delete`
- Disable extensions temporarily
- Try incognito mode

#### Firefox
- Clear cache: `Ctrl+Shift+Delete`
- Check Enhanced Tracking Protection settings
- Try private window

#### Safari
- Clear cache: Safari → Preferences → Privacy → Manage Website Data
- Check "Prevent cross-site tracking" setting
- Try private window

### Getting Help

If you're still having issues:

1. **Check existing issues**: [GitHub Issues](https://github.com/mariorazo97/statistical-pattern-analyzer/issues)
2. **Browser console**: Press F12 and check for errors
3. **Create an issue**: Include:
   - Browser version
   - Operating system
   - Steps to reproduce
   - Console errors
   - Screenshots

## 🔄 Updating

### Manual Update

1. **Download new version** from releases
2. **Replace old file** with new one
3. **Refresh browser** (Ctrl+F5 / Cmd+Shift+R)

### Git Update

```bash
# Navigate to repository
cd statistical-pattern-analyzer

# Pull latest changes
git pull origin main

# Refresh browser
```

### GitHub Pages Update

Automatic! Changes pushed to main branch will auto-deploy.

## 🧪 Verification

**Verify installation is working:**

1. **Open the file** in your browser
2. **Check for**:
   - ✅ Mock data generates automatically
   - ✅ All charts display
   - ✅ No console errors (F12)
   - ✅ Buttons work
   - ✅ Predictions can be generated

3. **Test features**:
   - Generate new mock data
   - Run full analysis
   - Generate prediction
   - Add custom data

## 📱 Mobile Installation

### iOS (Safari)

1. Open the file in Safari
2. Tap Share button
3. Select "Add to Home Screen"
4. Name it and tap "Add"
5. Access from home screen like an app

### Android (Chrome)

1. Open the file in Chrome
2. Tap menu (three dots)
3. Select "Add to Home screen"
4. Name it and tap "Add"
5. Access from home screen like an app

## 🔐 Security Considerations

### When Hosting Publicly

1. **Use HTTPS** always
2. **Set security headers** (see self-hosting section)
3. **Keep dependencies updated**
4. **Monitor access logs**

### When Using Locally

1. **Download from official source** only
2. **Verify file integrity** if possible
3. **Keep browser updated**
4. **Use virus scanner** on downloaded files

## 📊 Performance Tips

### For Best Performance

1. **Use Chrome or Edge** (fastest Chart.js rendering)
2. **Close unnecessary tabs**
3. **Use smaller datasets** for slower computers
4. **Disable browser extensions** if having issues
5. **Use desktop** for best experience

### For Mobile

1. **Use landscape orientation**
2. **Close other apps**
3. **Use WiFi** instead of cellular
4. **Latest iOS/Android** recommended

## 🎓 Next Steps

After installation:

1. **Read the README**: Understand features and methods
2. **Try the tutorial**: Follow usage examples
3. **Explore methods**: Learn about each statistical technique
4. **Experiment**: Try different datasets and configurations
5. **Contribute**: Consider improving the project

## 📞 Support

- **Documentation**: See README.md
- **Issues**: [GitHub Issues](https://github.com/mariorazo97/statistical-pattern-analyzer/issues)
- **Discussions**: [GitHub Discussions](https://github.com/mariorazo97/statistical-pattern-analyzer/discussions)

---

**Happy Analyzing! 🎉**