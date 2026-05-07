# Changelog

All notable changes to BitTasker are documented in this file.

---

## [1.1.3] - 2026-05-07

### 🔗 Deep Linking
- Added deep link navigation support across the application
- Implemented Apple deep link compatibility
- Improved authenticated navigation flows with `returnTo` redirects after login

### ⚡ Nostr Improvements
- Fixed metadata Nostr event handling when logging in with `nsec`
- Added safeguards to ensure metadata events are properly published

### 🎨 UI/UX Improvements
- Improved contract drawer layout and visual consistency

### 🐛 Bug Fixes
- Fixed navigation edge cases during login redirects
- Resolved minor contract drawer UI rendering issues

---

## [1.1.2] - 2026-05-06

### 🏠 Homepage Redesign
- Completely redesigned featured task and service cards
- Added prominent “Budget” and “Price” labels for better visibility
- Added location display with map marker icons
- Introduced line-clamped descriptions for consistent card sizing
- Removed duplicate “View Task” / “View Service” text labels
- Removed “View All” links from homepage section headers

### 🚨 Alert Experience Improvements
- Redesigned saved search alert cards to match platform card styles
- Replaced filter badges with icon + text metadata rows
- Added notification frequency display with bell icon
- Unified edit/delete action styling with service card actions
- Replaced alert edit/save modal with right-side drawer flow
- Removed active/inactive toggle (alerts now remain active until deleted)
- Changed default notification frequency from Weekly → Instant
- Improved alert filter summaries using icon-based layouts

### 🛠️ Services UX Improvements
- Unified service detail drawer with create-service preview component
- Renamed “View Quotes” → “Inquiries” with updated EN/ES translations
- Consolidated service action buttons into a single responsive row
- Added “New” CTA button next to the Map button on services browse page
- Added “List Your Service” CTA after scrolling through service results
- Reduced mobile header spacing on services pages

### 🧭 Navigation & Menu Updates
- Added “My Account” section to mobile bottom navigation
  - Includes Profile and Settings shortcuts
- Simplified logged-in support menu
  - Removed About Us, Terms of Service, and Privacy Policy entries
- Updated avatar dropdown navigation
  - Added Hiring and Earning shortcuts
  - Removed Dashboard, Find Tasks, and Contracts links
- Shortened Spanish login label from “Iniciar Sesión” → “Iniciar”

### 📅 Data & Display Refinements
- Simplified bid date formatting by removing year display
- Improved same-day date handling to avoid duplicate ranges
- Removed “USD” suffix from contract amount displays

### 🎨 UI/UX Improvements
- Improved layout consistency and responsive spacing across devices
- Fixed overlapping top navigation bars across platforms
- Fixed overlapping bottom navigation bars across platforms
- Resolved keyboard overlay issues covering input fields
- Centered app store badges in mobile footer
- Unified footer spacing between Hiring and Earning pages
- Improved theme-aware colors for three-dot menus

### 🐛 Bug Fixes
- Fixed service title visibility on filtered request cards
- Fixed create-service cancel button navigation behavior
- Moved filter drawer categories to the top for better discoverability
- Disabled swipe-to-close gesture on wallet payment modal

---

## [1.1.1] - 2026-05-05

### 💰 Bids UX Improvements
- Updated the “Your Offer” section UI
- Added icons for improved visual identification
- Improved date layout readability
- Standardized sats formatting for better consistency and precision

### 🎨 UI/UX Improvements
- Refined bid presentation and offer information hierarchy
- Improved readability across bidding flows

---

## [1.1.0] - 2026-04-30

### ⛽ Gasless Meta-Transactions (EIP-712)
- Implemented gasless relay for secure-payment contract writes
- Added EIP-712 compliant meta-transaction routing
- Enabled escrow operations without requiring gas tokens

### 🛠️ Services Platform
- Full service lifecycle implementation:
  - Service creation with pricing tiers, add-ons, and location
  - Service discovery by category and location
  - Instant booking with direct payments
  - Quote/inquiry workflow for providers
  - End-to-end service contract lifecycle
- Google Maps integration for location display
- Media gallery support (images/videos)

### 📜 Escrow V2 Contracts
- Complete escrow architecture overhaul
- Dynamic contract versioning for backward compatibility
- Service-specific contracts with agreement snapshots
- Improved lifecycle and state management

### 🎨 UI/UX Improvements
- Improved mobile keyboard handling (VisualViewport API)
- Enhanced wallet receive form validation
- Better mobile layout for network fee display
- Unified layout spacing across hiring/earning pages
- Improved service detail responsiveness

### 🔧 Infrastructure
- Migrated localStorage → Preferences for mobile compatibility
- Added reusable booking timeline components
- Introduced contract action UI variants with tests
- Added service provider location collection

### 🐛 Bug Fixes
- Fixed instant buy logic and translation issues
- Fixed topbar avatar dropdown behavior
- Fixed contract action loading states
- Fixed desktop service viewport height
- Fixed quote contract creation
- Fixed category dropdown infinite loop
- Resolved multiple translation inconsistencies

### 🌐 Translations
- Added full Spanish localization for core flows

---

## [1.0.6] - 2026-04-21

### ⌨️ Keyboard & Input
- Resolved layout conflicts with keyboard plugin updates
- Fixed bottom navigation overlap with active keyboard
- Improved navigation state handling to prevent wallet resets

### 💰 Wallet & Provider Infrastructure
- Refactored provider health checks to use RPC calls
- Fixed race conditions via strict initialization ordering
- Added retry logic with exponential backoff for balance fetching
- Introduced `softCleanup()` for graceful disconnections
- Improved price service reliability and error handling

---

## [1.0.5] - 2026-04-09

### 📱 Play Store Compliance & Privacy
- Implemented Google Play compliance requirements
- Added account deletion flow
- Refactored permissions (location, notifications)
- Disabled sending PII to Sentry
- Cleaned up Capacitor configuration

### 🚨 Reporting & Notifications
- Added in-app reporting and user mute
- Added notification opt-in banner

### 🌐 API & Localization
- Introduced API-driven translation system
- Migrated backend from GraphQL to REST

### 🎨 UX Improvements
- Reduced excessive haptic feedback
- Improved UI consistency and interaction polish

### 🔧 Maintenance
- Removed unused code and dependencies
- Improved overall stability and maintainability

---

## [1.0.4] - 2026-01-27

### 🔐 Escrow & Contracts
- Fixed bid acceptance reliability
- Fixed address checksum validation
- Improved contract UI and state handling
- Fixed infinite loading issues

### 💰 Wallet
- Fixed Lightning max amount calculation
- Fixed missing transaction records post-swap
- Improved wallet translations and UI

### 🎨 UI/UX
- Added user profile display component
- Improved task and bid layouts
- Added media lightbox with video support
- Improved dashboard and mobile layouts

### 🌐 Sharing & Localization
- Integrated native sharing
- Fixed translation conflicts
- Added new localized content

### 🔧 Technical
- Added Cloudflare Workers observability
- Replaced BSCScan with Binance RPC
- Fixed build issues and accessibility warnings
- Standardized date handling

### 🔑 Auth & Security
- Improved passkey handling
- Cleared user data on logout
- Fixed login redirect flow

### ⚡ Performance
- Improved caching and state management
- Optimized rendering performance

---

## [1.0.3] - 2026-01-22

### 🎨 UI/UX
- Improved layout stability and responsiveness
- Fixed bottom navigation overlap issues
- Enhanced mobile navigation experience

### 💰 Wallet & Payments
- Fixed RBTC calculations and fee estimation
- Fixed wallet initialization and balance loading
- Implemented EIP-1191 address checksums
- Patched Lightning invoice issues

### 🔔 Notifications
- Improved contract and messaging notifications
- Fixed duplicate notifications
- Updated notification UI

### 🔧 Technical
- Integrated Sentry error tracking
- Added Android live reload support
- Improved build system and caching

### 🧪 Developer Experience
- Added debug wallet tools
- Improved logging and diagnostics

### ✏️ Features & Content
- Increased task budget limits
- Refactored sharing and validation logic
- Removed native passkey button

### 🔍 SEO & Performance
- Improved structured data
- Added WEBP assets

---

## [1.0.2] - 2026-01-12

### 🔧 Authentication
- Fixed WebAuthn/Passkey support on Android
- Resolved RP ID validation issues
- Configured domain association and asset links

---

## [1.0.1] - 2026-01-09

- Minor release
- Internal updates and fixes

---

## [1.0.0] - 2026-01-09

### 🎉 Initial Release
- **Initial Release**: Launch of BitTasker on Android[cite: 1].
- **Payments**: Lightning Network (Breez SDK) and Liquid Network support[cite: 1].
- **Identity**: Nostr identity integration and NIP-44 encrypted messaging[cite: 1].
- **Core Features**: Task bidding, escrow system, and reputation/review system[cite: 1].
- **Security**: Client-side key management with biometric authentication[cite: 1].

---