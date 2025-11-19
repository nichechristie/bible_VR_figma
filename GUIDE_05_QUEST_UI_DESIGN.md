# GUIDE 05: Designing Quest UI for Bible VR in Figma

## Overview

This guide shows you how to design all the UI elements for the two pre-built biblical quests in Figma. You'll create screens for every scene, dialogue box, choice interface, and completion screen.

### The Two Quests

1. **The Calling** - Jesus calls His first disciples (5 scenes)
2. **Faith in the Storm** - Jesus calms the storm (5 scenes)

---

## Part 1: Quest UI Components Needed

### For Each Quest, Design:

1. **Quest Card** - Selection screen preview
2. **Quest Intro Screen** - Title, description, objectives
3. **Scene Narration** - Story text display
4. **Dialogue Box** - Character conversations
5. **Choice Interface** - Player decisions
6. **Reflection Prompt** - Spiritual questions
7. **Quest Complete** - Rewards and summary

---

## Part 2: Quest Selection Cards

### Quest Card: The Calling

**Frame Size:** 360 x 480

**Design Elements:**

```
┌────────────────────────────┐
│ [Sea of Galilee Image]     │
│                            │
│  ┌─────────────────────┐   │
│  │ 🎣 BEGINNER         │   │
│  └─────────────────────┘   │
├────────────────────────────┤
│                            │
│  The Calling               │
│  ─────────────             │
│  Walk with Jesus as He     │
│  calls His first disciples │
│                            │
│  ⏱ 15 min  📖 Matthew 4    │
│                            │
└────────────────────────────┘
```

**Specifications:**
- Image: Sea of Galilee at dawn (320 x 200)
- Badge: "BEGINNER" - Green pill shape
- Title: Cinzel Bold, 32px, Primary/Gold
- Description: Inter Regular, 20px, UI/Text Secondary
- Footer: Icons + text, 16px

### Quest Card: Faith in the Storm

**Same structure, different content:**

```
┌────────────────────────────┐
│ [Stormy Sea Image]         │
│                            │
│  ┌─────────────────────┐   │
│  │ ⛵ BEGINNER         │   │
│  └─────────────────────┘   │
├────────────────────────────┤
│                            │
│  Faith in the Storm        │
│  ─────────────────         │
│  Experience Jesus calming  │
│  the storm on Galilee      │
│                            │
│  ⏱ 12 min  📖 Mark 4       │
│                            │
└────────────────────────────┘
```

### Card States

Create variants:
- **Default** - Normal appearance
- **Hover** - Slight scale (102%), golden glow
- **Selected** - Gold border, checkmark if completed
- **Locked** - Grayscale, lock icon overlay

---

## Part 3: Quest Introduction Screen

### The Calling - Intro

**Frame Size:** 2560 x 1440 (Full VR view)

```
┌──────────────────────────────────────────────────┐
│                                                  │
│         ┌─────────────────────────────┐          │
│         │                             │          │
│         │  🎣 THE CALLING             │          │
│         │  ═══════════════            │          │
│         │                             │          │
│         │  Walk with Jesus as He      │          │
│         │  calls His first disciples  │          │
│         │                             │          │
│         │  ─────────────────────────  │          │
│         │                             │          │
│         │  SCRIPTURE                  │          │
│         │  Matthew 4:18-22            │          │
│         │  Mark 1:16-20               │          │
│         │  Luke 5:1-11                │          │
│         │                             │          │
│         │  ─────────────────────────  │          │
│         │                             │          │
│         │  YOU WILL LEARN             │          │
│         │  • The cost of discipleship │          │
│         │  • Immediate obedience      │          │
│         │  • Faith and trust          │          │
│         │                             │          │
│         │  ─────────────────────────  │          │
│         │                             │          │
│         │  COMPANION: Peter           │          │
│         │  TIME: ~15 minutes          │          │
│         │                             │          │
│         │      [ Begin Quest ]        │          │
│         │                             │          │
│         └─────────────────────────────┘          │
│                                                  │
└──────────────────────────────────────────────────┘
```

**Design Specifications:**

- Panel: 900 x 1000, UI/Panel at 90%, corner radius 24
- Title: Cinzel Bold, 64px, Primary/Gold
- Subtitle: Inter Medium, 32px, UI/Text Primary
- Section headers: Inter SemiBold, 24px, Primary/Gold
- Body text: Inter Regular, 24px, UI/Text Secondary
- List items: Bullet + text
- Button: Primary button component, 300 x 80

### Faith in the Storm - Intro

Same layout with different content:

**Scripture:** Mark 4:35-41, Matthew 8:23-27, Luke 8:22-25

**You Will Learn:**
- Jesus' power over nature
- Faith vs fear
- Trusting Jesus in chaos
- Who Jesus truly is

**Historical Context Section (Optional):**
"The Sea of Galilee is 13 miles long and sits 700 feet below sea level. Sudden violent storms are common..."

---

## Part 4: Scene Narration Screens

### Scene 1: Dawn at the Sea

**Narration Display:**

```
┌──────────────────────────────────────────────────┐
│                                                  │
│  ┌────────────────────────────────────────────┐  │
│  │                                            │  │
│  │  SCENE 1: DAWN AT THE SEA                  │  │
│  │  ════════════════════════                  │  │
│  │                                            │  │
│  │  The night fishing has ended. You see two  │  │
│  │  brothers, Simon (called Peter) and        │  │
│  │  Andrew, pulling their nets to shore.      │  │
│  │  They look tired but determined.           │  │
│  │                                            │  │
│  │  Their rough, weathered hands work the     │  │
│  │  nets with practiced skill. These are men  │  │
│  │  who know their trade—and they are good    │  │
│  │  at it.                                    │  │
│  │                                            │  │
│  │  In the distance, you notice a crowd       │  │
│  │  gathering. A man walks toward the shore,  │  │
│  │  and people follow Him, hanging on His     │  │
│  │  every word.                               │  │
│  │                                            │  │
│  │  ─────────────────────────────────────     │  │
│  │  📖 Matthew 4:18                           │  │
│  │                                            │  │
│  │              [ Continue → ]                │  │
│  │                                            │  │
│  └────────────────────────────────────────────┘  │
│                                                  │
└──────────────────────────────────────────────────┘
```

**Design Specifications:**

- Panel: 1200 x 900, UI/Panel at 85%
- Scene title: Cinzel SemiBold, 36px, Primary/Gold
- Narration: Inter Regular, 28px, UI/Text Primary
- Line height: 1.6 (comfortable reading)
- Scripture: Inter Italic, 20px, UI/Text Secondary
- Continue button: Ghost button with arrow

### Atmosphere Bar (Optional)

Add a subtle bar showing the scene's mood:

```
┌─────────────────────────────────────┐
│ 🌅 Cool mist • Fishing boats • Dawn │
└─────────────────────────────────────┘
```

- Small, top of panel
- Icons + text
- UI/Text Secondary color

---

## Part 5: Dialogue Box Design

### Character Dialogue

When Peter and Andrew speak:

```
┌──────────────────────────────────────────────────┐
│                                                  │
│  ┌────────────────────────────────────────────┐  │
│  │                                            │  │
│  │  ┌─────┐  PETER                            │  │
│  │  │ 👤  │  ──────                           │  │
│  │  └─────┘                                   │  │
│  │                                            │  │
│  │  "Andrew, help me with this net.           │  │
│  │   It is heavier than usual."               │  │
│  │                                            │  │
│  │                        [ Continue → ]      │  │
│  │                                            │  │
│  └────────────────────────────────────────────┘  │
│                                                  │
└──────────────────────────────────────────────────┘
```

**Design Specifications:**

- Panel: 1400 x 350, positioned bottom center
- Portrait: 80 x 80 circle, colored border (Peter = Blue #2196F3)
- Name: Cinzel SemiBold, 28px, character color
- Dialogue: Inter Regular, 32px, UI/Text Primary
- Quote marks: Larger, decorative

### Character Colors

Assign each character a color for their UI elements:

| Character | Color | Hex |
|-----------|-------|-----|
| Jesus | Divine Gold | #D4AF37 |
| Peter | Ocean Blue | #2196F3 |
| Andrew | Forest Green | #4CAF50 |
| James | Royal Purple | #9C27B0 |
| John | Warm Red | #E91E63 |
| Zebedee | Earth Brown | #795548 |

### Emotion Indicators (Optional)

Show character's emotion subtly:

```
┌─────┐
│ 👤  │  PETER
└─────┘  [focused]
```

Small tag under name showing: focused, tired, stunned, calm, etc.

---

## Part 6: Choice Interface

### Player Choices

When player must decide:

```
┌──────────────────────────────────────────────────┐
│                                                  │
│  ┌────────────────────────────────────────────┐  │
│  │                                            │  │
│  │  WHAT WILL YOU DO?                         │  │
│  │                                            │  │
│  │  ┌──────────────────────────────────────┐  │  │
│  │  │                                      │  │  │
│  │  │  Move closer to see who is           │  │  │
│  │  │  approaching                         │  │  │
│  │  │                                      │  │  │
│  │  └──────────────────────────────────────┘  │  │
│  │                                            │  │
│  │  ┌──────────────────────────────────────┐  │  │
│  │  │                                      │  │  │
│  │  │  Offer to help Peter and Andrew      │  │  │
│  │  │  with their nets                     │  │  │
│  │  │                                      │  │  │
│  │  └──────────────────────────────────────┘  │  │
│  │                                            │  │
│  └────────────────────────────────────────────┘  │
│                                                  │
└──────────────────────────────────────────────────┘
```

**Design Specifications:**

- Panel: 800 x 600
- Header: Inter SemiBold, 24px, UI/Text Secondary
- Choice buttons: Full-width, 100px height
- Text: Inter Medium, 28px, centered
- Spacing: 24px between choices

### Choice Button States

- **Default:** UI/Panel background, subtle border
- **Hover:** Golden border, slight glow
- **Selected:** Gold fill with darker text

### Choice Outcome

After selecting, show outcome briefly:

```
┌────────────────────────────────────┐
│                                    │
│  You walk toward the gathering     │
│  crowd, curious about this         │
│  teacher.                          │
│                                    │
│           [ Continue → ]           │
│                                    │
└────────────────────────────────────┘
```

- Smaller panel
- Outcome text: Inter Italic, 24px
- Brief display before next scene

---

## Part 7: Reflection Prompts

### Reflection Screen

After each scene's action:

```
┌──────────────────────────────────────────────────┐
│                                                  │
│         ┌─────────────────────────────┐          │
│         │                             │          │
│         │  ✨ REFLECT                 │          │
│         │  ═════════                  │          │
│         │                             │          │
│         │  "How would you have felt   │          │
│         │   watching this scene       │          │
│         │   unfold?"                  │          │
│         │                             │          │
│         │  ─────────────────────────  │          │
│         │                             │          │
│         │  Take a moment to consider  │          │
│         │  this question personally.  │          │
│         │                             │          │
│         │  ☐ I've reflected on this   │          │
│         │                             │          │
│         │       [ Continue ]          │          │
│         │                             │          │
│         └─────────────────────────────┘          │
│                                                  │
└──────────────────────────────────────────────────┘
```

**Design Specifications:**

- Panel: 700 x 600
- Header: Cinzel SemiBold, 36px, Spirit Purple
- Question: Inter Medium, 32px, UI/Text Primary
- Instruction: Inter Regular, 20px, UI/Text Secondary
- Checkbox: 24px, optional engagement tracker

### Key Reflection Prompts

**The Calling:**
- Scene 1: "How would you have felt watching this scene unfold?"
- Scene 2: "What would Jesus have to say to make you leave everything behind?"
- Scene 3: "What nets do you need to drop to follow Jesus fully?"
- Scene 4: "Why do you think Jesus chose fishermen rather than religious scholars?"
- Scene 5: "Jesus is still calling disciples today. How are you responding to His call?"

**Faith in the Storm:**
- Scene 2: "When have you felt like Jesus was 'asleep' during your storms?"
- Scene 3: "What does Jesus' power over nature tell you about who He is?"
- Scene 4: "What storms are you trying to handle without faith?"
- Scene 5: "Who do you say Jesus is? How does that affect how you trust Him?"

---

## Part 8: Quest Complete Screen

### The Calling - Complete

```
┌──────────────────────────────────────────────────┐
│                                                  │
│         ┌─────────────────────────────┐          │
│         │                             │          │
│         │  ✝ QUEST COMPLETE           │          │
│         │  ════════════════           │          │
│         │                             │          │
│         │  The Calling                │          │
│         │                             │          │
│         │  ─────────────────────────  │          │
│         │                             │          │
│         │  🏅 BADGE EARNED            │          │
│         │  "First Disciple"           │          │
│         │                             │          │
│         │  ─────────────────────────  │          │
│         │                             │          │
│         │  📚 KNOWLEDGE GAINED        │          │
│         │  • Immediate obedience of   │          │
│         │    the first disciples      │          │
│         │  • The cost of following    │          │
│         │    Jesus                    │          │
│         │  • Jesus' method of calling │          │
│         │    ordinary people          │          │
│         │                             │          │
│         │  ─────────────────────────  │          │
│         │                             │          │
│         │  📖 SCRIPTURES              │          │
│         │  Matthew 4:18-22            │          │
│         │  Mark 1:16-20               │          │
│         │  Luke 5:1-11                │          │
│         │                             │          │
│         │  ─────────────────────────  │          │
│         │                             │          │
│         │  +100 Faith Points          │          │
│         │                             │          │
│         │       [ Continue ]          │          │
│         │                             │          │
│         └─────────────────────────────┘          │
│                                                  │
└──────────────────────────────────────────────────┘
```

**Design Specifications:**

- Add golden glow/rays behind panel
- Badge icon: Custom design or emoji, 64px
- Badge name: Cinzel Bold, 28px
- Lists: Bullet points, Inter Regular
- Faith points: Large, Primary/Gold, animated feel

### Faith in the Storm - Complete

Same layout with:
- Badge: "Storm Survivor" ⛵
- Different knowledge points
- Mark 4:35-41 scriptures

---

## Part 9: Special UI for Storm Quest

### Storm Intensity Indicator

During the storm scene, show intensity:

```
┌─────────────────────────────┐
│ STORM INTENSITY             │
│ ████████████░░░░ 75%        │
└─────────────────────────────┘
```

- Top of screen during storm scenes
- Animated fill
- Red/orange color

### The Calm Moment

When Jesus speaks "Peace, be still" - special UI:

```
┌──────────────────────────────────────────────────┐
│                                                  │
│                                                  │
│                                                  │
│              "Peace, be still."                  │
│                                                  │
│                   — Jesus                        │
│                                                  │
│                                                  │
│                                                  │
└──────────────────────────────────────────────────┘
```

- Full screen
- Text centered
- Golden glow behind text
- Minimal UI
- Dramatic pause

### Before/After Contrast

Design two versions of the scene:
1. **Storm** - Dark, desaturated, chaotic UI elements
2. **Calm** - Bright, peaceful, clean UI

---

## Part 10: Scene-by-Scene UI List

### The Calling - All Screens

**Scene 1: Dawn at the Sea**
- [ ] Narration screen
- [ ] Dialogue: Peter (focused)
- [ ] Dialogue: Andrew (tired)
- [ ] Choice: Observe or Help
- [ ] Reflection prompt

**Scene 2: The Voice**
- [ ] Narration screen
- [ ] Dialogue: Jesus - "Come, follow Me..."
- [ ] Dialogue: Peter (stunned silence)
- [ ] Choice: Ask question or Think about risk
- [ ] Reflection prompt

**Scene 3: The Decision**
- [ ] Narration screen
- [ ] Dialogue: Peter *drops net*
- [ ] Dialogue: Andrew *follows*
- [ ] Choice: Reflect on obedience or Question
- [ ] Reflection prompt

**Scene 4: The Call Continues**
- [ ] Narration screen
- [ ] Dialogue: Jesus extends hand
- [ ] Dialogue: Zebedee watches
- [ ] Choice: Consider what Jesus saw
- [ ] Reflection prompt

**Scene 5: The Journey Begins**
- [ ] Narration screen
- [ ] Dialogue: Jesus leads
- [ ] Dialogue: Peter looks back, then forward
- [ ] Final reflection prompt
- [ ] Quest complete screen

### Faith in the Storm - All Screens

**Scene 1: Evening Calm**
- [ ] Narration screen (peaceful)
- [ ] No dialogue (setup)
- [ ] Auto-continue

**Scene 2: The Storm Rises**
- [ ] Narration screen (intense)
- [ ] Dialogue: Peter (panicked)
- [ ] Dialogue: Disciple (incredulous)
- [ ] Choice: Wake Jesus or Try yourself
- [ ] Reflection prompt

**Scene 3: Peace, Be Still**
- [ ] Narration screen
- [ ] Dialogue: Jesus - "Peace, be still."
- [ ] Special calm UI
- [ ] Choice: Marvel
- [ ] Reflection prompt

**Scene 4: The Question**
- [ ] Narration screen
- [ ] Dialogue: Jesus - "Why are you afraid?"
- [ ] Dialogue: Peter (overwhelmed)
- [ ] Reflection prompt (no choice)

**Scene 5: Who Is This?**
- [ ] Narration screen
- [ ] Dialogue: Disciples - "Who is this?"
- [ ] Final reflection prompt
- [ ] Quest complete screen

---

## Part 11: Creating the Prototype Flow

### Main Flow

```
[Quest Select] → [Quest Intro] → [Scene 1 Narration]
                                        ↓
                              [Scene 1 Dialogue 1]
                                        ↓
                              [Scene 1 Dialogue 2]
                                        ↓
                              [Scene 1 Choices]
                                        ↓
                              [Choice Outcome]
                                        ↓
                              [Scene 1 Reflection]
                                        ↓
                              [Scene 2 Narration]
                                        ↓
                                      ...
                                        ↓
                              [Scene 5 Reflection]
                                        ↓
                              [Quest Complete]
                                        ↓
                              [Quest Select]
```

### Prototype Connections

1. **Quest Card** → Quest Intro (On click)
2. **Begin Quest** → Scene 1 Narration (On click)
3. **Continue buttons** → Next screen (On click)
4. **Choice buttons** → Choice Outcome → Next Scene (On click)
5. **Quest Complete Continue** → Quest Select (On click)

### Animations

- **Scene transitions:** Dissolve, 400ms
- **Dialogue appear:** Slide up, 200ms
- **Choice buttons:** Fade in, staggered 100ms each
- **Reflection appear:** Dissolve, 300ms
- **Quest complete:** Slow dissolve, 600ms

---

## Part 12: Component Organization

### Create These Components

**Buttons:**
- Button/Primary
- Button/Secondary
- Button/Ghost
- Button/Choice

**Cards:**
- Card/Quest (with variants)
- Card/Character

**Panels:**
- Panel/Narration
- Panel/Dialogue
- Panel/Choice
- Panel/Reflection
- Panel/Complete

**Text Styles:**
- Already defined in Guide 01

**Icons:**
- Icon/Continue (arrow)
- Icon/Scripture (book)
- Icon/Time (clock)
- Icon/Reflect (sparkle)
- Icon/Badge (medal)

---

## Part 13: Export Checklist

### Assets to Export for Unreal

**Quest Cards:**
- [ ] The Calling - all states
- [ ] Faith in the Storm - all states

**Panels:**
- [ ] Narration panel background
- [ ] Dialogue box background
- [ ] Choice panel background
- [ ] Reflection panel background
- [ ] Complete screen background

**Character Portraits:**
- [ ] Jesus
- [ ] Peter
- [ ] Andrew
- [ ] James
- [ ] John
- [ ] Zebedee

**Icons:**
- [ ] All UI icons
- [ ] Badge: First Disciple
- [ ] Badge: Storm Survivor

**Buttons:**
- [ ] All button states

---

## Part 14: File Organization

### Figma Page Structure

```
Bible VR - Quest UI
├── Cover
├── Style Guide
├── Components
├── Quest Selection
├── The Calling
│   ├── Intro
│   ├── Scene 1
│   ├── Scene 2
│   ├── Scene 3
│   ├── Scene 4
│   ├── Scene 5
│   └── Complete
├── Faith in the Storm
│   ├── Intro
│   ├── Scene 1
│   ├── Scene 2
│   ├── Scene 3
│   ├── Scene 4
│   ├── Scene 5
│   └── Complete
├── Prototypes
└── Handoff
```

---

## Quick Reference

### Panel Sizes
- Narration: 1200 x 900
- Dialogue: 1400 x 350
- Choice: 800 x 600
- Reflection: 700 x 600
- Complete: 900 x 1100

### Key Colors
- Jesus: #D4AF37 (Gold)
- Peter: #2196F3 (Blue)
- Reflection: #9C27B0 (Purple)
- Success: #4CAF50 (Green)

### Typography
- Scene Title: Cinzel SemiBold, 36px
- Narration: Inter Regular, 28px
- Dialogue: Inter Regular, 32px
- Character Name: Cinzel SemiBold, 28px

---

## Next Steps

1. **Create all screens** listed in Part 10
2. **Build components** for reusability
3. **Connect prototype** following Part 11
4. **Export assets** using checklist
5. **Import to Unreal** following Guide 06

---

*Design each screen with intention. These aren't just interfaces—they're the frame through which players experience Scripture. Make them beautiful, readable, and reverent.*
