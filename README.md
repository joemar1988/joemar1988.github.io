# Simple Craps

[![Android API](https://img.shields.io/badge/API-23%2B-brightgreen.svg)](https://android-arsenal.com/api?level=23)
[![Kotlin](https://img.shields.io/badge/Kotlin-2.1-blue.svg)](https://kotlinlang.org)
[![Compose](https://img.shields.io/badge/Jetpack-Compose-orange.svg)](https://developer.android.com/jetpack/compose)

A professional-grade Craps simulator for Android, modeled after modern "Bubble Craps" electronic machines. Perfect for practicing strategies with authentic odds, full betting support, and a transparent, player-friendly advertising model.

## Key Features

- **Authentic Gameplay:** Complete support for Pass Line, Don't Pass, Come, Don't Come, Place, Buy, Lay, Hardways, and Proposition bets.
- **Game Modes:** Seamlessly toggle between **Classic**, **Crapless**, and **Easy Craps** variants.
- **True Odds:** Mathematically accurate payouts, including commissions (vig) for Buy and Lay bets.
- **Strategies & Tips:** Contextual strategy guides for every betting tab to help you master the game.
- **Modern UI:** A sleek, edge-to-edge Jetpack Compose interface that adapts beautifully to any screen size.
- **Privacy First:** No accounts, no trackers, and no data collection. All game data and roll history stay securely on your device.
- **Fair Ad Model:** Play ad-free with a $50 bankroll reset, or watch a single rewarded ad for a "High Roller" bankroll.
- **Pro Upgrade ($2.99):** A one-time purchase to remove the rewarded ad requirement forever and unlock a premium, ad-free experience.

## Tech Stack

- **Language:** Kotlin 2.1
- **UI Framework:** Jetpack Compose (Material 2)
- **Billing:** Google Play Billing Library 7.1.1
- **Ads:** Google Mobile Ads (AdMob) 25.3.0 with Meta Mediation
- **Architecture:** MVVM with State-driven UI

---

## Release History

### v1.20
- **Visual Bet Feedback & Lock Logic**: Added clear visual indicators (red prohibitory icons) and contextual "Bet Locked" explanations for contract bets and unavailable wagers.
- **Enhanced Ad Mediation**: Switched to a real-time bidding model with **Meta Audience Network** integration for better fill rates and improved battery/data efficiency.
- **Reliability & Safeguards**: Integrated a 30-second ad fallback timer (auto-granting rewards if ads fail) and a "LOADING..." state with interaction locks to prevent UI ghosting.
- **Maintenance**: Refined internal ad wrappers and optimized SDK lifecycle for broad Android 6.0 (API 23+) compatibility and memory safety.

### v1.19
- **NEW: "About Simple Craps" Section**. Added a dedicated "About" dialog in the top header that outlines the app\'s core philosophy, strategy-first focus, and the authentic "Risk vs Reward" ad model.
- **NEW: Table Limits & Denominations UI**. Replaced long descriptions in the Refresh Menu with a scannable table mapping bankroll ranges to their corresponding minimum chip values.
- **FIXED: Ad Lifecycle & Impressions**. Resolved a critical bug where the rewarded ad object was not cleared on early dismissal, preventing subsequent loads. Integrated full-lifecycle Firebase Analytics (load, show, dismiss, impression) for robust monitoring.
- **IMPROVED: Analytics Reliability**. Added explicit session initialization and ProGuard/R8 protection rules to ensure consistent tracking of active users.
- **IMPROVED: Philosophy & Purpose Documentation**. Formalized our commitment to pure simulation, realistic table limits, and respecting the player\'s time as a premier practicing tool.

### v1.18
- **NEW: Analytics Support**. Integrated Firebase Analytics for secure, anonymous session and event tracking to improve future game balancing.
- **IMPROVED: SDK & Build Maintenance**. Updated core components for enhanced privacy compliance. Enabled R8 Full Mode and optimized Gradle for a smaller, faster app.
- **IMPROVED: Statistics Clarity**. Simplified roll frequency columns (ODDS, SESS %, ALL %) and cleaned up table headers for better readability.
- **IMPROVED: Refresh Optimization**. Redesigned the bankroll refresh logic with on-demand loading, a transparent status timer, and a "Free Reset" fallback for better reliability.

### v1.17
- **NEW: Quick Actions & Strategy Tools**. Added dedicated **UNDO**, **REPEAT**, and **Bulk Betting** (Place/Buy/Press All) shortcuts. Complex actions are intelligently grouped so they can be reverted with a single **UNDO**.
- **NEW: Customizable Betting Unit**. Added a 6th customizable lime green chip to the selection bar. Set and save your own preferred unit (e.g., $7) for faster strategy execution.
- **IMPROVED: Professional Table UI**. Redesigned the top navigation, game mode selection, and control bar for perfect alignment, higher contrast, and better vertical readability.
- **IMPROVED: Authentic Logic & Help**. Standardized **Come/Don't Come** rules across all game modes and added informational tooltips ("i" icons) to explain specific mechanics and contract bet rules.
- **IMPROVED: Enhanced Realism & Feedback**. Updated dice and felt textures for a realistic table appearance. Added tactile pressed-state feedback to all landing screen and main interaction buttons.
- **IMPROVED: Smooth Navigation**. The Statistics menu now supports natural left/right swiping between the Hand, Session, and All-Time tabs.

### v1.16
- **NEW**: **Unified Come Points**. Merged established Come and Don't Come point bets into a single, compact 2-per-line grid on the Come tab.
- **NEW**: **Hop Bets**. Added a curated suite of Hop bets (one-roll bets on specific combinations) to the new **One-Roll** tab.
- **IMPROVED**: **Tab Reorganization**. Replaced "Hardways" and "Other" with **One-Roll** (Hop & Prop bets) and **Bonus & Hard** (ATS & Hardways) for a more logical betting flow.
- **IMPROVED**: **Enhanced Layouts**. Redesigned the Against tab with an Any 7 hedge shortcut and optimized the One-Roll tab with prominent Field/Any 7/Any Craps targets.
- **IMPROVED**: **Come Tab Layout**. The Come tab now features both Come and Don't Come betting bars at the top for faster access.
- **IMPROVED**: **Cleaned Navigation**. Removed redundant betting bars from the Against tab to maintain focus.

### Legacy Versions (v1.8 - v1.15)
- **v1.15**: Added Stats Persistence and Come/Don't Come chip stacking.
- **v1.14**: Added Last Roll Performance, Luck Color Coding, Odds/Field settings, and Statistics refinements.
- **v1.13**: Added Analytics Heatmap, Streak Tracking, and corrected ATS & Don't Come logic.
- **v1.12**: Added Custom Reset Amount and a redesigned, prioritized Reset Menu UI.
- **v1.11**: Added Strategies & Tips overlay, Persistent Bankroll, and Data Deletion options.
- **v1.10**: Added Screen Scaling, Easy Craps mode, and Session/Performance analytics.
- **v1.9**: Integrated Google Play Billing for Pro Upgrade and refined ATS betting descriptors.
- **v1.8**: Added Classic/Crapless toggles, Interactive Tutorial, and Android 15 compatibility.

---

## Roadmap

I am actively developing the following features to make Simple Craps the ultimate practice tool:

### Advanced Simulation & Logic
- **Strategy Assistance:** An interactive guide that highlights optimal betting placements based on selected systems (Iron Cross, Three-Point Molly, etc.).
- **Audio Calls:** High-quality audio implementation for authentic "Bubble Craps" atmosphere.

### Professional Analytics
- **Cloud Data Export:** Securely export roll history and session logs to Google Drive for advanced personal analysis.
- **Detailed Roll Profitability:** Track **Money Won vs. Money Lost per roll** to visualize volatility and strategy performance over time.
- **Auto Loading Ads:** Do not autoload ads after an ad is watched.
- 
### UI/UX Improvements
- **Tab Layout Manager:** A new customization tool to rearrange betting tab order or enable a **Split-View Mode**, allowing users to stack two betting areas (e.g., Pass Line and Hardways) on screen simultaneously.
- **Landscape Support:** A dedicated horizontal layout to provide a more immersive "Wide-Table" experience, especially for tablet users.
- **Quick Navigation:** Optional "Screen Jump" to return to the main betting area immediately after a roll.
- **ATS Grey Out:** Grey out ATS when a point is set.

---
*Created and maintained by Simple Craps.*