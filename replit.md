# Craig Clery Painting Contractor Website

## Overview

This is a professional website for Craig Clery Decorating and Roof Coatings, a painting contractor business established in 1990. The site serves as a digital presence to showcase services, display project portfolios, collect customer reviews, and facilitate quote requests. The application is built as a modern multi-page application with a focus on conversion optimization and visual appeal.

## Recent Changes

**October 2025 - UI Refinements:**
- Removed testimonials from home page (TestimonialsBanner and ReviewsSection components)
- Updated StatsSection background from gradient to light/neutral for cleaner look
- Changed section badges ("Our Services", "Our Values") to coral with coral glow effect
- Updated accent color system-wide to coral (0 100% 71%) for brand consistency

**October 2025 - Modern Visual Design Overhaul:**
- Complete redesign with vibrant yellow/orange brand colors and modern aesthetic
- Added gradient backgrounds, decorative elements, and blur effects throughout
- Enhanced with generous negative space and improved typography
- All sections feature hover animations, scale transforms, and color transitions
- Service cards with corner accents and image zoom effects on hover
- Stats section with dramatic yellow gradient background and floating number cards
- Mission cards with animated gradient bars and icon transforms
- Process steps with vertical accent bars and enhanced visual hierarchy
- Popular Colors section with elevated card effects and white badges
- Reviews section with subtle gradient background and blurred ornamental circles

**October 2025 - Home Page Expansion:**
- Updated hero headline to "Painting With The 'How It Used To Be' Quality"
- Added Popular Colours section showcasing 8 most requested paint colors
- Added Our Process section to home page
- Added Mission/Values section with company core values
- Added Testimonials section to home page
- Home page now includes: Hero, Stats, Services, Popular Colors, Process, Mission, and Reviews

**October 2025 - Multi-Page Restructuring:**
- Converted from single-page to multi-page architecture
- Added navigation header (Navbar component) with links to all pages
- Created dedicated pages: Home, About, Projects, Reviews, Contact
- About, Projects, Reviews sections available on dedicated pages
- Contact page includes form and map
- Mobile-responsive navigation with hamburger menu

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture

**Technology Stack:**
- **Framework**: React 18 with TypeScript
- **Routing**: Wouter (lightweight client-side routing)
- **Styling**: Tailwind CSS with custom design system
- **UI Components**: Shadcn/ui component library (Radix UI primitives)
- **State Management**: TanStack Query (React Query) for server state
- **Build Tool**: Vite

**Design System:**
The application implements a custom design system based on the brand colors from Craig Clery's branding:
- Primary Yellow (45 91% 63%) - Bold, energetic brand color
- Primary Blue (211 100% 64%) - Trust-building secondary color
- Accent Coral (0 100% 71%) - Warm accent color
- Typography uses Poppins for headings and Inter for body text
- Consistent spacing system using Tailwind's spacing primitives (4, 8, 12, 16, 20, 24, 32)

**Component Architecture:**
- Modular page components (Home, About, Projects, Reviews, Contact)
- Reusable section components (HeroSection, StatsSection, ServicesSection, etc.)
- Atomic UI components from Shadcn/ui for consistency
- Component examples directory for isolated component development

**Page Structure:**
- `/` - Home page with hero, stats, and services
- `/about` - About Craig and the business
- `/projects` - Portfolio showcase with process explanation
- `/reviews` - Customer testimonials
- `/contact` - Contact form and location map

### Backend Architecture

**Server Framework:**
- Express.js with TypeScript
- RESTful API architecture (routes prefixed with `/api`)
- Development: Vite middleware for HMR
- Production: Serves static build artifacts

**Storage Layer:**
The application currently uses an in-memory storage implementation (`MemStorage`) for user data. The storage interface is designed to be swappable, allowing easy migration to a persistent database solution.

**Key Architectural Decisions:**
- Separation of concerns: client, server, and shared code directories
- TypeScript throughout for type safety
- Modular route registration pattern for scalability
- Environment-based configuration (development vs. production)

### Data Storage Solutions

**Current Implementation:**
- In-memory storage (MemStorage class) for development/demo purposes
- Simple CRUD interface defined in `IStorage`

**Configured but Not Implemented:**
- Drizzle ORM configuration present for PostgreSQL
- Schema defined for users table
- Database URL environment variable expected
- Migration directory structure in place

**Future Database Integration:**
The project is configured to support PostgreSQL through Drizzle ORM. When a database is added, the MemStorage implementation should be replaced with a Drizzle-based implementation following the same IStorage interface.

### External Dependencies

**Third-Party UI Libraries:**
- Radix UI primitives (accordion, dialog, dropdown, etc.) - Accessible component foundations
- Embla Carousel - Touch-friendly image carousels
- Lucide React - Icon library
- Class Variance Authority (CVA) - Component variant styling
- CMDK - Command palette functionality

**Form Handling:**
- React Hook Form - Form state management
- Hookform Resolvers - Validation integration
- Zod - Schema validation
- Drizzle-Zod - Database schema to Zod schema conversion

**Date Utilities:**
- date-fns - Date formatting and manipulation

**Development Tools:**
- Replit-specific plugins for development environment
- ESBuild for server bundling
- PostCSS with Autoprefixer

**Maps Integration:**
- Google Maps embed for location display (embedded iframe, no API key required for basic embedding)

**Planned Integrations:**
The design guidelines reference inspiration from premium home service websites (HomeAdvisor, Thumbtack, Houzz), suggesting the application may eventually integrate:
- Google Reviews API for authentic review display
- Contact form submission handling (currently client-side only)
- Potential CMS for project portfolio management

**Database:**
- Neon Database serverless PostgreSQL (configured but not currently used)
- Drizzle ORM for type-safe database queries
- Connect-pg-simple for PostgreSQL session storage