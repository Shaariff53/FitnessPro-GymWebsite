# 💪 FitnessPro - Gym Management Website

A modern, responsive fitness gym website built with HTML, CSS, and JavaScript. This project showcases a professional web presence for a gym/fitness business with multiple pages, interactive tools, and engaging content.

## 🌟 Features

- **Home Page** - Eye-catching landing page with program overview
- **Services Page** - Detailed information about gym services and programs
- **About Us Page** - Company story and mission statement
- **Contact Us Page** - Contact information and Google Maps integration
- **BMI Calculator** - Interactive tool to calculate Body Mass Index
- **Blog Section** - News and fitness tips
- **Membership Plans** - Showcase different membership tiers
- **Partner Information** - Business partnerships and network details
- **Responsive Design** - Optimized for desktop, tablet, and mobile devices
- **Modern UI** - Clean and professional user interface with smooth interactions

## 🛠️ Tech Stack

- **HTML5** - Semantic markup for better accessibility
- **CSS3** - Modern styling with flexbox and responsive design
- **JavaScript** - Interactive features and calculations
- **Remixicon** - Beautiful icon library for UI elements

## 📁 Project Structure

```
gym-website/
├── README.md                 # Project documentation
├── CONTRIBUTING.md           # Contribution guidelines
├── LICENSE                   # MIT License
├── .gitignore               # Git ignore rules
├── .editorconfig            # Editor configuration
├── docs/                    # Documentation files
│   ├── SETUP.md            # Setup instructions
│   ├── FEATURES.md         # Detailed feature documentation
│   └── DEPLOYMENT.md       # Deployment guidelines
└── src/
    ├── pages/              # HTML pages
    │   ├── homepage.html
    │   ├── aboutus.html
    │   ├── services.html
    │   ├── contactus.html
    │   ├── bmi.html
    │   ├── blogs.html
    │   ├── checkout.html
    │   ├── network.html
    │   ├── partners.html
    │   ├── pp.html          # Privacy Policy
    │   ├── terms.html       # Terms & Conditions
    │   └── bussiness.html
    ├── css/                 # Stylesheets
    │   ├── homepage.css
    │   ├── aboutus.css
    │   ├── services.css
    │   ├── contactus.css
    │   ├── bmi.css
    │   └── [other styles]
    └── assets/
        ├── images/         # All image assets
        │   ├── logo.jpg
        │   ├── class1.jpg
        │   └── [other images]
        └── icons/          # Icon assets (if needed)
```

## 🚀 Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- No additional dependencies required - this is a vanilla HTML/CSS/JS project

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/gym-website.git
   cd gym-website
   ```

2. **Open the project**
   - Navigate to `src/pages/` directory
   - Open `homepage.html` in your web browser
   - Or use a local server (recommended for production)

3. **Using a Local Server (Optional)**
   ```bash
   # Using Python (if installed)
   python -m http.server 8000
   
   # Using Node.js (if installed)
   npx http-server
   
   # Using PHP (if installed)
   php -S localhost:8000
   ```

   Then open `http://localhost:8000/src/pages/homepage.html` in your browser.

## 📖 Usage

### Navigation
- Use the navigation bar at the top of each page to move between sections
- The "Join Now" button redirects to the contact page for membership inquiries
- Footer links provide quick access to important pages

### BMI Calculator
1. Navigate to the BMI Calculator page
2. Enter your weight (in kg) and height (in meters)
3. Click "Calculate BMI" to get your BMI value and health category

### Contact Information
- Visit the Contact Us page for business hours and location
- The embedded Google Map shows the gym location
- Multiple contact methods are available

## 🎨 Customization

### Updating Content
1. Edit the relevant HTML file in `src/pages/`
2. Modify text, images, or layout as needed
3. CSS files in `src/css/` contain all styling

### Adding New Pages
1. Create a new HTML file in `src/pages/`
2. Create a corresponding CSS file in `src/css/`
3. Update navigation links in all pages to include the new page
4. Follow the existing code structure for consistency

### Changing Colors & Styles
- Edit the CSS files in `src/css/`
- Look for color variables and modify them
- Test changes across different pages

## 🖼️ Images

All images are located in `src/assets/images/`. To add new images:
1. Place image files in `src/assets/images/`
2. Reference them in HTML using relative paths: `../assets/images/filename.jpg`

## 📱 Responsive Design

The website is designed to be responsive and work well on:
- Desktop computers (1920px and above)
- Tablets (768px - 1919px)
- Mobile devices (320px - 767px)

Test responsiveness using your browser's developer tools (F12 or Ctrl+Shift+I).

## 🔧 Browser Compatibility

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 📚 Learning Outcomes

This project demonstrates:
- ✅ Semantic HTML5 structure
- ✅ Responsive CSS3 design
- ✅ JavaScript interactivity
- ✅ Professional project organization
- ✅ Web accessibility best practices
- ✅ Git version control

## 🤝 Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

### Quick Contribution Steps
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Authors

**Original Developer:** Shaariff
- Created as part of ICT semester course
- First practical web development project

## 📞 Support

For issues, questions, or suggestions:
1. Open an issue on GitHub
2. Contact the development team
3. Check the [documentation](docs/) for more information

## 🎯 Future Enhancements

- [ ] Member login system
- [ ] Online booking for classes
- [ ] Payment gateway integration
- [ ] User progress tracking
- [ ] Mobile app version
- [ ] Admin dashboard
- [ ] Blog comment system
- [ ] Email subscription feature
- [ ] Multi-language support

## 📈 Performance

The website is optimized for:
- Fast loading times
- Smooth animations
- Mobile-first design
- SEO best practices

## 🔒 Security

- No sensitive data stored locally
- Form submissions should use HTTPS in production
- Regular security updates recommended

## 📝 Changelog

### Version 1.0 (Current)
- Initial project setup
- All core pages implemented
- Professional project structure
- Comprehensive documentation

---

**Last Updated:** May 2026

For more information, visit the [documentation](docs/) folder or check out [CONTRIBUTING.md](CONTRIBUTING.md).

---

⭐ If you find this project helpful, please consider giving it a star! ⭐
