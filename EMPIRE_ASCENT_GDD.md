# Empire Ascent — Complete Game Design Document

## Table of Contents
1. [Game Overview](#1-game-overview)
2. [Core Gameplay Loop](#2-core-gameplay-loop)
3. [Currency System](#3-currency-system)
4. [Onboarding & Tutorial](#4-onboarding--tutorial)
5. [User Interface Design](#5-user-interface-design)
6. [Stage System](#6-stage-system)
7. [Asset System](#7-asset-system)
8. [Production Line System](#8-production-line-system)
9. [Active Gameplay Mechanics](#9-active-gameplay-mechanics)
10. [Market System](#10-market-system)
11. [Board of Directors](#11-board-of-directors)
12. [Complete Economy Reference](#12-complete-economy-reference)
13. [Progression Timeline](#13-progression-timeline)
14. [Monetization](#14-monetization)
15. [Settings & Features](#15-settings--features)
16. [Technical Specifications](#16-technical-specifications)
17. [Appendix A: Complete Asset Upgrade Costs](#appendix-a-complete-asset-upgrade-costs)
18. [Appendix B: Achievement System](#appendix-b-achievement-system)
19. [Appendix C: Market Price Tables](#appendix-c-market-price-tables)
20. [Appendix D: Glossary](#appendix-d-glossary)

---

## 1. Game Overview
### 1.1 Concept Statement
Empire Ascent is a mobile idle/incremental tycoon game where players rise from humble beginnings with **$100** to commanding a multi-billion-dollar empire across five distinct economic stages. The game combines active mini-games, strategic resource management, production chain optimization, and idle progression mechanics.

### 1.2 Genre
- **Primary:** Idle/Incremental  
- **Secondary:** Tycoon/Business Simulation  
- **Tertiary:** Resource Management

### 1.3 Platform
- iOS (iPhone, iPad)  
- Android (Phone, Tablet)

### 1.4 Target Audience
- **Age:** 16-45  
- **Players who enjoy:** *AdVenture Capitalist*, *Idle Miner*, *Egg Inc.*, *Cookie Clicker*  
- **Session length:** 5-30 minutes active, unlimited idle

### 1.5 Unique Selling Points
- **Production chain depth** — Not just clicking; includes real manufacturing strategy.  
- **Meaningful automation** — Gradual transition from active to passive.  
- **Market trading** — Real-time price fluctuations and speculation.  
- **Five themed stages** — Each feels like a new game layer.  
- **No hard resets** — Continuous upward progression, no prestige wipes.

### 1.6 Core Pillars

| Pillar       | Description                                  |
|--------------|----------------------------------------------|
| Progression  | Constant sense of growth and achievement     |
| Strategy     | Meaningful decisions about resource allocation |
| Satisfaction | Rewarding feedback loops and collection mechanics |
| Accessibility| Easy to learn, deep to master                |

---

## 2. Core Gameplay Loop
### 2.1 Primary Loop (Minute-to-Minute)
```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│    ┌──────────┐                         ┌──────────┐       │
│    │  PRODUCE │                         │  COLLECT │       │
│    │   ────►  │                         │   ◄────  │       │
│    └──────────┘                         └──────────┘       │
│          │                                   ▲              │
│          ▼                                   │              │
│    ┌──────────┐                         ┌──────────┐       │
│    │  PROCESS │────────────────────────►│   SELL   │       │
│    └──────────┘                         └──────────┘       │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

**Actions:** Produce → Process → Sell → Collect  
- **Produce** — Generate base resources (active harvest or passive).  
- **Process** — Convert resources to higher-value goods (active mini-game or passive).  
- **Sell** — Exchange goods for cash (market or retail assets).  
- **Collect** — Gather accumulated income.

### 2.2 Secondary Loop (Hour-to-Hour)
**EARN → INVEST → UPGRADE → AUTOMATE → EARN MORE**

- **Earn** — Accumulate cash through the primary loop.  
- **Invest** — Purchase new assets.  
- **Upgrade** — Improve existing assets (Capacity, Speed, Automation).  
- **Automate** — Reduce active management requirements.  
- **Earn More** — Higher passive income enables faster growth.

### 2.3 Tertiary Loop (Day-to-Day)
**COMPLETE STAGE → UNLOCK BOARD → MAXIMIZE BONUS → UNLOCK NEXT STAGE**
- **Complete Stage** — Fully automate all 5 assets in a stage.  
- **Unlock Board** — Gain access to Board of Directors.  
- **Maximize Bonus** — Fill all 10 board seats for +100% income.  
- **Unlock Next Stage** — Reach net worth threshold and swipe to new stage.

### 2.4 Meta Loop (Week-to-Week)
**STAGE 1 → STAGE 2 → STAGE 3 → STAGE 4 → STAGE 5 → COMPLETE EMPIRE**  
Each stage represents ~25% more time investment than the previous, creating a long-term progression arc of **8-12 weeks** for full completion.

---

## 3. Currency System
### 3.1 Currency Overview

| Currency  | Symbol | Acquisition                          | Primary Use                   |
|-----------|--------|--------------------------------------|-------------------------------|
| Cash      | $      | Jobs, sales, assets                  | Everything                    |
| Produce/Resources | 🥕📦🏗️💵💾 | Production assets                   | Processing, selling           |
| Reputation| ⭐     | Milestones, achievements             | Unlocks, job slots            |
| Bitcoin   | ₿      | Mining, purchases, deals             | Premium features              |

### 3.2 Cash ($)
**Primary currency** for all gameplay.

**Earned through:** active jobs, asset task completion, passive income, market sales, deal completions.  
**Spent on:** asset purchases, upgrades (Capacity, Speed, Automation), board member hiring, market purchases.

**Display Format:**
- Under $1,000: `$XXX`
- $1,000–999,999: `$X.XXK` (e.g., $5.2K)
- $1M–999M: `$X.XXM` (e.g., $12.5M)
- $1B+: `$X.XXB` (e.g., $3.45B)

### 3.3 Resources (Stage-Specific)

| Stage | Base Resource | Refined Product | Premium Product            |
|-------|---------------|-----------------|----------------------------|
| 1     | 🥕 Produce    | 🍽️ Meals       | 🎪 Catering Packages       |
| 2     | 📦 Materials  | 🔧 Components   | 📱 Consumer Goods          |
| 3     | 🏗️ Development Rights | 🏢 Properties | 🌆 Complexes      |
| 4     | 💵 Capital    | 📈 Returns      | 🏦 Instruments             |
| 5     | 💾 Data       | 🧠 AI Models    | 🚀 Platform Revenue        |

**Resource Rules:**
- Resources are stage-specific.  
- Resources can be sold directly on the market (lower margin).  
- Resources gain value when processed through the production chain.  
- Resources decay slowly if not processed (incentivizes activity).

### 3.4 Reputation (⭐)
Secondary currency for progression gates.

**Earned through:** milestone achievements, stage completions, board completions, special events, daily login streaks.  
**Spent on:** additional job slots, premium job types, special market features, cosmetic upgrades.

**Reputation Thresholds**

| Reputation | Unlock            |
|------------|-------------------|
| ⭐ 100     | 3rd job slot      |
| ⭐ 500     | 4th job slot      |
| ⭐ 1,000   | Premium jobs      |
| ⭐ 2,500   | Market auto-trading |
| ⭐ 5,000   | Advanced analytics |
| ⭐ 10,000  | VIP market access |

### 3.5 Bitcoin (₿)
Premium currency with dual acquisition.

**Earned through:** real money purchase, in-game mining (late Stage 2+), rare events, achievement rewards.  
**Spent on:** task time skips, instant upgrades, premium boosts (2x income for 1 hour), exclusive cosmetics, market advantages.

**Mining Progression (Unlocked Stage 2+):**

| Mining Setup  | Cost          | Mining Rate   | ROI Time |
|---------------|---------------|---------------|----------|
| Basic PC      | $250,000      | ₿0.00001/hr   | ~28 days |
| Gaming Rig    | $1,000,000    | ₿0.0001/hr    | ~14 days |
| Mining Rig    | $5,000,000    | ₿0.001/hr     | ~7 days  |
| Mining Farm   | $50,000,000   | ₿0.01/hr      | ~7 days  |
| Data Center   | $1,000,000,000| ₿0.1/hr       | ~14 days |

Bitcoin value: **₿1 ≈ $100,000** in-game equivalent.

---

## 4. Onboarding & Tutorial
### 4.1 Tutorial Flow Overview
**START → MARKET INTRO → JOB INTRO → FIRST ASSET → FREE PLAY**  
Total tutorial time: ~5–6 minutes. Player ends with **$500+**, first asset owned, and understanding of core mechanics.

### 4.2 Step-by-Step Tutorial
1. **Welcome & Setup (30s):** Title card; tap **START GAME**.  
2. **The Friend’s Tip (1m):** Alex gifts $100 and hints at Produce price spike; Market tab highlights.  
3. **Market Tutorial (1.5m):** Buy 20 Produce at $5/unit; post-purchase prompt leads to jobs.  
4. **Jobs Tutorial (2m):** Start Lawn Mowing active mini-game; mid-task market alert signals rising prices.  
5. **Job Completion & Market Check (1m):** Collect $22; Alex prompts market check.  
6. **Selling & First Profit (30s):** Sell 20 Produce at $25/unit; profit $400 and earn ⭐50 achievement.  
7. **First Asset Purchase (30s):** Buy **Garden Plot** for $500; $22 remains.  
8. **Asset Introduction & Tutorial End (30s):** Harvest tutorial; Alex recap; goal: reach $1,000,000 to unlock Stage 2.

**Player ends tutorial with:** $22 cash, Garden Plot asset, ⭐50 Reputation, understanding of Market, Jobs, Assets.

### 4.3 Tutorial Summary

| Step | Duration | Player Learns            | Player Gains      |
|------|----------|--------------------------|-------------------|
| 1    | 30s      | Game start               | —                 |
| 2    | 30s      | Story/motivation         | $100              |
| 3    | 1.5m     | Market buying            | 20 Produce        |
| 4    | 2m       | Jobs, mini-games         | ~$22              |
| 5    | 30s      | Job completion           | Collect earnings  |
| 6    | 30s      | Market selling           | $500, ⭐50        |
| 7    | 30s      | Asset purchases          | Garden Plot       |
| 8    | 30s      | Asset management         | Understanding     |

---

## 5. User Interface Design
### 5.1 Screen Architecture Overview
- **Main Stage View:** Primary game screen per stage; swipe vertically between stages.  
- **Bottom Navigation:** Jobs (💼), Market (📊), Collect (⚡), Settings (⚙️).

### 5.2 Top Status Bar (Persistent)
Displays current cash, stage resource, and Bitcoin with hourly production rates. Tap actions open details (wallet, inventory, crypto wallet). Resource icon changes based on current stage.

### 5.3 Main Stage View
- Shows current stage name and assets (5 per stage in 3-asset top row, 2-asset bottom row).  
- Asset cards display icon, income/hr, automation bar/percent, and state (Locked, Idle, Active, Ready, Passive).  
- Stage transition indicator with progress to next stage; swipe up/down to navigate.

### 5.4 Asset Detail View
Displays asset level, income breakdown (base, passive, active), current task status, upgrades (Capacity, Speed, Automation), and stats (total produced, tasks completed, ownership time, efficiency rating).

### 5.5 Task Selection Modal
Offers task options with durations, yields, efficiency, and unlockable overtime. Highlights active potential and available resources.

### 5.6 Jobs Screen
- Shows job slots (unlockable with ⭐), active jobs with timers/boosts, available jobs with durations/payouts, and guidance emphasizing assets for long-term wealth.

### 5.7 Market Screen
- Stage filters, price charts, news hints, price ranges, holdings, bulk buy/sell sliders, alerts, auto-trade unlocks, and VIP access benefits.

### 5.8 Board Room Screen
- Displays stage income, board bonus progress, seats grid (10 seats, +10% each), bios, and hire costs. Full board doubles stage income.

### 5.9 Bottom Navigation Bar
- **Jobs (💼):** Open jobs screen.  
- **Market (📊):** Open market.  
- **Collect (⚡):** Collect all ready tasks; badge shows count.  
- **More (⚙️):** Settings, profile, help; notification dot for updates.

### 5.10 Settings & More Menu
Includes profile, gameplay toggles (auto-collect, auto-queue, default task length, offline cap), notifications, audio, display (number format, theme, animations), account (cloud save, linking, privacy), store (cash packs, Bitcoin bundles, VIP), and help/FAQ.

---

## 6. Stage System
### 6.1 Stage Overview

| Stage | Name              | Theme                    | Unlock Requirement           |
|-------|-------------------|--------------------------|------------------------------|
| 1     | Neighborhood      | Local food economy       | Start                        |
| 2     | Business District | Manufacturing & retail   | $1,000,000 net worth         |
| 3     | City Center       | Real estate & services   | $15,000,000 net worth        |
| 4     | Financial District| Capital markets          | $200,000,000 net worth       |
| 5     | Tech Campus       | Technology & scale       | $3,000,000,000 net worth     |

### 6.2 Stage Layout
Each stage contains 5 assets arranged:
```
┌─────┐    ┌─────┐    ┌─────┐
│  1  │    │  2  │    │  3  │
└─────┘    └─────┘    └─────┘
     ┌─────┐    ┌─────┐
     │  4  │    │  5  │
     └─────┘    └─────┘
```

### 6.3 Stage Completion States

| State     | Criteria                                 | Visual               | Benefit         |
|-----------|------------------------------------------|----------------------|-----------------|
| Locked    | Net worth below threshold                | Greyed out, requirement shown | None |
| Active    | Unlocked, assets in development          | Normal colors        | Playable        |
| Automated | All 5 assets at 100% automation          | Green border, ✅ icon | Board unlocked  |
| Complete  | All 10 board seats filled                | Gold border, 👑 icon | +100% income    |

### 6.4 Stage Transition
- Swipe down to next stage (if unlocked); swipe up to previous stage.  
- Progress indicator shows unlock threshold, current net worth, and bar to next stage.

---

## 7. Asset System
### 7.1 Asset Core Mechanics
Every asset has three upgrade dimensions:
- **Capacity:** Increases base production/income (Levels 1-10).  
- **Speed:** Reduces task completion time (Levels 1-10).  
- **Automation:** Increases passive income percentage (Levels 1-10).

### 7.2 Automation System
**Total Income = Base Income × 100%**  
**Passive Income = Base Income × Automation %**  
**Active Potential = Base Income × (100% - Automation %)**

Example: Garden with $100/hr base, 60% automation → Passive $60/hr, Active $40/hr.  
At 100% automation: asset is fully passive, produces max output automatically, green glow indicator.

**Automation Level Progression**

| Level | Automation % | Cost Multiplier |
|-------|--------------|-----------------|
| 0     | 0%           | —               |
| 1     | 10%          | 1×              |
| 2     | 20%          | 2×              |
| 3     | 30%          | 4×              |
| 4     | 40%          | 8×              |
| 5     | 50%          | 15×             |
| 6     | 60%          | 30×             |
| 7     | 70%          | 50×             |
| 8     | 80%          | 80×             |
| 9     | 90%          | 120×            |
| 10    | 100%         | 200×            |

### 7.3 Task Queue System
- One task per asset at a time; tasks must be collected to queue new ones.  
- Offline time counts toward completion.  
- **Task Types:**

| Task Type | Duration  | Yield                        | Efficiency          |
|-----------|-----------|------------------------------|---------------------|
| Quick     | 5 min     | 15% of potential             | 90%                 |
| Standard  | 30 min    | 40% of potential             | 100%                |
| Full Day  | 4 hours   | 100% of potential            | 100%                |
| Overtime  | 8 hours   | 120% of potential (unlockable)| 105%               |

### 7.4 Asset States

| State   | Icon | Meaning             | Player Action    |
|---------|------|---------------------|------------------|
| Locked  | 🔒   | Not purchased       | Buy asset        |
| Idle    | ⚠️   | No task running     | Queue task       |
| Active  | ⏱️   | Task in progress    | Wait/boost       |
| Ready   | ✅   | Task complete       | Collect          |
| Passive | 💚   | 100% automated      | None needed      |

---

## 8. Production Line System
### 8.1 Core Concept
Base resources flow through assets to create higher-value products.  
**BASE RESOURCE → PROCESSING → REFINED PRODUCT → SALE → CASH** (or sell raw via market at lower margin).

### 8.2 Stage 1: Neighborhood Production Chain
**Resources:** 🥕 Produce → 🍽️ Meals → 🎪 Catering Packages

**Flow**
```
┌──────────┐         ┌──────────┐         ┌──────────┐
│  GARDEN  │────────▶│  KITCHEN │────────▶│FOOD CART │
│    🌱    │ Produce │    🍳    │  Meals  │    🍔    │
│ Produces │         │ Converts │         │  Sells   │
│ Produce  │         │  3:1     │         │ Premium  │
└──────────┘         └──────────┘         └──────────┘
      │                                        ▲
      │              ┌──────────┐              │
      └─────────────▶│  MARKET  │──────────────┘
                     │  STALL   │ (Direct sale,
                     │    🏪    │  lower margin)
                     └──────────┘
                           │
                           ▼
                     ┌──────────┐
                     │ CATERING │
                     │    🎪    │
                     │ Bundles  │
                     │ 10 Meals │
                     └──────────┘
```

**Conversion Rates**
- 3 Produce → 1 Meal  
- 10 Meals + $50 overhead → 1 Catering Package

**Value Progression**

| Product  | Market Price | Value per Produce Used |
|----------|--------------|------------------------|
| Produce  | $5–8         | $5–8                   |
| Meals    | $18–25       | $6–8.33                |
| Catering | $350–400     | $10–13                 |

### 8.3 Stage 2: Business District Production Chain
**Resources:** 📦 Materials → 🔧 Components → 📱 Consumer Goods  
**Flow:** Warehouse (📦) → Workshop (🔧) → Assembly Line (🏭) → Outlet Store (🏬); Wholesale Center (🚛) enables B2B distribution.  
**Conversion:** 4 Materials → 1 Component; 3 Components → 1 Consumer Good.

### 8.4 Stage 3: City Center Production Chain
**Resources:** 🏗️ Development Rights → 🏢 Managed Properties → 🌆 Commercial Complexes  
**Flow:** Land Office (📋) → Construction (🏗️) → Property Mgmt (🏢) → Broker Firm (🤝); Development Corp (🌆) handles mega-projects.

### 8.5 Stage 4: Financial District Production Chain
**Resources:** 💵 Capital → 📈 Investment Returns → 🏦 Financial Instruments  
**Flow:** Brokerage (💵) → Investment Fund (📈) → Private Equity (💼) → Bank (🏦); Holding Company (👑) for ultimate control.

### 8.6 Stage 5: Tech Campus Production Chain
**Resources:** 💾 Data → 🧠 AI Models → 🚀 Platform Revenue  
**Flow:** Data Center (💾) → Analytics (📊) → Software Co (💻) → AI Lab (🧠) → Conglomerate (🚀).

---

## 9. Active Gameplay Mechanics
### 9.1 Jobs (Early Game Income)
Jobs provide active income when players lack assets or need quick cash.

**Job Types**

| Job Type          | Duration  | Payout        | Unlock             |
|-------------------|-----------|---------------|--------------------|
| Lawn Mowing       | 3 min (active tap) | $15 + tips | Start |
| Dog Walking       | 5 min (timer) | $25 | Start |
| Grocery Delivery  | 10 min (timer) | $45 | $500 earned |
| Package Sorting   | 15 min (active) | $55 | $1,000 earned |
| Street Performing | 10 min (active) | $15–60 | $2,000 earned |
| House Cleaning    | 30 min (timer) | $80 | $5,000 earned |
| Freelance Writing | 1 hour (timer) | $120 | $10,000 earned |
| Handyman Work     | 2 hours (timer) | $180 | ⭐1,000 |
| Consulting        | 4 hours (timer) | $400 | ⭐2,500 |

**Job Slots**
- Start with 2 slots; unlock Slot 3 (⭐500), Slot 4 (⭐1,000), Slot 5 (⭐2,500 max).

**Active vs Timer Jobs**
- **Timer Jobs:** Start and wait; offline time counts; collect on completion.  
- **Active Jobs:** Mini-games accelerate completion and boost tips/bonuses.

### 9.2 Mini-Games
- **Harvest Mini-Game:** Tap spawning resources before they fade; combo multiplier; performance bonuses (Good +10%, Perfect +25%).  
- **Processing Mini-Game:** Match/swap ingredients to complete recipes under time limit; each recipe converts resources.  
- **Sales Mini-Game:** Negotiate with customer archetypes (price-sensitive, quality-focused, impatient) to balance margin vs. volume.

### 9.3 Market Trading
- Prices change every 4 hours within ±30% of base; news telegraphs spikes/crashes; player speculation encouraged.  
- Trading actions: buy low/sell high, arbitrage between raw/processed goods, set alerts (⭐ unlock), auto-trade rules (premium), VIP market benefits.

---

## 10. Market System
### 10.1 Market Overview
Players buy and sell resources at fluctuating prices with charts, news, and unlockable tools.

### 10.2 Price Mechanics (Stage 1 Base Prices)

| Resource | Base Price | Range          |
|----------|------------|----------------|
| Produce  | $6.50      | $4.50–$8.50    |
| Meals    | $22.00     | $17.00–$27.00  |
| Catering | $375       | $300–$450      |

Price factors: 4-hour cycles, random events, news hints, optional global activity influence.

### 10.3 Market Features

| Feature        | Unlock    | Function                              |
|----------------|-----------|---------------------------------------|
| Basic Trading  | Start     | Buy/sell at current prices            |
| Price Charts   | Start     | View 24-hour price history            |
| Market News    | Start     | Hints about upcoming changes          |
| Price Alerts   | ⭐500     | Notification when price hits target   |
| Bulk Trading   | ⭐1,000   | Buy/sell in larger quantities         |
| Auto-Trade     | ⭐2,500   | Set automatic buy/sell conditions     |
| VIP Market     | ⭐10,000  | Better prices, exclusive goods        |

### 10.4 Market News Examples
- Produce shortage expected — prices may rise 15%.  
- New restaurant opening — meal demand increasing.  
- Competitor sale — prices dropping temporarily.  
- Holiday weekend — catering demand surging.  
- Supply chain issues — materials scarce.

---

## 11. Board of Directors
### 11.1 Board Overview
Unlocked when all 5 assets in a stage reach 100% automation. Provides permanent income multipliers per completed stage.

### 11.2 Board Structure
- 10 seats per stage; +10% income per seat; +100% max (doubles stage income).  
- Seats displayed in 2 rows of 5; progress bar shows filled seats/bonus.

### 11.3 Board Member Hiring (Stage 1 Costs)

| Seat | Cost       | Cumulative Cost | Cumulative Bonus |
|------|------------|-----------------|------------------|
| 1    | $50,000    | $50,000         | +10%             |
| 2    | $100,000   | $150,000        | +20%             |
| 3    | $175,000   | $325,000        | +30%             |
| 4    | $275,000   | $600,000        | +40%             |
| 5    | $400,000   | $1,000,000      | +50%             |
| 6    | $550,000   | $1,550,000      | +60%             |
| 7    | $725,000   | $2,275,000      | +70%             |
| 8    | $925,000   | $3,200,000      | +80%             |
| 9    | $1,150,000 | $4,350,000      | +90%             |
| 10   | $1,400,000 | $5,750,000      | +100%            |

### 11.4 Board Member Characters
Each member includes a name, portrait, quote, and bio. Example quotes:
- Patricia Wells — “Efficiency is just organized impatience.”  
- Marcus Chen — “Growth isn't a goal, it's a habit.”  
- Diana Okoye — “Numbers don't lie, but they do whisper.”  
- James Rodriguez — “The best investment is in people.”  
- Sarah Kim — “Innovation distinguishes between leaders and followers.”

---

## 12. Complete Economy Reference
### 12.1 Stage 1: Neighborhood
- **Assets & Costs**
  - Garden Plot 🌱 — Purchase $500; Max production 50 Produce/hr; Total max upgrade cost $27,075.
  - Market Stall 🏪 — Purchase $2,000 (requires Garden); Max income $180/hr; Total max upgrade cost $68,375.
  - Food Prep Kitchen 🍳 — Purchase $8,000 (requires 500 Produce sold); Converts Produce→Meals (3:1); Max 25 Meals/hr; Total max upgrade cost $222,650.
  - Food Cart 🍔 — Purchase $25,000 (requires Kitchen Level 3+ Automation); Sells Meals at +50% over market; Max $450/hr; Total max upgrade cost $583,125.
  - Catering Service 🎪 — Purchase $75,000 (requires all Stage 1 assets); Bundles Meals + service; Max $850/hr; Total max upgrade cost $1,401,600.

- **Stage Summary**
  - All assets (purchase): $110,500  
  - All upgrades (to max): $2,193,325  
  - Full board (10 seats): $5,750,000  
  - **Total Stage 1:** ~$8,053,825  
  - Max income: ~$2,430/hr → ~$4,860/hr with board.

### 12.2 Stage 2: Business District
- **Assets**

| Asset            | Purchase  | Full Upgrade Cost | Max Income        |
|------------------|-----------|-------------------|-------------------|
| Warehouse 📦     | $15,000   | $247,500          | 80 Materials/hr   |
| Workshop 🔧      | $50,000   | $735,000          | 35 Components/hr  |
| Assembly Line 🏭 | $150,000  | $2,092,500        | 25 Goods/hr       |
| Outlet Store 🏬  | $400,000  | $5,117,500        | $9,000/hr         |
| Wholesale Center 🚛| $1,000,000| $12,120,000     | $17,000/hr        |

- **Stage Summary:** All assets $1,615,000; upgrades $20,312,500; full board $57,500,000; **Total:** ~$79,427,500. Max income: ~$28,000/hr → ~$56,000/hr with board.

### 12.3 Stage 3: City Center
- **Assets**

| Asset                | Purchase   | Full Upgrade Cost | Max Income/Function |
|----------------------|------------|-------------------|---------------------|
| Land Office 📋       | $200,000   | $3,200,000        | Resource generation |
| Construction Co 🏗️   | $750,000   | $9,500,000        | Property generation |
| Property Mgmt 🏢      | $2,500,000 | $28,000,000       | $75,000/hr          |
| Broker Firm 🤝        | $7,500,000 | $72,000,000       | $150,000/hr         |
| Development Corp 🌆  | $20,000,000| $180,000,000      | $320,000/hr         |

- **Stage Summary:** Assets $30,950,000; upgrades $292,700,000; full board $575,000,000; **Total:** ~$898,650,000. Max income: ~$550,000/hr → ~$1,100,000/hr with board.

### 12.4 Stage 4: Financial District
- **Assets**

| Asset               | Purchase     | Full Upgrade Cost | Max Income/Function |
|---------------------|--------------|-------------------|---------------------|
| Brokerage 💵        | $3,000,000   | $45,000,000       | Capital generation  |
| Investment Fund 📈  | $12,000,000  | $140,000,000      | Returns generation  |
| Private Equity 💼   | $50,000,000  | $480,000,000      | $2,000,000/hr       |
| Bank 🏦             | $150,000,000 | $1,200,000,000    | $5,500,000/hr       |
| Holding Company 👑  | $500,000,000 | $3,500,000,000    | $12,000,000/hr      |

- **Stage Summary:** Assets $715,000,000; upgrades $5,365,000,000; full board $5,750,000,000; **Total:** ~$11,830,000,000. Max income: ~$20,000,000/hr → ~$40,000,000/hr with board.

### 12.5 Stage 5: Tech Campus
- **Assets**

| Asset                   | Purchase        | Full Upgrade Cost | Max Income/Function |
|-------------------------|-----------------|-------------------|---------------------|
| Data Center 💾          | $50,000,000     | $600,000,000      | Data generation     |
| Analytics Platform 📊   | $200,000,000    | $2,000,000,000    | Model generation    |
| Software Company 💻     | $800,000,000    | $7,000,000,000    | $50,000,000/hr      |
| AI Research Lab 🧠      | $3,000,000,000  | $25,000,000,000   | $150,000,000/hr     |
| Tech Conglomerate 🚀    | $15,000,000,000 | $100,000,000,000  | $400,000,000/hr     |

- **Stage Summary:** Assets $19,050,000,000; upgrades $134,600,000,000; full board $57,500,000,000; **Total:** ~$211,150,000,000. Max income: ~$600,000,000/hr → ~$1,200,000,000/hr with board.

### 12.6 Complete Game Economy

| Stage | Total Cost | Cumulative |
|-------|------------|------------|
| 1     | $8.05M     | $8.05M     |
| 2     | $79.4M     | $87.5M     |
| 3     | $898.7M    | $986.2M    |
| 4     | $11.83B    | $12.8B     |
| 5     | $211.15B   | $224B      |

**Max Income Scaling**

| Stage | Max Income/hr | With Board |
|-------|---------------|------------|
| 1     | $2,430        | $4,860     |
| 2     | $28,000       | $56,000    |
| 3     | $550,000      | $1,100,000 |
| 4     | $20,000,000   | $40,000,000|
| 5     | $600,000,000  | $1,200,000,000 |

---

## 13. Progression Timeline
### 13.1 Target Playtimes

| Milestone               | Target Active Time | Calendar Time  |
|-------------------------|--------------------|----------------|
| First Asset             | 5 minutes          | Day 1          |
| Stage 1 Complete        | 8–12 hours         | Day 1–2        |
| Stage 1 Full Board      | +8–12 hours        | Day 2–3        |
| Stage 2 Unlock          | 12–16 hours        | Day 2–3        |
| Stage 2 Complete        | +10–15 hours       | Day 4–5        |
| Stage 2 Full Board      | +10–15 hours       | Day 6–7        |
| Stage 3 Unlock          | 30–40 hours        | Week 1         |
| Stage 3 Complete        | +12–18 hours       | Week 2         |
| Stage 4 Unlock          | 50–70 hours        | Week 2–3       |
| Stage 4 Complete        | +15–20 hours       | Week 3–4       |
| Stage 5 Unlock          | 80–110 hours       | Week 4–5       |
| Stage 5 Complete        | +20–25 hours       | Week 5–6       |
| **Full Game**           | ~180 hours         | 8–12 weeks     |

### 13.2 Scaling Factor
Each stage takes ~25% longer than the previous:

| Stage | Relative Time |
|-------|---------------|
| 1     | 1.0×          |
| 2     | 1.25×         |
| 3     | 1.56×         |
| 4     | 1.95×         |
| 5     | 2.44×         |

### 13.3 Session Design
- **Casual (5–10m):** Collect ready tasks, queue new tasks, check market, collect passive income.  
- **Active (20–30m):** Play mini-games for bonuses, active job completion, market trading, purchase upgrades, plan strategy.  
- **Deep (1+ hr):** Major upgrade pushes, stage completion sprints, board member acquisition, full production chain optimization.

---

## 14. Monetization
### 14.1 Philosophy
- All content earnable; money buys speed, not exclusive power.  
- No pay-to-win; transparent value; ethical design with clear odds.

### 14.2 Cash Packs

| Pack     | Price  | Cash     | Bonus | Best For         |
|----------|--------|----------|-------|------------------|
| Starter  | $0.99  | $5,000   | —     | First purchase   |
| Worker   | $4.99  | $30,000  | +10%  | Early Stage 1    |
| Investor | $9.99  | $75,000  | +20%  | Late Stage 1     |
| Tycoon   | $19.99 | $200,000 | +35%  | Stage 2          |
| Mogul    | $49.99 | $750,000 | +50%  | Stage 3          |
| Empire   | $99.99 | $2,000,000 | +75%| Late game        |

### 14.3 Bitcoin Bundles

| Bundle | Price  | Bitcoin | Primary Use                |
|--------|--------|---------|----------------------------|
| Micro  | $1.99  | ₿0.01   | Skip single timer          |
| Mini   | $4.99  | ₿0.03   | Multiple skips             |
| Standard| $9.99 | ₿0.08   | Premium boosts             |
| Premium| $24.99 | ₿0.25   | Significant acceleration   |
| Whale  | $99.99 | ₿1.25   | Major advantage            |

**Bitcoin Uses:** Skip timers (₿0.001–0.01), instant upgrades (₿0.01–0.1), 2x income boost (₿0.05 for 1 hour), exclusive cosmetics (₿0.1–1.0).

### 14.4 VIP Subscription
**$9.99/month** — No ads, +50% offline earnings, auto-collect tasks, daily ₿0.001, 10% shop discount, exclusive board members (cosmetic), priority support.

### 14.5 Ad Integration
- Optional ads: 2x income for 30m, skip task timer, +25% market price on next sale, free daily reward spin.  
- Limits: Max 5 ad rewards/day; no forced ads; VIP removes ads.

### 14.6 Player Spending Profiles
- **Free Player:** Full access; 8–12 week timeline; ads optional.  
- **Light Spender ($5–20):** Occasional acceleration; 6–8 weeks.  
- **Moderate Spender ($20–50):** Consistent boosts; VIP likely; 4–6 weeks.  
- **Heavy Spender ($100+):** Significant acceleration; all premium content; 2–4 weeks.

---

## 15. Settings & Features
### 15.1 Gameplay Settings

| Setting              | Options                         | Default  |
|----------------------|---------------------------------|----------|
| Auto-collect tasks   | On/Off                          | Off      |
| Auto-queue on idle   | On/Off                          | Off      |
| Default task length  | Quick/Standard/Full/Overtime    | Standard |
| Offline earnings cap | 2hr/4hr/8hr/Unlimited           | 8hr      |

### 15.2 Notification Settings
Task completion, market alerts, idle reminders, daily bonus reminder, quiet hours (10 PM–8 AM).

### 15.3 Audio Settings
Music (70%), sound effects (90%), ambient income sounds (Off default).

### 15.4 Display Settings
Number format (Full/Abbreviated/Scientific — default Abbreviated), theme (Light/Dark/Auto — default Dark), animations (Full/Reduced/Off — default Full), color blind modes.

### 15.5 Account Features
Cloud save with real-time sync, cross-device play, account linking (Google/Apple/Facebook), data export, GDPR-compliant deletion.

---

## 16. Technical Specifications
### 16.1 Platform Requirements
- **iOS:** Minimum iOS 14; recommended iOS 16+; devices iPhone 8+/iPad 6th gen+.  
- **Android:** Minimum Android 8.0 (API 26); recommended Android 11+; RAM 2GB minimum (4GB recommended).

### 16.2 Data Storage
- Game state: local + cloud (real-time).  
- Settings: local (on change).  
- Analytics: remote (batched).

### 16.3 Offline Functionality
- Available offline: view state, collect accumulated income (to cap), view assets/stats, access settings.  
- Requires connection: market updates/trading, IAP, cloud sync, ad viewing.

### 16.4 Save System
- Auto-save every 30s; on background; on significant actions.  
- Cloud backup every 5 minutes when connected; manual sync available.

### 16.5 Performance Targets
- Launch <3s; 60 FPS; battery usage <5%/hour active; storage <200 MB; RAM <500 MB.

---

## Appendix A: Complete Asset Upgrade Costs
### Stage 1: Neighborhood — Garden Plot 🌱 ($500 purchase)
**Capacity Upgrades (Produce/hr)**

| Level | Effect | Cost | Cumulative |
|-------|--------|------|------------|
| 1 | 10/hr | $100 | $100 |
| 2 | 15/hr | $150 | $250 |
| 3 | 20/hr | $250 | $500 |
| 4 | 25/hr | $400 | $900 |
| 5 | 30/hr | $600 | $1,500 |
| 6 | 35/hr | $900 | $2,400 |
| 7 | 40/hr | $1,300 | $3,700 |
| 8 | 45/hr | $1,800 | $5,500 |
| 9 | 48/hr | $2,250 | $7,750 |
| 10 | 50/hr | — | $7,750 |

**Speed Upgrades (Task Time Reduction)**

| Level | Effect | Cost | Cumulative |
|-------|--------|------|------------|
| 1 | −5% | $75 | $75 |
| 2 | −10% | $115 | $190 |
| 3 | −15% | $190 | $380 |
| 4 | −20% | $300 | $680 |
| 5 | −25% | $450 | $1,130 |
| 6 | −30% | $680 | $1,810 |
| 7 | −35% | $975 | $2,785 |
| 8 | −40% | $1,350 | $4,135 |
| 9 | −45% | $1,940 | $6,075 |
| 10 | −50% | — | $6,075 |

**Automation Upgrades (Passive %)**

| Level | Effect | Cost | Cumulative |
|-------|--------|------|------------|
| 1 | 10% | $150 | $150 |
| 2 | 20% | $300 | $450 |
| 3 | 30% | $600 | $1,050 |
| 4 | 40% | $1,200 | $2,250 |
| 5 | 50% | $2,250 | $4,500 |
| 6 | 60% | $4,500 | $9,000 |
| 7 | 70% | $7,500 | $16,500 |
| 8 | 80% | $12,000 | $28,500 |
| 9 | 90% | $18,000 | $46,500 |
| 10 | 100% | $30,000 | $76,500 |

*(Similar detailed tables would follow for all 25 assets across 5 stages.)*

---

## Appendix B: Achievement System
### Achievement Categories
- **Wealth Milestones**
  - First $1,000 — “Pocket Change” ⭐25  
  - First $10,000 — “Getting Somewhere” ⭐50  
  - First $100,000 — “Five Figures” ⭐100  
  - First $1,000,000 — “Millionaire” ⭐250  
  - First $1,000,000,000 — “Billionaire” ⭐1,000  

- **Asset Milestones**
  - First asset purchased — “Property Owner” ⭐25  
  - First asset automated — “Hands Off” ⭐50  
  - Full stage automated — “Stage Master” ⭐250  
  - All stages automated — “Empire Complete” ⭐5,000  

- **Trading Milestones**
  - First trade — “Market Debut” ⭐25  
  - 100% profit trade — “Double Up” ⭐50  
  - 10 trades in one day — “Day Trader” ⭐100  
  - $1M in trade profits — “Market Maker” ⭐500  

- **Job Milestones**
  - First job completed — “Working Class” ⭐10  
  - 100 jobs completed — “Hard Worker” ⭐100  
  - All job types completed — “Jack of All Trades” ⭐200  

- **Board Milestones**
  - First board member — “Board Beginner” ⭐50  
  - Full board (one stage) — “Chairman” ⭐500  
  - Full board (all stages) — “Ultimate Chairman” ⭐10,000  

---

## Appendix C: Market Price Tables
### Base Prices and Ranges
**Stage 1**

| Resource | Base | Min  | Max  |
|----------|------|------|------|
| Produce  | $6.50| $4.50| $8.50|
| Meals    | $22.00| $17.00| $27.00|
| Catering | $375 | $300 | $450 |

**Stage 2**

| Resource    | Base | Min  | Max  |
|-------------|------|------|------|
| Materials   | $10  | $7   | $13  |
| Components  | $48  | $36  | $60  |
| Consumer Goods | $210 | $160 | $260 |

**Stage 3**

| Resource           | Base    | Min      | Max      |
|--------------------|---------|----------|----------|
| Development Rights | $500    | $375     | $625     |
| Properties         | $5,000  | $3,750   | $6,250   |
| Complexes          | $50,000 | $37,500  | $62,500  |

**Stage 4**

| Resource      | Base     | Min       | Max       |
|---------------|----------|-----------|-----------|
| Capital       | $1,000   | $750      | $1,250    |
| Returns       | $12,000  | $9,000    | $15,000   |
| Instruments   | $150,000 | $112,500  | $187,500  |

**Stage 5**

| Resource      | Base       | Min        | Max         |
|---------------|------------|------------|-------------|
| Data          | $2,500     | $1,875     | $3,125      |
| AI Models     | $50,000    | $37,500    | $62,500     |
| Platform Rev  | $1,000,000 | $750,000   | $1,250,000  |

---

## Appendix D: Glossary
| Term       | Definition                                               |
|------------|----------------------------------------------------------|
| Asset      | A purchasable business that generates income            |
| Automation | The percentage of income earned passively               |
| Base Income| Maximum possible income before bonuses                  |
| Board      | Leadership team providing income multipliers            |
| Capacity   | Upgrade that increases base production                  |
| Chain      | Production line converting resources to products        |
| IAP        | In-app purchase                                         |
| Idle       | Asset state with no active task                         |
| Passive    | Income earned without player action                     |
| Queue      | Assign a task to an asset                               |
| Speed      | Upgrade that reduces task time                          |
| Stage      | One of five game sections/environments                  |
| Task       | Timed work assignment for active income                 |

---

**Document End**
