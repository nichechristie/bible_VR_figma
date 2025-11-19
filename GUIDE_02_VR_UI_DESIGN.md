# GUIDE 02: Designing VR User Interfaces in Figma

## Overview

VR interfaces are different from regular screen designs. Users wear a headset and look around a 3D space. This guide teaches you how to design comfortable, readable UI for virtual reality.

---

## Part 1: VR Design Principles

### Why VR UI is Different

In VR:
- Users **look at** UI instead of touching it
- Text must be **larger** (harder to read in headsets)
- UI should be in a **comfortable viewing zone**
- Too much UI causes **visual fatigue**
- Depth and **3D positioning** matter

### The Comfort Zone

Users shouldn't strain their eyes or neck:

```
         ┌─────────────────┐
        /                   \
       /    COMFORT ZONE     \
      /      (Best area)      \
     │                         │
     │    ┌───────────────┐    │
     │    │   MAIN UI     │    │
     │    │   AREA        │    │
     │    └───────────────┘    │
     │                         │
      \                       /
       \    Avoid edges      /
        \                   /
         └─────────────────┘
```

**Best practices:**
- Keep important UI within **30° of center view**
- Avoid placing UI at extreme edges
- Don't put UI too close (causes eye strain)
- Don't put UI too far (hard to read)

### Optimal Distance

| Content Type | Distance | Figma Scale |
|--------------|----------|-------------|
| Tooltips, labels | 0.5 - 1m | Small (12-14px) |
| Main UI, menus | 1 - 2m | Medium (18-24px) |
| Large displays | 2 - 4m | Large (32px+) |

In Figma, you'll design at a larger scale to account for VR readability.

---

## Part 2: Setting Up Your VR Design File

### Canvas Size

For VR UI design, use these frame sizes:

**Curved Panel (Recommended):**
- **1920 x 1080** or **2560 x 1440**
- Represents what users see in headset

**Individual UI Elements:**
- Design at **2x or 3x scale**
- Example: A button that should be 100px in-game → Design at 300px

### Create VR Project Structure

In Figma, create these pages:

1. **Style Guide** - VR-specific colors, fonts, spacing
2. **HUD Elements** - Health, compass, objectives
3. **Menus** - Main menu, pause, settings
4. **Dialogue System** - Character speech bubbles
5. **Quest UI** - Quest tracker, completion screens
6. **Notifications** - Alerts, achievements
7. **Components** - Reusable VR UI elements

### VR Frame Template

Create a master frame for VR design:

1. Press **F** (Frame tool)
2. Create **2560 x 1440** frame
3. Add guides for comfort zone:
   - Inner rectangle at 1920 x 1080 (main content)
   - Outer area for secondary elements

---

## Part 3: VR Typography

### Font Size Guidelines

VR text must be **much larger** than regular UI:

| Element | Regular UI | VR UI | Figma Size |
|---------|------------|-------|------------|
| Body text | 14-16px | 24-32px | 48-64px |
| Headings | 24-32px | 40-56px | 80-112px |
| Buttons | 14-18px | 24-36px | 48-72px |
| Labels | 12px | 18-24px | 36-48px |
| Captions | 10px | 16-20px | 32-40px |

**Rule of thumb:** Design at **2-3x** normal size

### Best VR Fonts

Highly readable in VR:

**Sans-serif (Best for VR):**
- **Inter** - Excellent readability
- **Roboto** - Clean and clear
- **Open Sans** - Great at small sizes
- **Nunito** - Friendly and round

**Serif (For biblical feel):**
- **Cinzel** - Ancient/classical
- **Cormorant** - Elegant
- **Playfair Display** - Readable serif

**Avoid:**
- Thin/light weights
- Decorative fonts
- Script fonts for body text
- Fonts with tight spacing

### Text Styling for VR

1. **Increase letter spacing** slightly (+2-5%)
2. **Increase line height** (1.5 - 1.8)
3. **Use medium or bold weights** (easier to read)
4. **Add subtle shadow** for contrast

Example text style:
```
Font: Inter
Weight: Medium (500)
Size: 48px
Line height: 72px (1.5)
Letter spacing: 2%
Color: White (#FFFFFF)
Shadow: 0, 2, 4, Black 30%
```

---

## Part 4: VR Color Guidelines

### Contrast is Critical

VR headsets can have lower contrast than monitors:
- Use **high contrast** text (light on dark or dark on light)
- Avoid subtle color differences
- Test designs in actual VR if possible

### Background Colors

Dark backgrounds work best in VR:
- Reduces eye strain
- Makes light text pop
- Feels more immersive

**Recommended background colors:**
| Name | Hex | Use |
|------|-----|-----|
| Deep Black | #0D0D0D | Main backgrounds |
| Soft Black | #1A1A1A | Cards, panels |
| Dark Gray | #2D2D2D | Secondary panels |
| Translucent | #000000 60% | Overlays |

### Accent Colors for Bible VR

| Color | Hex | Meaning |
|-------|-----|---------|
| Divine Gold | #FFD700 | Holy, important |
| Heavenly White | #FFFEF5 | Purity, light |
| Sacred Blue | #4169E1 | Truth, heaven |
| Spirit Purple | #8A2BE2 | Spiritual |
| Life Green | #228B22 | Growth, healing |
| Warning Red | #DC143C | Danger, sacrifice |

### Transparency and Glass Effects

VR UI often uses semi-transparent panels:

1. Select frame/shape
2. Set Fill opacity to **60-80%**
3. Add **Background blur** effect:
   - Effects → + → Background blur
   - Amount: 20-40

This creates a "frosted glass" look that:
- Shows the world behind UI
- Keeps text readable
- Feels modern and clean

---

## Part 5: VR-Specific UI Elements

### Gaze Indicators

Show users what they're looking at:

**Simple Reticle:**
1. Create circle: 16px diameter
2. Stroke: 2px white
3. Fill: None or 30% white
4. Center on screen

**Animated Reticle (for prototyping):**
- Circle expands when hovering over interactive elements
- Changes color when active

### Progress Indicators

**Radial Progress (Best for VR):**
1. Create circle outline
2. Use stroke dash to show progress
3. Add percentage text in center

**Why radial?** Users can see it while looking at content

### Floating Panels

VR UI often floats in 3D space:

**Panel Design:**
1. Rounded corners (16-24px radius)
2. Subtle shadow for depth
3. Semi-transparent background
4. Clear border or glow

```
┌─────────────────────────┐
│                         │
│   QUEST COMPLETE        │
│   ─────────────────     │
│   The Empty Tomb        │
│                         │
│   [Continue]            │
│                         │
└─────────────────────────┘
```

### Spatial Anchoring

UI can be:
- **Head-locked** - Follows your view (HUD)
- **World-locked** - Stays in place (signs, labels)
- **Hand-attached** - On controller/hand

Design each type differently:
- Head-locked: Minimal, at edges
- World-locked: Can be more detailed
- Hand-attached: Compact, glanceable

---

## Part 6: Designing the HUD

The HUD (Heads-Up Display) shows constant information.

### HUD Placement

```
┌──────────────────────────────────┐
│ [Health]            [Compass]    │
│                                  │
│                                  │
│                                  │
│                                  │
│                                  │
│                                  │
│ [Objectives]      [Interaction]  │
└──────────────────────────────────┘
```

**Corners are best** for HUD elements - doesn't block main view.

### Bible VR HUD Elements

Design these for your game:

1. **Faith/Spirit Meter**
   - Replaces typical "health"
   - Golden light indicator
   - Subtle glow when full

2. **Compass**
   - Shows direction to objectives
   - Marks quest locations
   - Simple, not distracting

3. **Current Objective**
   - One line of text
   - Icon for quest type
   - Fades when not needed

4. **Interaction Prompt**
   - "Look to interact"
   - Shows when near interactive objects
   - Appears at bottom center

### HUD Design Tips

- Use **icons more than text**
- Keep elements **small and subtle**
- Allow HUD to **fade out** when not needed
- Use **animation** to draw attention when important

---

## Part 7: Menu Design for VR

### Main Menu Layout

VR menus work best as **large panels** in front of the user:

```
        ┌────────────────────────┐
        │                        │
        │    BIBLE VR QUEST      │
        │    ─────────────       │
        │                        │
        │    [ Begin Journey ]   │
        │    [ Continue ]        │
        │    [ Quest Select ]    │
        │    [ Settings ]        │
        │                        │
        └────────────────────────┘
```

### Menu Button Design

VR buttons need:
- **Large hit areas** (easy to target with gaze)
- **Clear hover states** (know what you're selecting)
- **Audio feedback** (confirm selection)

**Button states:**
1. **Default** - Normal appearance
2. **Hover** - Highlighted (gaze is on button)
3. **Active** - Pressed/selected
4. **Disabled** - Can't interact

Design all four states in Figma using **Variants** (covered in Guide 03).

### Settings Menu

Essential VR settings to design:

1. **Comfort**
   - Teleport vs smooth locomotion
   - Vignette strength
   - Snap turn angle

2. **Audio**
   - Master volume
   - Music volume
   - Voice volume
   - Subtitles on/off

3. **Graphics**
   - Quality presets
   - Brightness

4. **Accessibility**
   - Text size
   - High contrast mode
   - Colorblind options

---

## Part 8: Dialogue UI

### Dialogue Box Design

For character conversations:

```
┌──────────────────────────────────┐
│  [Avatar]   MARY MAGDALENE       │
│             ─────────────        │
│  "Peace be with you, friend.     │
│   The tomb lies ahead. Come,     │
│   let us see what awaits."       │
│                                  │
│             [Continue →]         │
└──────────────────────────────────┘
```

### Dialogue UI Elements

1. **Character name** - Clear, styled with character color
2. **Avatar/portrait** - Optional small image
3. **Dialogue text** - Large, readable
4. **Continue button** - Clear next action
5. **Background** - Semi-transparent, doesn't block view

### Subtitle Design

For voice-over without dialogue box:

- Position at **bottom center**
- Use **semi-transparent background**
- **Large text** (48px+)
- **Speaker name** in different color
- **Auto-fade** after audio ends

Example:
```
┌─────────────────────────────────────┐
│ MARY: "He is not here. He is risen."│
└─────────────────────────────────────┘
```

---

## Part 9: Notifications and Feedback

### Achievement/Quest Complete

**Full-screen celebration:**

```
        ╔════════════════════════╗
        ║                        ║
        ║   ✝ QUEST COMPLETE     ║
        ║   ═══════════════      ║
        ║                        ║
        ║   The Empty Tomb       ║
        ║                        ║
        ║   +100 Faith Points    ║
        ║                        ║
        ║      [Continue]        ║
        ╚════════════════════════╝
```

**Design tips:**
- Use glowing/radiant effects
- Gold and white colors
- Particle effects (design in Unreal, mockup in Figma)

### Toast Notifications

Brief messages that appear and disappear:

```
┌─────────────────────────┐
│ ✓ Faith Point Earned    │
└─────────────────────────┘
```

- Small, non-intrusive
- Appears at top or bottom edge
- Fades after 3-5 seconds
- Icon + short text

### Error/Warning Messages

When something goes wrong:

```
┌─────────────────────────┐
│ ⚠ Cannot proceed        │
│ Complete current        │
│ objective first         │
│        [OK]             │
└─────────────────────────┘
```

- Clear red/orange accent
- Simple language
- One clear action

---

## Part 10: Interaction Design

### Gaze-Based Selection

Most VR uses "look at to select":

**Design for gaze:**
1. Clear hover state (user knows they're targeting it)
2. Generous hit areas (forgiving)
3. Dwell indicator (fills up while looking)

**Dwell Indicator:**
```
    Default        Filling         Complete
      ○              ◐               ●
```

Create circular progress that fills while user gazes.

### Hand/Controller Selection

For pointing and clicking:

**Cursor design:**
- Small dot or ring
- Changes color on hover
- Shows when pointing at UI

### Button States

Design all states for each button:

| State | Appearance | When |
|-------|------------|------|
| Default | Normal | Not interacting |
| Hover | Highlighted, larger | Gaze/pointer on it |
| Active | Pressed look | During selection |
| Selected | Checkmark/highlight | Chosen option |
| Disabled | Grayed out | Can't interact |

---

## Part 11: Accessibility in VR

### Text Readability

- Minimum **48px** (in Figma scale)
- High contrast ratios (4.5:1 minimum)
- Avoid pure white on pure black (too harsh)
- Use **#F0F0F0** on **#1A1A1A** instead

### Colorblind Considerations

Don't rely on color alone:
- Add icons with colors
- Use patterns or textures
- Test with colorblind simulation

### Subtitles and Captions

- Always include subtitles option
- Show speaker name
- Large, readable font
- Background for contrast

### Reduced Motion

Some users get motion sick:
- Option to reduce animations
- Static alternatives to moving UI
- Gentle transitions instead of fast movement

---

## Part 12: Exporting for Unreal Engine

### Export Settings

When exporting UI for Unreal:

1. Select element to export
2. Right panel → Export
3. Settings:
   - **PNG** for images with transparency
   - **2x or 3x scale** for VR clarity
   - **SVG** for icons (scalable)

### Naming Convention

Name exports clearly:
```
UI_MainMenu_Button_Primary_Default.png
UI_MainMenu_Button_Primary_Hover.png
UI_HUD_Compass_Icon.svg
UI_Dialogue_Box_Background.png
```

### Asset Organization

Create folders:
```
Exports/
├── HUD/
├── Menus/
├── Dialogue/
├── Icons/
├── Buttons/
└── Backgrounds/
```

---

## Part 13: Practice Exercise

### Design a VR Quest Complete Screen

1. **Create frame**
   - 2560 x 1440
   - Background: #1A1A1A at 90% opacity

2. **Add container panel**
   - 1200 x 800 centered rectangle
   - Background: #2D2D2D at 80%
   - Corner radius: 24
   - Border: 2px #D4AF37 (gold)
   - Add drop shadow

3. **Add title**
   - "QUEST COMPLETE"
   - Font: Cinzel Bold
   - Size: 72px
   - Color: #FFD700 (gold)

4. **Add quest name**
   - "The Empty Tomb"
   - Font: Inter Medium
   - Size: 48px
   - Color: #FFFFFF

5. **Add reward**
   - "+100 Faith Points"
   - Size: 36px
   - Color: #87CEEB (light blue)

6. **Add button**
   - "Continue"
   - 300 x 80 button
   - Use your button component
   - Center at bottom of panel

7. **Add glow effect**
   - Select outer panel
   - Add outer glow: gold, 20px spread

---

## Quick Reference

### VR UI Sizing
- Text: 2-3x normal size
- Buttons: Large hit areas (min 80px)
- Spacing: Generous padding

### Color
- Dark backgrounds
- High contrast text
- Semi-transparent panels

### Comfort
- Keep UI in center 30° of view
- Not too close, not too far
- Avoid edges of vision

### Export
- PNG with transparency
- 2x or 3x scale
- Clear naming convention

---

## Next Steps

- **GUIDE_03_BIBLE_VR_ASSETS.md** - Creating specific Bible VR elements
- **GUIDE_04_PROTOTYPING.md** - Making interactive prototypes

---

*VR UI design is about comfort and clarity. Users should focus on the experience, not struggle with the interface. Keep it simple, keep it readable, keep it beautiful.*
