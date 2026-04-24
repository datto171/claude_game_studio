# Game Concept: Bag Blitz (Working Title)

*Created: 2026-04-22*
*Status: Draft*

---

## Elevator Pitch

> It's a portrait mobile roguelite where you arrange tetromino-shaped weapons,
> armor, and items into a bag that fights for you automatically — surviving
> 10 waves by optimizing your loadout between rounds.
>
> Like Vampire Survivors, AND ALSO your inventory is a spatial puzzle you
> solve between waves, and how you arrange your items determines what triggers,
> what combos, and what keeps you alive.

---

## Core Identity

| Aspect | Detail |
| ---- | ---- |
| **Genre** | Roguelite / Auto-battler / Inventory Puzzle |
| **Platform** | Mobile (iOS / Android) — portrait orientation |
| **Target Audience** | Mid-core mobile gamers, roguelite / optimization fans |
| **Player Count** | Single-player |
| **Session Length** | 15–20 minutes (10 waves per run) |
| **Monetization** | TBD |
| **Estimated Scope** | Medium (4–8 months, solo dev) |
| **Comparable Titles** | Backpack Hero, Vampire Survivors, Balatro |

---

## Core Fantasy

You are a master loadout engineer. You do not fight — your bag fights for you.
The thrill is in building the perfect combination of items, arranging them
optimally in your grid, and watching your automated arsenal tear through wave
after wave. When the bag is working, you do not touch a thing — you just watch
the carnage unfold and feel the satisfaction of a plan executed perfectly.

---

## Unique Hook

Like Vampire Survivors, AND ALSO your inventory is a tetromino grid you solve
between waves — how you spatially arrange items determines which adjacency bonds
activate, which cooldowns overlap, and whether your build survives wave 10.

---

## Visual Identity Anchor

**Direction:** Clean, high-contrast 2D with bold item iconography.

**One-line visual rule:** Every element in the bag must be readable at a glance
on a 6-inch phone screen — clarity over decoration.

**Supporting principles:**
- Bag / inventory panel uses a dark, grounded palette (leather, stone, or tech
  grid aesthetic) so colorful item icons pop with immediate readability.
- Combat panel (upper half) uses high-contrast, animated effects — item-fire
  animations must feel punchy and satisfying even at small scale.
- Cooldown bars are always visible on bag tiles; their fill animation IS the
  game's primary feedback loop and must be polished before anything else.

**Color philosophy:** Functional color coding first. Each adjacency tag (Fire,
Ice, Holy, Shadow) has a distinct, colorblind-accessible hue used consistently
across icons, borders, and aura effects.

---

## Player Experience Analysis (MDA Framework)

### Target Aesthetics (What the player FEELS)

| Aesthetic | Priority | How We Deliver It |
| ---- | ---- | ---- |
| **Challenge** (obstacle course, mastery) | 1 | Spatial optimization puzzle; escalating wave difficulty; item trade-off decisions |
| **Submission** (relaxation, comfort zone) | 2 | Auto-combat — once the bag is set, the player watches; no execution pressure |
| **Discovery** (exploration, secrets) | 3 | Adjacency bond combinations; rare item interactions; character trait variety |
| **Expression** (self-expression, creativity) | 4 | Build variety; character selection shapes strategic approach |
| **Sensation** (sensory pleasure) | 5 | Item-fire animations; satisfying cooldown-pop feedback; screen juice |
| **Fantasy** (make-believe, role-playing) | 6 | Light character identity through distinct traits |
| **Narrative** (drama, story arc) | N/A | Story is flavor text on items only |
| **Fellowship** (social connection) | N/A | No multiplayer at launch |

### Key Dynamics (Emergent player behaviors)

- Players experiment with item placement to discover which adjacency bonds
  activate and what bonus they produce.
- Players develop "signature builds" that they iterate and optimize across runs.
- Players feel urgency to place new items efficiently in the brief window between
  waves — the planning phase has natural time pressure.
- Players evaluate character traits at run start and mentally pre-plan their
  preferred upgrade path before wave 1 begins.

### Core Mechanics (Systems we build)

1. **Tetromino bag grid** — 5×5 to 6×6 tile grid with locked slots that unlock
   progressively. Items come in 5 shapes (1×1, 1×2, 2×1, 2×2, L-shape).
2. **Item auto-trigger** — each item has a cooldown bar; when full, it fires
   automatically. Cooldown bars are frozen during the planning phase.
3. **Adjacency bond system** — items sharing the same tag (Fire, Ice, Holy,
   Shadow) placed in adjacent tiles activate a passive aura that boosts both
   items (e.g., +15% damage, reduced cooldown).
4. **Wave-based upgrade selection** — after each wave, player picks 1 of 3
   randomly drawn upgrade options (economy, power, survivability, or utility).
5. **Item roll & placement** — after wave, player is offered new items to
   drag-place into the bag; can sacrifice existing items to make room.

---

## Player Motivation Profile

### Primary Psychological Needs Served

| Need | How This Game Satisfies It | Strength |
| ---- | ---- | ---- |
| **Autonomy** (freedom, meaningful choice) | Player controls full bag layout, item selection, upgrade path, and character choice | Core |
| **Competence** (mastery, skill growth) | Spatial optimization skill grows with item knowledge; experienced players spot adjacency bonds others miss | Core |
| **Relatedness** (connection, belonging) | Minimal — character identity provides light flavor; no social features at launch | Minimal |

### Player Type Appeal (Bartle Taxonomy)

- [x] **Achievers** — completing 10-wave runs, unlocking characters, maximizing
  damage output, chasing high-efficiency builds
- [x] **Explorers** — discovering adjacency bond combos, uncovering rare item
  interactions, understanding the full item system
- [ ] **Socializers** — not a target at launch
- [ ] **Killers/Competitors** — no PvP; leaderboard is a potential future addition

### Flow State Design

- **Onboarding curve**: Waves 1–2 act as a soft tutorial — sparse bag, single
  basic weapon, limited upgrade choices. Complexity is introduced gradually as
  slots unlock and the item pool grows.
- **Difficulty scaling**: Enemy count, health, and damage scale per wave. Locked
  slot patterns change challenge geometry (center-locked = more disruptive than
  corner-locked). Wave 10 is the highest-pressure survival gauntlet.
- **Feedback clarity**: Cooldown bar fills visually per tile; item-fire triggers
  an animation in both the bag and the combat panel simultaneously; floating
  damage numbers confirm impact. Players always know their bag state.
- **Recovery from failure**: A failed run takes 15–20 min. Failure is educational
  — the bag is visible and the player can identify what went wrong. Quick restart
  preserves momentum.

---

## Core Loop

### Moment-to-Moment (30 seconds)

The bag is frozen. Cooldown bars fill on each tile. When a bar completes, the
item fires automatically — triggering an animation in the bag tile and a
corresponding attack or effect in the combat panel above. The player watches,
feels the rhythm of their build, and monitors their HP bar. No input required
or possible during a wave.

### Short-Term (5 minutes — one wave cycle)

1. Wave starts — enemies spawn and advance in the combat panel
2. Bag auto-fires until wave is cleared or player dies
3. Wave ends → upgrade choice (pick 1 of 3 options)
4. Item roll → new item offered, player decides to place or skip
5. Planning phase → drag items to new positions, activate adjacency bonds
6. Next wave begins; bag locks again

### Session-Level (15–20 minutes — full run)

- **Waves 1–3**: Sparse bag (many locked slots), few items, low stakes; learning
  item behavior and the upgrade menu
- **Waves 4–6**: Mid-run; adjacency bonds becoming possible; first meaningful
  build decisions emerging; difficulty spikes noticeable
- **Waves 7–9**: Near-full bag; optimization under pressure; every new item offer
  forces a trade-off against existing layout
- **Wave 10**: Maximum enemy pressure; player survives with what they have built;
  run ends in success or failure

### Long-Term Progression

Run-earned gold accumulates across sessions as meta-currency. Spent to:
- Unlock additional characters (new bag traits)
- Add rare items permanently to the loot pool

**No permanent power increases** — all meta-progression unlocks options, not
stats, preserving roguelite fairness. Every run is winnable from the start.

### Retention Hooks

- **Curiosity**: "What does this rare item do? What happens if I place these two
  next to each other? I haven't tried that character yet."
- **Investment**: Near-miss psychology — "I was at wave 9, I know what I'd change."
- **Mastery**: Players build mental models of item synergies and optimal placement
  patterns; skill visibly improves across sessions.
- **Social**: Minimal at launch — potential future: async run sharing or score
  comparison.

---

## Game Pillars

### Pillar 1: The Bag IS the Game

Every meaningful decision lives in the inventory. Combat is the reward for good
planning — not the challenge itself. The bag is the primary screen real estate
and the primary design investment.

*Design test*: If we're debating whether to add any mechanic, ask: "Does it
involve the bag?" If no, it needs exceptional justification to exist.

### Pillar 2: Spatial Clarity

The bag must be readable at a glance on a phone screen. Players should never
need to open a tooltip to understand the current state of their build. Icon
design, color coding, and cooldown visualization must be unambiguous.

*Design test*: If adding an item or effect requires reading 3+ lines of text
to understand during a wave, it does not ship in its current form.

### Pillar 3: Player-Driven Tactics

Characters offer distinct strategic starting points and playstyle options that
shape which upgrades and items a player prioritizes — without mandating a
completely different build to win. Players choose their approach; multiple paths
to wave 10 survival are valid.

*Design test*: If a character trait does not meaningfully change which upgrades
or items a player prioritizes across the run, the trait is not doing enough work.

### Pillar 4: Passive Satisfaction

Auto-combat animations, item-fire effects, and cooldown feedback are the core
emotional payoff of every session. These are not decoration — they are the game's
primary sensory reward. A good bag *sounds* and *looks* right.

*Design test*: If a new item's fire animation does not feel satisfying to watch
in isolation, it is not ready to ship — regardless of its mechanical value.

### Pillar 5: Respect the 15-Minute Session

A complete run takes 15–20 minutes. Every wave should feel tense without feeling
unfair. No run ends purely from a random spike with no counterplay available.
The planning phase must be long enough to make meaningful decisions but short
enough to maintain momentum.

*Design test*: If a wave 8 player can be killed by an RNG spike with no
decision they could have made to prevent it, the wave design is too punishing.

### Anti-Pillars (What This Game Is NOT)

- **NOT a reflex game**: No timing windows, skill shots, or precise taps required
  during combat. All execution skill is expressed in the planning phase.
- **NOT a story game**: Narrative is flavor text on item descriptions only. No
  story structure, cutscenes, or dialogue systems.
- **NOT a multiplayer game**: Single-player at launch. No async PvP, guilds, or
  social obligations.
- **NOT a grind-gate game**: All characters unlockable within 5–10 runs. No
  content locked behind 50+ hour paywalls.

---

## Item System Design

### Tetromino Shape Vocabulary

| Shape | Tiles | Examples | Role |
| ---- | ---- | ---- | ---- |
| 1×1 | 1 | Potion, Ring, Rune | Filler; gap-use; small utility |
| 1×2 | 2 | Sword, Wand, Dagger | Primary weapons; common |
| 2×1 | 2 | Bow, Crossbow | Ranged weapons; common |
| 2×2 | 4 | Shield, Tome, Bomb | High-power, space-cost trade-off; rare |
| L-shape | 3 | Scythe, Staff | High-value; rare / epic tier only |

Keeping to 5 shapes provides spatial variety without exploding placement
complexity for a solo dev scope.

### Adjacency Tag System

Each item carries one tag. Items sharing a tag placed in adjacent tiles activate
a passive aura boosting both items. Four tags:

| Tag | Passive Aura Effect | Visual Identity |
| ---- | ---- | ---- |
| Fire | +15% damage | Orange border glow |
| Ice | -10% cooldown on both | Blue border pulse |
| Holy | +10% healing on healing items | Yellow soft halo |
| Shadow | +5% chance to trigger twice | Purple flicker |

**Design rule**: No item has more than one tag. Adjacency bonds are binary
(active or inactive) — no stacking beyond the first adjacent pair per item.
Players see bonds activate via border color immediately on placement.

### Item Rarity Tiers

Shown as colored orbs (no percentages displayed to players):

| Tier | Visual | Availability |
| ---- | ---- | ---- |
| Common | Grey orb | Waves 1–10 |
| Rare | Blue orb | Waves 3–10 |
| Epic | Purple orb | Waves 6–10 |

---

## Character System

Characters are selected at run start. Each has:
- A distinct **bag trait** (functional difference, not just stats)
- A **starting item** aligned to their trait
- The same base grid size (modified by trait)

**Planned characters (4 total for full release):**

| Character | Key Trait | Strategic Angle |
| ---- | ---- | ---- |
| Warrior | Larger bag (6×6 vs 5×5) | More items, more adjacency opportunity |
| Rogue | Random buff applied to bag each wave | Volatile; high ceiling, unpredictable |
| Merchant | Chance for extra gold on kill | Economy-focused; buy more upgrades |
| Alchemist | Some tiles trigger items twice | Cooldown-heavy builds; Fire/Ice synergy |

---

## Wave & Upgrade System

### Upgrade Option Categories

After each wave, player picks 1 of 3 randomly drawn options:

| Category | Example Options |
| ---- | ---- |
| Economy | Gain gold directly; unlock extra inventory slot |
| Power | +X% damage all items; -X% all cooldowns |
| Survivability | Restore 50% / 100% HP; reduce future enemy HP by 20% |
| Utility | 1 free item reroll next turn; randomly upgrade 1 item in bag by 1 tier |
| RNG | Random buff applied to bag; increase Epic drop chance |

### Bag Interaction Rule

Items may only be rearranged **between waves**. During a wave, the bag is
completely locked. This is a deliberate design constraint: the tension of
"I can see this isn't working but I can't fix it mid-wave" makes the planning
phase feel high-stakes and consequential.

---

## Inspiration and References

| Reference | What We Take | What We Do Differently | Why It Matters |
| ---- | ---- | ---- | ---- |
| Backpack Hero | Spatial inventory as the core mechanic | Auto-execution (no manual combat); mobile-first portrait | Proves inventory puzzle is a viable primary loop |
| Vampire Survivors | Auto-combat + wave survival | Inventory is the skill expression, not weapon evolution | Proves passive auto-combat satisfies mobile players |
| Balatro | "Simple rules, deep optimization" roguelite | Spatial grid instead of card deck; mobile portrait format | Proves optimization loops thrive without complex execution |
| Brotato | Character variety shaping run strategy | Bag is the primary UI; no active shooting | Proves character-level differentiation adds replay value |

---

## Target Player Profile

| Attribute | Detail |
| ---- | ---- |
| **Age range** | 18–35 |
| **Gaming experience** | Mid-core |
| **Time availability** | 15–20 minute sessions; commute, breaks, before bed |
| **Platform preference** | Mobile (primary gaming device) |
| **Current games they play** | Vampire Survivors, Balatro, TFT, Brotato |
| **What they're looking for** | Satisfying optimization game; low execution pressure; short but complete sessions |
| **What would turn them away** | Pay-to-win mechanics; slow pacing; mandatory landscape orientation; tutorial longer than 2 minutes |

---

## Technical Considerations

| Consideration | Assessment |
| ---- | ---- |
| **Engine** | Unity — strong mobile tooling, touch input system, solo dev familiarity |
| **Key Technical Challenges** | Touch drag-and-drop precision (snap, rotate, ghost preview); cooldown animation performance at scale; item icon readability at small tile sizes |
| **Art Style** | 2D stylized — clean vector or readable pixel art for tile icons |
| **Art Pipeline Complexity** | Low-Medium — icon-based items, simple enemy sprites, polished UI |
| **Audio Needs** | Moderate — item-fire SFX per item type (essential per Pillar 4); ambient wave music |
| **Networking** | None at launch |
| **Content Volume** | 25+ items, 4 characters, 10 wave difficulty tiers |
| **Procedural Systems** | Wave enemy composition; item roll pool; upgrade option draw |

---

## Risks and Open Questions

### Design Risks

- Touch drag-and-drop feel could be frustrating if snap/rotate isn't polished —
  this is the most critical UX piece and must be prototyped first.
- Item readability at small tile sizes on phone screens may force icon redesign
  post-prototype.
- Wave 7–10 balance requires significant playtesting; solo dev time budget must
  account for iteration cycles.

### Technical Risks

- Smooth drag-to-grid with ghost preview, snap-to-valid-slot, and one-tap rotation
  on touch input is non-trivial in Unity — needs early prototyping.
- Performance: simultaneous cooldown animations + enemy spawn effects + floating
  damage numbers must be profiled on low-end Android devices.

### Market Risks

- Auto-battler and roguelite mobile markets are crowded; the inventory puzzle
  angle is the key differentiator that must be communicated clearly in store
  assets.
- App store discoverability without marketing budget is a challenge for solo dev
  launches.

### Scope Risks

- 25+ items × balance × adjacency bond combinations = long design iteration time;
  start with 8 items and expand only after core loop is validated.
- Art scope: each item needs a readable icon + fire animation — may require
  contracting an artist for final polish if solo dev time runs short.

### Open Questions

- Does between-waves-only rearrangement feel satisfying, or do playtests reveal
  players want minimal mid-wave input? → Resolve via prototype playtest (wave 1–5
  build, 5 external testers).
- Are adjacency bonds discoverable without a tutorial? → Test with first-time
  players in prototype; add visual hint system if discovery rate is low.
- Is 10 waves the right session length? → Prototype with 5 waves; playtest data
  will indicate whether sessions feel complete or truncated.

---

## MVP Definition

**Core hypothesis**: Players find the tetromino bag placement + auto-combat
loop engaging enough to complete a 5-wave session and want to immediately
start another run.

**Required for MVP**:
1. 5×5 bag with 3 item shapes (1×1, 1×2, 2×2); drag-to-place with snap and
   one-tap rotation
2. 8 items total with cooldown auto-trigger and visible cooldown bars
3. 5 waves with escalating enemy count and HP
4. 3 upgrade options per wave (at least 1 from each category)
5. 1 character (Warrior — straightforward, no special trait)
6. Basic item-fire animation per item type

**Explicitly NOT in MVP**:
- Meta-progression / gold carry-over
- Multiple characters
- Adjacency bond system (validate base loop before adding complexity)
- Rare / L-shaped items
- Character trait system

### Scope Tiers

| Tier | Content | Features | Timeline (solo) |
| ---- | ---- | ---- | ---- |
| **Prototype** | 1 character, 8 items, 5 waves | Core bag loop only — drag, snap, auto-trigger, basic upgrades | Weeks 4–6 |
| **MVP** | 1 character, 12 items, 10 waves | Full wave progression, all upgrade types, adjacency bonds | Month 3–4 |
| **Alpha** | 2–3 characters, 20+ items, 10 waves | Character traits, adjacency system, rough balance | Month 5–6 |
| **Full Vision** | 4 characters, 25+ items, full polish | All features, polished VFX/SFX, meta-progression, store-ready | Month 6–8 |

---

## Next Steps

- [ ] Run `/setup-engine` to configure Unity and populate version-aware reference docs
- [ ] Run `/art-bible` to establish visual identity before writing any GDDs
- [ ] Run `/design-review design/gdd/game-concept.md` to validate concept completeness
- [ ] Run `/map-systems` to decompose the concept into individual systems with dependencies
- [ ] Author per-system GDDs with `/design-system` (start with: bag grid, item system, wave system)
- [ ] Run `/create-architecture` to produce the master architecture blueprint
- [ ] Record key decisions with `/architecture-decision` (drag-and-drop system, adjacency model, cooldown architecture)
- [ ] Prototype the drag-to-place mechanic first with `/prototype bag-placement` — this is the make-or-break interaction
- [ ] Run `/playtest-report` after prototype to validate the core hypothesis
- [ ] Plan first sprint with `/sprint-plan new`
