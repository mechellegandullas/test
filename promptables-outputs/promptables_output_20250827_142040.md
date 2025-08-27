# Promptables Generated Content

Generated on: 2025-08-27 14:20:40

## Canvas Output

```json
{
  "designGuidelines": {
    "appName": "Hearth",
    "generalDesignOverview": {
      "purpose": "Hearth provides a secure, private digital space for families and close friends to share life updates, coordinate schedules, and preserve memories without the noise, algorithms, or data exploitation of public social media. It's the digital equivalent of gathering around the family hearth.",
      "toneAndPersonality": "Warm, trustworthy, and intimate. The design should feel like a cozy, well-organized family scrapbook – inviting yet sophisticated, simple yet powerful. It should radiate warmth and security.",
      "userGoals": [
        "Securely share photos, videos, and life updates with a strictly defined inner circle",
        "Coordinate events, schedules, and tasks within the family/group",
        "Create and preserve a private, shared history of memories",
        "Communicate easily and authentically without performance or external judgment"
      ]
    },
    "coreDesignPrinciples": [
      "Clarity & Simplicity: The interface must be instantly understandable across generations. Zero learning curve for core functions.",
      "Warm Minimalism: Avoid cold, sterile minimalism. Use warmth through color, texture, and micro-interactions to create emotional engagement.",
      "Trust Through Transparency: The UI must constantly, but subtly, reinforce its security and privacy-first nature. Users should always feel in control of their data."
    ],
    "colorScheme": {
      "primary": {
        "name": "Hearth Amber",
        "hex": "#E67E22",
        "purpose": "Primary brand color. Used for main CTAs, key interactive elements, and to provide warmth and energy. Evokes warmth, comfort, and home."
      },
      "secondary": {
        "name": "Deep Forest",
        "hex": "#2C3E50",
        "purpose": "Used for primary text, headers, and navigation bars. Provides a strong, trustworthy, and calm foundation that contrasts well with the warmth of the primary."
      },
      "accent": {
        "name": "Soft Clay",
        "hex": "#D7DBDD",
        "purpose": "Used for backgrounds, secondary button fills, and dividers. A warm, off-white neutral that prevents the UI from feeling cold or clinical."
      },
      "status": {
        "success": "#27AE60",
        "warning": "#F39C12",
        "error": "#E74C3C"
      }
    },
    "typography": {
      "fontFamily": {
        "primary": "Inter",
        "secondary": "Inter"
      },
      "fontWeightsAndHierarchy": {
        "h1": {
          "size": "28px",
          "weight": "700",
          "useCase": "Page titles, major section headers"
        },
        "h2": {
          "size": "22px",
          "weight": "600",
          "useCase": "Sub-section headers, post author names"
        },
        "body": {
          "size": "16px",
          "weight": "400",
          "useCase": "Primary body text for posts, comments, and descriptions"
        },
        "secondaryText": {
          "size": "14px",
          "weight": "400",
          "useCase": "Timestamps, captions, meta-information"
        },
        "buttonsCta": {
          "size": "16px",
          "weight": "600",
          "useCase": "All button text, clear and legible"
        }
      }
    },
    "uiComponentsByPage": {
      "onboardingAuthFlow": {
        "layout": "Centered, single-column layout with ample whitespace. Focus on one task per screen.",
        "interactiveElements": [
          "Phone number input field with country code selector",
          "Verification code input (auto-read if possible)",
          "'Continue' CTA button",
          "Subtle link to 'Use Email Instead'"
        ],
        "colorAndBehavior": "Clean background (Soft Clay). Hearth Amber used for the primary CTA button. Buttons have a slight roundedness (8px radius). A subtle, reassuring animation confirms code submission.",
        "mobileFirstNotes": "Full-screen takeover. Large input fields for easy tapping. Number pad is the default keyboard for phone input."
      },
      "homeFeed": {
        "layout": "A single, reverse-chronological feed. Each post is a distinct card on the main background.",
        "interactiveElements": [
          "Floating Action Button (FAB) for creating new posts",
          "Heart/Like button on each post",
          "Comment button",
          "Post options menu (•••) for editing/deleting",
          "Tapable user avatars and media"
        ],
        "colorAndBehavior": "Post cards have a subtle shadow and a white background for clarity. The Hearth Amber FAB is the primary action point. Interactions provide subtle tactile feedback (light fill or scale animation).",
        "mobileFirstNotes": "Infinite scroll. FAB is anchored to the bottom right. Swipe-to-refresh gesture to check for new posts."
      },
      "postCreationModal": {
        "layout": "Modal sheet that slides up from the bottom (on mobile) or centered overlay (on web). Step-by-step process: media selection -> caption -> audience.",
        "interactiveElements": [
          "Media picker (camera roll, camera, document)",
          "Text input for caption",
          "Audience selector (pre-selected to current group)",
          "Post button"
        ],
        "colorAndBehavior": "Clear, focused design. The 'Post' button is enabled only when content is added. A small lock icon next to the audience selector reinforces privacy.",
        "mobileFirstNotes": "Native device UI for media picker and camera. Modal should be easily dismissible by dragging down."
      },
      "groupManagement": {
        "layout": "List of groups the user is in. Tapping a group goes to its specific feed. Separate 'New Group' section.",
        "interactiveElements": [
          "Group list items",
          "'Create New Group' button",
          "Invite via link button",
          "Group settings navigation"
        ],
        "colorAndBehavior": "Calm and organized. A small group avatar accompanies each list item. Invitation links have a 'copy' button with a clear success state animation.",
        "mobileFirstNotes": "Swipe-left actions on group list items (e.g., mute, leave)."
      }
    },
    "mobileUxAccessibility": {
      "navigation": "Bottom tab bar navigation for primary sections (Feed, Calendar, Messages, Groups, Profile). Simple and thumb-friendly.",
      "tapTargets": "Minimum tap target size of 44x44 points for all interactive elements.",
      "contrast": "All text must meet WCAG AA minimum contrast ratios (4.5:1 for normal text). The color palette has been chosen with this in mind.",
      "feedback": "All actions must provide immediate feedback: buttons have pressed states, likes animate, loading spinners are present for async actions, and success/error states are clear and informative."
    },
    "iconsVisualStyle": {
      "iconSet": "Rounded, line-style icons with a consistent stroke weight (1.5px). Friendly but not childish. Slightly rounded corners to match the overall soft aesthetic.",
      "visualGuidelines": "User-uploaded photos are displayed in a balanced grid or aspect-ratio-filled containers. Avoid heavy filters. The app uses no stock photography. Any illustrative elements (e.g., empty states) should be warm, simple, and line-based."
    },
    "microinteractionsAnimations": {
      "transitions": "Subtle slide and fade transitions between screens. No jarring jumps.",
      "states": "All buttons have clear :hover, :active, and :focus states. Focus states are crucial for keyboard navigation on web.",
      "animations": "Functional and delightful: A small heart animation when liking, a gentle 'shimmer' when loading content, a satisfying 'click' effect on the FAB. All animations are brief and non-intrusive."
    },
    "performanceConsiderations": {
      "optimization": "Images and videos are optimised and served in modern formats (WebP, AVIF) and appropriate resolutions for the device. Lazy-loading is implemented for media below the fold.",
      "offline": "Core UI is cached. Recently viewed posts and comments are stored locally to allow for reading and drafting replies while offline. Syncs seamlessly upon reconnection."
    },
    "securityPrivacyDesign": {
      "authExperience": "The auth flow is simple but clearly communicates security. A brief explainer tooltip on the phone verification screen: 'We use your number to secure your account. We never share it.'",
      "dataSafety": "A shield icon is always visible in the profile tab, linking to a simple 'Privacy & Security' settings page. This page explains E2E encryption in simple terms: 'Your conversations are locked with a key only your family has.' Settings for message expiration and device management are located here."
    },
    "conclusion": "Hearth's design is a direct reflection of its core mission: to create a warm, secure, and simple digital home for families. Every design decision, from the warm color palette to the robust privacy indicators, is made to build trust and foster genuine connection. The interface prioritizes emotional clarity and ease-of-use above all else, ensuring it feels like a welcome respite from the complexity of the digital world, not an addition to it."
  }
}
```

---

## Blueprint Output

```markdown
# Master Plan: Haven

## App Overview & Objectives
- **Purpose:** Create a secure, private digital space for families and close friends to share life moments without data mining or advertising. A sanctuary for genuine connection in a hyper-connected world.
- **Target Audience:** Privacy-conscious families, close-knit friend groups, and individuals seeking authentic digital sharing without corporate surveillance.

## Core Features & Functionality
- End-to-end encrypted content sharing (photos, videos, text updates)
- Private group creation and management with invitation-only access
- Chronological timeline with memory preservation
- Simple, intuitive commenting and reactions
- Secure media storage with user-controlled encryption keys

## High-Level Technical Stack
- **Frontend:** React Native (iOS/Android) with responsive web companion
- **Backend & Database:** Supabase with Row Level Security
- **Authentication:** Phone number verification with optional email backup
- **Media Storage:** Encrypted cloud storage with client-side encryption

## Conceptual Data Model
- Users (verified identities)
- Groups (private containers for sharing)
- Posts (encrypted content with metadata)
- Media (encrypted files with access controls)
- Comments (encrypted interactions)

## User Interface Principles
- Mobile-first, intuitive navigation
- Warm, inviting aesthetic with focus on content
- Minimalist design that prioritizes privacy and ease of use

## Security Considerations
- End-to-end encryption for all user-generated content
- Zero-knowledge architecture where possible
- Regular security audits and transparency reports

## Development Phases
- **MVP:** Core sharing, group management, and basic timeline
- **V1:** Enhanced media handling, memory features, web companion
- **V2:** Advanced privacy controls, family organization tools, legacy features

## Potential Challenges & Solutions
- **Encryption Key Management:** Implement secure key storage with recovery options
- **Cross-Platform Sync:** Use conflict-free replicated data types for consistency
- **User Onboarding:** Streamlined invitation and verification process
```

```markdown
# Implementation Plan

## Phase 1: MVP
1.  Set up React Native project with TypeScript and secure foundation
2.  Configure Supabase project with Row Level Security policies
3.  Implement phone number authentication flow
4.  Build group creation and invitation system
5.  Develop encrypted posting and timeline functionality
6.  Create basic media upload and viewing with encryption
7.  Implement commenting and reaction system

## Phase 2: V1 Launch
1.  Enhance media handling with compression and progressive loading
2.  Develop web companion application
3.  Implement "On This Day" memory features
4.  Add advanced privacy controls and sharing permissions
5.  Create admin tools for group management

## Phase 3: V2 Expansion
1.  Develop family organization features (calendars, tasks)
2.  Implement legacy and digital inheritance options
3.  Add advanced search and organization tools
4.  Create export and data portability features

## Team & Tools Recommendations
- **Core Team:** 2-3 developers (frontend, backend, security focus)
- **Key Tools:** React Native, Supabase, Cloudflare R2, Twilio Verify
- **Monitoring:** Sentry for error tracking, PostHog for analytics (privacy-focused)
```

```markdown
# Design Guidelines

## Visual Style
- **Primary Font:** Inter (clean, readable, modern)
- **Color Palette:**
  - Primary: `#4A6FA5` (trustworthy blue)
  - Secondary: `#FF9F1C` (warm accent)
  - Background: `#F8F9FA` (light neutral)
  - Text: `#2D3748` (dark gray)
- **Layout Approach:** Mobile-first, card-based content with generous whitespace

## Accessibility
- **Target Compliance:** WCAG AA
- **Tap Target Size:** Minimum 44px
- **Color Contrast:** Minimum 4.5:1 for text
- **Screen Reader Support:** Full ARIA labels and semantic HTML

## Interaction Design
- **Gestures:** Simple swipe actions for common tasks
- **Feedback:** Subtle animations and haptic feedback
- **Loading States:** Skeleton screens with progressive content loading

## Component Principles
- Consistent spacing (8px grid system)
- Rounded corners (8px radius)
- Subtle shadows for depth
- Focus states for all interactive elements
```

```markdown
# App Flow: Pages & User Roles

## User Roles
- **Member:** Can view, post, comment, and react to content in their groups
- **Admin:** Can manage group settings, invite/remove members, moderate content
- **Owner:** Full control over group, including deletion and ownership transfer

## Page Definitions
- **Onboarding:** Phone verification, profile setup, first group creation
- **Home Timeline:** Chronological feed of all group content with new post button
- **Group View:** Focused view of a single group's content and members
- **New Post:** Simple composer with media attachment and privacy options
- **Profile:** User settings, group memberships, privacy controls
- **Notifications:** Activity alerts and group invitations

## User Journeys
- **New User:** Verification → Profile Setup → Create/Join Group → First Post
- **Existing User:** Open App → View Timeline → Interact → Create Content
- **Group Admin:** Manage Members → Adjust Settings → Moderate Content → Invite New Users

## Navigation Structure
- Bottom tab bar for primary navigation (Home, Groups, Notifications, Profile)
- Modal overlays for creation and detailed views
- Swipe gestures for quick actions on posts and comments
```

---
*Generated by Promptables Platform*
