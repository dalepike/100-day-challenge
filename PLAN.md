# 100-Day Reading Challenge Tracker

## Project Overview

A simple, elegant web app for tracking daily reading progress over 100 days (or variable). Designed for family sharing via GitHub Pages.

**Repository:** github.com/dalepike/100-day-challenge
**Hosted URL:** dalepike.github.io/100-day-challenge

---

## Core Features

1. **Visual Progress Grid** - 10x10 grid (or adaptive) showing completed days
2. **One-Click Day Toggle** - Tap a day to mark complete/incomplete
3. **Personalization** - Set your name (displayed as title)
4. **Variable Duration** - Default 100 days, configurable (30, 60, 100, etc.)
5. **Export to PNG** - Download shareable image of your progress
6. **Local Persistence** - Progress saved in browser localStorage
7. **Progress Stats** - Show days completed / total days

---

## Technical Approach

### Stack
- **Single HTML file** with embedded CSS and JavaScript
- **No build tools** - just HTML/CSS/JS
- **html2canvas** library (CDN) for PNG export
- **localStorage** for persistence
- **GitHub Pages** for hosting

### Why Single File?
- Simplest possible deployment
- Can also be downloaded and used offline
- No dependencies to manage
- Easy to maintain

---

## Implementation Plan

### Step 1: Create Base HTML Structure
- Semantic HTML5 document
- Meta tags for mobile responsiveness
- Clean, minimal structure

### Step 2: Design the UI (CSS)
- Clean, modern aesthetic
- Mobile-first responsive design
- Grid layout for day squares
- Smooth transitions for interactions
- Print-friendly export area

### Step 3: Core JavaScript Functionality
- State management (name, days completed, total days)
- localStorage read/write
- Day toggle handler
- Settings panel (name, day count)

### Step 4: PNG Export Feature
- html2canvas integration
- Export button
- Clean export area (hide UI chrome, show just the tracker)
- Filename includes name and date

### Step 5: Polish & Edge Cases
- First-time user welcome/setup
- Reset/clear progress option (with confirmation)
- Handle localStorage unavailable (private browsing)
- Keyboard accessibility

### Step 6: Deploy to GitHub Pages
- Create repository on dalepike account
- Push code
- Enable GitHub Pages
- Test live URL

---

## UI Design Specifications

### Layout
```
┌─────────────────────────────────────┐
│         [Name]'s                    │
│    100 Days Reading Challenge       │
│         ⚙️ Settings                 │
├─────────────────────────────────────┤
│  ┌──┬──┬──┬──┬──┬──┬──┬──┬──┬──┐   │
│  │1 │2 │3 │4 │5 │6 │7 │8 │9 │10│   │
│  ├──┼──┼──┼──┼──┼──┼──┼──┼──┼──┤   │
│  │11│12│13│  │  │  │  │  │  │20│   │
│  ├──┼──┼──┼──┼──┼──┼──┼──┼──┼──┤   │
│  │  │  │  │  │  │  │  │  │  │  │   │
│  │  ... (10 rows x 10 cols) ...    │
│  │  │  │  │  │  │  │  │  │  │100   │
│  └──┴──┴──┴──┴──┴──┴──┴──┴──┴──┘   │
├─────────────────────────────────────┤
│     Progress: 12/100 (12%)          │
│     [📸 Export Image]               │
└─────────────────────────────────────┘
```

### Color Palette
- Background: Warm off-white (#faf9f6)
- Incomplete day: Light gray (#e8e8e8)
- Completed day: Warm green (#4ade80) with subtle checkmark
- Text: Dark gray (#333)
- Accent: Soft blue for buttons (#3b82f6)

### Typography
- System font stack (no external fonts to load)
- Clean, readable sizes

---

## Data Model

```javascript
{
  name: "Dale",           // User's display name
  totalDays: 100,         // Challenge duration
  completedDays: [1, 2, 3, 5, 7],  // Array of completed day numbers
  startDate: "2026-01-03" // Optional: track when started
}
```

**localStorage key:** `reading-challenge-data`

---

## Export Image Specifications

- **Dimensions:** ~800x900px (good for social sharing)
- **Content:**
  - Title: "[Name]'s 100 Days Reading Challenge"
  - The progress grid
  - Progress count: "Day 12 of 100"
  - Small footer: "Track your journey at dalepike.github.io/100-day-challenge"
- **Format:** PNG
- **Filename:** `reading-challenge-[name]-[date].png`

---

## Files to Create

```
100-day-challenge/
├── index.html      # The entire app (single file)
├── README.md       # GitHub repo readme
└── PLAN.md         # This file
```

---

## Testing Checklist

- [ ] Works on mobile (iPhone, Android)
- [ ] Works on desktop (Chrome, Safari, Firefox)
- [ ] localStorage persists across sessions
- [ ] Export creates clean PNG
- [ ] Settings changes persist
- [ ] Reset clears all data
- [ ] Handles 30, 60, 100 day variations
- [ ] Accessible via keyboard
- [ ] Works offline after first load

---

## Distribution to Family

Once deployed, share:
1. **URL:** dalepike.github.io/100-day-challenge
2. **Instructions:**
   - Open the link
   - Enter your name
   - Tap a day when you've read
   - Export and share your progress anytime!

---

## Future Enhancements (Not in v1)

- Share button (native share API)
- Dark mode toggle
- Custom challenge title (not just "Reading")
- Streak counter
- Start date tracking with calendar view
