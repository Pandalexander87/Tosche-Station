# Tosche Station - GAC Meta Overlay

**Version 13 - March 18, 2026**

A character prioritization tool for Star Wars: Galaxy of Heroes that helps you make smarter farming decisions based on **actual GAC performance data**.

---

## What Is This?

Tosche Station is a resource optimizer that ranks every SWGOH character by their **real-world value** in Grand Arena Championships (GAC). Unlike basic checklists that just tell you "farm this GL next," Tosche Station incorporates:

- **Meta adoption rates**: Which omicrons and zetas are actually being used by top players
- **Unlock requirements**: Which characters unlock GLs, Journey Guide characters, and capital ships
- **Multi-event value**: Characters required for assault battles, raids, and Territory Wars
- **GAC tier ratings**: Characters ranked by their competitive performance

The result: **The Stranger and Rey (Dark Side Vision) rank higher than characters with more GL requirements**, because their GAC omicrons have 85%+ adoption rates among relic players.

---

## How to Use It

### Quick Start

1. **Open the HTML file** in any modern browser
2. **Load your roster** using one of three methods:
   - Enter your ally code and click "Fetch from SWGOH.gg"
   - Upload a JSON file from SWGOH.gg
   - The tool caches your last roster automatically
3. **Browse the character table** - it's automatically sorted by score
4. **Use filters** to narrow down to specific character types

### Understanding the Interface

#### Main Character Table

Each row shows:
- **Rank & Score**: Higher = more valuable investment
- **Character Name**: With subtitle showing faction/source
- **Stars & Relic**: Your current progression
- **Unlock Badges**: What this character unlocks (GLs, JG events, ships)
- **Omicron/Zeta Info**: Which abilities are meta-relevant

#### Key Filters (Top Bar)

- **All**: Show everything
- **GL Req**: Characters required for Galactic Legend events
- **Unlocks GL/JG/Capital Ship**: Characters that unlock major content
- **Assault Battle**: AB-eligible characters
- **Active Raids**: Raid-eligible characters
- **Has Ship**: Characters with fleet pilots
- **Omicron**: Characters with omicron abilities (GAC meta focus)
- **Raid/Conquest/LST Eligible**: Content-specific filters
- **GAC GL Tier**: Top-tier GAC performers
- **Kyber Zetas**: Characters with 6+ Kyber-tier zetas

#### Sort Options

- **Score ▼** (default): Highest value characters first
- **Relic ▲**: Lowest relic first (find quick wins)
- **Efficiency**: Score-per-relic ratio (ROI ranking)
- **GAC Tier**: Pure GAC performance ranking
- **Zeta Value**: Characters with most valuable zeta abilities

---

## How the Meta Overlay Works

### The Problem Tosche Station Solves

Traditional farming guides treat all characters equally within a tier. But in reality:
- **The Stranger** with 3 GAC omicrons at 85% adoption is worth MORE than characters in 5 GL requirements
- **Rey (Dark Side Vision)** with her 81-86% adoption omicron suite outperforms many "mandatory" GL reqs
- **Starkiller's** "There is Much Conflict in You" (88% adoption) makes him a higher-priority farm than characters with more unlock value

### Meta Weight Calculation

**For Each Character:**
```
Meta Weight = (Σ GAC omicron adoption rates × 2.0) + (Σ zeta adoption rates × 1.0)
```

**Data Source:** SWGOH.gg adoption statistics (% of relic+ players who have the ability)

**GAC Omicrons Only:**
- Includes: GAC, GAC 3v3, GAC 5v5 modes
- Excludes: TW, TB, Conquest omicrons (not GAC-relevant)

**Example Weights:**
- **Rey (Dark Side Vision)**: 7.92 meta weight
  - 3 GAC omicrons: "In Our Nature" (86%), "Malevolent Lineage" (81%), "Don't Be Afraid" (81%)
  - 3 zetas
- **The Stranger**: 6.69 meta weight
  - 3 GAC omicrons: "I Want a Pupil" (85%), "You Might Call Me...Sith" (81%), "An Acolyte Kills" (72%)
  - 2 zetas
- **Starkiller**: 6.25 meta weight
  - 3 GAC omicrons including "There is Much Conflict" (88%)
  - 2 zetas

### Scoring Formula

#### Character Score (Main Table)
```
Base Score = 
  (GL unlocks × 3) + 
  (JG unlocks × 2) + 
  (Capital ships × 2) + 
  (Own ship × 2) + 
  (Assault battles × 2) + 
  (Active raids × 2) + 
  (Conquest × 1) + 
  (GAC tier points) + 
  (S-omicron × 2) + 
  (A-omicron × 1) + 
  (Zeta value × 0.4)

Meta Bonus = Meta Weight × 2

Final Score = Base Score + Meta Bonus
```

**Impact Example:**
- **The Stranger** (before meta): ~8 points → (after meta): ~21 points (+13)
- **Rey (Dark Side Vision)** (before): ~8 points → (after): ~24 points (+16)
- **General Skywalker** (before): ~12 points → (after): ~20 points (+8)

Result: The Stranger jumps ahead of GAS when filtering by Omicron, because his GAC value is demonstrably higher.

#### Event Score (Roster Planner)
```
Base Score = 
  (# characters × 10) + 
  (avg relic level × 5) + 
  (type bonus: GL=100, JG=50)

Meta Bonus = Σ(character meta weights) × 5

Final Score = Base Score + Meta Bonus
```

Events requiring high-meta characters (Rey DSV, The Stranger, Baylan Skoll) score 30-50 points higher in your unlock priority list.

---

## Top Meta Characters (As of March 2026)

### Tier S+ (7.0+ Meta Weight)
1. **Rey (Dark Side Vision)**: 7.92 - All 3 GAC omis widely adopted
2. **Baylan Skoll**: 7.11 - "It's All Inevitable" meta leader
3. **Bo-Katan Mandalor**: 7.07 - Mandalorian GAC core

### Tier S (6.0-7.0 Meta Weight)
4. **The Stranger**: 6.69 - Sith GAC leader, 85% adoption
5. **Third Sister**: 6.62 - Inquisitor GAC anchor
6. **Starkiller**: 6.25 - "Conflict in You" at 88%
7. **Queen Amidala**: 6.07 - Gungan/Naboo leader

### High-Value GLs (Zeta-Heavy)
13. **Ahsoka Tano (GL)**: 4.98 - 5 top-tier zetas, no GAC omis
14. **Pirate King Hondo (GL)**: 4.97 - Complete zeta suite
15. **Jabba the Hutt (GL)**: 4.97 - All zetas near-universal
16. **Leia Organa (GL)**: 4.97 - Full adoption on all abilities
17. **Rey (GL)**: 4.96 - Standard GL zeta package
18. **Lord Vader**: 4.96 - High-value but no new omicrons
19. **Jedi Master Kenobi**: 4.95 - Solid GL foundation
20. **Jedi Master Luke**: 4.94 - Classic GL, universal zetas

---

## Understanding the Data

### What "Adoption Rate" Means

When we say Starkiller's "There is Much Conflict in You" has **88% adoption**:
- 88% of relic-level Starkiller owners have that omicron applied
- This signals: *"This ability is so good, almost everyone who can use it does"*
- Contrast: Low adoption (30-40%) = niche/optional ability

### Why Omicrons Are Weighted 2× Zetas

1. **Omicrons are GAC-specific** - they only work in the mode we're optimizing for
2. **Omicrons are mode-locked** - you can't use a TW omicron in GAC
3. **Zetas work everywhere** - universal value, but not mode-optimized

By weighting GAC omicrons at 2×, we prioritize characters whose kits are **designed for the content we care about**.

### Data Freshness

Meta weights are based on **March 2026 SWGOH.gg data**:
- 92 GAC omicrons analyzed
- 100 top zetas included
- 75 characters with meta weights
- Adoption rates from relic+ player base

---

## Advanced Features

### Roster Planner Section

Below the main table, you'll find the **Unlock Priority Planner**:

1. **Shows all unlockable content** (GLs, JG, capital ships)
2. **Calculates your gap** (how many characters/relics needed)
3. **Ranks by ROI** (score ÷ total gap)
4. **Color-coded progress bars** for visual tracking

**Filters:**
- All / GL Only / JG Only / Ships Only / LST Battles Only

**Sort Options:**
- Nearest: Smallest gap first (quick wins)
- Furthest: Largest gap first (long-term plans)
- Highest Score: Most valuable unlocks first (meta-weighted)

### Search Function

Type character names, factions, or keywords:
- "Sith" - All Sith characters
- "Conquest" - All Conquest characters
- "Executor" - Characters for Executor unlock

---

## Why "Tosche Station"?

> "But I was going into Tosche Station to pick up some power converters!" - Luke Skywalker

In the original Star Wars, Tosche Station is where Luke wanted to go to get equipment upgrades. In SWGOH, this tool is where you go to figure out which character upgrades (relics, omicrons, zetas) will actually power up your GAC performance.

It's about making informed decisions on where to spend your resources, not just blindly following a farming order.

---

## Technical Details

### Data Sources

1. **Character Database**: Built-in comprehensive character data including:
   - All GL requirements (exact relic tiers)
   - Journey Guide events
   - Assault Battle eligibility
   - Raid requirements
   - Omicron/zeta tier classifications

2. **Meta Weights**: Derived from SWGOH.gg adoption rate statistics
   - % of Relic+ players with each ability
   - Filtered to GAC-relevant omicrons only
   - Top 100 most-adopted zetas

3. **Roster Data**: Fetched from SWGOH.gg API
   - Your current stars/relics/gear
   - Ally code lookup
   - Automatic caching

### Browser Compatibility

- Chrome/Edge: Full support
- Firefox: Full support
- Safari: Full support
- Mobile: Works but better on tablet/desktop for table viewing

### File Format

- **Standalone HTML** - No internet required after initial load (except for roster fetch)
- **No external dependencies** - Everything self-contained
- **Works offline** - Load once, use anywhere
- **JSON export/import** - Save your roster locally

---

## Frequently Asked Questions

**Q: Why does The Stranger rank higher than characters in more GL requirements?**  
A: Because The Stranger's GAC omicrons have 72-85% adoption rates. Being required for 1 GL doesn't matter if your kit wins GAC matches. Meta overlay prioritizes *winning* over *unlocking*.

**Q: Should I skip GL requirements to farm high-meta characters?**  
A: No! Use this as a *tiebreaker*. If you're choosing between two similar farms, pick the one with higher meta weight. Don't skip JML requirements for The Stranger, but DO prioritize Rey DSV over a lower-value GL req if the unlock timelines are similar.

**Q: Why aren't TW omicrons included?**  
A: Because we're optimizing for GAC, not TW. A character with TW-only omicrons has zero additional GAC value, so they shouldn't score higher in a GAC farming guide.

**Q: How often should meta weights be updated?**  
A: Every 2-3 months as the meta shifts. New character releases, omicron additions, and balance changes affect adoption rates.

**Q: What if a character I'm farming isn't listed in META_WEIGHTS?**  
A: They get a meta weight of 0 (neutral). Their base score from unlocks/raids/ABs still applies. Only the top ~75 meta-relevant characters have weights.

**Q: Can I add my own custom weights?**  
A: Yes - open the HTML file in a text editor, find the `META_WEIGHTS` object (around line 2190), and modify the values. Save and reload.

---

## Version History

**v13 (March 18, 2026)** - GAC Meta Overlay  
- Added meta weighting system (92 GAC omicrons, 100 top zetas)
- Character scoring now includes adoption-rate-driven bonuses
- Event unlock priorities factor in meta weights
- Fixed initialization order bugs
- Rebranded to Tosche Station

**v12 (Prior)** - DB Integrated  
- Comprehensive GL/JG/AB databases
- Roster planner with gap analysis
- Multiple sort/filter options

---

## Credits & Attribution

- **Meta Data Source**: SWGOH.gg adoption rate statistics
- **Character Data**: Official SWGOH game data + community research
- **Tool Development**: Custom SWGOH optimization framework
- **Inspiration**: The need to answer "What should I farm?" with data, not guesses

---

## Support & Feedback

Found a bug? Have a suggestion? Want updated meta weights?

This is a living tool - as the game meta evolves, the weights should be refreshed to reflect current GAC reality.

**May the Force be with your farming priorities.**

---

*Last Updated: March 18, 2026*  
*Data Accuracy: Based on March 2026 SWGOH.gg adoption rates*  
*Next Recommended Update: June 2026 (post-meta-shift)*
