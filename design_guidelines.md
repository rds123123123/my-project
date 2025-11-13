# Design Guidelines: Craig Clery Painting Contractor Website

## Design Approach
**Reference-Based Approach** - Drawing inspiration from premium home service websites (HomeAdvisor, Thumbtack, Houzz) with strong focus on visual project showcases combined with conversion-optimized lead generation. The design balances professional credibility with approachable, local service provider warmth.

## Brand Colors (from provided assets)
- **Primary Yellow**: 45 91% 63% - Bold, energetic yellow from branding
- **Primary Blue**: 211 100% 64% - Bright, trustworthy blue
- **Accent Coral**: 0 100% 71% - Warm, friendly coral/red
- **Dark**: 0 0% 13% - Charcoal for text and depth
- **Light**: 0 0% 97% - Off-white for backgrounds
- **Dark Mode Background**: 222 47% 11% - Deep blue-gray for dark theme

## Typography
- **Headings**: 'Poppins' - Bold, modern sans-serif (weights: 600, 700, 800)
- **Body**: 'Inter' - Clean, readable (weights: 400, 500, 600)
- **Scale**: text-5xl/6xl for hero headlines, text-3xl/4xl for section headers, text-lg/xl for body content

## Layout System
**Spacing Primitives**: Use Tailwind units of 4, 8, 12, 16, 20, 24, 32 for consistent rhythm
- Section padding: py-16 md:py-24 lg:py-32
- Component spacing: space-y-8 to space-y-12
- Card padding: p-6 to p-8
- Container: max-w-7xl mx-auto px-4 sm:px-6 lg:px-8

## Hero Section Layout
**Two-Column Split Design**:
- Left Column (55% width): Hook/headline with compelling tagline about Craig's expertise, brief value proposition, trust indicators (years in business, certifications)
- Right Column (45% width): Prominent quote request form with yellow CTA button, fields for name, email, phone, service type, message
- Background: Large hero image of Craig's best work (painted exterior/interior) with subtle dark overlay (opacity-40) for text readability
- Height: min-h-screen on desktop, stacks to single column on mobile

## Statistics Section
**Animated Counter Cards** (4 metrics in grid):
- Grid layout: grid-cols-2 md:grid-cols-4 gap-8
- Metrics: "30+ Years Experience", "500+ Projects Completed", "100% Satisfaction Rate", "5-Star Average Rating"
- Card style: White background with subtle yellow left border (border-l-4), hover lift effect
- Numbers: Large bold yellow text (text-yellow-500) with animated count-up
- Background: Light gray (bg-gray-50) section

## Reviews Section
**Google Reviews Display**:
- Layout: 3-column grid (grid-cols-1 md:grid-cols-2 lg:grid-cols-3) with 6 dummy reviews
- Card design: White cards with shadow, yellow star ratings at top, review text, customer name and date at bottom
- Include mix of 5-star and 4-star ratings for authenticity
- Section background: White with yellow accent stripe at top

## Maps Integration
**Location Section**:
- Two-column layout: Map on left (60%), Contact info and hours on right (40%)
- Map: Full-height embedded Google Maps iframe with business location pin
- Right side: Address with blue location icon, phone with coral icon, email, business hours
- Background: Light gray gradient

## About Craig Section
**Single Column Centered Content**:
- Max-width: max-w-4xl for optimal reading
- Include professional photo of Craig (left-aligned with text wrapping)
- Content: Opening paragraph about 1990 founding, expertise areas (interior/exterior painting, wallpaper, commercial/residential), values and approach
- Background: White with subtle yellow accent elements
- CTA at bottom: "Request a Free Quote" button in coral

## Projects Gallery
**Masonry-Style Portfolio Grid**:
- Layout: 3-column masonry grid (Tailwind: columns-1 md:columns-2 lg:columns-3)
- 9-12 project images with before/after comparisons where possible
- Hover effect: Image zoom with overlay showing project title and category
- Filter tabs above grid: "All", "Residential", "Commercial", "Exterior", "Interior"
- Background: Soft gradient from yellow-50 to white

## Images Required
1. **Hero Image**: High-quality photo of beautifully painted interior or exterior (bright, professional, showcasing Craig's best work) - full-width background
2. **About Section**: Professional portrait photo of Craig Clery on site or with painting equipment
3. **Project Gallery**: 9-12 high-resolution before/after or completed project photos showing variety (interiors, exteriors, different color schemes, residential and commercial)

## Component Library
- **Buttons**: Primary (bg-yellow-500 hover:bg-yellow-600), Secondary (bg-blue-500), Outline (border-2 with backdrop-blur-sm when over images)
- **Form Inputs**: Rounded-lg, border-gray-300, focus:border-blue-500 with floating labels
- **Cards**: shadow-lg hover:shadow-xl transition, rounded-xl
- **Icons**: Heroicons for all UI elements (stars, location pin, phone, email, checkmarks)
- **Navigation**: Sticky top navigation with logo left, menu center, "Get Quote" CTA right in yellow

## Animations
Use sparingly:
- Number counter animations in statistics section (count-up effect)
- Smooth scroll to sections on navigation click
- Subtle fade-in on scroll for section reveals
- Card hover lifts (transform translate-y-1)

## Dark Mode Considerations
All form inputs and text fields maintain consistent dark mode styling with proper contrast against dark backgrounds.