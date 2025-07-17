# Company Profile Template ----------------------------------------------------------->

## Basic Information
- **Business Name**: [Your Business Name]
- **Business Type**: [e.g., Café, Restaurant, Retail Store, etc.]
- **Tagline**: [Your Business Tagline]
- **Establishment Date**: [Year Founded]

## Contact Information
- **Address**: [Full Business Address]
- **Phone**: [Primary Contact Number]
- **Email**: [Business Email]
- **Operating Hours**:
  - Monday-Friday: [e.g., 7:00 AM - 8:00 PM]
  - Saturday-Sunday: [e.g., 8:00 AM - 9:00 PM]
  - Holidays: [Special Hours if any]

## Social Media
- **Facebook**: [URL]
- **Instagram**: [URL]
- **Twitter**: [URL]
- **LinkedIn**: [URL]
- **TikTok**: [URL]

## Brand Identity
- **Primary Color**: [HEX Code, e.g., #4A90E2]
- **Secondary Color**: [HEX Code]
- **Accent Color**: [HEX Code]
- **Fonts**:
  - Heading Font: [e.g., Pacifico, Playfair Display]
  - Body Font: [e.g., Inter, Open Sans]
- **Logo**: [File name in assets folder]

## Business Description
[2-3 sentences describing your business, its mission, and unique value proposition]

## Key Features/Services
1. [Main Feature/Service 1]
2. [Main Feature/Service 2]
3. [Main Feature/Service 3]
4. [Add more as needed]






## Core Website Sections ------------------------------------------------------------->
- **Hero Section** [Priority: Essential]
  - [ ] Full-width Image/Slider
  - [ ] Headline & Subheading
  - [ ] Call-to-Action Button
  - [ ] Background Video Option
  - Style: [Modern/Classic/Minimal/Dynamic]

- **About/Story** [Priority: High]
  - [ ] Company Story
  - [ ] Mission/Vision
  - [ ] Team Section
  - [ ] Awards/Recognition
  - Style: [Text-focused/Image-rich/Timeline]

- **Services/Products** [Priority: Essential]
  - [ ] Featured Items
  - [ ] Categories Display
  - [ ] Pricing Tables
  - [ ] Service Details
  - Style: [Grid/List/Cards/Carousel]

- **Social Proof** [Priority: High]
  - [ ] Customer Reviews
  - [ ] Testimonials
  - [ ] Ratings Display
  - [ ] Client Logos
  - Style: [Carousel/Grid/Cards]

- **Call-to-Action Sections** [Priority: Essential]
  - [ ] Primary CTA
  - [ ] Newsletter Signup
  - [ ] Booking/Reservation
  - [ ] Contact Form
  - Style: [Full-width/Boxed/Floating]

- **Gallery/Portfolio** [Priority: Flexible]
  - [ ] Image Gallery
  - [ ] Project Showcase
  - [ ] Virtual Tour
  - [ ] Before/After
  - Style: [Masonry/Grid/Slider]

- **Contact Section** [Priority: Essential]
  - [ ] Contact Form
  - [ ] Map Location
  - [ ] Business Hours
  - [ ] Contact Details
  - Style: [Split/Full-width/Compact]

- **Footer** [Priority: Essential]
  - [ ] Quick Links
  - [ ] Social Media
  - [ ] Newsletter
  - [ ] Contact Info
  - [ ] Legal Links
  - Style: [Multi-column/Simple/Expanded]

- **Additional Sections** [Priority: Optional]
  - [ ] FAQ
  - [ ] Blog/News
  - [ ] Events Calendar
  - [ ] Special Offers
  - [ ] Partner Logos
  - Style: [Accordion/Cards/Timeline]

Note: For each section, check what's relevant for your business type and choose an appropriate style. Priority levels indicate importance but can be adjusted based on business needs.


## Forms Required
- [ ] Contact Form
- [ ] Book a Table
- [ ] Newsletter Signup
- [ ] Consultation Request
- [ ] Feedback Form
- [ ] [Add custom forms as needed]

## Menu/Products Section
- **Categories**:
  1. [Category 1]
  2. [Category 2]
  3. [Add more as needed]

## Image Requirements
- Hero Section: [Description of desired hero image]
- About Section: [Description of about/story images]
- Gallery: [Number and types of images needed]
- Menu Items: [Image specifications for menu items]

## Optional Sections
- [ ] Blog/News
- [ ] Events Calendar
- [ ] Customer Reviews
- [ ] Team Members
- [ ] FAQ
- [ ] Career Opportunities
- [ ] Gift Cards
- [ ] Loyalty Program

## Special Features
- [ ] Online Ordering
- [ ] Reservation System
- [ ] Live Chat
- [ ] Virtual Tour
- [ ] download services/menu
- [ ] [Add custom features as needed]

## Mobile Navigation (Burger Menu)
- **Animation Style**: [Slide]
 **Menu Icon Style**: [Classic Three Lines]
- **Menu Type**: [Choose one]
  - [ ] Slide from Left
  - [ ] Slide from Right
  - [ ] Slide from Top
  - [ ] Slide from Bottom
  - [ ] Fade In Center
  - [ ] Full Screen Overlay



## Instructions for AI Implementation for editing index.html ------------------------->

## Section Implementation Instructions

1. **Folder Structure Analysis**:
   - Scan the `/sections` directory
   - Each section type has its own subdirectory (e.g., `/sections/hero`, `/sections/about`)
   - Section variants are numbered (e.g., `hero-1.html`, `hero-2.html`)

2. **Section Selection Process**:
   ```
   /sections/
   ├── hero/
   │   ├── hero-1.html      # Modern, full-width image
   │   ├── hero-2.html      # Video background
   │   └── hero-3.html      # Minimal, text-focused
   ├── about/
   │   ├── about-1.html     # Story-focused
   │   └── about-2.html     # Team-focused
   ...
   ```

3. **Selection Criteria**:
   - Check business type from Company Profile
   - Scan checked items in Core Website Sections
   - Match section style preference if specified
   - Consider section priority level
   - Evaluate section components needed

4. **Implementation Flow**:
   ```
   For each CHECKED section in Core Website Sections:
     1. Read priority level [Essential/High/Flexible/Optional]
     2. Read style preference [e.g., Modern/Classic/Minimal]
     3. Read required components [e.g., Form/Gallery/Map]
     4. Scan /sections/{section_name}/ directory
     5. Select best matching variant based on:
        - Business type compatibility
        - Style match
        - Required components
     6. If no exact match, select closest match
     7. Implement selected section
   ```

5. **Component Requirements**:
   - Essential sections must include all checked components
   - High priority sections should include most checked components
   - Flexible/Optional sections can be more loosely matched

6. **Style Consistency**:
   - Maintain selected color scheme across all sections
   - Use specified fonts consistently
   - Adapt section padding/spacing to match design
   - Ensure responsive behavior is consistent

7. **Content Integration**:
   - Replace placeholder content with business information
   - Scale images to specified dimensions
   - Implement interactive elements as specified
   - Connect forms to appropriate endpoints

8. **Fallback Strategy**:
   If exact match not found:
   1. Use closest matching section variant
   2. Modify to include missing components
   3. Adjust styling to match requirements
   4. Document modifications needed

Example Implementation:
```javascript
// Pseudo-code for section selection
function selectSection(sectionType, businessType, style, components) {
  const sectionPath = `/sections/${sectionType}/`;
  const variants = scanDirectory(sectionPath);
  
  return variants
    .map(variant => ({
      variant,
      score: calculateMatchScore(variant, {
        businessType,
        style,
        components
      })
    }))
    .sort((a, b) => b.score - a.score)[0];
}
```

## Image Requirements ---------------------------------------------------------------->

### Hero Section
- Location: `assets/hero/{best fit image}`
- best fit image for container and topic
- Optimization: Compress without losing quality

### About Section
- Location: `assets/about/{best fit image}`
- best fit image for container and topic

### Gallery
- Location: `assets/gallery/{best fit image}`
- best fit image for container and topic

### Menu-Service Section
- Location: `assets/menu-services/{best fit image}`
- best fit image for container and topic

### Customer-feedback Section
- Location: `assets/customer-feedback/{best fit image}`
- best fit image for container and topic

## Content Replacement -------------------------------------------------------------->

1. **Content Replacement**:
   - Replace all placeholder text in the website with information from this profile
   - Maintain the specified brand colors and fonts throughout if not provided - provide the best possible implementation
   - Use provided images from assets folder, or generate appropriate images if not provided - provide the best possible implementation

2. **Structural Changes**:
   - Include only the checked optional sections
   - Implement the checked forms with proper validation
   - Add any special features marked as required

3. **Style Implementation**:
   - If no colors are specified, use:
     - Primary: Use the color from the company profile, if not provided Use best possible implementation
     - Secondary: Use the color from the company profile, if not provided Use best possible implementation
     - Accent: Use the color from the company profile, if not provided Use best possible implementation
   - If no fonts specified, use:
     - Headings: Use the font from the company profile, if not provided Use best possible implementation
     - Body: Use the font from the company profile, if not provided Use best possible implementation

4. **Responsive Design**:
   - Ensure all content is mobile-responsive
   - Optimize images for different screen sizes
   - Maintain readability across devices
   - Implement burger menu according to selected configuration above
   - Apply smooth transitions for menu interactions (300ms duration)
   - Ensure touch-friendly tap targets (minimum 44px)
   - Maintain brand consistency in mobile view

5. **SEO Optimization**:
   - Use business name and location in meta tags
   - Implement proper heading hierarchy
   - Include alt text for all images

6. **Form Handling**:
   - Set up form submissions to specified email
   - Implement proper validation and error handling
   - Add success/error messages (best is that the button will turned into a loading state and will show a success/error message)
   - the form will be using netlify for submissions

7. **Performance**:
   - Optimize image sizes
   - Implement lazy loading for images
   - Minimize CSS/JS files