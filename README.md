# Bible VR Game - Figma Design Guide

A comprehensive guide for designing VR user interfaces for the Bible VR experience using Figma.

## Overview

This repository contains everything you need to design professional UI for a VR Bible study game. From basic Figma skills to VR-specific design patterns, these guides will help you create beautiful, functional interfaces.

---

## Guides Included

### For Complete Beginners

| Guide | Description |
|-------|-------------|
| **[GUIDE_01_FIGMA_BASICS.md](./GUIDE_01_FIGMA_BASICS.md)** | Installing Figma, interface overview, basic controls, keyboard shortcuts, creating your first design |
| **[GUIDE_02_VR_UI_DESIGN.md](./GUIDE_02_VR_UI_DESIGN.md)** | VR-specific design principles, comfort zones, typography, colors, HUD design, menus |
| **[GUIDE_03_BIBLE_VR_ASSETS.md](./GUIDE_03_BIBLE_VR_ASSETS.md)** | Creating components, buttons, panels, dialogue systems, quest UI, icons, settings |
| **[GUIDE_04_PROTOTYPING.md](./GUIDE_04_PROTOTYPING.md)** | Interactive prototypes, animations, testing, developer handoff |

---

## Quick Start

1. **Create Figma account** at [figma.com](https://figma.com) (free)
2. **Read Guide 01** for basics
3. **Set up your project** with the style guide from Guide 03
4. **Design your first screen** following VR principles from Guide 02
5. **Create prototype** using Guide 04

---

## Design System Overview

### Color Palette

| Name | Hex Code | Usage |
|------|----------|-------|
| Divine Gold | #D4AF37 | Primary accent, holy elements |
| Sacred White | #FFFEF5 | Text, highlights |
| Deep Black | #0D0D0D | Backgrounds |
| Panel Gray | #2D2D2D | Cards, containers |
| Heaven Blue | #87CEEB | Peace, sky |
| Spirit Purple | #9C27B0 | Spiritual elements |

### Typography

For VR readability, use **2-3x normal sizes**:

| Element | Figma Size | Font |
|---------|------------|------|
| Title | 96px | Cinzel Bold |
| Heading | 72px | Cinzel Bold |
| Subtitle | 48px | Inter SemiBold |
| Body | 32-36px | Inter Regular |
| Button | 32px | Inter Medium |
| Caption | 20-24px | Inter Regular |

### VR Comfort Guidelines

- Keep main UI within **30° of center view**
- Use **high contrast** (light text on dark backgrounds)
- **Large touch targets** (minimum 80px buttons)
- **Semi-transparent panels** with blur effects
- **Generous spacing** between elements

---

## UI Elements Checklist

### Core Components

- [ ] Buttons (Primary, Secondary, Ghost)
- [ ] Icon buttons
- [ ] Panels/Cards
- [ ] Input fields
- [ ] Sliders
- [ ] Toggles
- [ ] Dropdowns

### Screens to Design

- [ ] Main Menu
- [ ] Quest Selection
- [ ] Quest Detail
- [ ] Loading Screen
- [ ] Game HUD
- [ ] Dialogue System
- [ ] Settings Menu
- [ ] Quest Complete
- [ ] Notifications

### Icons Needed

- [ ] Navigation (arrows, menu, close, back)
- [ ] Actions (play, pause, settings)
- [ ] Status (check, lock, warning)
- [ ] Biblical (cross, dove, flame, scroll)

---

## Project Organization

### Recommended Figma Pages

1. **Cover** - Project title and description
2. **Style Guide** - Colors, typography, spacing
3. **Components** - All reusable elements
4. **Main Menu** - Title screen
5. **Quest UI** - Selection and tracking
6. **HUD** - In-game interface
7. **Dialogue** - Character conversations
8. **Settings** - Configuration screens
9. **Prototypes** - Interactive flows
10. **Handoff** - Developer documentation

### File Naming

```
Bible VR - [Type] - [Version]
```

Examples:
- `Bible VR - Main UI - v1`
- `Bible VR - Icons - v2`
- `Bible VR - Prototypes - v1`

---

## Exporting for Unreal Engine

### Export Settings

**For UI elements:**
- Format: PNG
- Scale: 2x or 3x
- Background: Transparent

**For icons:**
- Format: SVG (or PNG)
- Scale: 1x
- Background: Transparent

### Naming Convention

```
UI_[Category]_[Element]_[State].png
```

Examples:
- `UI_Button_Primary_Default.png`
- `UI_Button_Primary_Hover.png`
- `UI_HUD_Compass_Icon.svg`

---

## Learning Path

### Week 1: Figma Basics
- Complete Guide 01
- Practice navigation and basic shapes
- Create simple buttons and text

### Week 2: VR Design Principles
- Complete Guide 02
- Understand VR comfort zones
- Design your first HUD element

### Week 3: Building Components
- Complete Guide 03
- Create full component library
- Design main menu and quest UI

### Week 4: Prototyping
- Complete Guide 04
- Make screens interactive
- Test with users
- Prepare for handoff

---

## Resources

### Free Figma Resources

- **Figma Community** - Free UI kits and templates
- **Iconify Plugin** - Thousands of free icons
- **Unsplash Plugin** - Free photos
- **Google Fonts** - Free typography

### VR Design References

- [Oculus VR Design Guidelines](https://developer.oculus.com/design/)
- [Google VR Design Principles](https://designguidelines.withgoogle.com/cardboard/designing-for-google-cardboard.html)

### Figma Learning

- [Figma Official Tutorials](https://help.figma.com/hc/en-us/categories/360002051613)
- [Figma YouTube Channel](https://www.youtube.com/@Figma)

---

## Keyboard Shortcuts

### Essential Shortcuts

| Shortcut | Action |
|----------|--------|
| V | Move/Select |
| F | Frame |
| R | Rectangle |
| T | Text |
| I | Eyedropper |
| Ctrl/Cmd + D | Duplicate |
| Ctrl/Cmd + G | Group |
| Ctrl/Cmd + Alt + K | Create component |
| Shift + A | Add auto layout |
| Ctrl/Cmd + Enter | Play prototype |

### Navigation

| Shortcut | Action |
|----------|--------|
| Space + drag | Pan |
| Ctrl/Cmd + scroll | Zoom |
| Shift + 1 | Zoom to fit |

---

## Companion Repository

For Unreal Engine development guides, see:
**[unrealengine_guide](https://github.com/nichechristie/unrealengine_guide)**

Contains:
- Unreal Engine basics
- Scene and environment setup
- Cesium GPS terrain
- VR implementation

---

## License

Educational and personal use.

---

*Good design serves the experience. For Bible VR, that means interfaces that are readable, comfortable, and don't distract from the spiritual journey. Take time to refine your designs - they're the bridge between player and Scripture.*
