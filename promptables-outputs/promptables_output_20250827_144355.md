# Promptables Generated Content

Generated on: 2025-08-27 14:43:55

# Design Guidelines for Hearth

## 1. General Design Overview
**Purpose:** To provide a private, secure, and intimate digital space for small groups of trusted individuals to share life's moments without the noise and privacy concerns of traditional social media.
**Tone & Personality:** Warm, trustworthy, secure, and personal. The app should feel like a cozy, digital living room.
**User Goals:** Easily create and manage private groups, seamlessly share photos and updates, feel confident in the app's privacy and security, and maintain genuine connections with a close circle.

### 1.1 Core Design Principles
- **Trust & Security:** The UI must constantly communicate safety and privacy through clear language and intuitive controls.
- **Intimacy & Warmth:** The visual design should feel personal, welcoming, and human-centric, not cold or corporate.
- **Simplicity & Clarity:** The interface must be effortless to use, minimizing cognitive load so the focus remains on connection, not on figuring out the app.

## 2. Color Scheme
**Primary (Hearth Glow):** `#FF9F66` - Used for primary buttons, key interactive elements, and subtle highlights. Evokes warmth and comfort.
**Secondary (Charcoal):** `#36454F` - Used for primary text, headers, and navigation bars. Provides a strong, trustworthy, and readable foundation.
**Accent (Cream):** `#F8F4E6` - Used for backgrounds and card containers. Creates a soft, warm, and inviting canvas.
**Success/Positive (Moss):** `#4A7C59` - Used for confirmations and positive actions.

## 3. Typography
### 3.1 Font Family
**Primary:** Inter (A highly readable, modern sans-serif with a warm and friendly tone.)
**Secondary:** System UI (Fallback)
### 3.2 Font Weights & Hierarchy
- **H1:** 24px, 700 - Page titles and major headings.
- **H2:** 20px, 600 - Section headers and group names.
- **Body:** 16px, 400 - Primary content and readable text.
- **Buttons/CTA:** 16px, 600 - All call-to-action text.
- **Caption:** 14px, 400 - Secondary information, timestamps.

## 4. UI Components by Page
### Onboarding & Authentication
- **Layout:** Minimal, single-column centered card on a `Cream (#F8F4E6)` background. Focus is on the form.
- **Interactive Elements:** Email input, password input, "Sign Up"/"Log In" CTA button (Hearth Glow `#FF9F66`), "Forgot Password?" link.
- **Color & Behavior:** Buttons have a subtle hover state (slightly darker shade). Form fields have a clear focus state.
- **Mobile-First Notes:** Full-screen takeover. Form is comfortably sized for thumb interaction.

### Home/Dashboard (Group Feed)
- **Layout:** A single, reverse-chronological feed of shared content. A floating action button (FAB) in the bottom-right for new posts. A top app bar with the app logo and a navigation drawer icon.
- **Interactive Elements:** FAB, posts (tappable for options like comment/love), navigation menu icon.
- **Color & Behavior:** Posts are displayed as cards on the `Cream (#F8F4E6)` background with a soft shadow. The FAB uses the primary `Hearth Glow` color and has a gentle scale animation on press.
- **Mobile-First Notes:** Feed is optimized for vertical scrolling. FAB is positioned within the thumb's natural reach zone.

### Group Management Screen
- **Layout:** List of current groups. A "Create New Group" button at the top. Each group list item shows the group name, a thumbnail of member avatars, and a chevron.
- **Interactive Elements:** "Create New Group" button, group list items, settings icon for each group.
- **Color & Behavior:** Tapping a group navigates to its feed. A long press on a group reveals a context menu (Edit, Leave).
- **Mobile-First Notes:** Simple list view is easy to scroll and tap.

### Create/Edit Post Screen
- **Layout:** A minimal composer. A top bar with "Post" and "Cancel" buttons. A large, tappable area for adding media. A text input field below.
- **Interactive Elements:** Media attachment button, text input, "Post" CTA.
- **Color & Behavior:** The "Post" button is enabled only when content (text or media) is present. Media preview appears above the text input.
- **Mobile-First Notes:** The keyboard appears immediately, focusing the text input. Media attachment is a clear, large button.

## 5. Mobile UX & Accessibility
- **Navigation:** Bottom navigation bar for primary sections (Home, Groups, Notifications, Profile). Navigation drawer for secondary options (Settings, Invite Friends).
- **Tap Targets:** Minimum 44x44pt for all interactive elements.
- **Contrast:** All text meets WCAG AA minimum contrast ratios (4.5:1) against their backgrounds.
- **Feedback:** All buttons and tappable elements have visual feedback (opacity change or fill) on touch. Haptic feedback on key actions.

## 6. Icons & Visual Style
- **Icon Set:** Rounded, medium-weight line icons (e.g., Feather Icons style) for a friendly and modern feel.
- **Visual Guidelines:** User-generated photos are displayed in a natural aspect ratio with slightly rounded corners (4px). Avoid corporate stock imagery; the only visuals should be from users.

## 7. Microinteractions & Animations
- **Transitions:** Subtle slide animations for page transitions. Fade animations for modals.
- **States:** All interactive elements have defined hover, active, and focus states.
- **Animations:** A gentle "heart" animation when liking a post. A smooth circular progress indicator for any loading state.

## 8. Performance Considerations
- **Optimization:** All user-uploaded images are automatically optimized and served in modern formats (WebP/AVIF). Implement lazy loading for images in the feed.
- **Offline:** Core UI is cached. Draft posts are saved locally if created offline.

## 9. Security & Privacy Design
- **Auth Experience:** The sign-up flow clearly explains what data is collected (minimal) and why. A simple, jargon-free Privacy Policy and Terms of Service are linked.
- **Data Safety:** UI elements like "Invite Link" screens have clear explanations of their function and security ("Only share this link with people you trust"). Settings clearly show data management options (e.g., "Delete All My Data").

### Conclusion
The design of Hearth must consistently reinforce its core values: it is a warm, safe, and simple place for real connection. Every design decision, from the color palette to the copywriting, should serve to build user trust and eliminate friction, making private sharing feel effortless and secure.

```markdown
# Master Plan: Hearth

## App Overview & Objectives
- **Purpose:** To create a sustainable, privacy-first platform for intimate social networking, monetized directly by its users to ensure alignment with their interests.
- **Target Audience:** Individuals and small groups (families, close friends, clubs) seeking a more private and meaningful alternative to mainstream social media.

## Core Features & Functionality
- Private Group Creation & Management (via invite links)
- Multimedia Feed (Photo, Text, Video)
- End-to-End Encrypted Messaging (Optional, V2)
- Subscription-based Monetization

## High-Level Technical Stack
- **Frontend:** React Native (for iOS/Android cross-platform development)
- **Backend & Database:** Supabase (PostgreSQL database, auth, realtime, and storage)
- **Authentication:** Supabase Auth (Email + Password, with secure magic links for recovery)
- **CMS:** Notion (for internal documentation and content planning)

## Conceptual Data Model
- `profiles` (public user data)
- `groups` (group details, owner_id)
- `members` (junction table for users<->groups)
- `posts` (content, linked to a group and author)
- `subscriptions` (links users to Stripe subscription IDs)

## User Interface Principles
- Mobile-first, warm, and minimalist design prioritizing content.

## Security Considerations
- All data access controlled via Row Level Security (RLS) policies in Supabase. Sensitive operations require server-side validation.

## Development Phases
- **MVP:** Core group creation, feed, and photo sharing. Annual subscription via Stripe.
- **V1:** Enhanced media support (video), push notifications, improved onboarding.
- **V2:** End-to-end encryption for messages, event planning features, shared albums.

## Potential Challenges & Solutions
- **Challenge:** Ensuring user privacy and data security is paramount.
  - **Solution:** Strict RLS policies, minimal data collection, and clear, transparent privacy controls in the UI.
- **Challenge:** Overcoming the "network effect" hurdle for a social app.
  - **Solution:** Focus on the value proposition for existing real-world groups (families, friends) who have a pre-existing reason to use the app together.
```
```markdown
# Implementation Plan

## Phase 1: MVP
1.  Set up React Native project with TypeScript and navigation (React Navigation).
2.  Initialize Supabase project, configure databases tables with RLS policies.
3.  Implement Supabase authentication flows (Sign Up, Login, Password Reset).
4.  Build core UI: Tab navigator, Group List screen, Group Feed screen.
5.  Implement group creation and joining via invite links.
6.  Build post creation and display functionality (text and images using Supabase Storage).
7.  Integrate Stripe for annual subscriptions using Stripe Customer Portal.
8.  Deploy a production build to TestFlight and Google Play Beta.

## Phase 2: V1 Launch
1.  Implement video upload and playback.
2.  Add push notifications for new posts and comments (using Supabase Realtime and a service like OneSignal).
3.  Polish onboarding flow and add empty states throughout the app.
4.  Conduct beta testing with a small group of users.
5.  Launch on App Store and Google Play.

## Team & Tools Recommendations
- A solo full-stack developer can manage this stack effectively.
- **Key Tools:** React Native, Supabase, Stripe, GitHub/GitLab for version control, Visual Studio Code.
```
```markdown
# Design Guidelines

## Visual Style
- **Primary Font:** Inter
- **Color Palette:**
  - Primary: `#FF9F66` (Hearth Glow)
  - Text: `#36454F` (Charcoal)
  - Background: `#F8F4E6` (Cream)
  - Accent: `#4A7C59` (Moss)
- **Layout Approach:** Mobile-first. Content is king, presented on a warm, neutral background with clear card separators.

## Accessibility
- **Target Compliance:** WCAG 2.1 AA
- **Tap Target Size:** Minimum 44x44pt
- **Contrast:** All text must have a contrast ratio of at least 4.5:1 against its background.
```
```markdown
# App Flow: Pages & User Roles

## User Roles
- **User:** Can create groups, invite members, post content to groups they are in, and comment on/like posts.
- **Group Admin (Creator):** Has all User permissions plus the ability to remove members and delete the group.

## Page Definitions
- **Authentication:** Handles user sign-up and login.
- **Groups List:** The default home screen after login. Lists all groups the user is a member of.
- **Group Feed:** The main content view for a selected group. Displays a feed of posts.
- **Create Post:** A modal or screen for composing a new post (text, image, video).
- **Profile/Settings:** User can manage account settings, subscription, and logout.

## User Journeys
- **New User:** Download App -> Sign Up -> Create First Group (or enter invite code) -> See empty group feed -> Create first post.
- **Existing User:** Open App -> Login -> See list of groups -> Select a group -> View feed and interact with content.
```

---
*Generated by Promptables Platform*
