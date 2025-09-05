# Promptables Generated Content

Generated on: 2025-09-05 01:59:32

## Canvas Output

# Design Guidelines for Perfume Cyclopedia

## 1. General Design Overview
**Purpose:** To create a trusted, community-driven resource for fragrance discovery, enabling users to find, review, and discuss perfumes based on real-user experiences regarding performance, longevity, and occasion appropriateness.
**Tone & Personality:** Authoritative yet welcoming, sophisticated yet accessible, trustworthy, and community-focused.
**User Goals:** Discover new fragrances, share personal reviews and insights, track personal scent preferences, find the perfect scent for any occasion, and connect with a community of like-minded enthusiasts.

### 1.1 Core Design Principles
- **Clarity:** Information is presented in a scannable, digestible manner. The user should never feel overwhelmed by data.
- **Minimalism:** A clean, uncluttered interface that puts the focus squarely on the fragrances and community content. Decoration is secondary to function.
- **Trust:** The design must foster a sense of credibility and reliability, emphasizing community-driven data and transparent reviews.

## 2. Color Scheme
**Primary (Violet Majesty):** `#7C3AED` - Used for primary buttons, key interactive elements, and highlights. Evokes luxury, creativity, and sophistication.
**Secondary (Emerald Fresh):** `#10B981` - Used for positive actions, success states, ratings, and accents. Suggests freshness, nature, and quality.
**Neutral (Slate Text):** `#1F2937` - Used for all primary body text and headings for maximum readability.
**Neutral (Cloud Background):** `#F9FAFB` - Used for main page backgrounds and card insets to create a light, airy, and clean canvas.

## 3. Typography
### 3.1 Font Family
**Primary:** Inter
**Secondary:** Inter (Maintaining a single, highly-readable typeface supports the minimalist principle.)

### 3.2 Font Weights & Hierarchy
- **H1:** 32px, Semibold (600) - Page titles and major headings.
- **H2:** 24px, Semibold (600) - Section headers (e.g., "Community Reviews").
- **H3:** 20px, Semibold (600) - Sub-section headers and perfume names.
- **Body:** 16px, Regular (400) - Primary content and review text.
- **Small/Meta:** 14px, Regular (400) - Supporting information, labels, and timestamps.
- **Buttons/CTA:** 16px, Medium (500) - All button text for clear action cues.

## 4. UI Components by Page

### Homepage
- **Layout:** Single-column layout on mobile, transitioning to a multi-column grid for featured sections on desktop. Hero section at top, followed by vertically stacked content sections with ample whitespace.
- **Interactive Elements:** Prominent search bar, "Browse by Occasion" chip buttons, perfume cards (image, name, rating), "See All Reviews" CTA.
- **Color & Behavior:** The hero search bar uses a white background with a subtle border. `Violet Majesty` is used for the search button and primary CTAs. `Emerald Fresh` highlights ratings. Cards have a subtle shadow on hover to indicate interactivity.
- **Mobile-First Notes:** The hero tagline may stack above the search bar on very small screens. The "Browse by Occasion" chips will scroll horizontally. Content sections stack vertically.

### Fragrance Directory / Search & Filter Page
- **Layout:** Top-aligned sticky header with search and filter controls. Results displayed in a responsive grid below. Filters can be a dismissible sheet on mobile or a left sidebar on desktop.
- **Interactive Elements:** Search input, filter toggles (Brand, Scent Family, etc.), "Apply Filters" button, grid/list view toggle, pagination controls.
- **Color & Behavior:** Active filters are tagged with `Violet Majesty`. The "Apply" button is a primary button. The grid/list toggle uses outlined icons. The results grid uses the same card component as the homepage.
- **Mobile-First Notes:** The filter panel is a full-bottom-sheet or modal. The view toggle and sort options are in the sticky header bar.

### Individual Perfume Page
- **Layout:** Scrollable single-column layout. Key details at the top, followed by a horizontal scroller for community ratings, then the review submission form, and finally the list of user reviews.
- **Interactive Elements:** Affiliate link buttons, "Write a Review" form elements (rating sliders, textarea, submit button), review voting buttons.
- **Color & Behavior:** Affiliate links are styled as secondary buttons (`Slate Text` on a `Cloud Background` with a border) to distinguish them from primary actions. The review form is revealed upon clicking a CTA. The "Occasion Appropriateness" section uses horizontal progress bars in `Emerald Fresh`.
- **Mobile-First Notes:** The perfume image is full-width at the top. The occasion tags and ratings are stacked. The review form is simplified for small screens.

### User Profiles
- **Layout:** Profile header with avatar and stats, followed by a tabbed interface for "Reviews" and "Favorites".
- **Interactive Elements:** Follow button, tabs, review cards.
- **Color & Behavior:** The "Follow" button toggles its state (outlined when not following, solid `Violet Majesty` when following). The active tab is underlined with `Violet Majesty`.
- **Mobile-First Notes:** Profile stats are stacked. The tab bar can scroll horizontally if needed.

### Community / Reviews Feed
- **Layout:** A continuous feed of review cards, each containing the user info, perfume info, and review text.
- **Interactive Elements:** Review cards, like/helpful buttons.
- **Color & Behavior:** This page is content-first. Interaction is minimal, with `Emerald Fresh` used for the "Helpful" button counts.
- **Mobile-First Notes:** Standard vertical scroll feed.

## 5. Mobile UX & Accessibility
- **Navigation:** Bottom navigation bar on mobile for key app sections (Home, Search, Community, Profile).
- **Tap Targets:** All interactive elements maintain a minimum size of 44x44pt.
- **Contrast:** All text-to-background contrast ratios meet or exceed WCAG AA standards (4.5:1 for body text).
- **Feedback:** All buttons and tappable elements have clear :active states (e.g., slight darkening or scaling) to provide immediate tactile feedback.

## 6. Icons & Visual Style
- **Icon Set:** Use a consistent line icon set (e.g., Lucide or Heroicons) with a 2px stroke weight and rounded end caps/corners to match the modern, clean aesthetic.
- **Visual Guidelines:** Perfume images must be high-quality, on a consistent white or neutral background. User-generated photos in reviews should be cropped to a standard aspect ratio (e.g., 1:1). Avoid decorative illustrations; use icons and whitespace for visual rhythm.

## 7. Microinteractions & Animations
- **Transitions:** Page transitions are swift and minimal (e.g., fade). In-page transitions (like revealing a form) use a subtle slide-up or fade-in.
- **States:** Interactive elements have clear hover, focus, and active states, typically involving a change in background color (`bg-primary/10` for hover) or a slight elevation increase.
- **Animations:** Used sparingly and functionally. Examples: a subtle glow on a submitted review, a smooth scroll after applying filters, a loading skeleton screen for content.

## 8. Performance Considerations
- **Optimization:** All perfume images must be modern formats (WebP/AVIF) served responsively (e.g., using `next/future/image`). Implement lazy loading for images and below-the-fold content.
- **Offline:** Core app shell is cached via a service worker for instant reloads. Recently viewed perfume pages are cached for offline reading.

## 9. Security & Privacy Design
- **Auth Experience:** The login/signup modal is simple and clear, offering Email and "Continue with Google" as equally prominent options. Clearly explain why an email is needed (to protect community quality).
- **Data Safety:** Privacy settings are easily accessible from the profile. The UI uses clear language to explain what data is public (reviews) and what is private (email). A shield icon and simple language convey security around authentication.

### Conclusion
The design for Perfume Cyclopedia must consistently project an image of a premium, trustworthy, and inclusive community hub. Every design decision, from the luxurious color palette to the clean typography and intuitive layout, should serve the core mission of making fragrance discovery effortless and reliable. The experience should feel elevated yet entirely frictionless for both new users and seasoned experts.

---

## Blueprint Output

```markdown
# Master Plan: Perfume Cyclopedia

## App Overview & Objectives
- **Purpose:** Create a trusted community-driven platform where fragrance enthusiasts can discover, review, and discuss perfumes based on real-user experiences for performance, longevity, and occasion appropriateness.
- **Target Audience:** Perfume newbies seeking guidance, seasoned collectors tracking their opinions, and everyday users looking for reliable scents for specific occasions.

## Core Features & Functionality
- Community fragrance reviews with ratings for sillage, longevity, and overall experience
- Advanced search and filtering by scent notes, brand, occasion, and ratings
- User profiles with review history and favorite perfumes
- Social features including user following and community feed
- Affiliate integration for monetization through retailer partnerships

## High-Level Technical Stack
- **Frontend:** Next.js 14 with TypeScript
- **Backend & Database:** Supabase for real-time data, authentication, and storage
- **Authentication:** Email/password with Google OAuth integration
- **CMS:** Supabase tables managed through admin dashboard for content management

## Conceptual Data Model
- Users (profiles, authentication)
- Perfumes (brand, name, scent notes, images)
- Reviews (ratings, written content, user associations)
- Occasions and Scent Families (taxonomy for categorization)
- User relationships (following, favorites)

## User Interface Principles
- Mobile-first responsive design with clean, minimalist aesthetic
- Card-based layout with ample whitespace for easy scanning
- Intuitive navigation focused on discovery and community engagement

## Security Considerations
- Secure user authentication and authorization through Supabase
- Data validation and sanitization for user-generated content
- Privacy-focused approach to user data and review information

## Development Phases
- **MVP:** Core fragrance directory, basic search, user reviews, and authentication
- **V1:** Advanced filtering, user profiles, social features, and affiliate integration
- **V2:** AI scent finder wizard, enhanced community features, and mobile app

## Potential Challenges & Solutions
- **Content Moderation:** Implement automated filtering and community reporting system
- **Database Scalability:** Leverage Supabase's scalable architecture with proper indexing
- **User Engagement:** Gamification elements and community building features to encourage active participation
```

```markdown
# Implementation Plan

## Phase 1: MVP (4-6 weeks)
1. Set up Next.js project with TypeScript and Tailwind CSS configuration
2. Configure Supabase project with initial database schema for users, perfumes, and reviews
3. Implement authentication system with email/password and Google OAuth
4. Build core fragrance directory with basic search functionality
5. Create individual perfume pages with review display and submission
6. Develop homepage with featured content and trending perfumes
7. Implement basic user profiles with review history

## Phase 2: V1 Launch (3-4 weeks)
1. Add advanced filtering system for scent notes, occasions, and ratings
2. Implement user following system and community feed
3. Integrate affiliate linking system for major retailers
4. Add favorite perfumes functionality to user profiles
5. Implement ad slot integration for non-intrusive monetization
6. Enhance search with autocomplete and suggestion features
7. Add comprehensive testing and performance optimization

## Phase 3: V2 Features (4-6 weeks)
1. Develop AI Scent Finder wizard with questionnaire-based recommendations
2. Implement advanced community features (discussion forums, groups)
3. Add mobile app using React Native or progressive web app enhancements
4. Integrate social sharing and referral system
5. Develop admin dashboard for content moderation and analytics

## Team & Tools Recommendations
- **Frontend Developer:** Next.js, TypeScript, Tailwind CSS expertise
- **Backend Developer:** Supabase, PostgreSQL, real-time data experience
- **Designer:** UI/UX focus on community platforms and e-commerce
- **Content Manager:** For initial perfume database population and moderation

**Key Tools:**
- Vercel for deployment and hosting
- Supabase for backend services
- Google AdSense for advertising
- Amazon Associates for affiliate linking
- Sentry for error tracking
```

```markdown
# Design Guidelines

## Visual Style
- **Primary Font:** Inter for clean, modern readability
- **Color Palette:**
  - Primary: `#7C3AED` (Sophisticated purple for luxury and creativity)
  - Accent: `#10B981` (Fresh green for accents and calls-to-action)
  - Text: `#1F2937` (Dark gray for primary text)
  - Background: `#F9FAFB` (Light gray for clean backgrounds)
  - Secondary: `#6B7280` (Medium gray for secondary text and elements)
- **Layout Approach:** Mobile-first, card-based design with generous whitespace

## Component Design Principles
- **Cards:** Rounded corners, subtle shadows, consistent spacing
- **Buttons:** Clear hierarchy with primary, secondary, and ghost variants
- **Forms:** Clean, accessible inputs with clear validation states
- **Navigation:** Simple, intuitive menu structure with clear current state indicators

## Accessibility
- **Target Compliance:** WCAG AA standards
- **Tap Target Size:** Minimum 44px for interactive elements
- **Color Contrast:** Ensure 4.5:1 ratio for text and interactive elements
- **Keyboard Navigation:** Full keyboard accessibility throughout the application
- **Screen Reader Support:** Semantic HTML and proper ARIA labels

## Interaction Design
- **Loading States:** Skeleton screens for content loading
- **Transitions:** Subtle animations for page transitions and interactions
- **Feedback:** Clear visual feedback for user actions (success, errors, warnings)
- **Microinteractions:** Thoughtful animations for enhancing user experience

## Content Strategy
- **Tone:** Knowledgeable yet approachable, welcoming to all expertise levels
- **Hierarchy:** Clear information architecture with scent information as priority
- **Imagery:** High-quality perfume bottle photos with consistent styling
```

```markdown
# App Flow: Pages & User Roles

## User Roles
- **Guest User:** Browse perfumes, read reviews, use basic search
- **Authenticated User:** Submit reviews, create profile, save favorites, follow other users
- **Admin:** Manage content, moderate reviews, update perfume database, manage taxonomy

## Page Definitions
- **Homepage:** Entry point with hero search, featured perfumes, occasion browsing, and recent reviews
- **Fragrance Directory:** Comprehensive search and filter interface with grid/list views
- **Perfume Detail Page:** Individual scent presentation with details, community ratings, reviews, and affiliate links
- **User Profile:** Public profile showing review history, favorites, and follower count
- **Community Feed:** Chronological feed of recent reviews from across the platform
- **Search Results:** Filtered perfume listings based on user queries and selections
- **Authentication Pages:** Login, registration, and password management flows

## User Journeys
- **New User Discovering Scents:**
  Homepage → Search/Filters → Perfume Page → Read Reviews → Register to Save Favorites

- **Seasoned Collector Sharing Knowledge:**
  Login → Perfume Search → Submit Review → Check Profile → Follow Other Experts → Community Feed

- **Everyday User Finding Occasion Scents:**
  Homepage → Browse by Occasion → Filter Results → Read Reviews → Check Affiliate Links

- **Admin Managing Content:**
  Login → Admin Dashboard → Moderate Reviews → Update Perfume Data → Manage Taxonomy → Analytics

## Key User Flows
- **Review Submission:** Perfume Page → Click "Add Review" → Rating Input → Written Review → Submit → Confirmation
- **Advanced Search:** Directory Page → Apply Filters → View Results → Refine Search → Select Perfume
- **Social Interaction:** User Profile → Click Follow → See Their Reviews in Personalized Feed
- **Affiliate Conversion:** Perfume Page → Click Retailer Link → External Site → Purchase → Commission Tracking

## Navigation Structure
- **Primary Navigation:** Home, Browse, Community, Search
- **Secondary Navigation:** User Menu (Profile, Settings, Logout)
- **Footer Navigation:** About, Contact, Privacy, Terms
- **Contextual Navigation:** Breadcrumbs, related perfumes, popular searches
```

---
*Generated by Promptables Platform*
