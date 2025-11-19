# GUIDE 03: Creating Bible VR UI Assets in Figma

## Overview

This guide walks you through creating all the UI elements you need for your Bible VR game: menus, HUD, dialogue systems, icons, and more.

---

## Part 1: Setting Up Your Style Guide

Before creating assets, establish your design system.

### Create the Style Guide Page

1. Create new page called **"Style Guide"**
2. This will contain all your reusable styles

### Color Palette

Create these color styles (4 dots menu → + → Create style):

**Primary Colors:**
| Style Name | Hex | Usage |
|------------|-----|-------|
| Primary/Gold | #D4AF37 | Main accent, divine |
| Primary/White | #FFFEF5 | Text, highlights |
| Primary/Dark | #1A1A1A | Backgrounds |

**UI Colors:**
| Style Name | Hex | Usage |
|------------|-----|-------|
| UI/Background | #0D0D0D | Main background |
| UI/Panel | #2D2D2D | Cards, containers |
| UI/Border | #4A4A4A | Borders, dividers |
| UI/Text Primary | #FFFFFF | Main text |
| UI/Text Secondary | #B0B0B0 | Secondary text |

**Semantic Colors:**
| Style Name | Hex | Usage |
|------------|-----|-------|
| Semantic/Success | #4CAF50 | Complete, good |
| Semantic/Warning | #FF9800 | Caution |
| Semantic/Error | #F44336 | Error, danger |
| Semantic/Info | #2196F3 | Information |

**Biblical Themes:**
| Style Name | Hex | Usage |
|------------|-----|-------|
| Biblical/Heaven | #87CEEB | Sky, peace |
| Biblical/Spirit | #9C27B0 | Spiritual |
| Biblical/Earth | #8B7355 | Grounding |
| Biblical/Life | #228B22 | Growth |

### Typography Styles

Create text styles for VR (remember: 2-3x normal size):

**Headings:**
| Style Name | Font | Size | Weight |
|------------|------|------|--------|
| H1/Display | Cinzel | 96px | Bold |
| H2/Title | Cinzel | 72px | Bold |
| H3/Subtitle | Inter | 48px | SemiBold |

**Body:**
| Style Name | Font | Size | Weight |
|------------|------|------|--------|
| Body/Large | Inter | 36px | Regular |
| Body/Normal | Inter | 32px | Regular |
| Body/Small | Inter | 24px | Regular |

**UI Text:**
| Style Name | Font | Size | Weight |
|------------|------|------|--------|
| UI/Button | Inter | 32px | Medium |
| UI/Label | Inter | 24px | Medium |
| UI/Caption | Inter | 20px | Regular |

---

## Part 2: Creating Components

### Button Component

Let's create a versatile button with all states.

#### Step 1: Create the Base Button

1. Frame tool (F) → Draw 320 x 80 rectangle
2. Name it: `Button`
3. Style:
   - Fill: #D4AF37
   - Corner radius: 12
   - Padding: 24px horizontal

4. Add text:
   - Text: "Button Text"
   - Style: UI/Button
   - Color: #1A1A1A

5. Center the text (Align tools)

#### Step 2: Make it a Component with Variants

1. Select the button frame
2. Press **Ctrl/Cmd + Alt + K** (Create component)
3. With component selected, click **"Add variant"** in right panel

Now create these variants:

**Variant Properties:**
- **State:** Default, Hover, Active, Disabled
- **Type:** Primary, Secondary, Ghost

**Primary/Default:** (already made)
- Gold background
- Dark text

**Primary/Hover:**
- Background: #E5C158 (lighter gold)
- Add subtle glow effect

**Primary/Active:**
- Background: #B8962F (darker gold)
- Scale: 98%

**Primary/Disabled:**
- Background: #4A4A4A
- Text: #808080
- Opacity: 60%

**Secondary variants:**
- Outline style (no fill, gold border)
- Same states as Primary

**Ghost variants:**
- No background or border
- Just text that highlights on hover

#### Step 3: Add Auto Layout

1. Select button component
2. Press **Shift + A** (Add auto layout)
3. Settings:
   - Direction: Horizontal
   - Padding: 24 horizontal, 16 vertical
   - Gap: 8 (if adding icon)

Now the button resizes based on text length!

---

### Icon Button Component

For icon-only buttons (close, menu, etc.):

1. Create 64 x 64 frame
2. Add icon (from Iconify plugin or draw)
3. Size icon at 32 x 32, centered
4. Background: UI/Panel color
5. Corner radius: 12

Variants:
- Default, Hover, Active

---

### Panel/Card Component

Reusable container for content:

1. Create frame: 800 x 600
2. Style:
   - Fill: UI/Panel at 90% opacity
   - Corner radius: 24
   - Border: 1px UI/Border

3. Add effects:
   - Drop shadow: X:0, Y:8, Blur:24, #000000 25%
   - Background blur: 20

4. Add auto layout:
   - Padding: 32px
   - Gap: 24px (between items)

Make it a component, add variants:
- **Size:** Small, Medium, Large
- **Style:** Default, Highlighted (gold border)

---

### Input Field Component

For settings and forms:

1. Create frame: 400 x 64
2. Background: #0D0D0D
3. Border: 2px UI/Border
4. Corner radius: 8
5. Add placeholder text: "Enter text..."
6. Style: Body/Normal, UI/Text Secondary

Variants:
- **State:** Default, Focused (gold border), Error (red border)

---

## Part 3: Creating the Main Menu

### Main Menu Frame

1. Create frame: 2560 x 1440
2. Background: Gradient or image of biblical scene

### Menu Panel

1. Use your Panel component
2. Size: 800 x 900
3. Center on screen

### Title

1. Text: "BIBLE VR QUEST"
2. Style: H1/Display
3. Color: Primary/Gold
4. Add subtle glow effect

### Menu Buttons

Stack these buttons vertically:
1. "Begin Journey" - Primary
2. "Continue" - Primary (or disabled if no save)
3. "Select Quest" - Secondary
4. "Settings" - Ghost
5. "Exit" - Ghost

Use auto layout with 16px gap between buttons.

### Decorative Elements

Add biblical touches:
- Subtle cross icon near title
- Vine/olive branch decorations at edges
- Soft golden glow behind panel

---

## Part 4: Creating the HUD

### HUD Frame

1. Create frame: 2560 x 1440
2. Background: None (transparent)
3. This represents the VR view

### Faith Meter (Top Left)

Replaces typical health bar:

1. Create container: 300 x 60
2. Position: Top-left with 48px margin

**Elements:**
- Icon: Flame or dove (32px)
- Background bar: Rounded rectangle, dark
- Fill bar: Golden gradient
- Text: "100%" or just visual

### Compass (Top Center)

1. Create: 400 x 80 container
2. Position: Top-center

**Elements:**
- Horizontal strip with direction markers
- N, S, E, W labels
- Quest marker icon
- Center indicator (triangle pointing down)

### Current Objective (Top Right)

1. Create container: 400 x auto
2. Position: Top-right with 48px margin

**Elements:**
- Quest icon (small)
- Objective text: "Approach the tomb"
- Optional: Distance "50m"

### Interaction Prompt (Bottom Center)

Appears when looking at interactive objects:

1. Create: 300 x auto
2. Position: Bottom-center, 100px from bottom

**Elements:**
- Eye icon (gaze indicator)
- Text: "Look to interact"
- Or: "Press A to examine"

---

## Part 5: Creating the Dialogue System

### Dialogue Box

1. Create frame: 1600 x 400
2. Position: Bottom of screen
3. Background: UI/Panel at 85% opacity

**Layout:**

```
┌──────────────────────────────────────────┐
│ [Avatar]  CHARACTER NAME                 │
│           ──────────────                 │
│           "Dialogue text goes here.      │
│            This is what the character    │
│            is saying to the player."     │
│                                          │
│                        [Continue →]      │
└──────────────────────────────────────────┘
```

### Character Portrait

1. Circle frame: 120 x 120
2. Border: 3px character color
3. Image fill: Character portrait

### Character Name

1. Text style: H3/Subtitle
2. Color: Character-specific
   - Mary Magdalene: #E91E63
   - Peter: #2196F3
   - John: #9C27B0

### Dialogue Text

1. Text style: Body/Large
2. Color: UI/Text Primary
3. Max width: 1200px
4. Auto-height

### Continue Button

1. Small button or icon
2. Arrow pointing right
3. Pulses to indicate action needed

---

### Dialogue Choice UI

When player has options:

```
┌──────────────────────────────────────────┐
│ [Avatar]  MARY MAGDALENE                 │
│           "Will you enter the tomb?"     │
│                                          │
│   [ Yes, I will enter ]                  │
│   [ Tell me more first ]                 │
│   [ I need a moment ]                    │
└──────────────────────────────────────────┘
```

Use button variants for choices:
- Highlight on gaze
- Show selection indicator

---

## Part 6: Quest UI Elements

### Quest Selection Screen

Grid of available quests:

```
┌────────────────────────────────────────────────┐
│  SELECT YOUR QUEST                             │
│  ═════════════════                             │
│                                                │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐     │
│  │ [Image]  │  │ [Image]  │  │ [Image]  │     │
│  │ Empty    │  │ Sea of   │  │ Temple   │     │
│  │ Tomb     │  │ Galilee  │  │ Mount    │     │
│  │ ✓ Done   │  │ New      │  │ Locked   │     │
│  └──────────┘  └──────────┘  └──────────┘     │
│                                                │
│  [Back]                                        │
└────────────────────────────────────────────────┘
```

### Quest Card Component

1. Create frame: 320 x 400
2. Auto layout, vertical

**Elements:**
- Thumbnail image: 320 x 200
- Title: Quest name
- Status badge: Complete/New/Locked
- Description (on hover/select)

**Variants:**
- State: Available, Completed, Locked
- Selection: Default, Hover, Selected

### Quest Complete Screen

See Practice Exercise in Guide 02.

Add these elements:
1. Trophy/achievement icon
2. Quest title
3. Scripture reference
4. Rewards earned
5. Reflection prompt
6. Continue button

### Quest Tracker

In-game progress indicator:

```
┌─────────────────┐
│ THE EMPTY TOMB  │
│ ────────────    │
│ ○ Enter garden  │
│ ● Find tomb     │
│ ○ Witness light │
└─────────────────┘
```

- Filled circle: Complete
- Empty circle: Incomplete
- Current: Highlighted

---

## Part 7: Notification System

### Toast Notification

Brief messages:

1. Create frame: 480 x 80
2. Background: UI/Panel
3. Auto layout, horizontal

**Elements:**
- Icon (24px): Success/Info/Warning
- Message text
- Optional close button

**Variants by type:**
- Success (green accent)
- Info (blue accent)
- Warning (orange accent)
- Error (red accent)

### Achievement Popup

More prominent celebration:

1. Create frame: 600 x 200
2. Centered on screen
3. Golden border and glow

**Elements:**
- Achievement icon
- "Achievement Unlocked"
- Achievement name
- Description

### Tutorial Tooltip

For teaching mechanics:

```
     ┌──────────────────┐
     │ Look at objects  │
     │ to interact      │
     │      [Got it]    │
     └────────┬─────────┘
              ▼
         (points to element)
```

---

## Part 8: Settings Menu

### Settings Panel Layout

```
┌────────────────────────────────────────┐
│  SETTINGS                              │
│  ════════                              │
│                                        │
│  ┌──────┐ ┌────────────────────┐      │
│  │Comfrt│ │                    │      │
│  │Audio │ │  [Current Section  │      │
│  │Grphcs│ │   Content Here]    │      │
│  │Access│ │                    │      │
│  └──────┘ └────────────────────┘      │
│                                        │
│  [Back]              [Apply]           │
└────────────────────────────────────────┘
```

### Settings Controls

**Slider:**
1. Track: 300 x 8, rounded
2. Fill: Shows current value
3. Knob: 24 x 24 circle
4. Label and value text

**Toggle:**
1. Track: 64 x 32, rounded
2. Knob: 28 x 28 circle
3. States: Off (gray), On (gold)

**Dropdown:**
1. Button showing current value
2. Chevron icon
3. Dropdown panel with options

**Radio Buttons:**
1. Circle: 24px
2. States: Unselected (outline), Selected (filled)
3. Label text

---

## Part 9: Creating Icons

### Icon Style Guidelines

For consistency:
- Size: 32px standard (can scale)
- Stroke: 2px
- Style: Rounded corners
- Color: Single color (inherits from parent)

### Essential Icons to Create

**Navigation:**
- Arrow left/right/up/down
- Menu (hamburger)
- Close (X)
- Back
- Home

**Actions:**
- Play
- Pause
- Settings/Gear
- Search
- Info

**Status:**
- Check/Complete
- Lock/Locked
- Star/Favorite
- Warning
- Error

**Biblical:**
- Cross
- Dove
- Flame
- Scroll
- Fish
- Bread
- Olive branch

### Creating an Icon

Example: Cross icon

1. Press **L** (Line tool)
2. Draw vertical line: 24px
3. Draw horizontal line: 16px
4. Position to form cross
5. Select both, right-click → **Outline stroke**
6. Union the shapes (Boolean operation)
7. Frame it: 32 x 32
8. Make component

---

## Part 10: Loading and Transition States

### Loading Screen

1. Frame: 2560 x 1440
2. Background: Dark with biblical imagery

**Elements:**
- Logo/Title
- Loading indicator:
  - Circular progress
  - Or animated dove/flame
- Loading text: "Entering the Garden..."
- Progress bar (optional)

### Loading Spinner

Create an animated-looking spinner:

1. Circle: 64 x 64
2. Arc stroke (not full circle)
3. Color: Primary/Gold

For prototyping, you'll rotate this in Figma prototyping or Unreal.

### Scene Transition

Design fade overlay:

1. Full-screen frame
2. Black fill
3. Opacity variants: 0%, 50%, 100%

---

## Part 11: Exporting Assets

### Export All Components

1. Go to your Components page
2. Select all main components
3. Add export settings to each:
   - PNG, 2x scale
   - Or SVG for icons

### Batch Export

1. Select multiple items
2. Right panel → Export
3. Each item exports separately

### Export Checklist

**Buttons:**
- [ ] Primary (all states)
- [ ] Secondary (all states)
- [ ] Ghost (all states)
- [ ] Icon buttons

**Panels:**
- [ ] Default panel
- [ ] Highlighted panel
- [ ] Dialogue box

**HUD:**
- [ ] Faith meter
- [ ] Compass
- [ ] Objective tracker
- [ ] Interaction prompt

**Icons:**
- [ ] All navigation icons
- [ ] All action icons
- [ ] All status icons
- [ ] All biblical icons

**Screens:**
- [ ] Main menu
- [ ] Quest select
- [ ] Settings
- [ ] Loading

---

## Part 12: Handoff to Unreal

### Developer Handoff

Figma has a built-in inspect mode:

1. Share file with developer (view access)
2. They switch to **"Inspect"** mode
3. Can see:
   - Exact colors (hex codes)
   - Font sizes and styles
   - Spacing and dimensions
   - Export assets directly

### Creating a Handoff Document

In your Figma file, add a page called **"Handoff"** with:

1. **Asset list** - All exportable assets with names
2. **Color reference** - All colors with hex codes
3. **Typography** - All text styles
4. **Spacing system** - Standard margins and padding
5. **Animation notes** - How things should move

---

## Part 13: Practice Exercise

### Create a Complete Quest Card

1. **Frame setup**
   - Size: 360 x 480
   - Background: UI/Panel
   - Corner radius: 16
   - Add shadow

2. **Add thumbnail**
   - Rectangle: 360 x 200
   - Top corners rounded (16), bottom square
   - Add placeholder image

3. **Add badge**
   - Small pill shape
   - Position: Top-right of thumbnail
   - Text: "NEW" or "COMPLETE"
   - Color: Green for complete, Blue for new

4. **Add title**
   - Text: "The Empty Tomb"
   - Style: H3/Subtitle
   - Padding: 24px sides

5. **Add description**
   - Text: "Witness the resurrection morning at the garden tomb."
   - Style: Body/Small
   - Color: UI/Text Secondary

6. **Add footer**
   - Divider line
   - "3 Objectives" with checkmark icon
   - "~15 min" with clock icon

7. **Create variants**
   - Available (normal)
   - Completed (checkmark badge)
   - Locked (grayscale, lock icon)

8. **Add hover state**
   - Subtle scale up (102%)
   - Golden border glow

**Make it a component and use across your quest selection screen!**

---

## Quick Reference

### Creating Components
1. Design element
2. Select all layers
3. Ctrl/Cmd + Alt + K = Create component
4. Add variants for different states

### Auto Layout
- Shift + A = Add auto layout
- Set padding and gap
- Elements resize automatically

### Export
- Select component
- Right panel → Export
- PNG 2x for images
- SVG for icons

### Naming
- `Category/Subcategory/Name`
- Example: `Button/Primary/Default`

---

## Next Steps

- **GUIDE_04_PROTOTYPING.md** - Making interactive prototypes
- Export your assets and import to Unreal Engine

---

*Consistent components make your design system powerful. Build once, use everywhere, update easily. Your Bible VR game will have a polished, professional look.*
