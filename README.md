# Simple Craps

[![Android API](https://img.shields.io/badge/API-23%2B-brightgreen.svg)](https://android-arsenal.com/api?level=23)
[![Kotlin](https://img.shields.io/badge/Kotlin-2.1-blue.svg)](https://kotlinlang.org)
[![Compose](https://img.shields.io/badge/Jetpack-Compose-orange.svg)](https://developer.android.com/jetpack/compose)

A professional-grade Craps simulator for Android, modeled after modern "Bubble Craps" electronic machines. Perfect for practicing strategies with authentic odds, full betting support, and a transparent, player-friendly advertising model.

## Key Features

- **Authentic Gameplay:** Complete support for Pass Line, Don't Pass, Come, Don't Come, Place, Buy, Lay, Hardways, and Proposition bets.
- **Game Modes:** Seamlessly toggle between **Classic**, **Crapless**, and **Easy Craps** variants.
- **Practice Mode:** Enable "Betless Rolls" in settings to throw dice without active bets, ideal for testing strategies or tracking streaks.
- **True Odds:** Mathematically accurate payouts, including commissions (vig) for Buy and Lay bets.
- **Strategies & Tips:** Contextual strategy guides for every betting tab to help you master the game.
- **Modern UI:** A sleek, edge-to-edge Jetpack Compose interface that adapts beautifully to any screen size.
- **Privacy First:** No accounts, no trackers, and no data collection. All game data and roll history stay securely on your device.
- **Fair Ad Model:** Play ad-free with a $50 bankroll reset, or watch a single rewarded ad for a "High Roller" bankroll.
- **Pro Upgrade ($3.99):** A one-time purchase to remove the rewarded ad requirement forever, unlock the **Sevenless** practice mode, and enjoy a premium, ad-free experience.

## Tech Stack

- **Language:** Kotlin 2.1
- **UI Framework:** Jetpack Compose (Material 2)
- **Billing:** Google Play Billing Library 9.1.0
- **Ads:** Google Mobile Ads (AdMob) 25.4.0 with Meta Mediation
- **Architecture:** MVVM with State-driven UI

## Release History

### v1.24 (In Development)
- **Analytics Precision**: Renamed custom ad reward events to `sevenless_reward_granted` to prevent double-counting of standard AdMob `ad_reward_earned` events.
- **Sevenless Reward Guard**: Implemented a 20-roll stacking limit to prevent excessive accumulation of "loaded dice" rolls.
- **Smart Ad Optimization**: Maintained the 5-minute request cooldown for background ad loading to protect the app's Match Rate, while keeping manual reward buttons always accessible via the 30-second fallback timer.

### v1.23
- **Practice Mode Evolution**: Renamed "Free Rolls" to **Betless Rolls** and added a **Roll Animation** toggle to allow for faster, strategy-focused practice sessions.
- **Pro Upgrade Value Increase**: Adjusted Pro Upgrade price to **$3.99** and included the **Sevenless** mode as a permanent premium feature.
- **Sevenless Practice (Ad-Supported)**: Added the ability to watch a single rewarded ad to unlock **10 Sevenless Rolls** (no 7s), allowing users to practice strategy setups or track long-roll scenarios without the risk of a "Seven Out."
- **Statistical Integrity**: Sevenless rolls (Pro or Rewarded) are automatically excluded from Heatmaps, Roll Frequency, and All-Time Records to ensure user statistics remain authentic and reflect true casino variance.
- **UI Enhancements**: Added high-visibility indicators for **Sevenless Rolls** and remaining rewarded rolls directly in the game header. Updated layouts for full **Target SDK 37** compliance.
- **IMPROVED: Ad Request Backoff**: Implemented a 5-minute cooldown following ad load failures. This prevents redundant background requests during network instability, protecting the app's Match Rate and maintaining a high eCPM.
- **Robust Hop Bets**: Refactored Hop bet win-detection from string-based parsing to a robust, data-driven model within the `BetType` enum.
- **Enhanced Custom Chips**: Expanded the chip selection bar to include two fully customizable slots (5th and 6th). Introduced a new **Lime Green** color tier for high-value units and added a "Reset" option to easily revert to wealth-based defaults.

### v1.22
- **UI & Transparency**: Introduced contextual roll history coloring for 7s, interactive payout formulas, and detailed financial summaries in the roll breakdown. Redesigned indicators and buttons for theme consistency.
- **Customization & Layout**: Added the ability to cycle through classic number layouts and swap Place/Buy vertical positions for personalized ergonomics.
- **Ad Reliability & Economics**: Implemented a "Smart Loading" model with late caching, background ad promotion, and an enforced 30s fair-wait policy to stabilize impressions and revenue.
- **Enhanced Physics**: Re-engineered dice animations with a 3-phase decelerating sequence and synchronized haptics for a more realistic tactile feel.
- **Practice Features**: Added a toggle to roll the dice without active bets (originally "Free Rolls"), ideal for practicing throws or tracking streaks without risking bankroll.
- **Platform & Maintenance**: Full compatibility with **Android 16 (API 36)**, Billing Library **v9.1.0**, and optimized R8 shrinking for smaller, faster performance.

### v1.21
- **Enhanced Payout Feedback**: New status bar showing exactly how your bank and bets changed on each roll.
- **Display Toggles**: Easily switch between detailed payout breakdowns and traditional "Won" readouts.
- **Roll Breakdown**: Itemized "Last Roll" summary showing exactly which of your bets won or lost.
- **UI Refinements**: Reorganized game status and dice layout for better center-screen visibility.
- **Bug Fixes**: Corrected potential payout displays and optimized bet category mappings.

### v1.20
- **Visual Bet Feedback & Lock Logic**: Added clear visual indicators (red prohibitory icons) and contextual "Bet Locked" explanations for contract bets and unavailable wagers.
- **Enhanced Ad Mediation**: Switched to a real-time bidding model with **Meta Audience Network** integration for better fill rates and improved battery/data efficiency.
- **Reliability & Safeguards**: Integrated a 30-second ad fallback timer (auto-granting rewards if ads fail) and a "LOADING..." state with interaction locks to prevent UI ghosting.
- **Maintenance**: Refined internal ad wrappers and optimized SDK lifecycle for broad Android 6.0 (API 23+) compatibility and memory safety.

### Legacy Versions (v1.10 - v1.19)
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

### Professional Analytics
- **Cloud Data Export:** Securely export roll history and session logs to Google Drive for advanced personal analysis.

### UI/UX Improvements
- **Tab Layout Manager:** A new customization tool to rearrange betting tab order or enable a **Split-View Mode**, allowing users to stack two betting areas (e.g., Pass Line and Hardways) on screen simultaneously.
- **Landscape Support:** A dedicated horizontal layout to provide a more immersive "Wide-Table" experience, especially for tablet users.
- **Quick Navigation:** Optional "Screen Jump" to return to the main betting area immediately after a roll.

---
*Created and maintained by Simple Craps.*