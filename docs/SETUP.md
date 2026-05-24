# Setup Instructions

## Prerequisites

Before you begin, ensure you have the following:

- A modern web browser (Chrome, Firefox, Safari, or Edge)
- Text editor for code editing (VS Code, Sublime Text, Atom, etc.)
- Git installed on your machine (for cloning the repository)
- (Optional) Local web server software (Python, Node.js, or PHP)

## Installation Steps

### Step 1: Clone the Repository

```bash
# Clone the repository
git clone https://github.com/yourusername/gym-website.git

# Navigate to the project directory
cd gym-website
```

### Step 2: Verify Project Structure

The project should have the following structure:

```
gym-website/
├── README.md
├── CONTRIBUTING.md
├── LICENSE
├── .gitignore
├── .editorconfig
├── docs/
├── src/
│   ├── pages/
│   ├── css/
│   └── assets/
└── [other files]
```

### Step 3: Open the Project

#### Option A: Direct Browser Opening (Simple)

1. Navigate to `src/pages/` folder
2. Right-click on `homepage.html`
3. Select "Open with" and choose your browser
4. The website should load

#### Option B: Using a Local Server (Recommended)

**Using Python 3:**

```bash
# Navigate to the project root
cd gym-website

# Start local server
python -m http.server 8000

# Open in browser
# http://localhost:8000/src/pages/homepage.html
```

**Using Python 2:**

```bash
python -m SimpleHTTPServer 8000
```

**Using Node.js (requires Node.js installation):**

```bash
# Install http-server globally (one-time)
npm install -g http-server

# Start server
http-server

# Open in browser
# http://localhost:8080/src/pages/homepage.html
```

**Using PHP:**

```bash
# Navigate to project root
cd gym-website

# Start PHP server
php -S localhost:8000

# Open in browser
# http://localhost:8000/src/pages/homepage.html
```

## Verification

After setup, verify the following:

1. ✅ Homepage loads without errors
2. ✅ All navigation links work
3. ✅ Images load correctly
4. ✅ CSS styling is applied
5. ✅ No console errors (F12 → Console tab)

## Configuration

### Environment Setup

No special environment configuration is needed for this project. However, you may want to:

1. **Set up your editor**:
   - Install an EditorConfig plugin
   - Use the provided `.editorconfig` file
   - Set up auto-formatting

2. **Configure Git** (if needed):
   ```bash
   git config user.name "Your Name"
   git config user.email "your.email@example.com"
   ```

### Recommended VS Code Extensions

If using Visual Studio Code:

1. **Live Server** - Live reload during development
2. **Prettier** - Code formatting
3. **HTML Hint** - HTML validation
4. **CSS Peek** - CSS navigation
5. **W3C Web Validator** - Web validation

## Troubleshooting

### Images Not Loading

**Problem**: Images show as broken icons

**Solution**:
- Check that images are in `src/assets/images/`
- Verify file paths use `../assets/images/filename.jpg`
- Check file names match exactly (case-sensitive on some systems)
- Clear browser cache (Ctrl+Shift+Del)

### CSS Not Applied

**Problem**: Website looks unstyled

**Solution**:
- Verify CSS files are in `src/css/`
- Check that HTML references correct CSS path: `../css/filename.css`
- Clear browser cache
- Open browser console (F12) to check for 404 errors

### Local Server Not Starting

**Problem**: "Address already in use" or similar error

**Solution**:
- Try a different port: `python -m http.server 8001`
- Kill existing process on port 8000
- Windows: `netstat -ano | findstr :8000`
- Mac/Linux: `lsof -i :8000`

### Links Not Working

**Problem**: Navigation links return 404

**Solution**:
- Verify page files exist in `src/pages/`
- Check link paths don't have extra `../`
- Links between pages should be just filename: `aboutus.html`
- Links to assets should use `../assets/images/`

## Next Steps

After setup:

1. Read the [README.md](../README.md) for project overview
2. Check [FEATURES.md](FEATURES.md) for detailed features
3. Review the code structure
4. Make modifications as needed
5. Follow [CONTRIBUTING.md](../CONTRIBUTING.md) for contributions

## Getting Help

- Check existing documentation
- Review HTML/CSS files for comments
- Open an issue on GitHub
- Contact the development team

---

**Need more help?** See [DEPLOYMENT.md](DEPLOYMENT.md) for deployment instructions.
