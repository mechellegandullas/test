# Promptables Generated Content

Generated on: 2025-08-27 14:33:10

```markdown
# Design Guidelines for Hearth

## 1. General Design Overview
**Purpose:** A private social networking app for families and close friends to share moments securely without data mining or advertising. End-to-end encryption ensures only intended recipients see content.
**Tone & Personality:** Warm, trustworthy, intimate, and simple. Feels like a digital family hearth rather than a social media platform.
**User Goals:** Securely share photos/videos with loved ones, create private groups for different circles, maintain genuine connections without algorithmic interference.

### 1.1 Core Design Principles
- Privacy by Design: Security features are visible and understandable
- Emotional Warmth: Design evokes feelings of closeness and comfort
- Simplicity: Minimalist interface that's easy for all ages to use
- Intimacy: Visual design reinforces small-group sharing concept

## 2. Color Scheme
**Primary:** Hearth Orange - #FF6B35 - Primary buttons, key actions, warmth indicator
**Secondary:** Charcoal Gray - #2D3142 - Backgrounds, text, neutral elements
**Accent:** Soft White - #F8F5F2 - Cards, content backgrounds, clean contrast
**Success:** Forest Green - #4CAF50 - Confirmation states, positive actions

## 3. Typography
### 3.1 Font Family
**Primary:** Inter (Clean, readable, warm sans-serif)
**Secondary:** System default fallbacks

### 3.2 Font Weights & Hierarchy
- **H1:** 24px, Semibold (600) - Group names, main headings
- **H2:** 20px, Medium (500) - Section headers
- **Body:** 16px, Regular (400) - Primary content text
- **Small:** 14px, Regular (400) - Metadata, captions
- **Buttons/CTA:** 16px, Semibold (600) - Action buttons

## 4. UI Components by Page

### Group Selection Screen
- **Layout:** Grid of circular group avatars with names below, floating action button for creating new groups
- **Interactive Elements:** Group cards (tap to enter), + FAB for new group creation
- **Color & Behavior:** Warm orange FAB, gray background, group avatars use warm palette
- **Mobile-First Notes:** 2-column grid on mobile, 3-4 columns on tablet

### Group Feed
- **Layout:** Chronological feed of posts, sticky header with group info and options
- **Interactive Elements:** Like hearts, comment bubbles, share button, new post FAB
- **Color & Behavior:** Posts as cards on white background, interactions use orange accents
- **Mobile-First Notes:** Infinite scroll, optimized image loading for mobile data

### Post Creation
- **Layout:** Full-screen modal with media picker, caption field, and group selection
- **Interactive Elements:** Media upload, text input, privacy toggle, post button
- **Color & Behavior:** Clean minimal interface, orange primary action button
- **Mobile-First Notes:** Native camera/gallery integration, optimized for mobile workflows

## 5. Mobile UX & Accessibility
- **Navigation:** Bottom tab bar for main navigation, contextual headers
- **Tap Targets:** Minimum 44px touch targets for all interactive elements
- **Contrast:** AA compliance minimum (4.5:1 for text), high contrast mode support
- **Feedback:** Subtle haptics for actions, clear loading states, success confirmations

## 6. Icons & Visual Style
- **Icon Set:** Rounded line icons with warm, friendly appearance
- **Visual Guidelines:** Authentic photography only (no stock), rounded corners on all containers
- **Avatar Style:** Circular avatars with gradient backgrounds for groups without images

## 7. Microinteractions & Animations
- **Transitions:** Smooth fade transitions between screens, gentle scale animations
- **States:** Subtle opacity changes for pressed states, clear focus indicators
- **Animations:** Loading spinners, success checkmarks, gentle page transitions

## 8. Performance Considerations
- **Optimization:** Progressive image loading, lazy loading for feeds, optimized asset delivery
- **Offline:** Cached recent posts and media, queue for posting when connection resumes

## 9. Security & Privacy Design
- **Auth Experience:** Clean login with clear privacy policy, biometric authentication options
- **Data Safety:** Visual indicators of encryption status, clear explanations of privacy features
- **Permissions:** Contextual permission requests with clear value explanations

### Conclusion
Hearth's design prioritizes emotional warmth and absolute privacy. The interface should feel like a digital extension of family gatherings—comfortable, secure, and free from the performative pressure of public social media. Every design decision reinforces trust and intimacy.

```markdown
# Master Plan: Hearth

## App Overview & Objectives
- **Purpose:** Create a private, encrypted social platform for families and close friends to share moments without data mining or advertising
- **Target Audience:** Families with dispersed members, close friend groups, privacy-conscious individuals seeking authentic connection

## Core Features & Functionality
- End-to-end encrypted group messaging and media sharing
- Private group creation with invitation-only access
- Chronological, algorithm-free feed
- Mobile-first responsive design
- Secure media storage and sharing

## High-Level Technical Stack
- **Frontend:** Next.js with React Native for mobile
- **Backend & Database:** Supabase with PostgreSQL
- **Authentication:** Email + optional social OAuth with biometric fallback
- **Encryption:** libsodium for client-side E2E encryption

## Conceptual Data Model
- Users → Groups (many-to-many)
- Groups → Posts (one-to-many)
- Posts → Comments/Likes (one-to-many)
- All content encrypted at rest and in transit

## User Interface Principles
- Mobile-first, warm and accessible design
- Privacy indicators throughout interface
- Minimalist approach focusing on content

## Security Considerations
- Zero-knowledge architecture: server never sees unencrypted content
- Client-side key management and encryption
- Regular security audits and penetration testing

## Development Phases
- **MVP:** Basic group creation, E2E encrypted posts, mobile app
- **V1:** Media optimization, advanced sharing controls, web version
- **V2:** Family features (calendar, polls), enhanced media management

## Potential Challenges & Solutions
- **E2E Encryption Complexity:** Use established cryptographic libraries with thorough testing
- **Cross-platform Sync:** Implement robust conflict resolution and offline-first design
- **User Onboarding:** Create intuitive security setup flows for non-technical users
```

```markdown
# Implementation Plan

## Phase 1: MVP (Weeks 1-6)
1.  Set up Next.js project with TypeScript and Tailwind CSS
2.  Configure Supabase project with database schema and Row Level Security
3.  Implement authentication system with email and social providers
4.  Build group creation and management system
5.  Develop E2E encryption framework for posts and messages
6.  Create basic feed interface and post creation flow
7.  Implement mobile app shell using React Native

## Phase 2: V1 Launch (Weeks 7-12)
1.  Add media upload and optimization pipeline
2.  Implement comments and reactions system
3.  Build web version and ensure responsive design
4.  Add advanced privacy controls and settings
5.  Implement offline capability and sync system
6.  Conduct security audit and penetration testing

## Team & Tools Recommendations
- **Core Team:** Full-stack developer, mobile specialist, security consultant
- **Key Tools:** GitHub for version control, Vercel for deployment, Sentry for error tracking
- **Testing:** Jest for unit tests, Cypress for E2E testing, BrowserStack for cross-device testing
```

```markdown
# Design Guidelines

## Visual Style
- **Primary Font:** Inter
- **Color Palette:**
  - Primary: `#FF6B35` (Hearth Orange)
  - Secondary: `#2D3142` (Charcoal Gray)
  - Background: `#F8F5F2` (Soft White)
  - Success: `#4CAF50` (Forest Green)
- **Layout Approach:** Mobile-first, card-based design with generous whitespace

## Accessibility
- **Target Compliance:** WCAG AA
- **Tap Target Size:** Minimum 44px
- **Contrast Ratio:** Minimum 4.5:1 for text elements
- **Screen Reader Support:** Full ARIA labels and semantic HTML
- **Reduced Motion:** Support for prefers-reduced-motion
```

```markdown
# App Flow: Pages & User Roles

## User Roles
- **Standard User:** Can create groups, post content, invite members
- **Group Admin:** Additional permissions to manage group settings and members
- **Guest:** Limited to viewing content in groups they're invited to

## Page Definitions
- **Onboarding:** Account creation, security setup, privacy explanation
- **Group Selection:** Grid view of user's groups with creation option
- **Group Feed:** Chronological post feed with creation FAB
- **Post Creation:** Media picker, caption, privacy options
- **Settings:** Account management, privacy controls, notification preferences

## User Journeys
- **New User:** Onboarding → Group creation → Invite members → First post
- **Existing User:** Login → Group selection → View feed → Create post
- **Family Member:** Accept invitation → Setup security → View family content → Engage with posts
```

---
*Generated by Promptables Platform*
