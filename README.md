# Simple Craps 🎲

[![Android API](https://img.shields.io/badge/API-23%2B-brightgreen.svg)](https://android-arsenal.com/api?level=23)
[![Kotlin](https://img.shields.io/badge/Kotlin-2.1-blue.svg)](https://kotlinlang.org)
[![Compose](https://img.shields.io/badge/Jetpack-Compose-orange.svg)](https://developer.android.com/jetpack/compose)

A professional-grade Craps simulator for Android, modeled after modern "Bubble Craps" electronic machines. Perfect for practicing strategies with authentic odds, full betting support, and a transparent, player-friendly ad model.

## ✨ Key Features

- **🎰 Authentic Gameplay:** Complete support for Pass Line, Don't Pass, Come, Don't Come, Place, Buy, Lay, Hardways, and Proposition bets.
- **🔄 Game Modes:** Seamlessly toggle between **Standard**, **Crapless**, and **Easy Craps** variants.
- **⚖️ True Odds:** Mathematically accurate payouts, including commissions (vig) for Buy and Lay bets.
- **📘 Strategies & Tips:** Contextual strategy guides for every betting tab to help you master the game.
- **📱 Modern UI:** A sleek, edge-to-edge Jetpack Compose interface that adapts beautifully to any screen size.
- **🔒 Privacy First:** No accounts, no trackers, and no data collection. All game data and roll history stay securely on your device.
- **💎 Fair Ad Model:** Play ad-free with a $50 bankroll reset, or watch a single rewarded ad for a "High Roller" bankroll.
- **🏆 Pro Upgrade ($2.99):** A one-time purchase to remove the rewarded ad requirement forever and unlock a premium, ad-free experience.

## 🛠 Tech Stack

- **Language:** Kotlin 2.1
- **UI Framework:** Jetpack Compose (Material 3)
- **Billing:** Google Play Billing Library 7.1
- **Ads:** Google Mobile Ads (AdMob)
- **Architecture:** MVVM with State-driven UI

---

## 📝 Release History

### v1.15
- **NEW**: **Stats Persistence**. The Statistics dialog now remembers your last active tab (Hand/Session/All-Time) across app restarts.
- **IMPROVED**: **Come/Don't Come Stacking**. Multiple chips of any denomination can now be placed on the Come and Don't Come bars before a point is established.

### v1.14
- **NEW**: Added **Last Roll Performance**. Review your last 2 rolls from point to 7 out and see how you did.
- **NEW**: Added **Luck Color Coding**. Roll percentages are now color-coded (Green for lucky, Red for unlucky) relative to theoretical probability, with 7s being opposite.
- **NEW**: Added **Odds Limit Setting**. Toggle between different odds limits (3x-4x-5x, 10x) for Pass and Come bets.
- **NEW**: Added **Field 12 Payout Setting**. Toggle Field payout on 12 (3:1).
- **IMPROVED**: Refined **All-Time Records**. Session-based records (like "Most Rolls Without 7") now update only upon session finalization (manual reset) for greater accuracy and purpose-driven practice.
- **IMPROVED**: Refined **Statistics UI**. Merged redundant roll records into a cleaner, more focused layout that prioritizes your longest hot streaks.

### v1.13
- **NEW:** Added **Professional Analytics Heatmap**. View a color-coded frequency distribution of your last 100 rolls (Hot/Warm/Avg/Cool/Cold) compared to theoretical probability.
- **NEW:** Added **Streak Tracking**. Monitor "Rolls Since Last 7" in real-time and compete against your all-time record for the longest "hot streak" without a 7.
- **NEW:** Added **Upgrade Prompt** in the Refresh Bankroll menu for a quicker, more convenient path to the Pro version.
- **FIXED:** Corrected **ATS (All-Tall-Small) Logic**. Bonus bets now correctly clear from the table immediately upon a 7-out, matching authentic casino rules.
- **FIXED:** Resolved **Don't Come Payout Bug**. Corrected the math for established points on the Don't Come line; the bet now correctly loses when the point hits and wins only on a 7-out.
- **IMPROVED:** Standardized **Dialog UI**. Refined the Strategies, Tips, and Stats windows with a consistent professional layout featuring fixed headers and rounded surfaces.
- **IMPROVED:** Enhanced **Data Persistence**. Roll history and advanced statistics now persist across app restarts using serialized JSON storage.
- **IMPROVED:** Updated **SDK Compatibility**. Aligned project with `compileSdk 36` to support the latest AndroidX library metadata requirements.

### v1.12
- **NEW:** Added **Custom Reset Amount**. All players can now set and save their own preferred bankroll refresh value directly within the reset menu for faster, more personalized practicing.
- **NEW:** Added **PRO Interface Debug Toggle**. Developers can now seamlessly switch between PRO and non-PRO interface modes in debug builds to test both user experiences.
- **IMPROVED:** Redesigned **Reset Menu** UI with a new two-row button layout. Featured options like "Default" and "50" are now prioritized, followed by an organized grid of high-roller selections.
- **IMPROVED:** Refined custom input logic; the custom amount field now defaults to empty, and reset actions are enabled only when a valid positive value is entered.

### v1.11
- **NEW:** Added **Strategies & Tips** overlay for every betting tab. Learn classic systems like the Three-Point Molly, Iron Cross, and more directly while playing.
- **NEW:** Added **Persistent Bankroll & Bets**. Your balance and active bets are now saved automatically and restored when you reopen the app.
- **NEW:** Added **Data Deletion** option in Settings. Users can now permanently erase all local app data and statistics directly from the device.
- **IMPROVED:** Redesigned **Settings & Statistics** menus with fixed "sticky" headers and footers for a smoother, more professional navigation experience.
- **IMPROVED:** Added **In-App Rating Button** to the home screen, highlighting our "no-interruption" philosophy and allowing users to easily support the app.
- **IMPROVED:** Added **System Font Override** to prevent layout distortion on devices with large accessibility font settings.
- **IMPROVED:** Refined **Bankruptcy Protection**; if your total value (bank + bets) falls below $50, the app will automatically reset to a fresh $50 bankroll if closed and reopened.

### v1.10
- **NEW:** Added **Screen Scaling** to ensure a perfect fit across diverse Android device sizes and aspect ratios.
- **NEW:** Added **Easy Craps** mode, streamlining the game by eliminating the need for Place/Buy bets.
- **NEW:** Added **Performance Tracking** to monitor your "Highest Win Percentage" and session trends.
- **NEW:** Added **Session Analytics** to view "Average Plays per Session" and other statistics to gauge bankroll longevity.

### v1.9
- **NEW:** Integrated **Google Play Billing** for the Pro Upgrade.
- **NEW:** Refined betting descriptors for **ATS (All-Tall-Small)** bets.
- **NEW:** Expanded customization with additional dice and felt colors in Settings.

### v1.8
- **NEW:** Added "Standard" and "Crapless" mode toggles (Pucks).
- **IMPROVED:** Interactive tutorial for new players.
- **IMPROVED:** Full compliance with **Android 15** edge-to-edge requirements.
- **LEGAL:** Updated Privacy Policy and Terms of Service transparency.

---

## 🚀 Roadmap

I am actively developing the following features to make Simple Craps the ultimate practice tool:

### 🎮 Advanced Simulation & Logic
- **Strategy Assistance:** An interactive guide that highlights optimal betting placements based on selected systems (Iron Cross, Three-Point Molly, etc.).
- **Stickman Calls:** High-quality audio implementation for authentic "Bubble Craps" atmosphere.

### 📊 Professional Analytics
- **Cloud Data Export:** Securely export roll history and session logs to Google Drive for advanced personal analysis.

### 🎨 UI/UX Improvements
- **Unified Come/Don't Come Tab:** Merge Come and Don't Come betting areas into a single tab for more efficient navigation, featuring both betting bars at the top and a combined list of established point bets below.
- **Compact Established Bets:** Redesign the established bet layout to use a more space-efficient 2-bets-per-line grid, optimizing screen real estate for players with multiple active points.
- **Tab Layout Manager:** A new customization tool to rearrange betting tab order or enable a **Split-View Mode**, allowing users to stack two betting areas (e.g., Pass Line and Hardways) on screen simultaneously.
- **Landscape Support:** A dedicated horizontal layout to provide a more immersive "Wide-Table" experience, especially for tablet users.
- **Quick Navigation:** Optional "Screen Jump" to return to the main betting area immediately after a roll.
- **Visual Enhancements:** More detailed animations for chip placement and win celebrations.

---
*Created and maintained by Simple Craps.*
