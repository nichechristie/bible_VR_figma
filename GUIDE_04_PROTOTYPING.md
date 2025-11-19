# GUIDE 04: Prototyping and Developer Handoff

## Overview

Prototyping in Figma lets you create interactive mockups that show how your Bible VR UI will work. This is essential for testing your designs before building in Unreal Engine.

---

## Part 1: Introduction to Prototyping

### What is a Prototype?

A prototype is a clickable version of your design that simulates:
- Navigation between screens
- Button interactions
- Animations and transitions
- User flow

### Why Prototype?

1. **Test ideas** before coding
2. **Show stakeholders** how it will work
3. **Find usability issues** early
4. **Save development time**

### Accessing Prototype Mode

1. Open your Figma file
2. Click **"Prototype"** tab (top right, next to "Design")
3. The right panel shows prototype settings

---

## Part 2: Creating Connections

### Connecting Frames

To make buttons navigate to other screens:

1. Switch to **Prototype** mode
2. Select the element (button, card, etc.)
3. A blue circle appears on the right edge
4. **Drag from the blue circle** to the destination frame
5. An arrow connects them

### Connection Settings

When you create a connection, the right panel shows:

**Interaction:**
- **Trigger:** What starts the interaction
  - On click/tap
  - On hover (mouse enters)
  - While pressing
  - Key/gamepad
  - After delay

- **Action:** What happens
  - Navigate to
  - Open overlay
  - Swap with (for variants)
  - Back (previous screen)
  - Close overlay
  - Open link

**Animation:**
- **Type:** Instant, Dissolve, Move in, Push, Slide in
- **Direction:** Left, Right, Top, Bottom
- **Duration:** In milliseconds (ms)
- **Easing:** Ease in, Ease out, Ease in and out, Linear

### Example: Button to New Screen

1. Select "Begin Journey" button
2. Drag connection to "Quest Select" frame
3. Settings:
   - Trigger: On click
   - Action: Navigate to
   - Animation: Dissolve
   - Duration: 300ms
   - Easing: Ease out

---

## Part 3: Creating Interactive Components

### Component States with Variants

Remember those button variants you created? Now make them interactive.

**Step 1: Open Component**
1. Find your button component
2. Double-click to enter edit mode

**Step 2: Add Interactions**
1. Switch to Prototype mode
2. Select the "Default" variant
3. Add interaction:
   - Trigger: While hovering
   - Action: Change to
   - State: Hover variant
   - Animation: Smart animate
   - Duration: 150ms

**Step 3: Add More States**
- Default → Hover (on hover)
- Hover → Default (on hover end)
- Default → Active (while pressing)
- Active → Default (on press end)

Now every instance of this button will be interactive!

### Smart Animate

Smart Animate creates smooth transitions between variants:
- Elements move to new positions
- Colors blend between states
- Sizes interpolate smoothly

**Requirements:**
- Layers must have **same names**
- Works best with similar structure

---

## Part 4: Creating Overlays

Overlays appear on top of current content (like pop-ups).

### Creating an Overlay

**Step 1: Design the Overlay**
1. Create new frame for overlay content
2. Make background semi-transparent
3. Add the popup content (dialog, menu, etc.)

**Step 2: Connect as Overlay**
1. Select trigger element (e.g., Settings button)
2. Create connection to overlay frame
3. In settings:
   - Action: **Open overlay**
   - Position: Center (or manual)
   - Close when clicking outside: Checked (optional)
   - Add background: Checked (dims background)

### Example: Confirmation Dialog

1. Create frame: 600 x 400
2. Add content:
   - Title: "Exit Game?"
   - Message: "Your progress will be saved."
   - Buttons: "Cancel", "Exit"

3. Connect trigger:
   - Exit button → Dialog (Open overlay)

4. Connect dialog buttons:
   - Cancel → Back (closes overlay)
   - Exit → Main Menu (Navigate to)

---

## Part 5: Common VR Prototype Interactions

### Gaze Selection Simulation

Simulate looking at elements:

**Hover States:**
1. Element Default → Element Hover (While hovering)
2. Add delay before selection

**Dwell Timer:**
1. Create circular progress indicator
2. Animate it filling on hover
3. After delay, trigger action

### Menu Navigation

**Quest Selection Grid:**
1. Quest Card → Quest Detail overlay (on click)
2. Quest Detail "Start" → Loading Screen (on click)
3. Loading Screen → Game Level (after delay)

### Dialogue Flow

1. Dialogue Box 1 → Dialogue Box 2 (on click Continue)
2. Add after delay for auto-advance (optional)
3. Last dialogue → Close overlay or next screen

---

## Part 6: Adding Animations

### Transition Types

| Type | Description | Best For |
|------|-------------|----------|
| **Instant** | No animation | Testing |
| **Dissolve** | Fade between | Gentle transitions |
| **Move in** | Slides from direction | Menus appearing |
| **Push** | Pushes old content out | Navigation depth |
| **Slide in** | New content slides over | Overlays |
| **Smart animate** | Morphs between states | Component changes |

### Animation Timing

**Duration guidelines:**
- Quick feedback: 100-150ms
- Button states: 150-200ms
- Screen transitions: 300-400ms
- Overlay appear: 200-300ms
- Loading indicators: 1000-2000ms

**Easing:**
- **Ease out:** Starts fast, ends slow (entering)
- **Ease in:** Starts slow, ends fast (exiting)
- **Ease in out:** Smooth both ends (natural)
- **Linear:** Constant speed (mechanical)

### Creating Loading Animation

1. Design loading spinner
2. Create multiple frames showing rotation
3. Connect frames with **After delay** trigger
4. Loop back to first frame

Or use Smart Animate:
1. Duplicate spinner frame
2. Rotate the spinner element
3. Connect with Smart Animate + After delay

---

## Part 7: Creating a Complete Flow

### User Flow: Quest Selection

Let's prototype the complete quest selection flow:

**Screens needed:**
1. Main Menu
2. Quest Select Grid
3. Quest Detail Overlay
4. Loading Screen
5. Game HUD (placeholder)

**Connections:**

```
[Main Menu]
    │
    ├─ "Begin Journey" → [Quest Select]
    ├─ "Settings" → [Settings Overlay]
    └─ "Exit" → [Exit Confirmation]

[Quest Select]
    │
    ├─ Quest Card 1 → [Quest 1 Detail Overlay]
    ├─ Quest Card 2 → [Quest 2 Detail Overlay]
    └─ "Back" → [Main Menu]

[Quest Detail Overlay]
    │
    ├─ "Begin Quest" → [Loading Screen]
    └─ "Back" → Close Overlay

[Loading Screen]
    │
    └─ After 3000ms → [Game HUD]
```

### Creating the Flow

1. Design all screens
2. Switch to Prototype mode
3. Create connections following the map above
4. Set appropriate animations for each transition

---

## Part 8: Testing Your Prototype

### Preview Mode

1. Click **Play button** (top right) or press **Ctrl/Cmd + Enter**
2. Prototype opens in new tab
3. Click through your design
4. Press **R** to restart

### Presentation Mode

For showing others:
1. In preview, click **Options** (top right)
2. Enable **"Hide Figma UI"**
3. Use **arrow keys** to navigate between flows

### Device Preview

Test on actual devices:
1. Download **Figma Mirror** app (iOS/Android)
2. Sign in to same account
3. Your prototype appears on phone/tablet

### Sharing Prototype

1. Click **Share** button
2. Select **"Anyone with the link"**
3. Check **"Allow opening in Present mode"**
4. Copy link and send

---

## Part 9: Gathering Feedback

### Comments in Figma

1. Press **C** to enter comment mode
2. Click anywhere to add comment
3. Others can reply
4. Mark resolved when addressed

### Usability Testing

Have others test your prototype:

**Things to observe:**
- Where do they get confused?
- Do they find buttons easily?
- Is text readable?
- Are transitions too fast/slow?

**Questions to ask:**
- "What would you expect this button to do?"
- "Can you find the settings?"
- "How would you start a quest?"

---

## Part 10: Developer Handoff

### Inspect Mode

Developers can access your designs:

1. Share file with developers (view access)
2. They open in Figma
3. Right panel shows **"Inspect"** tab
4. Click any element to see:
   - Dimensions
   - Colors
   - Typography
   - Spacing
   - CSS properties

### Preparing for Handoff

**Create a Handoff page with:**

1. **Component Documentation**
   - All components laid out
   - Variants shown
   - Usage guidelines

2. **Spacing System**
   - Standard margins: 16, 24, 32, 48
   - Standard padding: 8, 16, 24
   - Standard gaps: 8, 16, 24

3. **Color Reference**
   - All colors with names and hex codes
   - Usage examples

4. **Typography Reference**
   - All text styles
   - Usage examples

5. **Icon Reference**
   - All icons with names
   - Download links or exports

### Annotation

Add notes for developers:

1. Create text layer
2. Style: Small, red or blue
3. Content: Technical notes
   - "Animate on hover"
   - "Load content from API"
   - "Plays sound on select"

### Export All Assets

Create export-ready versions:

1. Select all exportable elements
2. Add export settings:
   - PNG @2x for images
   - SVG for icons
   - PNG @1x as backup

3. In Inspect mode, developers can download

---

## Part 11: Organizing for Production

### Version Control

Keep track of changes:

1. **Use branches** (Figma paid feature)
   - Main: Production ready
   - Development: In progress

2. **Or use copies**
   - `Bible VR UI - v1.0`
   - `Bible VR UI - v1.1`
   - Keep old versions

### Documentation

**Create a README frame:**
```
PROJECT: Bible VR Game UI
VERSION: 1.0
LAST UPDATED: [Date]

PAGES:
1. Cover - Project overview
2. Style Guide - Colors, typography, spacing
3. Components - All reusable elements
4. Main Menu - Title screen and navigation
5. Quest UI - Selection and tracking
6. HUD - In-game interface
7. Dialogue - Character conversations
8. Settings - Configuration screens
9. Prototypes - Interactive flows
10. Handoff - Developer documentation
11. Archive - Old versions
```

### File Organization

**Folder structure in Figma:**
```
Bible VR Game/
├── Bible VR - UI Design
├── Bible VR - Icons
├── Bible VR - Prototypes
└── Bible VR - Archive
```

---

## Part 12: Importing to Unreal Engine

### Exporting from Figma

**For UI elements:**
1. Select element
2. Export as PNG @2x
3. Use transparent background

**For icons:**
1. Export as SVG
2. Convert to PNG if needed

### Importing to Unreal

1. In Unreal, go to Content Browser
2. Create folder: `Content/UI/`
3. Click **Import**
4. Select your PNG files

### Creating UMG Widgets

1. Right-click in Content Browser
2. **User Interface** → **Widget Blueprint**
3. Use your Figma designs as reference
4. Match colors, sizes, fonts exactly

### Matching Figma to UMG

| Figma | Unreal UMG |
|-------|------------|
| Frame | Canvas Panel |
| Auto Layout | Horizontal/Vertical Box |
| Text | Text Widget |
| Rectangle | Image or Border |
| Component | User Widget |

---

## Part 13: Practice Exercise

### Create Interactive Quest Flow

**Step 1: Set up screens**
1. Main Menu (1920 x 1080)
2. Quest Select (1920 x 1080)
3. Quest Detail overlay (800 x 600)
4. Loading Screen (1920 x 1080)

**Step 2: Design each screen**
- Main Menu: Title, 4 buttons
- Quest Select: Grid of 3 quest cards
- Quest Detail: Image, description, Start button
- Loading: Logo, progress bar

**Step 3: Create connections**

Main Menu:
- "Begin Journey" → Quest Select (Dissolve, 300ms)
- Back button in Quest Select → Main Menu (Slide in Right)

Quest Select:
- Quest Card → Quest Detail (Open overlay, Center)

Quest Detail:
- "Start Quest" → Loading (Dissolve, 200ms)
- "Back" → Close overlay

Loading:
- After 3000ms → Quest Select (Dissolve)

**Step 4: Add component interactions**
- Button hover states
- Card hover states

**Step 5: Test**
- Click Play
- Go through entire flow
- Check all interactions work

---

## Part 14: Advanced Prototyping

### Scrolling Content

1. Create content longer than frame
2. Select the frame
3. In Design panel: **Overflow** → **Scroll**
4. Choose direction: Vertical, Horizontal, Both

### Variables (New Feature)

Figma now has variables for advanced prototypes:
- Store values (numbers, text)
- Conditionals
- Dynamic content

Use for:
- Score tracking
- Inventory systems
- Form validation

### External Prototyping Tools

For more advanced interactions:
- **ProtoPie** - Complex animations
- **Principle** - Mac only, powerful
- **Framer** - Code-based

---

## Quick Reference

### Prototype Mode Shortcuts
| Shortcut | Action |
|----------|--------|
| Ctrl/Cmd + Enter | Play prototype |
| R | Restart prototype |
| ← → | Navigate frames in present |

### Common Triggers
- **On click** - User clicks/taps
- **While hovering** - Mouse over element
- **After delay** - Time passes

### Common Actions
- **Navigate to** - Go to frame
- **Open overlay** - Show on top
- **Change to** - Swap variant
- **Back** - Previous screen

### Animation Settings
- Quick: 150ms, Ease out
- Standard: 300ms, Ease in out
- Slow: 500ms, Ease in out

---

## Handoff Checklist

Before sending to developers:

- [ ] All screens designed
- [ ] All components documented
- [ ] All states shown (hover, active, disabled)
- [ ] Colors documented with hex codes
- [ ] Typography documented
- [ ] Spacing system documented
- [ ] Icons exported
- [ ] Interactions annotated
- [ ] Prototype working
- [ ] File organized and named

---

## Next Steps

1. **Finish your prototype** - All screens and interactions
2. **Test with users** - Get feedback
3. **Export assets** - Prepare for Unreal
4. **Hand off to development** - Or import yourself!

---

*Prototyping is where your designs come to life. Take time to get interactions right in Figma, and development in Unreal will be much smoother. Test early and often!*
