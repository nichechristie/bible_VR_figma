# Guide 06: NPC Character Design for Bible VR

A comprehensive Figma guide for designing NPC (Non-Player Character) UI elements, dialogue systems, and character cards for biblical figures in your VR experience.

---

## Table of Contents

1. [Overview](#overview)
2. [Character Card Design](#character-card-design)
3. [NPC Dialogue UI](#npc-dialogue-ui)
4. [Character Portraits](#character-portraits)
5. [Name Tags and Labels](#name-tags-and-labels)
6. [Emotion Indicators](#emotion-indicators)
7. [NPC Interaction Prompts](#npc-interaction-prompts)
8. [Character Information Panels](#character-information-panels)
9. [Biblical Figure Categories](#biblical-figure-categories)
10. [Crowd and Group UI](#crowd-and-group-ui)
11. [Complete NPC UI Components](#complete-npc-ui-components)

---

## Overview

NPCs (Non-Player Characters) need clear, readable UI elements in VR. This guide covers designing all the interface components that accompany biblical figures in your game.

### What You'll Design

- Character cards showing NPC information
- Dialogue boxes for conversations
- Name tags that float above characters
- Emotion/mood indicators
- Interaction prompts
- Character relationship displays

### Design Principles for NPC UI

1. **Readable at VR distances** - Large text, high contrast
2. **Non-intrusive** - Don't block the character
3. **Contextual** - Show relevant info at the right time
4. **Consistent** - Same style across all NPCs
5. **Thematic** - Match the biblical/ancient aesthetic

---

## Character Card Design

Character cards display NPC information when players inspect or meet a character.

### Step 1: Create the Card Frame

1. Press **F** to create a Frame
2. Set size to **600 x 800 px** (portrait orientation)
3. Apply these styles:
   - Fill: `#1A1A1A` (90% opacity)
   - Corner radius: `24 px`
   - Drop shadow: `0, 8, 32, #000000 (40%)`

### Step 2: Add Character Portrait Area

1. Draw a **Rectangle** at the top
2. Size: **600 x 350 px**
3. Corner radius: `24 24 0 0` (top corners only)
4. This will hold the character image

### Step 3: Design Info Section

1. Below portrait, add padding: `32 px`
2. Create text hierarchy:

```
Character Name        - Cinzel Bold, 48px, #D4AF37
Role/Title           - Inter SemiBold, 28px, #FFFEF5 (70%)
━━━━━━━━━━━━━━━━━━━
Description text     - Inter Regular, 24px, #FFFEF5
```

### Step 4: Add Scripture Reference

1. At bottom of card
2. Style: Inter Italic, 20px, #87CEEB
3. Example: "Matthew 4:18-20"

### Complete Character Card Layout

```
┌─────────────────────────┐
│                         │
│    [Character Image]    │
│                         │
├─────────────────────────┤
│  PETER                  │
│  Apostle • Fisherman    │
│  ─────────────────────  │
│  "Upon this rock I      │
│  will build my church"  │
│                         │
│  Matthew 16:18          │
└─────────────────────────┘
```

---

## NPC Dialogue UI

Design conversation interfaces for when players talk to NPCs.

### Basic Dialogue Box

1. Create Frame: **1400 x 300 px**
2. Position: Bottom center of screen
3. Styles:
   - Fill: `#0D0D0D` (85% opacity)
   - Border: `2px solid #D4AF37`
   - Corner radius: `16 px`
   - Blur behind: `20 px`

### Dialogue Box Components

#### Speaker Name

1. Position: Top left, outside the box
2. Create a small tab shape
3. Text: Cinzel Bold, 32px, #D4AF37
4. Background: #0D0D0D

```
    ┌─ PETER ─┐
┌───┴─────────┴───────────────────┐
│                                 │
│  "Come, follow me, and I will   │
│  make you fishers of men."      │
│                                 │
│              [Continue ▶]       │
└─────────────────────────────────┘
```

#### Dialogue Text

- Font: Inter Regular, 36px
- Color: #FFFEF5
- Line height: 150%
- Padding: 40px

#### Continue Indicator

1. Right side of dialogue box
2. Text: "Continue" or arrow icon
3. Subtle pulse animation hint
4. Color: #D4AF37 (50% opacity)

### Dialogue with Choices

When players can respond:

```
┌─────────────────────────────────┐
│  "Will you come with me to      │
│   Jerusalem for the Passover?"  │
│                                 │
│  ┌─────────────────────────┐    │
│  │  Yes, I will follow     │    │
│  └─────────────────────────┘    │
│  ┌─────────────────────────┐    │
│  │  Tell me more first     │    │
│  └─────────────────────────┘    │
│  ┌─────────────────────────┐    │
│  │  I need time to decide  │    │
│  └─────────────────────────┘    │
└─────────────────────────────────┘
```

#### Choice Button Styling

1. Size: **520 x 64 px**
2. Fill: `#2D2D2D`
3. Border: `1px solid #D4AF37 (30%)`
4. Corner radius: `8 px`
5. Text: Inter Medium, 28px, #FFFEF5
6. Padding: `16 px`

#### Choice Button States

**Default:**
- Fill: #2D2D2D
- Border: 30% opacity

**Hover/Selected:**
- Fill: #3D3D3D
- Border: 100% opacity
- Glow effect

---

## Character Portraits

Design portrait thumbnails for dialogue and UI.

### Portrait Sizes

Create these standard sizes:

| Use Case | Size | Shape |
|----------|------|-------|
| Dialogue box | 120 x 120 px | Circle |
| Character card | 600 x 350 px | Rounded rectangle |
| Mini HUD | 64 x 64 px | Circle |
| Relationship | 80 x 80 px | Circle |

### Portrait Frame Design

1. Create circle: **120 x 120 px**
2. Add stroke: `3px solid #D4AF37`
3. Add outer glow: `0, 0, 12, #D4AF37 (30%)`
4. Inner shadow for depth: `inset 0, 4, 8, #000000 (30%)`

### Portrait with Role Indicator

Add a small badge showing character type:

```
    ┌───────┐
   ╱  IMG  ╲
  │         │
   ╲       ╱
    └──┬──┘
      [A]     ← Role badge (Apostle)
```

Role badge colors:
- Apostle: #D4AF37 (Gold)
- Prophet: #9C27B0 (Purple)
- Angel: #FFFEF5 (White)
- Roman: #C41E3A (Red)
- Pharisee: #1E3A5F (Blue)

---

## Name Tags and Labels

Floating labels that appear above NPCs in the world.

### Basic Name Tag

1. Create Frame: Auto-width, **48 px** height
2. Auto Layout: Horizontal, padding `16 px`
3. Fill: `#0D0D0D` (70% opacity)
4. Corner radius: `8 px`
5. Text: Inter SemiBold, 28px, #FFFEF5

### Name Tag with Title

```
┌─────────────────┐
│  PETER          │
│  Apostle        │
└─────────────────┘
```

- Name: Inter Bold, 28px, #FFFEF5
- Title: Inter Regular, 20px, #D4AF37

### Interactive Name Tag

When player can interact:

```
┌──────────────────┐
│  ✦ PETER         │
│  Press A to talk │
└──────────────────┘
```

- Add interaction icon (star, hand)
- Add prompt text below name
- Pulse animation on icon

### Name Tag Visibility States

Design these variants:
1. **Far** - Name only, small
2. **Medium** - Name + title
3. **Near** - Name + title + interact prompt
4. **Talking** - Hidden (dialogue open)

---

## Emotion Indicators

Show NPC emotional state during conversations.

### Emotion Icon Set

Create icons for these emotions:

| Emotion | Icon | Color |
|---------|------|-------|
| Happy | 😊 | #FFD700 |
| Sad | 😢 | #87CEEB |
| Angry | 😠 | #FF4444 |
| Surprised | 😮 | #FF9800 |
| Peaceful | 😌 | #4CAF50 |
| Thoughtful | 🤔 | #9C27B0 |
| Worried | 😟 | #FFA726 |
| Hopeful | 🙏 | #D4AF37 |

### Emotion Display Design

1. Small indicator next to portrait
2. Size: **40 x 40 px**
3. Circle background matching emotion color (20% opacity)
4. Icon in center

```
┌─────┐  ┌───┐
│ IMG │  │😊 │  ← Emotion indicator
└─────┘  └───┘
```

### Emotion Transition

Show emotion changes:
1. Old emotion fades out (200ms)
2. New emotion fades in (300ms)
3. Subtle color shift on portrait border

---

## NPC Interaction Prompts

UI that appears when player is near an interactable NPC.

### Basic Interaction Prompt

1. Frame: **300 x 80 px**
2. Fill: `#0D0D0D` (80% opacity)
3. Corner radius: `12 px`
4. Border: `1px solid #D4AF37`

Contents:
```
┌──────────────────┐
│  [A] Talk        │
└──────────────────┘
```

- Button icon in circle: 40x40, #D4AF37 fill
- Text: Inter Medium, 28px, #FFFEF5

### Multiple Interactions

When NPC has several options:

```
┌──────────────────┐
│  [A] Talk        │
│  [X] Give item   │
│  [Y] Follow      │
└──────────────────┘
```

### Context-Sensitive Prompts

Different prompts for different NPCs:

**Merchant:**
```
[A] Trade    [X] Browse goods
```

**Quest NPC:**
```
[A] Continue quest    [Y] Ask about quest
```

**Companion:**
```
[A] Talk    [X] Inventory    [Y] Commands
```

---

## Character Information Panels

Detailed info panels for the journal/codex.

### Full Character Profile

Size: **800 x 1000 px** (scrollable)

```
┌─────────────────────────────────┐
│  [Portrait]                     │
│                                 │
│  MARY MAGDALENE                 │
│  Faithful Follower              │
│  ═══════════════════════════    │
│                                 │
│  BACKGROUND                     │
│  First witness to the           │
│  resurrection of Jesus...       │
│                                 │
│  KEY SCRIPTURE                  │
│  John 20:11-18                  │
│                                 │
│  RELATIONSHIP                   │
│  ████████░░ Trusted             │
│                                 │
│  ENCOUNTERS                     │
│  • Met at the Empty Tomb        │
│  • Spoke in Jerusalem           │
│                                 │
└─────────────────────────────────┘
```

### Section Styling

**Section Headers:**
- Font: Cinzel Bold, 28px, #D4AF37
- Uppercase
- Letter spacing: 4px
- Line below: 1px #D4AF37 (30%)

**Body Text:**
- Font: Inter Regular, 24px, #FFFEF5
- Line height: 160%

**Relationship Bar:**
- Height: 12px
- Background: #2D2D2D
- Fill: Gradient based on level
- Corner radius: 6px

Relationship colors:
- Stranger: #666666
- Acquaintance: #87CEEB
- Friendly: #4CAF50
- Trusted: #D4AF37
- Devoted: #9C27B0

---

## Biblical Figure Categories

Design category-specific UI elements.

### Jesus Christ

**Special Treatment:**
- Golden glow around portrait
- Larger name text
- "The Messiah" subtitle
- White/gold color scheme

```
       ✦ ✦ ✦
    ┌─────────┐
   ╱│   IMG   │╲
  ✦ │         │ ✦
   ╲│         │╱
    └─────────┘
       ✦ ✦ ✦

   JESUS CHRIST
   The Messiah
```

### The Twelve Apostles

Create consistent cards with:
- Apostle badge (gold)
- Calling/profession subtitle
- Associated symbol icon

**Apostle Symbols:**

| Apostle | Symbol |
|---------|--------|
| Peter | Keys |
| Andrew | X-cross |
| James | Shell |
| John | Eagle |
| Philip | Cross/loaves |
| Bartholomew | Knife |
| Matthew | Money bag |
| Thomas | Spear |
| James (Lesser) | Club |
| Thaddaeus | Axe |
| Simon | Saw |
| Judas | Money bag (dark) |

### Angels

**Special Effects:**
- White glowing border
- Ethereal blur effect
- Wings icon in corner
- Light blue accent color

```
    ╱ ╲
   ╱   ╲
  │ IMG │  ✦
   ╲   ╱
    ╲ ╱

  GABRIEL
  Archangel
```

### Roman Soldiers

**Military Style:**
- Red accent color (#C41E3A)
- Sharp corners (4px radius)
- Rank indicator
- Legion number

```
┌─────────────────┐
│ ▌MARCUS         │
│  Centurion      │
│  X Legion       │
└─────────────────┘
```

### Religious Leaders

**Formal Style:**
- Blue accent (#1E3A5F)
- Ornate border pattern
- Title emphasis
- Scroll icon

```
╔═════════════════╗
║  CAIAPHAS       ║
║  High Priest    ║
╚═════════════════╝
```

---

## Crowd and Group UI

Design UI for groups of NPCs.

### Crowd Indicator

When multiple generic NPCs are present:

```
┌─────────────────────┐
│  👥 Crowd of 12     │
│  Jerusalem Market   │
└─────────────────────┘
```

- Group icon
- Count number
- Location/type

### Group Conversation

When talking to multiple NPCs:

```
┌─ PHARISEES ─────────────────────┐
│  👤👤👤                          │
│                                 │
│  "By what authority do you      │
│   do these things?"             │
│                                 │
└─────────────────────────────────┘
```

- Multiple portrait icons
- Group name as speaker
- Collective dialogue

### Named NPCs in Crowd

Highlight important figures:

```
  👤 👤 👤 ⭐ 👤 👤
         ↑
      NICODEMUS
    [A] to approach
```

---

## Complete NPC UI Components

### Component Library Checklist

Create these Figma components:

**Cards:**
- [ ] Character Card (Basic)
- [ ] Character Card (Detailed)
- [ ] Mini Character Card

**Dialogue:**
- [ ] Dialogue Box (Basic)
- [ ] Dialogue Box (With Choices)
- [ ] Dialogue Box (With Portrait)

**Labels:**
- [ ] Name Tag (Simple)
- [ ] Name Tag (With Title)
- [ ] Name Tag (Interactive)

**Portraits:**
- [ ] Portrait Circle (Large)
- [ ] Portrait Circle (Medium)
- [ ] Portrait Circle (Small)
- [ ] Portrait with Badge

**Indicators:**
- [ ] Emotion Icon Set
- [ ] Relationship Bar
- [ ] Interaction Prompt

**Special:**
- [ ] Jesus Card
- [ ] Apostle Card
- [ ] Angel Card
- [ ] Roman Card

### Master Component Setup

1. Create a page called "NPC Components"
2. Organize by category
3. Use variants for states:
   - Default
   - Hover
   - Active
   - Disabled

### Color Variables

Set up these as Figma variables:

```
NPC/Apostle = #D4AF37
NPC/Prophet = #9C27B0
NPC/Angel = #FFFEF5
NPC/Roman = #C41E3A
NPC/Pharisee = #1E3A5F
NPC/Neutral = #87CEEB
```

---

## Exporting NPC UI Assets

### Export Settings

**For Unreal Engine:**

1. Select component
2. Click **Export** in right panel
3. Settings:
   - Format: PNG
   - Scale: 2x
   - Background: Transparent

### Naming Convention

```
UI_NPC_[Type]_[Element]_[State].png
```

Examples:
- `UI_NPC_Apostle_Card_Default.png`
- `UI_NPC_Dialogue_Box_WithChoices.png`
- `UI_NPC_NameTag_Interactive_Hover.png`

### Slice Exports

For 9-slice scaling panels:
1. Add export settings for slices
2. Mark slice boundaries
3. Export as separate images

---

## Design Best Practices

### Accessibility

1. **Minimum text size**: 24px for VR
2. **High contrast**: 4.5:1 ratio minimum
3. **Color coding + icons**: Don't rely on color alone
4. **Clear focus states**: Show what's selected

### Performance

1. Keep assets under 2048x2048
2. Use compressed PNGs
3. Minimize gradients (use solid colors)
4. Reuse components

### Consistency

1. Use the same portrait size across all NPCs
2. Keep dialogue box in same position
3. Consistent animation timing
4. Same interaction prompt style

---

## Next Steps

After completing this guide:

1. **Create all component variants** in Figma
2. **Test in VR prototype** for readability
3. **Export assets** for Unreal Engine
4. **Document** all component specifications

### Related Guides

- **GUIDE_03_BIBLE_VR_ASSETS.md** - Basic components
- **GUIDE_05_QUEST_UI_DESIGN.md** - Quest-related NPC UI

---

## Quick Reference

### NPC UI Sizes

| Element | Size |
|---------|------|
| Character Card | 600 x 800 px |
| Dialogue Box | 1400 x 300 px |
| Portrait Large | 120 x 120 px |
| Portrait Small | 64 x 64 px |
| Name Tag | Auto x 48 px |
| Choice Button | 520 x 64 px |

### NPC Colors

| Category | Primary | Accent |
|----------|---------|--------|
| Apostle | #D4AF37 | #FFFEF5 |
| Angel | #FFFEF5 | #87CEEB |
| Roman | #C41E3A | #FFFEF5 |
| Pharisee | #1E3A5F | #D4AF37 |

### Typography

| Element | Font | Size |
|---------|------|------|
| Character Name | Cinzel Bold | 48px |
| Dialogue Text | Inter Regular | 36px |
| Name Tag | Inter SemiBold | 28px |
| Subtitle | Inter Regular | 20px |

---

*Well-designed NPC UI creates connection between player and character. Make it readable, consistent, and beautiful - these are the faces of your biblical story.*
