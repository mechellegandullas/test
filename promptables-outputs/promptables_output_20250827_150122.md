# Promptables Generated Content

Generated on: 2025-08-27 15:01:22

## Canvas Output

```markdown
# Design Guidelines for Hearth

## 1. General Design Overview
**Purpose:** To provide a secure, ad-free, and effortless platform for small, intimate groups like families and close friends to privately share life's moments.
**Tone & Personality:** Warm, trustworthy, simple, and approachable. The design should feel like a digital extension of a cozy living room.
**User Goals:** Easily share photos and updates with a select group, communicate privately without fear of data exploitation, and maintain connections with loved ones in a low-friction environment.

### 1.1 Core Design Principles
- **Clarity:** The interface should be immediately understandable, even for non-technical users.
- **Trust:** Every design decision should reinforce the user's sense of privacy and security.
- **Warm Minimalism:** A clean, uncluttered interface that uses soft shapes and a warm color palette to feel inviting, not cold or corporate.

## 2. Color Scheme
**Primary (Passion):** `#E11D48` - Used for primary buttons, key interactive elements, and icons to draw attention to actions that connect people.
**Secondary (Trust):** `#0EA5E9` - Used for links, secondary information, and highlights to evoke a sense of reliability and clarity.
**Neutral (Background):** `#FFFFFF`, `#F9FAFB`, `#F3F4F6` - Used for backgrounds, cards, and UI elements to create a clean, light, and airy canvas.
**Neutral (Text):** `#111827` (primary text), `#374151` (secondary text) - For high-contrast, accessible readability.

## 3. Typography
### 3.1 Font Family
**Primary:** Inter
**Secondary:** Inter (Using different weights for hierarchy)
### 3.2 Font Weights & Hierarchy
- **H1:** `2rem (32px)`, `Semibold (600)` - Page titles and major headings.
- **H2:** `1.5rem (24px)`, `Semibold (600)` - Section headings.
- **H3:** `1.25rem (20px)`, `Semibold (600)` - Sub-section headings and post author names.
- **Body:** `1rem (16px)`, `Regular (400)` - Primary body text for posts and comments.
- **Meta/Secondary:** `0.875rem (14px)`, `Regular (400)` - Timestamps, minor information.
- **Buttons/CTA:** `1rem (16px)`, `Medium (500)` - All button text for clear action cues.

## 4. UI Components by Page
### Onboarding & Authentication
- **Layout:** Single-column, centered card layout on a soft gray (`#F9FAFB`) background. Minimal fields per screen.
- **Interactive Elements:** Large, friendly input fields, a prominent `#E11D48` "Continue" button, and a clear "Copy Invite Link" component for the Circle Admin.
- **Color & Behavior:** Use the `#0EA5E9` blue for the privacy policy link. Success states (e.g., link copied) should provide clear, positive feedback.
- **Mobile-First Notes:** Full-viewport height steps. Inputs and buttons are full-width with comfortable tap targets.

### The Circle Feed (Homepage)
- **Layout:** A single, endless-scroll column of content cards. A floating action button (FAB) in `#E11D48` for creating a new post.
- **Interactive Elements:** Post cards, FAB, heart icon (`#E11D48` on tap), comment icon, user avatars.
- **Color & Behavior:** Post cards have a white background with a subtle shadow for depth. The heart icon fills with color immediately on tap to provide satisfying feedback.
- **Mobile-First Notes:** Cards span nearly the full width with generous padding. The FAB is fixed to the bottom right for easy thumb access.

### E2E Encrypted Group Messaging
- **Layout:** Classic messaging UI: a header bar, a scrollable message list (newest at bottom), and a fixed message input at the bottom.
- **Interactive Elements:** Message bubbles, text input, send button.
- **Color & Behavior:** User's messages are on the right in `#0EA5E9` (lightened to `#E0F2FE` for the bubble, dark text). Others' messages are on the left in `#F3F4F6` (light gray). A small lock icon is subtly displayed in the header to constantly reinforce the encrypted status.
- **Mobile-First Notes:** Optimize for one-handed typing. The message input bar sticks to the virtual keyboard.

### Circle Members & Profiles
- **Layout:** A simple grid (2-3 across on mobile) of user avatar circles and names.
- **Interactive Elements:** Tappable user cards that lead to a minimalist profile view (avatar, name, maybe a bio field).
- **Color & Behavior:** Clean and functional. The Admin should have a subtle badge (`#E11D48` outline).
- **Mobile-First Notes:** Grid auto-adjusts for different screen sizes.

## 5. Mobile UX & Accessibility
- **Navigation:** Bottom navigation bar (iOS-like) with 3-4 key tabs: Feed, Messages, Circle, Profile.
- **Tap Targets:** All interactive elements maintain a minimum size of 44x44pt.
- **Contrast:** All text meets WCAG AA minimum contrast ratios (4.5:1 for normal text). Primary button (`#E11D48` on white) is 4.6:1.
- **Feedback:** All buttons and tappable elements have a slight opacity change or scale transformation on press. Toasts are used for system feedback (e.g., "Post published").

## 6. Icons & Visual Style
- **Icon Set:** Rounded, line-style icons (e.g., Feather Icons, Lucide) to match the soft, friendly aesthetic. Consistent stroke width of 1.5-2px.
- **Visual Guidelines:** User-uploaded photos and videos are the primary visual content. The UI should frame this content without competing with it. Avoid stock photography.

## 7. Microinteractions & Animations
- **Transitions:** Subtle fade and slide animations between pages for a connected, fluid feeling.
- **States:** Buttons have clear `:hover`, `:active`, and `:focus` states (slight darkening/lightening and a focus ring for accessibility).
- **Animations:** A simple, smooth loading skeleton animation for the feed. The FAB should have a gentle pulsing effect when first arriving on the feed to hint at its function.

## 8. Performance Considerations
- **Optimization:** All user-uploaded images are automatically compressed and converted to modern formats (WebP) before being encrypted and stored. Implement lazy loading for images in the feed.
- **Offline:** The app will cache previously loaded feed posts and messages. A small indicator will show "Offline" or "Connecting..." if the network is unavailable. New posts composed offline are queued.

## 9. Security & Privacy Design
- **Auth Experience:** The login/signup flow is simple but serious. The value prop of privacy is stated upfront. The process of joining via an encrypted invite link is a key part of the UX that builds trust.
- **Data Safety:** The UI must communicate security transparently. This includes:
    - A persistent, subtle lock icon in the messaging header.
    - A clear, simple explanation of End-to-End Encryption during onboarding ("Only you and your circle can read your messages. Not even us.").
    - A dedicated "Privacy & Security" section in the user profile settings.

### Conclusion
The design of Hearth must first and foremost build trust through clarity and transparency. Its warmth and simplicity should make users feel comfortable and focused on their connections, not the technology. Every pixel should align with the core mission of creating a private digital hearth for loved ones.
```

---

## Blueprint Output

```markdown
# Master Plan: Hearth

## App Overview & Objectives
- **Purpose:** To provide a private, secure, and ad-free platform for small intimate groups to effortlessly share life's moments without compromising their privacy.
- **Target Audience:** Families, close-knit friend groups, and small communities prioritizing privacy over public visibility.

## Core Features & Functionality
- Private Circle creation with secure invite links
- End-to-end encrypted feed for posts, photos, and videos
- E2E encrypted group messaging within Circles
- Simple user profiles and Circle member management
- Mobile-optimized responsive web interface

## High-Level Technical Stack
- **Frontend:** Next.js 14 with App Router, Tailwind CSS
- **Backend & Database:** Supabase (PostgreSQL) for auth and metadata
- **Authentication:** Email/password with Circle invite validation
- **Encryption:** Client-side libsodium-wrappers for E2E encryption
- **Storage:** Supabase Storage for encrypted media files

## Conceptual Data Model
- Users belong to one or more Circles (premium feature)
- Circles contain Posts, Messages, and Media, all encrypted client-side
- Invite links are cryptographically secure and single-use
- User metadata (names, avatars) stored unencrypted for display purposes

## User Interface Principles
- Mobile-first responsive design with warm, approachable aesthetics
- Minimalist interface that prioritizes content over UI elements
- Intuitive navigation with clear visual hierarchy

## Security Considerations
- Zero-knowledge architecture: Server never sees unencrypted user content
- Client-side encryption for all user-generated content
- Secure invite system prevents unauthorized Circle access
- Regular security audits and penetration testing required

## Development Phases
- **MVP:** Single Circle functionality, basic feed, E2E messaging, media sharing
- **V1:** Premium features (multiple Circles, increased storage, custom reactions)
- **V2:** Advanced features like event planning, shared calendars, memory highlights

## Potential Challenges & Solutions
- **E2E Encryption Complexity:** Use established libsodium library with thorough documentation
- **User Onboarding Friction:** Streamlined invite process with clear instructions
- **Cross-Device Sync:** Implement secure key management system for multiple devices
```

```markdown
# Implementation Plan

## Phase 1: MVP
1.  Set up Next.js project with TypeScript and Tailwind CSS
2.  Configure Supabase project with authentication and database schema
3.  Implement secure invite system with cryptographic link generation
4.  Build client-side encryption layer using libsodium-wrappers
5.  Create Circle feed with post creation and media upload functionality
6.  Implement E2E encrypted messaging system within Circles
7.  Develop user profiles and Circle member management interface
8.  Test encryption implementation and security measures thoroughly

## Phase 2: V1 Launch
1.  Implement premium subscription system with Stripe integration
2.  Add multiple Circles functionality for premium users
3.  Develop advanced storage management tools
4.  Create custom emoji reaction system
5.  Implement basic event planning features
6.  Add comprehensive onboarding tutorials and help documentation

## Team & Tools Recommendations
- **Core Team:** Full-stack developer, UI/UX designer, security specialist
- **Key Tools:** Vercel for deployment, Stripe for payments, Sentry for error monitoring
- **Development Approach:** Agile methodology with 2-week sprints, focus on security testing
```

```markdown
# Design Guidelines

## Visual Style
- **Primary Font:** Inter (Google Fonts)
- **Color Palette:**
  - Primary: `#E11D48` (warm pink/red for CTAs and accents)
  - Accent: `#0EA5E9` (trustworthy blue for links and highlights)
  - Background: `#FFFFFF`, `#F9FAFB`, `#F3F4F6` (clean whites and soft grays)
- **Layout Approach:** Mobile-first, card-based design with generous whitespace
- **Border Radius:** 8px for cards, 6px for buttons (soft, approachable feel)

## Accessibility
- **Target Compliance:** WCAG AA
- **Tap Target Size:** Minimum 44px for interactive elements
- **Color Contrast:** Ensure 4.5:1 ratio for text and interactive elements
- **Screen Reader Support:** Semantic HTML structure with proper ARIA labels
- **Reduced Motion:** Respect user preference for animations and transitions
```

```markdown
# App Flow: Pages & User Roles

## User Roles
- **Circle Admin:** Creates Circle, manages invites, can remove members (first user who creates Circle)
- **Circle Member:** Can view feed, post content, message, view other members (all invited users)
- **Premium Member:** Additional features like multiple Circles, increased storage (upgraded members)

## Page Definitions
- **Landing Page:** Simple value proposition, login/signup, privacy promise highlight
- **Onboarding Flow:** Email signup, Circle creation or join via invite link, profile setup
- **Circle Feed:** Main homepage showing chronological posts from Circle members
- **Messaging View:** Dedicated tab for E2E encrypted group messaging within Circle
- **Members Page:** List of all Circle members with basic profile information
- **Settings:** User preferences, account management, subscription upgrade

## User Journeys
- **New User:** Landing → Signup → Create/Join Circle → Profile Setup → Feed
- **Existing User:** Login → Feed (default view) → Switch between Feed/Messaging/Members
- **Circle Admin:** Additional access to invite management and member removal in Settings
- **Premium User:** Access to multiple Circles switcher and advanced features
```

---
*Generated by Promptables Platform*
