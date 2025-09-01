# Promptables Generated Content

Generated on: 2025-09-01 12:25:15

```markdown
# Design Guidelines for "Naughty Helper"

## 1. General Design Overview
**Purpose:** A playful, engaging app that delivers humorous or mischievous content/interactions in a safe, controlled environment, balancing fun with user trust.
**Tone & Personality:** Witty, slightly mischievous, but ultimately friendly and trustworthy. Avoids mean-spiritedness.
**User Goals:** Discover entertaining content, share lighthearted moments, customize their experience, feel a sense of playful surprise.

### 1.1 Core Design Principles
- Playful Engagement: The interface should feel fun and responsive.
- Clear Boundaries: Users should always feel in control; pranks/content are never harmful or truly embarrassing.
- Delightful Surprise: Use micro-interactions and animations to create moments of unexpected joy.

## 2. Color Scheme
**Primary (Trust/Base):** "Confident Blue" - `#4361EE` - Used for primary branding, key headers, and establishing a trustworthy base.
**Secondary (Playfulness):** "Energetic Coral" - `#FF6B6B` - Used for primary CTAs, highlights, and interactive elements to inject energy.
**Accent (Surprise):** "Vibrant Yellow" - `#FFD166` - Used sparingly for warnings, special notifications, or celebratory moments.

## 3. Typography
### 3.1 Font Family
**Primary:** Nunito Sans (A friendly, highly readable sans-serif with rounded terminals)
**Secondary:** Nunito Sans (Used consistently for hierarchy)
### 3.2 Font Weights & Hierarchy
- **H1:** 32px, 800 - Page titles
- **H2:** 24px, 700 - Section headers
- **Body:** 16px, 400 - Primary content text
- **Buttons/CTA:** 16px, 700 - All button labels

## 4. UI Components by Page
### Homepage / Content Feed
- **Layout:** Card-based feed. Large, tappable image/video preview at the top of each card with title and short description below.
- **Interactive Elements:** "Try It" button (Coral), "Save for Later" icon button, "Share" icon button.
- **Color & Behavior:** Cards have a white background with a subtle shadow. The "Try It" button is the main action. A gentle scale animation occurs on card tap.
- **Mobile-First Notes:** Single-column layout. Cards stretch full width with comfortable padding.

### Detail / Interaction Page
- **Layout:** Focused view. Media (image/video/GIF) occupies top 60% of screen. Title and description below. Action button fixed to bottom for easy access.
- **Interactive Elements:** Primary action button, back button, share button.
- **Color & Behavior:** The primary action button uses the accent yellow on this page to heighten the sense of a special, one-off action.
- **Mobile-First Notes:** Media is responsive. Fixed bottom button ensures accessibility.

## 5. Mobile UX & Accessibility
- **Navigation:** Bottom navigation bar for main sections (Home, Saved, Profile). Clear and easily reachable.
- **Tap Targets:** Minimum 44x44pt for all interactive elements.
- **Contrast:** All text meets WCAG AA minimum contrast ratios (4.5:1) against its background.
- **Feedback:** Subtle button press animations, haptic feedback on actions where appropriate (e.g., when a "prank" is activated).

## 6. Icons & Visual Style
- **Icon Set:** Rounded, line-style icons (e.g., Feather Icons or Material Symbols Rounded) for a modern, friendly feel.
- **Visual Guidelines:** Use of playful GIFs and short, silent, auto-playing videos is encouraged. Illustrations should be colorful and cartoonish. Avoid realistic photography.

## 7. Microinteractions & Animations
- **Transitions:** Smooth fade and slide transitions between pages.
- **States:** Buttons have clear pressed states (scale down slightly, background darkens).
- **Animations:** Playful, spring-based animations for success states or reveals. Purpose is to delight, not distract.

## 8. Performance Considerations
- **Optimization:** All images and videos are lazy-loaded. Videos are compressed for web. GIFs are used sparingly; video formats (MP4) are preferred for longer animations.
- **Offline:** Basic app shell is cached for offline viewing. Saved content is available offline.

## 9. Security & Privacy Design
- **Auth Experience:** Simple, social login-first (Google/Apple) with optional email. Focus on quick entry. Clear permissions asked *in context* (e.g., "Allow access to contacts to prank a friend?").
- **Data Safety:** A dedicated, easily accessible "Privacy & Safety" section in the app explains what data is collected (minimal) and how it's used. Uses simple language and icons.

### Conclusion
The design balances whimsy with clarity, ensuring users always feel safe and in control while being delighted by the app's content and interactions. The visual language is modern, friendly, and performance-conscious.
```

```markdown
# Master Plan: Naughty Helper

## App Overview & Objectives
- **Purpose:** To provide a platform for discovering and sharing lighthearted, humorous digital pranks and interactions in a safe and consensual environment.
- **Target Audience:** Adults (18-35) looking for fun ways to interact with friends digitally, and content creators interested in the "prank" genre.

## Core Features & Functionality
- Curated feed of interactive "pranks" (e.g., fake notification generators, screen takeover gags, harmless friend challenges)
- User profiles to save favorite pranks
- Social sharing and friend challenges
- Content creation wizard (for power users)

## High-Level Technical Stack
- **Frontend:** Next.js (App Router) for SSR, SEO, and excellent React performance.
- **Backend & Database:** Supabase for real-time database, authentication, and serverless functions.
- **Authentication:** Supabase Auth with Google OAuth and Email/Password.
- **CMS:** Sanity.io for managing the curated feed of prank content (allows non-devs to add new content).

## Conceptual Data Model
- `Users` (id, auth_id, username, ...)
- `Pranks` (id, title, description, content_url, created_by, ...)
- `UserSavedPranks` (junction table for favorites)
- `UserActivity` (log of pranks used, shared, etc.)

## User Interface Principles
- Mobile-first, gesture-driven design focused on delight and ease of use.

## Security Considerations
- All user-generated content and interactions must be vetted to prevent abuse. Supabase RLS (Row Level Security) will be crucial for data isolation.

## Development Phases
- **MVP:** Curated feed, basic prank interaction, social sharing, user auth.
- **V1:** User profiles, "Saved" functionality, enhanced creation tools, basic analytics.
- **V2:** Friend system, push notifications for challenges, advanced content creator platform.

## Potential Challenges & Solutions
- **Challenge:** Ensuring content is truly safe and consensual.
  - **Solution:** Implement a robust reporting/moderation system from day one. Start with a pre-vetted, curated feed.
- **Challenge:** Performance of media-heavy interactions.
  - **Solution:** Leverage Next.js image optimization and serve videos from a optimized CDN.
```
```markdown
# Implementation Plan

## Phase 1: MVP
1.  Set up Next.js project with TypeScript and Tailwind CSS.
2.  Configure Supabase project, database schema, and authentication.
3.  Integrate Sanity.io CMS and define the content model for `Pranks`.
4.  Build the main feed, pulling and displaying data from Sanity.
5.  Implement basic prank interaction pages (static examples first).
6.  Build authentication flows (Login/Signup).
7.  Implement social sharing (using `next-share` or similar).

## Phase 2: V1 Launch
1.  Develop user profile pages and "Save for Later" functionality.
2.  Build the core of the content creation wizard.
3.  Implement basic analytics (e.g., using Supabase for simple event tracking).
4.  Conduct closed beta testing and gather feedback.

## Team & Tools Recommendations
- A solo full-stack developer can build the MVP focusing on front-end and leveraging BaaS (Supabase).
- **Key Tools:** Vercel (hosting), Supabase (BaaS), Sanity.io (CMS), Tailwind CSS (styling).
```
```markdown
# Design Guidelines

## Visual Style
- **Primary Font:** Nunito Sans
- **Color Palette:**
  - Primary: `#4361EE`
  - Accent: `#FF6B6B`
  - Secondary: `#FFD166`
- **Layout Approach:** Mobile-first, card-based layout using CSS Grid/Flexbox.

## Accessibility
- **Target Compliance:** WCAG 2.1 AA
- **Tap Target Size:** Minimum 44x44px
- **Focus States:** Clearly visible focus rings for keyboard navigation (`:focus-visible`).
```
```markdown
# App Flow: Pages & User Roles

## User Roles
- **User:** Can browse feed, interact with pranks, save favorites, share content.
- **Content Creator (Future):** Can submit pranks for review, view performance metrics.

## Page Definitions
- **Homepage (/):** The main feed of curated pranks.
- **Prank Detail (/prank/[id]):** The page to view and interact with a specific prank.
- **Profile (/profile):** User's saved pranks and activity history.
- **Auth (Login/Signup):** Modal or dedicated page for authentication.

## User Journeys
- **New User:** Lands on homepage -> Browses feed -> Clicks a prank -> Reads details -> Uses "Try It" -> Prompted to sign up/share -> Creates account -> interaction completes -> Returns to feed.
- **Returning User:** Logs in -> Checks feed or goes directly to saved items -> Shares a prank with a friend.
```

---
*Generated by Promptables Platform*
