# luma-chat
Next gen chat app
# Luma

> **Your people, your space.**

Luma is a premium, privacy-first mobile social chat application built around private conversations, social rooms, shared memories, meaningful activities, and calm digital presence.

Luma is designed to help people feel close even when they are apart.

---

## Table of Contents

- [Project Status](#project-status)
- [Product Vision](#product-vision)
- [Core Product Concept](#core-product-concept)
- [Product Principles](#product-principles)
- [Target Users](#target-users)
- [Version 1 Scope](#version-1-scope)
- [Features Excluded from Version 1](#features-excluded-from-version-1)
- [Mobile App Experience](#mobile-app-experience)
- [How to View the App During Development](#how-to-view-the-app-during-development)
- [Brand and Design Direction](#brand-and-design-direction)
- [Design Tokens](#design-tokens)
- [Aura System](#aura-system)
- [Motion and Haptics](#motion-and-haptics)
- [Accessibility](#accessibility)
- [Technical Architecture](#technical-architecture)
- [Planned Repository Structure](#planned-repository-structure)
- [Application Layers](#application-layers)
- [Data Storage Strategy](#data-storage-strategy)
- [Backend Architecture](#backend-architecture)
- [Messaging Architecture](#messaging-architecture)
- [Offline-First Behavior](#offline-first-behavior)
- [Planned Data Models](#planned-data-models)
- [Security and Privacy](#security-and-privacy)
- [End-to-End Encryption Policy](#end-to-end-encryption-policy)
- [Media and Notifications](#media-and-notifications)
- [Implementation Roadmap](#implementation-roadmap)
- [Immediate Mobile Prototype Plan](#immediate-mobile-prototype-plan)
- [Release Gates](#release-gates)
- [Development Workflow](#development-workflow)
- [Documentation Map](#documentation-map)
- [Contribution Guidance](#contribution-guidance)
- [Security Reporting](#security-reporting)
- [Current Status Checklist](#current-status-checklist)
- [What to Build Next](#what-to-build-next)

---

## Project Status

Luma is currently in the early foundation and planning stage.

The repository currently contains the initial README and the first branding asset:

```text
README.md
assets/
└── branding/
    └── luma-logo.svg
```

The following systems are **not yet implemented**:

- Production authentication
- Real-time messaging
- Backend services
- Production database
- Push notifications
- Media uploads
- Voice notes
- Voice calls
- Video calls
- Public discovery
- Purchases or subscriptions
- Full gamification
- End-to-end encryption
- Production security review

The first implementation milestone is a viewable mobile prototype using Expo, React Native, TypeScript, and mock data.

---

## Product Vision

Luma is more than a traditional messaging application.

A conventional messaging app asks:

> “What message did someone send me?”

Luma should ask:

> “What are my people doing, feeling, and experiencing right now?”

Luma combines:

- Private one-to-one conversations
- Small private group rooms
- Optional presence and moods
- Shared memories
- Group activities
- Room identity and progression
- Personalization
- Calm digital presence
- Privacy and safety controls

The product should feel like entering a beautiful private digital lounge where the people who matter are gathered.

---

## Core Product Concept: Living Social Rooms

A Luma conversation is not limited to a list of messages.

A room can become:

- A chat
- A hangout
- A planning space
- A memory timeline
- A shared activity
- A group identity
- A private digital home

The core differentiator is the idea of **living social rooms**.

Each room may eventually include:

- Messages
- Presence
- Mood or status
- Shared images
- Important memories
- Events and plans
- Group prompts
- Room themes
- Room progression
- Shared milestones
- Optional activities

---

## Product Principles

Every feature should follow these principles.

### Privacy first

- Collect only data required for the selected feature.
- Keep private conversations private.
- Make visibility and presence optional.
- Avoid unnecessary tracking.
- Do not expose sensitive message content through notifications or logs.
- Give users control over their account and data.
- Provide account deletion and privacy controls.

### Meaningful connection

Luma should encourage genuine interaction rather than empty activity.

Features should help people:

- Talk
- Plan
- Remember
- Participate
- Support one another
- Feel present together

### Premium experience

The application should feel:

- Calm
- Elegant
- Modern
- Atmospheric
- Personal
- Reliable
- Polished
- High quality

### Social depth

Users should feel present with one another, not merely exchange messages.

### Trust and safety

Safety is a product requirement, not a later addition.

The product must eventually include:

- Blocking
- Reporting
- Abuse prevention
- Account protection
- Permission checks
- Privacy controls
- Safe account recovery
- Secure deletion workflows

### No manipulative engagement

Luma must not pressure users through:

- Fear of losing streaks
- Excessive notifications
- Public embarrassment
- Artificial popularity
- Forced daily activity
- Paywalls on essential communication

The desired feeling is:

> “I want to come back because something meaningful is happening.”

Not:

> “I am afraid to miss something.”

---

## Target Users

Luma is initially designed for:

- Close friends
- Families
- Couples
- Long-distance relationships
- Study groups
- Gaming groups
- Creative teams
- Small communities
- Private interest groups
- People seeking a more personal alternative to ordinary chat applications

### Example use cases

#### Friend group

A group creates a “Weekend Crew” room to chat, plan activities, complete prompts, and preserve shared memories.

#### Family

A family uses a private room for updates, photos, birthdays, events, and important memories.

#### Study group

Students create a study room with optional statuses such as “studying,” shared check-ins, and scheduled activities.

#### Gaming group

Friends use a room for text chat, shared presence, gaming sessions, and event planning.

#### Close relationship

Two people use a private room with personalized themes, shared memories, voice notes in a later version, and meaningful check-ins.

---

## Version 1 Scope

Version 1 focuses on a reliable, polished, privacy-first mobile chat foundation.

### V1 goals

- Establish the Luma brand and visual language.
- Create a viewable Expo mobile application.
- Build a secure authentication foundation.
- Support direct messaging.
- Support small private group rooms.
- Provide basic privacy and visibility controls.
- Prepare an offline-ready local architecture.
- Document security and privacy requirements.
- Avoid premature feature expansion.

### V1 authentication

Planned authentication features:

- Email registration
- Email verification
- Sign in
- Password reset
- Secure session handling
- Sign out
- Session revocation
- Device and session management
- Account deletion request

Phone login and social login may be considered later.

### V1 profiles

Planned profile fields and controls:

- Username
- Display name
- Avatar
- Optional biography
- Optional mood or status
- Presence visibility
- Notification preferences
- Blocked users list

Users should not be required to reveal:

- Phone number
- Exact location
- Online status
- Last-seen time
- Contact list

### V1 direct messaging

Planned direct-message features:

- One-to-one text messages
- Timestamps
- Sent status
- Delivered status
- Read status
- Typing indicator
- Message reactions
- Reply to message
- Edit message
- Delete message
- Failed-message retry
- Offline queue
- Cursor-based pagination
- Message drafts

### V1 private group rooms

Planned room features:

- Create a private room
- Invite members
- Remove members when authorized
- Member roles
- Admin role
- Room title
- Room icon
- Room accent color
- Room theme
- Leave room
- Mute room
- Block users
- Report users
- Small initial member limit

### V1 presence

Presence should be optional and user-controlled.

Possible statuses include:

- Available
- Free to chat
- Listening to music
- Studying
- Gaming
- Working
- Outside
- Quiet mode
- I will reply later

Presence must be:

- Easy to disable
- Configurable by audience
- Privacy-friendly
- Never required for normal communication

### V1 memories

The first memory system should remain simple.

Possible memory types:

- Important messages
- Shared images
- Selected moments
- Room milestones
- Basic shared timelines

Advanced automatic recaps and AI-generated summaries are postponed.

### V1 media

Version 1 should begin with images only.

Requirements:

- Image compression
- File-size limits
- MIME-type validation
- Secure upload flow
- Short-lived access URLs
- No public media URLs
- Malware and file checks
- Authorized media access
- Secure deletion behavior

Voice notes should be introduced only after the core messaging flow is stable.

### V1 notifications

Planned notification features:

- New-message notifications
- Room notifications
- Mute options
- Quiet hours
- Notification preferences
- Deep links into rooms

Notifications must not reveal plaintext message content by default.

Preferred:

```text
New message in a private room.
```

Avoid:

```text
Sarah: I sent you the private document.
```

---

## Features Excluded from Version 1

The following features are intentionally postponed:

- Full production end-to-end encryption claims
- Voice calls
- Video calls
- Drop-in audio rooms
- Public discovery
- Large public communities
- AI-generated summaries
- Automatic memory recaps
- Advanced gamification
- Glow points
- Streak systems
- Purchases
- Subscriptions
- Creator tools
- Location-based discovery
- Voice notes
- Large-scale media galleries
- Public social feeds

These may be considered in later milestones after the core product is reliable and secure.

---

## Mobile App Experience

Luma is a **mobile-first application**.

The primary experience will be designed for:

- iPhone
- Android phones
- Portrait-oriented mobile layouts
- Touch interaction
- Mobile accessibility
- Mobile performance
- Mobile notifications
- Device secure storage

The web preview is useful for basic development checks, but it is not the primary product target.

### Planned navigation

```text
Home
Rooms
Discover
Memories
```

### Home

Home should not feel like a conventional inbox.

Potential sections:

```text
NOW
What your people are doing right now

ROOMS
Your private conversations and communities

MEMORIES
Shared moments and recent highlights

ACTIVITY
Optional prompts and room activities
```

Home may include:

- Personalized greeting
- Optional friend presence
- Active room activity
- Recent memories
- Unread activity
- Suggested meaningful activities
- Room aura cards

### Rooms

Rooms will show:

- Direct conversations
- Private group rooms
- Unread messages
- Room status
- Room themes
- Room activity
- Member presence
- Room settings

### Discover

Discover is postponed or heavily restricted in Version 1.

A future Discover area may include:

- Interest-based rooms
- Study spaces
- Gaming communities
- Creative communities
- Local events
- Invite-only groups
- Public communities

If public discovery is introduced, it must include:

- Privacy controls
- Age safety
- Moderation
- Block and report tools
- Message-request controls
- No unsolicited direct messages by default

### Memories

Memories will eventually show:

- Shared photos
- Important messages
- Voice notes
- Room milestones
- Group memories
- “On this day” moments
- Shared timelines
- Recap designs

---

## How to View the App During Development

Once the Expo mobile foundation is created, the app can be viewed on a real phone using Expo Go.

### Physical Android or iPhone

The expected workflow is:

1. Install Expo Go from the Google Play Store or Apple App Store.
2. Start the Expo development server on the computer.
3. A QR code appears in the terminal or development interface.
4. Scan the QR code with Expo Go.
5. The Luma mobile preview opens on the phone.
6. Changes can usually be refreshed immediately during development.

### Android emulator

Developers may use an Android emulator through Android Studio.

### iOS simulator

Developers using macOS may use the iOS Simulator through Xcode.

### Web preview

Expo can provide an optional browser preview for basic checks. The web preview is not a replacement for testing on a real mobile device.

### What the first prototype should contain

```text
Luma splash screen
        ↓
Welcome screen
        ↓
Sign in / Create account
        ↓
Privacy onboarding
        ↓
Home
        ↓
Rooms
        ↓
Chat mockup
        ↓
Memories mockup
```

The first prototype will use mock data. Real authentication and backend services should be added only after the visual mobile experience has been reviewed.

---

## Brand and Design Direction

Luma should feel like a private digital social lounge.

### Brand personality

- Premium
- Warm
- Private
- Calm
- Emotional
- Modern
- Futuristic
- Social
- Intimate
- Elegant

### Visual inspiration

The design direction may take general inspiration from:

- Apple: spacing, restraint, and polish
- Linear: precision and hierarchy
- Calm: peaceful atmosphere
- Locket: intimacy
- Nothing: distinctive identity
- Clubhouse: live social presence

Luma must not copy another product’s interface.

### Logo asset

The current branding asset is:

```text
assets/branding/luma-logo.svg
```

The logo should eventually have:

- Primary symbol
- Wordmark
- App icon treatment
- Dark-background version
- Light-background version
- Monochrome version
- Small-size version
- Splash-screen presentation

The symbol should remain recognizable without gradients or glow effects.

---

## Design Tokens

### Base colors

| Token | Hex | Purpose |
|---|---:|---|
| Deep Space | `#0B0D12` | Primary application background |
| Soft Black | `#11141B` | Secondary background |
| Elevated Surface | `#181C25` | Elevated panels |
| Card Surface | `#202531` | Cards and room surfaces |
| Primary Text | `#F5F7FA` | Main text |
| Secondary Text | `#98A2B3` | Supporting text |
| Muted Text | `#687386` | Low-emphasis metadata |

### Accent colors

| Token | Hex | Purpose |
|---|---:|---|
| Electric Violet | `#8B5CF6` | Primary brand accent |
| Aurora Blue | `#38BDF8` | Secondary accent |
| Soft Coral | `#FB7185` | Warm social accent |
| Mint Glow | `#5EEAD4` | Positive or calm state |
| Golden Light | `#FBBF24` | Milestones and highlights |

### Visual rules

- Dark-first interface
- Soft gradients
- Rounded surfaces
- Subtle borders
- Atmospheric glows
- Premium typography
- Strong contrast
- Minimal clutter
- Restrained color usage
- No childish arcade-style design
- No overwhelming animations

---

## Aura System

Each room may have a subtle aura based on:

- Room theme
- Current mood
- Time of day
- Room activity
- Member presence
- User customization
- Room progression

Example aura directions:

| Room type | Suggested aura |
|---|---|
| Family | Warm amber |
| Study | Calm teal |
| Gaming | Electric green |
| Chill | Violet-blue |
| Date planning | Coral-pink |

Auras must remain subtle and must not reduce readability or accessibility.

Aura effects should be treated as enhancement, not as a requirement for understanding the interface.

---

## Typography

Typography should use:

- Large expressive headings
- Medium-weight room names
- Compact metadata
- Generous line spacing
- Limited font weights
- Strong hierarchy through spacing and scale

The interface should not rely on many colors or excessive font styles to communicate hierarchy.

---

## Motion and Haptics

Animations should feel calm and intentional.

Possible motion:

- Gentle logo fade-in
- Subtle aura pulsing
- Smooth message appearance
- Natural card expansion
- Spatially consistent room transitions
- Restrained unlock animations
- Smooth progress-ring changes
- Soft presence indicators

Avoid:

- Excessive bouncing
- Loud confetti
- Constant flashing
- Unnecessary motion
- Overstimulating effects

Reduced-motion preferences must be respected.

Haptics may be used for meaningful actions such as:

- Sending a message
- Completing a group activity
- Joining a room
- Reacting to a message
- Unlocking a theme
- Receiving an important social interaction

Haptics should confirm actions, not create noise.

---

## Accessibility

Accessibility is part of the design foundation.

The application should support:

- Strong text contrast
- Dynamic text sizing where practical
- Screen-reader labels
- Clear touch targets
- Keyboard navigation where relevant
- Reduced-motion preferences
- Meaningful non-color status indicators
- Readable error states
- Accessible focus order
- Avoidance of flashing content
- Dark-theme readability
- Accessible loading and empty states

Aura, gradient, and animation effects must never be necessary to understand core information.

---

## Technical Architecture

### Mobile framework

- React Native
- Expo
- TypeScript

### Local storage

- SQLite or WatermelonDB for structured offline data
- MMKV for small non-sensitive preferences
- iOS Keychain for sensitive credentials and keys
- Android Keystore for sensitive credentials and keys

### Backend

- Node.js
- NestJS or Fastify
- PostgreSQL
- Redis
- WebSockets or Socket.IO
- Background workers
- Object storage for media
- Push notification services

### Infrastructure

- Docker
- Managed PostgreSQL
- Managed Redis
- HTTPS
- Secrets management
- Monitoring
- Error tracking
- Backups
- Database migrations
- CI/CD
- Dependency scanning
- Secret scanning

### Potential services

Supabase Auth may be considered for an initial authentication layer, but it does not automatically secure the entire application.

The application must still implement and test:

- Authorization
- Session handling
- Role checks
- Rate limits
- Account recovery
- Data deletion
- Logging controls

Cloudflare R2 or equivalent object storage may be considered for media storage.

LiveKit may be considered later for voice, video, and audio-room functionality.

---

## Planned Repository Structure

The repository is expected to evolve toward the following structure:

```text
luma-chat/
├── app/
│   ├── screens/
│   │   ├── SplashScreen.tsx
│   │   ├── WelcomeScreen.tsx
│   │   ├── SignInScreen.tsx
│   │   ├── SignUpScreen.tsx
│   │   ├── PrivacyOnboardingScreen.tsx
│   │   ├── HomeScreen.tsx
│   │   ├── RoomsScreen.tsx
│   │   ├── DiscoverScreen.tsx
│   │   ├── MemoriesScreen.tsx
│   │   ├── ChatScreen.tsx
│   │   ├── RoomDetailsScreen.tsx
│   │   ├── ProfileScreen.tsx
│   │   └── SettingsScreen.tsx
│   ├── navigation/
│   │   ├── RootNavigator.tsx
│   │   ├── AuthNavigator.tsx
│   │   └── MainTabNavigator.tsx
│   ├── components/
│   │   ├── Logo.tsx
│   │   ├── Button.tsx
│   │   ├── Surface.tsx
│   │   ├── RoomCard.tsx
│   │   ├── MessageBubble.tsx
│   │   ├── PresenceIndicator.tsx
│   │   ├── MemoryCard.tsx
│   │   └── EmptyState.tsx
│   ├── theme/
│   │   ├── colors.ts
│   │   ├── spacing.ts
│   │   ├── typography.ts
│   │   ├── radii.ts
│   │   ├── shadows.ts
│   │   └── index.ts
│   ├── hooks/
│   ├── state/
│   ├── services/
│   ├── storage/
│   ├── types/
│   └── mock-data/
├── assets/
│   ├── icons/
│   ├── fonts/
│   └── branding/
│       └── luma-logo.svg
├── docs/
│   ├── product-constitution.md
│   ├── version-1-specification.md
│   ├── security-threat-model.md
│   ├── security-requirements.md
│   ├── privacy-requirements.md
│   ├── design-system.md
│   ├── architecture.md
│   ├── roadmap.md
│   └── decision-log.md
├── backend/
│   ├── auth/
│   ├── users/
│   ├── conversations/
│   ├── messages/
│   ├── media/
│   ├── notifications/
│   ├── workers/
│   └── security/
├── tests/
│   ├── unit/
│   ├── integration/
│   ├── authorization/
│   ├── security/
│   └── mobile/
├── App.tsx
├── app.json
├── package.json
├── tsconfig.json
└── README.md
```

This structure is a target architecture. Directories and files should be added incrementally as implementation begins.

---

## Application Layers

### Presentation layer

Responsible for:

- Screens
- Components
- Navigation
- Layout
- Visual states
- Accessibility
- Animations
- User interaction

### Application state layer

Responsible for:

- Authentication state
- Current user
- Conversation state
- Room state
- Presence state
- Draft state
- Sync state
- Notification preferences

### Domain layer

Responsible for:

- Message rules
- Room membership rules
- Permission checks
- Presence behavior
- Memory behavior
- Offline synchronization rules

### Infrastructure layer

Responsible for:

- API client
- WebSocket client
- Local database
- Secure storage
- Push notifications
- Media uploads
- Error reporting

### Backend layer

Responsible for:

- Authentication
- Authorization
- Data persistence
- Real-time events
- Media access
- Notifications
- Rate limits
- Abuse controls
- Audit logging

---

## Data Storage Strategy

### SQLite or WatermelonDB

Use structured local storage for:

- Messages
- Conversations
- Room membership
- Offline queues
- Sync state
- Recent chat history
- Draft messages

### MMKV

Use only for small, non-sensitive local values such as:

- Theme preference
- Non-sensitive settings
- Feature flags
- Small local state values

Do not store sensitive tokens or cryptographic keys in ordinary local storage.

### iOS Keychain and Android Keystore

Use secure platform storage for:

- Refresh tokens
- Device identity material
- Encryption keys when implemented
- Sensitive credentials
- Secure session data

Passwords must not be stored locally.

---

## Backend Architecture

The backend is planned around the following services or modules:

### Authentication

- Registration
- Email verification
- Login
- Password reset
- Session creation
- Session refresh
- Session revocation
- Device management
- Account deletion

### Users

- Profile management
- Visibility settings
- Presence settings
- Blocked users
- Notification preferences

### Conversations

- Direct conversations
- Group rooms
- Room membership
- Room roles
- Room settings
- Mute settings

### Messages

- Message creation
- Message retrieval
- Message editing
- Message deletion
- Reactions
- Replies
- Delivery status
- Read status
- Pagination

### Media

- Upload authorization
- MIME validation
- File-size limits
- Malware scanning
- Object storage
- Short-lived signed URLs
- Access authorization
- Deletion workflows

### Notifications

- Push token management
- Message notifications
- Room notifications
- Quiet hours
- Notification privacy
- Deep links

### Security

- Rate limits
- Abuse detection
- Audit logging
- Access monitoring
- Suspicious activity controls
- Security event handling

---

## Messaging Architecture

The planned real-time message flow is:

```text
User writes a message
        ↓
Message appears locally immediately
        ↓
App sends the message to the backend
        ↓
Backend authenticates the user
        ↓
Backend verifies room membership
        ↓
Backend validates the message
        ↓
Backend stores the message
        ↓
Backend publishes a real-time event
        ↓
Recipient receives the message
        ↓
Delivery status is recorded
        ↓
Read status is recorded
```

Every outgoing message should include a unique `client_message_id`.

This identifier is used to:

- Prevent duplicate messages
- Make retries safe
- Support offline queues
- Reconcile local and server state
- Handle poor network conditions

The backend must treat message creation as idempotent when the same authenticated user submits the same `client_message_id`.

---

## Offline-First Behavior

The app should remain useful during poor connectivity.

Requirements:

- Cache recent conversations.
- Cache recent messages.
- Save drafts offline.
- Queue unsent messages.
- Retry automatically.
- Show sending state.
- Show failed state.
- Sync after reconnection.
- Prevent duplicate messages.
- Resolve conflicts safely.

### Message states

```text
Draft
Sending
Sent
Delivered
Read
Failed
```

The user should always be able to understand whether a message:

- Has not been sent
- Is currently sending
- Was accepted by the server
- Reached the recipient device
- Was read
- Failed and can be retried

---

## Planned Data Models

### User

```text
id
username
display_name
email
avatar_url
bio
presence_status
presence_visibility
created_at
updated_at
deleted_at
```

### Conversation

```text
id
type: direct | group
title
avatar_url
created_by
room_theme
room_accent
created_at
updated_at
last_message_id
```

### Conversation Member

```text
conversation_id
user_id
role: member | admin
joined_at
muted_until
last_read_message_id
```

### Message

```text
id
conversation_id
sender_id
client_message_id
type: text | image | system
content_or_ciphertext
reply_to_message_id
created_at
edited_at
deleted_at
```

### Message Status

```text
message_id
user_id
status: sent | delivered | read
updated_at
```

### Memory

```text
id
conversation_id
created_by
type
title
media_reference
message_reference
created_at
```

These models are planning references and may change during implementation.

---

## Security and Privacy

Security is a release-blocking requirement.

### Security goals

- Protect user accounts.
- Prevent unauthorized room access.
- Protect messages and media.
- Minimize data exposure.
- Prevent account takeover.
- Prevent abuse.
- Avoid sensitive notification leakage.
- Provide safe recovery and deletion.
- Avoid unsupported security claims.

### Threats to consider

- Credential theft
- Account takeover
- Session hijacking
- Unauthorized room access
- IDOR/BOLA vulnerabilities
- Message tampering
- Replay attacks
- Malicious media uploads
- Spam and invitation abuse
- Fake or modified clients
- Push-notification leakage
- Device theft
- Rooted or jailbroken devices
- Reverse engineering
- Dependency compromise
- Insider misuse
- Denial of service

### Required controls

- TLS for every network connection
- Secure WebSockets
- Short-lived access tokens
- Refresh-token rotation
- Session revocation
- Device and session management
- Server-side authorization for every protected resource
- Input validation
- Output validation
- Rate limiting
- Brute-force protection
- Secure media handling
- File-size limits
- MIME validation
- Malware scanning
- Minimal logging
- No message plaintext in logs
- No secrets in source code
- No secrets in mobile bundles
- Secret scanning
- Dependency scanning
- Software bill of materials
- Audit logging
- Account recovery controls
- Abuse detection
- Block and report systems
- Database backups
- Secure deletion workflows
- Least-privilege service accounts
- Production access controls

### Mobile security

- Use platform secure storage.
- Do not store passwords.
- Do not store sensitive keys in MMKV or plain files.
- Avoid sensitive clipboard use.
- Prevent notification content leakage.
- Review screenshots and app-switcher behavior.
- Review deep links.
- Avoid sensitive logs.
- Test local database extraction.
- Test behavior on rooted and jailbroken devices.
- Avoid hardcoded secrets.
- Minimize sensitive data stored offline.

---

## End-to-End Encryption Policy

Luma must not claim to be fully end-to-end encrypted until a complete, mature, reviewed system has actually been implemented and tested.

Cryptographic primitives alone are not enough.

A secure messaging system may require:

- Identity keys
- Device keys
- Session keys
- Key exchange
- Key rotation
- Forward secrecy
- Replay protection
- Group key management
- Multi-device support
- Device replacement handling
- Recovery design
- Key verification
- Secure deletion
- Media encryption
- Backup behavior
- Protocol testing
- Independent cryptographic review

Luma must not invent a new cryptographic protocol casually.

Where practical, a mature and reviewed protocol should be used. Strong security claims should be made only after implementation, testing, review, and evidence.

---

## Media and Notifications

### Media

The media system should use:

- Authorized uploads
- Encrypted transport
- MIME validation
- File-size limits
- Malware scanning
- Private object storage
- Short-lived signed URLs
- Server-side access checks
- Deletion handling
- No public media URLs

Sensitive data must not be placed in URLs.

### Notifications

Notifications should be privacy-preserving by default.

Do not include plaintext message content unless the user explicitly enables that behavior and the platform experience supports it safely.

Notification preferences should eventually include:

- All notifications
- Mentions only
- Room-specific notifications
- Quiet hours
- Preview controls
- Muted rooms
- Device-specific settings

---

## Implementation Roadmap

### Phase 0: Planning

- Confirm product name and tagline.
- Confirm visual direction.
- Confirm Version 1 scope.
- Create threat model.
- Create privacy requirements.
- Create design system.
- Create data model plan.
- Create repository documentation.
- Create decision log.

### Phase 1: Brand Foundation

- Expo project
- TypeScript setup
- Theme tokens
- Splash animation
- Luma logo treatment
- Welcome screen
- Sign-in UI
- Sign-up UI
- Privacy onboarding
- Navigation shell
- Initial Home mockup

### Phase 2: Account Foundation

- Real authentication
- Email verification
- Session management
- Profile setup
- Privacy settings
- Notification settings
- Account deletion workflow
- Device and session management

### Phase 3: Core Chat

- Conversation list
- Direct messages
- Message persistence
- Message states
- Typing indicators
- Offline queue
- Retry logic
- Pagination
- Message reactions
- Reply, edit, and delete

### Phase 4: Private Rooms

- Create group rooms
- Invite members
- Room roles
- Room themes
- Presence
- Mute controls
- Block and report tools
- Room settings

### Phase 5: Security Validation

- Authentication tests
- Authorization tests
- IDOR/BOLA tests
- WebSocket security tests
- Rate-limit tests
- Local-storage tests
- Notification leakage tests
- Dependency scanning
- Secret scanning
- Mobile security review
- Privacy review

### Phase 6: Social Depth

- Shared prompts
- Mood and presence improvements
- Memory timeline
- Group activities
- Room progression
- Glow points
- Weekly challenges
- Shared milestones

### Phase 7: Premium Expansion

- Voice notes
- Audio rooms
- Video calls
- Room atmosphere packs
- Premium cosmetics
- Encrypted media storage tiers
- Subscription system
- Seasonal visual collections

---

## Immediate Mobile Prototype Plan

The first implementation should focus on creating a viewable mobile application with mock data.

### Milestone 1

1. Create Expo and React Native foundation.
2. Configure TypeScript.
3. Add theme tokens.
4. Add branding assets.
5. Create the splash screen.
6. Create the Welcome screen.
7. Create Sign In and Sign Up interfaces.
8. Create privacy onboarding.
9. Create the navigation shell.
10. Create the Home screen mockup.
11. Create the Rooms screen mockup.
12. Create a chat screen mockup.
13. Create a Memories screen mockup.
14. Add mock room and message data.
15. Add basic loading, empty, and error states.
16. Test the prototype with Expo Go on a mobile device.
17. Review the visual direction before backend implementation.

### Important sequencing rule

Do not add the following before the visual prototype is reviewed:

- Production authentication
- Real-time messaging
- End-to-end encryption
- Purchases
- Voice calls
- Video calls
- Public discovery

The purpose of the first milestone is to make Luma visible, navigable, and reviewable as a real mobile experience.

---

## Release Gates

Luma should not launch publicly until the following gates are satisfied.

### Product gates

- Core messaging works reliably.
- Offline retry works.
- Account deletion works.
- Block and report work.
- Privacy settings work.
- Notifications do not leak sensitive text.
- Room authorization works.
- Failed messages are handled safely.

### Security gates

- Authentication has been tested.
- Authorization has been tested server-side.
- No critical unresolved vulnerabilities remain.
- Secrets are not exposed.
- Dependencies have been reviewed.
- Logs do not contain message content.
- Media uploads are validated.
- Sessions can be revoked.
- Abuse controls are functioning.
- Security documentation is current.

### Privacy gates

- Data collection is documented.
- Privacy policy is accurate.
- Retention rules are defined.
- Deletion behavior is tested.
- User visibility controls work.
- Notification privacy is tested.
- Analytics do not collect sensitive content.

### Quality gates

- TypeScript passes.
- Automated tests pass.
- Android builds work.
- iOS builds work.
- Poor-network behavior is tested.
- Accessibility is reviewed.
- Reduced-motion behavior works.
- Crash reporting is configured safely.
- Performance is acceptable.
- Large chat histories are tested.

---

## Development Workflow

### Current repository state

The repository is currently documentation and branding focused. A complete Expo application has not yet been created.

Before using commands, confirm that `package.json` and the required scripts exist.

### Planned local workflow

After the Expo project is created, the expected workflow will be similar to:

```bash
npm install
npx expo start
```

Then choose one of the available previews:

- Scan the QR code with Expo Go.
- Press the Android emulator option.
- Press the iOS simulator option on macOS.
- Open the optional web preview.

These commands should be treated as planned until the Expo project and `package.json` are added.

### Suggested development sequence

1. Work on a focused feature or milestone.
2. Update related documentation.
3. Test on a real mobile device when possible.
4. Test loading, empty, success, offline, and error states.
5. Check accessibility and reduced motion.
6. Avoid adding features outside the approved milestone.
7. Keep security and privacy requirements visible during implementation.
8. Record important decisions in `docs/decision-log.md`.

---

## Documentation Map

The repository should eventually include:

| Document | Purpose |
|---|---|
| `docs/product-constitution.md` | Product principles and non-negotiable direction |
| `docs/version-1-specification.md` | Detailed Version 1 requirements |
| `docs/security-threat-model.md` | Threats, risks, and mitigations |
| `docs/security-requirements.md` | Security controls and release requirements |
| `docs/privacy-requirements.md` | Data collection, visibility, retention, and deletion |
| `docs/design-system.md` | Colors, typography, spacing, motion, and components |
| `docs/architecture.md` | Mobile, backend, storage, sync, and infrastructure architecture |
| `docs/roadmap.md` | Phased product and engineering roadmap |
| `docs/decision-log.md` | Important decisions and their reasoning |
| `README.md` | Main developer-facing project guide |

Documentation should be updated when implementation decisions change.

---

## Contribution Guidance

Contributions should preserve the core Luma direction.

Before adding a feature, confirm:

- Is it part of the approved milestone?
- Does it support meaningful connection?
- Does it respect privacy?
- Does it avoid manipulative engagement?
- Is the mobile experience clear?
- Is the feature accessible?
- Does it require new data collection?
- Does it introduce security or abuse risks?
- Does it need documentation or threat-model updates?

Avoid adding features simply because they are common in other social applications.

The product should remain focused, calm, private, and meaningful.

---

## Security Reporting

Do not include secrets, private credentials, user data, message content, or sensitive security details in public issues.

For a suspected vulnerability:

1. Use the repository's private security reporting mechanism if available.
2. Otherwise, use a private GitHub Security Advisory report.
3. Include a clear description of the issue.
4. Include reproduction steps where safe.
5. Explain the potential impact.
6. Avoid publicly disclosing the issue before it is assessed and resolved.

Security reports should not be used to share private user information.

---

## Current Status Checklist

### Product

- [x] Product name selected: Luma
- [x] Tagline selected: “Your people, your space.”
- [x] Living social rooms concept defined
- [x] Premium dark-first direction defined
- [x] Version 1 scope defined
- [x] Future roadmap defined

### Branding

- [x] Initial SVG logo asset created
- [ ] Final logo symbol approved
- [ ] Wordmark created
- [ ] App icon version created
- [ ] Monochrome version created
- [ ] Splash-screen composition created
- [ ] Brand preview approved

### Mobile application

- [ ] Expo project created
- [ ] React Native foundation created
- [ ] TypeScript configured
- [ ] Theme tokens created
- [ ] Navigation created
- [ ] Splash screen created
- [ ] Welcome screen created
- [ ] Authentication UI created
- [ ] Privacy onboarding created
- [ ] Home mockup created
- [ ] Rooms mockup created
- [ ] Chat mockup created
- [ ] Memories mockup created
- [ ] Expo Go preview tested

### Backend and security

- [ ] Production authentication implemented
- [ ] Backend created
- [ ] Database created
- [ ] Real-time messaging implemented
- [ ] Offline synchronization implemented
- [ ] Push notifications implemented
- [ ] Media uploads implemented
- [ ] Security testing completed
- [ ] Privacy review completed
- [ ] Independent security review completed

---

## What to Build Next

The next implementation milestone is:

1. Create the Expo mobile foundation.
2. Add TypeScript configuration.
3. Add Luma theme tokens.
4. Add the logo and branding assets.
5. Build the splash screen.
6. Build the Welcome screen.
7. Build Sign In and Sign Up interfaces.
8. Build privacy onboarding.
9. Build the navigation shell.
10. Build Home, Rooms, Chat, and Memories mockups.
11. Add mock data.
12. Test the mobile prototype through Expo Go.
13. Review the visual structure before starting production backend work.

The goal is to create a real, viewable mobile prototype that demonstrates the Luma experience before adding authentication, real-time messaging, media, or advanced features.

---

## Final Product Statement

Luma is a premium, privacy-first social chat application where people do more than exchange messages.

They create private rooms, share their presence, plan activities, preserve memories, complete meaningful group experiences, and build a digital space that feels like it belongs to them.

> **Luma — Your people, your space.**