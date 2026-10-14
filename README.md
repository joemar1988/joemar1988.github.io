# Simple Craps

[![Android API](https://img.shields.io/badge/API-24%2B-brightgreen.svg)](https://android-arsenal.com/api?level=24)
[![Kotlin](https://img.shields.io/badge/Kotlin-2.1-blue.svg)](https://kotlinlang.org)
[![Compose](https://img.shields.io/badge/Jetpack-Compose-orange.svg)](https://developer.android.com/jetpack/compose)

A professional-grade Craps simulator for Android, modeled after modern "Bubble Craps" electronic machines. Perfect for practicing strategies with authentic odds, full betting support, and a transparent, player-friendly advertising model.

## Key Features

- **Authentic Gameplay:** Complete support for Pass Line, Don't Pass, Come, Don't Come, Place, Buy, Lay, Hardways, and Proposition bets.
- **Game Modes:** Seamlessly toggle between **Classic**, **Crapless**, and **Easy Craps** variants.
- **Full Table View:** Toggle between traditional betting tabs and an immersive, zoomable 2D Full Craps Table layout with dual-orientation auto-fit, 3-tier point squares, and customizable 2-row splits for Crapless/Easy Craps.
- **Practice Mode:** Enable "Betless Rolls" in settings to throw dice without active bets, or use "Sevenless Practice" to isolate point strategy testing.
- **True Odds:** Mathematically accurate payouts, including commissions (vig) for Buy and Lay bets.
- **Strategies & Tips:** Contextual strategy guides for every betting tab to help you master the game.
- **Modern UI:** A sleek, edge-to-edge Jetpack Compose interface that adapts beautifully to portrait and landscape screen orientations.
- **Google Play Games on PC & Desktop:** Full compatibility with Google Play Games for PC and Chromebooks, featuring mouse/trackpad controls, custom window resizing, and dark felt launch window styling.
- **Sevens Streak Analytics (7S Tab):** Dedicated 4-column statistical table tracking rolls between sevens (0 to 30+) compared against theoretical geometric probabilities formatted to 2 decimal places.
- **Full Table View & Section Minimization:** Toggle between traditional betting tabs and a zoomable 2D Full Craps Table layout featuring 1-tap `−` / `+` minimization controls for One-Roll and Hardways sections to maximize screen space on any device.
- **Privacy First:** No accounts required. All game data and roll history stay securely on your device, with full Google UMP consent support.
- **Fair Ad Model:** Play ad-free with a $50 bankroll reset, or watch a single rewarded ad for a "High Roller" bankroll.
- **Pro Upgrade ($4.99):** A one-time purchase to remove the rewarded ad requirement forever, unlock the **Sevenless** practice mode, and enjoy a premium, ad-free experience.

## Tech Stack

- **Language:** Kotlin 2.1
- **UI Framework:** Jetpack Compose (Material 2)
- **Billing:** Google Play Billing Library 9.1.0
- **Ads & Privacy:** Google Mobile Ads (AdMob) 25.4.0 with Meta Mediation (6.22.0.1) & Google UMP 4.0.0
- **Analytics:** Firebase Analytics (BOM 34.19.0)
- **Architecture:** MVVM with State-driven UI

## Release History

### v1.29
- **Unified Quick Bulk Betting**: Added 1-tap `BUY ALL` (1st) and `PLACE ALL` / `PRESS ALL` (2nd) buttons above point numbers in Full Table View across all game modes and orientations.
- **Classic Don't Come Layout**: Added a 50/50 split `DON'T COME` line and dedicated Don't Come / Don't Odds rows on point cards in Classic Craps mode.
- **Table Section Minimization Controls (`−` / `+`)**: Added 1-tap collapse/expand toggles for One-Roll & Hop Bets and Hardways sections in Full Table View (collapsing into 36dp vertical strips in landscape or 1-line bars in portrait) to give players complete screen real estate flexibility.
- **House Rules Customizations**: Added new House Rules settings for Any 7 Payouts (4:1 Standard vs 5:1 Generous) and Don't Pass Max Odds limits (Same as Pass, 2x Pass Odds, 4x Pass Odds, or custom multipliers).
- **Top Bar Layout Stability**: Locked top action buttons (Stats, Cash/Reset, Email, Info, Settings) to fixed dimensions, preventing top bar overflow or Settings button clipping when increasing UI Scale.
- **Sevens Streak Frequency Table (7S Tab)**: Added a 4th tab in the Statistics dialog tracking rolls between sevens (0 to 30+) with 2-decimal accuracy against exact theoretical geometric distribution odds.
- **Google Play Games on PC Optimization**: Added dark casino felt window background (`android:windowBackground`) and non-blocking UMP consent handling for instant desktop launching.
- **Table Layout Analytics**: Added dedicated Firebase Analytics logging for Full Table View vs Tabbed View toggles and user preference trends.
- **Enhanced Settings Event Tracking**: Extended analytics tracking across all settings toggles, dice color selections, and felt theme customizations.

### v1.28
- **Full Table View Layout Mode**: Added an authentic, zoomable 2D Full Craps Table layout with dual-orientation support (3-column spread in landscape, vertical stack in portrait).
- **Crapless & Easy Craps Come Bet Logic**: Updated Come bet logic so `2`, `3`, `11`, and `12` establish valid Come Points with mathematically accurate true odds payouts.
- **Startup State & Dice Restoration**: Ensured dice, active point, puck status, and table bets restore right where the player left off on app relaunch (defaulting to snake eyes `1, 1` on first startup).
- **Platform & Dependency Upgrades**: Upgraded to minSdk 24 for Play Protection, Android 15 edge-to-edge compliance, Meta Mediation (6.22.0.1), Firebase BOM (34.19.0), and Kotlin 2.1.
- **Bet Layout & UX Enhancements**: Set BUY bets to top by default, standardized item heights (`55dp`), and optimized bet placement hit targets.

### v1.27
- **Pro Upgrade List Price**: Updated the Pro upgrade list price to $4.99 ($4.99 one-time purchase).
- **Enhanced Analytics**: Added Firebase Analytics tracking for bankroll resets, distinguishing between Pro and regular user resets (`user_type`, `is_pro_user`, and reset events).
- **Lay Odds & Payout Fixes**: Fixed Lay Odds potential win calculations to use zero-vig true odds and corrected 1:1 payout displays for Don't Pass and Don't Come bets.
- **Terminology & Visual Roll History**: Standardized odds labels to Pass Line / Don't Pass Odds and added semantic color-matched miniature dice pair icons to roll history.
- **Session Stats & Profit Calculations**: Ensured session roll history and heatmaps persist across restarts until bankroll reset, and updated net profit percentage calculations.

### v1.26
- **Touch Target Layering Fix**: Resolved critical regression making Information (i) and Close (X) buttons unclickable on bets and the BETS puck.
- **Icon Standardization**: Restored betting icons to original compact size with consistent, large hit-targets.
- **Preset Confirmation**: Added clear confirmation dialogs when saving Manual Bet Presets.
- **Settings & Audio Persistence**: Restored "Set Default" bankroll persistence and fixed audio/haptics toggles continuing when disabled.
- **Core Architecture Sync**: Improved state synchronization between the game engine and repository to eliminate preference UI lag.

### v1.25
- **Ergonomic Landscape Layout**: Added dedicated landscape view with immersive full-screen mode, safe-area sidebars, and high-density betting rows.
- **Contextual Roll History**: Redesigned roll history with bright green (wins), blue (points), red (7-out), and light blue (point set) status coding.
- **Rotation & State Persistence**: All volatile state, active dialogs, statistics, and roll breakdowns now persist through screen rotation.
- **Manual Bet Presets & Clean Mode**: Added preset table saving/loading and a setting to hide informational (i) icons for a minimalist UI.
- **Architecture Refactor**: Decoupled ViewModel from storage with a dedicated `SettingsRepository` for cleaner state management.

### Legacy Versions (v1.10 - v1.24)
- **v1.24**: Added Sevenless Practice mode, Lime Green custom chip slot, Betless Rolls evolution, and Android 16 compatibility.
- **v1.23**: Identical to v1.24, with a bankroll refresh bug where users couldn't set their default refresh value.
- **v1.22**: Added contextual roll history, cycling number layouts, smart ad loading, and 3-phase dice animations.
- **v1.21**: Added payout status bar, itemized roll breakdown, and UI layout refinements.
- **v1.20**: Added "Bet Locked" feedback, Meta Ad Mediation, and 30-second reward safety timers.
- **v1.19**: Added "About" section, Table Limits UI, and fixed Ad Lifecycle bugs.
- **v1.18**: Added Firebase Analytics support and optimized build performance with R8 Full Mode.
- **v1.17**: Added Quick Actions (Undo/Repeat), Custom Betting Unit, and UI/Navigation improvements.
- **v1.16**: Added Unified Come Points, Hop Bets, and Betting Tab reorganization.
- **v1.15**: Added Stats Persistence and Come/Don't Come chip stacking.
- **v1.14**: Added Last Roll Performance, Luck Color Coding, Odds/Field settings, and Statistics refinements.
- **v1.13**: Added Analytics Heatmap, Streak Tracking, and corrected ATS & Don't Come logic.
- **v1.12**: Added Custom Reset Amount and a redesigned, prioritized Reset Menu UI.
- **v1.11**: Added Strategies & Tips overlay, Persistent Bankroll, and Data Deletion options.
- **v1.10**: Added Screen Scaling, Classic/Crapless/Easy Craps mode, analytics, and tutorial.

---

## Roadmap

I am actively developing the following features to make Simple Craps the ultimate practice tool:

### Advanced Simulation & Logic
- **Strategy Assistance:** An interactive guide that highlights optimal betting placements based on selected systems (Iron Cross, Three-Point Molly, etc.).
- **Audio Calls:** High-quality audio implementation for authentic "Bubble Craps" atmosphere.
- **Choose your roll:** Add in functionality for the user to choose their next roll (or for pro users to turn on choosing their roll)

### Professional Analytics
- **Cloud Data Export:** Securely export roll history and session logs to Google Drive for advanced personal analysis.

### UI/UX Improvements
- **Big Wins:** More Celebration on ATS or any other bigger wins.

---
*Created and maintained by Simple Craps.*