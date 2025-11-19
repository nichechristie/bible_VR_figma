# GUIDE 01: Figma Basics for Complete Beginners

## What is Figma?

Figma is a free, web-based design tool used for creating:
- User interfaces (UI)
- App and game mockups
- Prototypes and wireframes
- Icons, graphics, and illustrations

For your Bible VR game, you'll use Figma to design menus, HUD elements, dialogue boxes, and plan your visual style before building in Unreal Engine.

---

## Part 1: Getting Started with Figma

### Step 1: Create a Free Account

1. Open your web browser
2. Go to: **https://www.figma.com**
3. Click **"Sign up free"**
4. Enter your email or sign up with Google
5. Verify your email

### Step 2: Open Figma

You can use Figma in two ways:

**Option A: Web Browser (Easiest)**
- Just go to figma.com and sign in
- Works on any computer

**Option B: Desktop App**
- Download from figma.com/downloads
- Better performance for large files

### Step 3: Create Your First File

1. After signing in, you'll see your **Home** dashboard
2. Click **"+ New design file"** (top right)
3. A blank canvas opens - this is your workspace!

---

## Part 2: Understanding the Figma Interface

When you open a file, you'll see:

```
+--------------------------------------------------+
|  TOOLBAR (top)                                   |
+----------+---------------------------+-----------+
|          |                           |           |
|  LAYERS  |      CANVAS               |  DESIGN   |
|  PANEL   |      (work area)          |  PANEL    |
|  (left)  |                           |  (right)  |
|          |                           |           |
+----------+---------------------------+-----------+
```

### Main Panels

#### 1. Toolbar (Top)
The main tools you'll use:
- **Move tool (V)** - Select and move objects
- **Frame tool (F)** - Create containers/screens
- **Rectangle (R)** - Draw rectangles
- **Ellipse (O)** - Draw circles
- **Text (T)** - Add text
- **Pen (P)** - Draw custom shapes

#### 2. Layers Panel (Left)
Shows everything in your file:
- Pages (like tabs)
- Frames (screens)
- All objects organized hierarchically

#### 3. Canvas (Center)
Your main workspace:
- Infinite space to work in
- Scroll with mouse wheel
- Zoom with Ctrl/Cmd + scroll

#### 4. Design Panel (Right)
Properties of selected object:
- Position and size
- Colors and effects
- Typography settings

---

## Part 3: Essential Controls

### Navigation

| Action | Control |
|--------|---------|
| Pan around canvas | Hold **Space** + drag |
| Zoom in/out | **Ctrl/Cmd + scroll** |
| Zoom to fit | **Shift + 1** |
| Zoom to selection | **Shift + 2** |
| Zoom to 100% | **Ctrl/Cmd + 0** |

### Selecting Objects

| Action | Control |
|--------|---------|
| Select | **Click** on object |
| Multi-select | **Shift + click** |
| Select all | **Ctrl/Cmd + A** |
| Deselect | **Escape** or click empty space |
| Select through groups | **Ctrl/Cmd + click** |

### Basic Operations

| Action | Control |
|--------|---------|
| Copy | **Ctrl/Cmd + C** |
| Paste | **Ctrl/Cmd + V** |
| Duplicate | **Ctrl/Cmd + D** |
| Delete | **Delete** or **Backspace** |
| Undo | **Ctrl/Cmd + Z** |
| Redo | **Ctrl/Cmd + Shift + Z** |

---

## Part 4: Creating Your First Design

### Step 1: Create a Frame

Frames are like screens or artboards - containers for your designs.

1. Press **F** (Frame tool)
2. In the right panel, choose a preset:
   - **Phone** - iPhone, Android sizes
   - **Tablet** - iPad sizes
   - **Desktop** - Various screen sizes
3. Or click and drag on canvas to create custom size

For VR UI, create a custom size: **1920 x 1080** (standard HD)

### Step 2: Add a Rectangle

1. Press **R** (Rectangle tool)
2. Click and drag on the canvas
3. A rectangle appears!

**Adjust properties (right panel):**
- **X, Y** - Position
- **W, H** - Width and Height
- **Fill** - Color
- **Stroke** - Border
- **Corner radius** - Rounded corners

### Step 3: Add Text

1. Press **T** (Text tool)
2. Click on canvas and type
3. Or click and drag to create a text box

**Text properties (right panel):**
- **Font** - Choose typeface
- **Size** - Font size
- **Weight** - Bold, regular, light
- **Color** - Text color
- **Alignment** - Left, center, right

### Step 4: Add Colors

1. Select an object
2. In the right panel, find **Fill**
3. Click the color square
4. Choose a color using:
   - Color picker
   - Hex code (e.g., #FF5500)
   - RGB values

---

## Part 5: Organizing Your Work

### Using Layers

Every object appears in the Layers panel (left):
- Drag to reorder (top = front)
- Click eye icon to hide/show
- Click lock icon to prevent editing
- Double-click to rename

### Naming Convention

Name your layers clearly:
- `Button/Primary`
- `Icon/Menu`
- `Text/Title`
- `Background/Main`

### Grouping Objects

Select multiple objects, then:
- **Ctrl/Cmd + G** = Group
- **Ctrl/Cmd + Shift + G** = Ungroup

Groups keep related items together.

### Using Frames for Organization

Frames are better than groups because:
- They clip content (hide overflow)
- They can have their own backgrounds
- They're better for prototyping

To frame objects:
1. Select objects
2. Press **Ctrl/Cmd + Alt + G**

---

## Part 6: Working with Colors

### Creating a Color Style

Save colors to reuse them:

1. Select an object with the color you want
2. In the right panel, click the **4 dots** next to Fill
3. Click **+** to create a style
4. Name it (e.g., "Primary/Gold")
5. Click **Create Style**

Now you can apply this color anywhere!

### Color Palette for Bible VR

Suggested colors for your project:

| Name | Hex Code | Use For |
|------|----------|---------|
| Divine Gold | #D4AF37 | Holy light, highlights |
| Sacred White | #FFFEF5 | Pure light, text |
| Ancient Stone | #8B7355 | UI backgrounds |
| Parchment | #F5E6C8 | Text backgrounds |
| Deep Purple | #4A2C5A | Royalty, divinity |
| Sky Blue | #87CEEB | Heaven, peace |
| Earth Brown | #654321 | Grounding elements |
| Blood Red | #8B0000 | Sacrifice, important |

---

## Part 7: Typography

### Choosing Fonts

For biblical/ancient feel:
- **Serif fonts** - Cinzel, Trajan, Times New Roman
- **Script fonts** - Great Vibes, Tangerine (for quotes)

For readability:
- **Sans-serif** - Inter, Roboto, Open Sans

### Creating Text Styles

1. Select text with formatting you like
2. In right panel, click **4 dots** next to Text
3. Click **+** to create style
4. Name it (e.g., "Heading/Large")

### Typography Hierarchy

Create consistent text styles:

| Style Name | Size | Weight | Use For |
|------------|------|--------|---------|
| H1/Title | 48px | Bold | Main titles |
| H2/Subtitle | 32px | Semi-bold | Section headers |
| Body/Large | 18px | Regular | Main text |
| Body/Small | 14px | Regular | Secondary text |
| Caption | 12px | Regular | Labels, hints |
| Button | 16px | Medium | Button text |

---

## Part 8: Components (Reusable Elements)

### What are Components?

Components are reusable design elements. Change the main component, and all copies update automatically.

### Creating a Component

1. Design an element (e.g., a button)
2. Select it
3. Press **Ctrl/Cmd + Alt + K**
4. Or right-click > **Create component**

The element now has a **purple border** - it's a main component!

### Using Component Instances

1. Find your component in the left panel (Assets tab)
2. Drag it onto the canvas
3. This creates an **instance** (copy)

Instances have a **hollow diamond** icon.

### Editing Components

- Edit **main component** = All instances update
- Edit **instance** = Only that copy changes (override)

To reset an instance to match main:
- Right-click > **Reset all overrides**

---

## Part 9: Essential Keyboard Shortcuts

Print this and keep it handy!

### Tools
| Shortcut | Tool |
|----------|------|
| V | Move/Select |
| F | Frame |
| R | Rectangle |
| O | Ellipse |
| L | Line |
| T | Text |
| P | Pen |
| I | Eyedropper (pick color) |

### View
| Shortcut | Action |
|----------|--------|
| Space + drag | Pan |
| Ctrl/Cmd + scroll | Zoom |
| Shift + 1 | Zoom to fit |
| Ctrl/Cmd + \\ | Hide UI panels |

### Edit
| Shortcut | Action |
|----------|--------|
| Ctrl/Cmd + C | Copy |
| Ctrl/Cmd + V | Paste |
| Ctrl/Cmd + D | Duplicate |
| Ctrl/Cmd + G | Group |
| Ctrl/Cmd + Alt + K | Create component |
| Ctrl/Cmd + Z | Undo |

### Arrange
| Shortcut | Action |
|----------|--------|
| Ctrl/Cmd + ] | Bring forward |
| Ctrl/Cmd + [ | Send backward |
| Ctrl/Cmd + Shift + ] | Bring to front |
| Ctrl/Cmd + Shift + [ | Send to back |

---

## Part 10: Saving and Sharing

### Auto-Save

Figma automatically saves your work to the cloud!
- No need to manually save
- See "Saved" in the top bar

### Naming Your File

1. Click on "Untitled" at the top
2. Type your file name: `Bible VR - UI Design`
3. Press Enter

### Sharing with Others

1. Click **Share** button (top right)
2. Enter email address
3. Choose permission:
   - **Can view** - Look only
   - **Can edit** - Full access
4. Click **Send invite**

### Exporting Assets

To export designs for use in Unreal:

1. Select the element to export
2. In right panel, scroll to **Export**
3. Click **+** to add export setting
4. Choose format:
   - **PNG** - Images with transparency
   - **SVG** - Scalable graphics
   - **PDF** - Documents
5. Click **Export [name]**

---

## Part 11: Practice Exercise

### Create a Simple Button

1. **Create a frame**
   - Press F
   - Draw a 200 x 60 rectangle

2. **Style the background**
   - Select the frame
   - Fill: #D4AF37 (gold)
   - Corner radius: 8

3. **Add text**
   - Press T
   - Type "BEGIN QUEST"
   - Font: Cinzel or similar
   - Size: 18px
   - Color: #FFFFFF (white)
   - Center the text

4. **Add effects**
   - Select the frame
   - In right panel, click **+** next to Effects
   - Add **Drop shadow**
   - X: 0, Y: 4, Blur: 8
   - Color: Black at 25% opacity

5. **Make it a component**
   - Select the frame
   - Press Ctrl/Cmd + Alt + K
   - Name it "Button/Primary"

**Congratulations!** You've created your first reusable UI component!

---

## Part 12: Figma Resources

### Free Resources

**Icons:**
- Figma Community (built-in)
- Iconify plugin
- Feather Icons

**UI Kits:**
- Search "UI Kit" in Figma Community
- Many free complete design systems

**Fonts:**
- Google Fonts (free)
- Figma has many built-in

### Installing Plugins

1. Click the Figma icon (top left) or use menu
2. Go to **Plugins** > **Browse plugins in Community**
3. Search for what you need
4. Click **Install**

**Useful plugins:**
- **Iconify** - Thousands of icons
- **Unsplash** - Free photos
- **Content Reel** - Placeholder text/images
- **Contrast** - Check color accessibility

---

## Part 13: Organizing Your Bible VR Project

### Recommended Page Structure

In Figma, create these pages (tabs at the top of layers panel):

1. **Cover** - Project title, description
2. **Style Guide** - Colors, fonts, components
3. **Main Menu** - Title screen, settings
4. **HUD** - In-game interface
5. **Dialogue** - Character speech UI
6. **Quest UI** - Quest selection, completion
7. **Components** - All reusable elements
8. **Icons** - All icon designs
9. **Archive** - Old versions

### File Naming

`Bible VR - [Type] - [Version]`

Examples:
- `Bible VR - Main UI - v1`
- `Bible VR - Icons - v2`
- `Bible VR - Prototypes - v1`

---

## Next Steps

Now that you understand Figma basics, continue to:

- **GUIDE_02_VR_UI_DESIGN.md** - Designing interfaces for VR
- **GUIDE_03_BIBLE_VR_ASSETS.md** - Creating specific Bible VR elements
- **GUIDE_04_PROTOTYPING.md** - Making interactive prototypes

---

## Quick Reference

**Create:** Frame (F), Rectangle (R), Ellipse (O), Text (T)

**Navigate:** Space + drag (pan), Ctrl + scroll (zoom)

**Organize:** Ctrl + G (group), Ctrl + Alt + K (component)

**Edit:** Ctrl + D (duplicate), Ctrl + Z (undo)

**Export:** Select → Right panel → Export → Choose format

---

*Figma is where your ideas become visual. Take time to learn the basics well, and you'll design beautiful UI for your Bible VR game!*
