# Contributing to FitnessPro

Thank you for your interest in contributing to FitnessPro! We appreciate your help in making this project better. This document provides guidelines and instructions for contributing.

## Code of Conduct

### Our Pledge
We are committed to providing a welcoming and inspiring community for all. Please read and adhere to our Code of Conduct:

- **Be Respectful**: Treat all contributors with respect and kindness
- **Be Inclusive**: We welcome contributors of all skill levels and backgrounds
- **Be Professional**: Keep discussions focused and constructive
- **Report Issues**: If you encounter harassment, report it to the project maintainers

## How Can I Contribute?

### 1. Reporting Bugs

If you find a bug, please open an issue with the following information:

**Title**: Clear, descriptive title
```
[BUG] Issue title
```

**Description**:
- What you expected to happen
- What actually happened
- Steps to reproduce the issue
- Screenshots (if applicable)
- Browser and OS information

**Example**:
```
[BUG] Navigation menu not responsive on mobile

**Expected Behavior**: Menu should be accessible on small screens

**Actual Behavior**: Menu items are cut off on mobile devices (iPhone 12)

**Steps to Reproduce**:
1. Open homepage on iOS Safari
2. Resize browser window to mobile size (375px)
3. Try to access navigation

**Screenshots**: [attach image]
**Browser**: iOS Safari 15.2
```

### 2. Suggesting Enhancements

Have an idea to improve FitnessPro? We'd love to hear it!

**Title**: Clear description of the feature
```
[FEATURE] Feature description
```

**Description**:
- What problem does this solve?
- How would this benefit users?
- Possible implementation approach (optional)
- Alternative approaches (if any)

**Example**:
```
[FEATURE] Dark mode support

**Problem**: Users prefer dark mode for evening browsing

**Solution**: Implement CSS variables for theme switching

**Benefits**: 
- Improved user experience
- Reduced eye strain at night
- Modern web feature
```

### 3. Submitting Code Changes

#### Fork and Clone

```bash
# Fork the repository on GitHub
# Clone your fork
git clone https://github.com/YOUR-USERNAME/gym-website.git
cd gym-website

# Add upstream remote
git remote add upstream https://github.com/ORIGINAL-OWNER/gym-website.git
```

#### Create a Feature Branch

```bash
# Update your local main
git fetch upstream
git checkout main
git merge upstream/main

# Create a feature branch
git checkout -b feature/your-feature-name

# Or for bug fixes
git checkout -b fix/bug-description
```

#### Make Your Changes

1. **Follow the existing code style**:
   - Use consistent indentation (2 spaces)
   - Follow HTML semantic structure
   - Use meaningful CSS class names
   - Write clean, readable JavaScript

2. **Update related files**:
   - If you change HTML structure, update related CSS
   - If you add a new page, update navigation in all pages
   - Update documentation if needed

3. **Test your changes**:
   - Test on multiple browsers (Chrome, Firefox, Safari, Edge)
   - Test on mobile devices or use browser dev tools
   - Verify links and functionality work correctly
   - Check for console errors (F12 → Console tab)

#### Commit Your Changes

```bash
# Add your changes
git add .

# Commit with clear message
git commit -m "type: brief description

Longer explanation if needed.
Explain why this change is needed.

Closes #issue-number (if applicable)"
```

**Commit Message Types**:
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, missing semicolons, etc.)
- `refactor`: Code refactoring
- `test`: Adding or updating tests
- `chore`: Maintenance tasks

**Examples**:
```
feat: Add dark mode toggle button

fix: Correct BMI calculation for metric units

docs: Add deployment instructions

style: Fix CSS indentation in homepage.css

refactor: Reorganize CSS variables

chore: Update .gitignore
```

#### Push Your Changes

```bash
# Push to your fork
git push origin feature/your-feature-name
```

#### Open a Pull Request

1. Go to the original repository on GitHub
2. Click "New Pull Request"
3. Select your branch
4. Fill in the PR template with:
   - **Title**: Clear description of changes
   - **Description**: What changed and why
   - **Related Issues**: Link to related issues (#123)
   - **Screenshots**: If UI changes were made
   - **Testing**: How you tested the changes

**PR Template**:
```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update
- [ ] Refactoring
- [ ] Other: ____

## Related Issues
Closes #issue-number

## Testing
Describe how you tested this change:
- [ ] Tested on Chrome
- [ ] Tested on Firefox
- [ ] Tested on Safari
- [ ] Tested on mobile

## Screenshots
If applicable, add screenshots of UI changes

## Checklist
- [ ] Code follows project style guidelines
- [ ] All links and paths are correct
- [ ] Changes tested on multiple browsers
- [ ] Documentation updated (if needed)
- [ ] No console errors or warnings
```

## Development Workflow

### Project Structure

```
src/
├── pages/          # HTML files
├── css/            # Stylesheets
└── assets/
    └── images/     # Image files
```

### Adding a New Page

1. **Create HTML file**:
   ```bash
   # In src/pages/
   touch newpage.html
   ```

2. **Create CSS file**:
   ```bash
   # In src/css/
   touch newpage.css
   ```

3. **Link CSS in HTML**:
   ```html
   <link rel="stylesheet" href="../css/newpage.css">
   ```

4. **Update navigation**:
   - Add link in all pages' navigation menus
   - Update footer links if needed

5. **Test**:
   - Verify page loads correctly
   - Check navigation links work
   - Test responsive design

### CSS Guidelines

- **Use consistent naming**: `class-name` (hyphenated)
- **Group related styles**: Group by component
- **Use semantic structure**: `.header`, `.main-content`, `.footer`
- **Avoid inline styles**: Use external CSS files
- **Comment complex sections**: Add comments for clarity

**Example**:
```css
/* Navigation */
.nav {
  display: flex;
  justify-content: space-between;
}

.nav__logo {
  font-weight: bold;
}

/* Main Content */
.section {
  padding: 2rem;
}
```

### HTML Guidelines

- **Use semantic tags**: `<header>`, `<nav>`, `<main>`, `<footer>`, `<section>`, `<article>`
- **Meaningful IDs and classes**: Descriptive names
- **Proper nesting**: Elements properly nested and indented
- **Alt text for images**: All images have descriptive alt text
- **Accessibility**: ARIA labels where needed

**Example**:
```html
<section class="section__container">
  <header class="section__header">
    <h2>Section Title</h2>
  </header>
  <div class="section__content">
    <img src="image.jpg" alt="Descriptive text">
  </div>
</section>
```

### JavaScript Guidelines

- **Keep code clean**: Clear variable names
- **Add comments**: Explain complex logic
- **Avoid inline scripts**: Use external files
- **Error handling**: Check for null/undefined values
- **Performance**: Minimize DOM manipulations

## Testing

### Browser Testing

Test your changes on:
- ✅ Chrome (Desktop)
- ✅ Firefox (Desktop)
- ✅ Safari (Desktop)
- ✅ Edge (Desktop)
- ✅ Mobile browsers (iPhone, Android)

### Responsive Testing

- Desktop: 1920px and above
- Tablet: 768px - 1919px
- Mobile: 320px - 767px

Use browser dev tools (F12) → Device Emulation to test responsive design.

### Functionality Testing

- All links work correctly
- Forms submit properly
- Interactive features work as expected
- No console errors
- Images load correctly
- Navigation is intuitive

## Documentation

### Update Documentation When

- Adding new features
- Changing how features work
- Adding new pages
- Significant refactoring
- Security updates

### Documentation Files

- **README.md**: Main project documentation
- **docs/SETUP.md**: Setup instructions
- **docs/FEATURES.md**: Detailed feature documentation
- **Code comments**: Complex logic explanations

## Merge Requirements

Your PR will be merged when:

1. ✅ All checks pass
2. ✅ Code review approved
3. ✅ Changes tested thoroughly
4. ✅ Documentation updated (if applicable)
5. ✅ No conflicts with main branch

## Questions or Need Help?

- Open an issue for questions
- Check existing issues and PRs
- Review project documentation
- Contact maintainers

## Attribution

Contributors will be recognized in the project README. Thank you for your contributions!

---

Thank you for contributing to FitnessPro! 🎉
