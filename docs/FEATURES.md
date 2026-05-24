# FitnessPro Features Documentation

Detailed documentation of all features in the FitnessPro gym website.

## 📋 Table of Contents

1. [Navigation](#navigation)
2. [Home Page](#home-page)
3. [Services Page](#services-page)
4. [About Us Page](#about-us-page)
5. [Contact Us Page](#contact-us-page)
6. [BMI Calculator](#bmi-calculator)
7. [Additional Pages](#additional-pages)

## Navigation

### Global Navigation Menu

Located at the top of every page, the navigation menu includes:

- **Home** - Links to the homepage
- **Services** - Displays available services and programs
- **About** - Company information and mission
- **Community** - Contact page with location information
- **BMI Calculator** - Interactive BMI calculation tool
- **Join Now Button** - Call-to-action button

**Features**:
- Fixed navigation bar for easy access
- Active page highlighting
- Responsive design for mobile devices
- Logo link returns to homepage
- Smooth navigation between pages

### Footer Navigation

Every page includes a footer with:

- Quick links to all main pages
- Social media links
  - Facebook
  - Twitter
  - Instagram
  - LinkedIn
- Copyright information
- Privacy Policy link
- Terms & Conditions link

## Home Page

The landing page that introduces FitnessPro.

### Sections

#### 1. Hero Section
- Eye-catching header image
- Main headline: "BEST GYM IN THE TOWN"
- Subheading: "GET IN SHAPE TODAY"
- Motivational tagline
- Call-to-action button: "Get Started"

#### 2. Explore Programs Section
Four program cards with icons:

1. **Strength**
   - Icon: Boxing icon
   - Description: Explore strength dimensions
   - Action: "Join Now" button

2. **Physical Fitness**
   - Icon: Pulse icon
   - Description: Health and strength activities
   - Action: "Join Now" button

3. **Fat Loss**
   - Icon: Running icon
   - Description: Workout routines for weight loss
   - Action: "Join Now" button

4. **Weight Gain**
   - Icon: Shopping basket icon
   - Description: Sustainable weight gain program
   - Action: "Join Now" button

#### 3. Classes Section
- Two class images showcasing facilities
- Class descriptions
- Different program information

#### 4. Members Section
- Team member profiles
- Member images
- Member information

#### 5. Social Media Links
- Links to follow on social platforms
- Icons for each platform

## Services Page

Detailed information about gym services and programs.

**Content**:
- Service descriptions
- Pricing information (if applicable)
- Program details
- Class schedules
- Trainer information

**Features**:
- Clear service listings
- Professional presentation
- Easy to update content

## About Us Page

Company information and mission statement.

**Content**:
- Company history: "FITNESS ESTD 2000"
- Mission statement
- Company values
- Team information
- Company achievements

**Key Messages**:
- "Fitness is about more than just working out"
- Empowerment and support
- Community focus
- Expert trainers and equipment
- Welcoming environment

## Contact Us Page

Communication and location information.

### Features

#### 1. Contact Information
- Phone number
- Email address
- Physical address
- Business hours

#### 2. Embedded Google Maps
- Interactive map showing gym location
- Location coordinates pre-set
- Zoom and pan capabilities
- Satellite and street view options

#### 3. Contact Form
- Name input field
- Email input field
- Message textarea
- Submit button

#### 4. Contact Methods Display
- Phone icon with number
- Email icon with address
- Location icon with full address

**Location**: Fitness Studio GYM, Islamabad, Pakistan

## BMI Calculator

Interactive tool for calculating Body Mass Index.

### How It Works

#### Inputs
1. **Weight** - Input in kilograms (kg)
   - Accepts decimal values (e.g., 75.5)
2. **Height** - Input in meters (m)
   - Accepts decimal values (e.g., 1.75)

#### Calculation
The calculator uses the standard BMI formula:
```
BMI = Weight (kg) / (Height (m) × Height (m))
```

#### Results Display
After clicking "Calculate BMI", displays:
- **BMI Value** - The calculated number
- **Category** - Health status category:
  - Underweight: BMI < 18.5
  - Normal Weight: BMI 18.5 - 24.9
  - Overweight: BMI 25.0 - 29.9
  - Obese: BMI ≥ 30.0

### Features
- Real-time calculation
- Error handling for invalid inputs
- Clear result display
- Responsive design

### Technical Implementation
- Implemented in JavaScript
- Located in [bmi.html](../src/pages/bmi.html)
- Styled with [bmi.css](../src/css/bmi.css)

## Additional Pages

### Blogs Page
- Fitness news and tips
- Article listings
- Blog category information

### Checkout Page
- Membership package selection
- Payment information (if integrated)
- Order summary
- Member details form

### Network Page
- Network information
- Branch locations
- Partner information

### Partners Page
- Partnership details
- Featured partners
- Business collaboration information

### Privacy Policy Page
- Privacy statement
- Data collection information
- User rights
- GDPR compliance (if applicable)

### Terms & Conditions Page
- Terms of service
- Usage policies
- Liability information
- User agreements

### Business Page
- Business information
- Partnership opportunities
- Franchise information
- B2B services

---

## Feature Statistics

- **Total Pages**: 12
- **Interactive Features**: BMI Calculator
- **Forms**: Contact form, BMI calculator
- **External Integrations**: Google Maps, Remixicon Icons, Social Media
- **Responsive Breakpoints**: Mobile (320px), Tablet (768px), Desktop (1920px+)

## Browser Support

All features work on:
- ✅ Chrome (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Edge (latest)
- ✅ Mobile browsers

## Future Feature Ideas

- [ ] Member login system
- [ ] Class booking system
- [ ] Payment gateway
- [ ] User progress tracking
- [ ] Email notifications
- [ ] Live chat support
- [ ] Video tutorials
- [ ] Member testimonials
- [ ] Blog comment system
- [ ] Newsletter subscription

---

For setup instructions, see [SETUP.md](SETUP.md)
For deployment guidelines, see [DEPLOYMENT.md](DEPLOYMENT.md)
