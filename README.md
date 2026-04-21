# Age Calculator

A professional, fully responsive age calculator web application with dual calculation modes, rich insights, beautiful glassmorphism animations, and comprehensive age breakdowns.

**Live Demo:** [https://why-age-calculator.vercel.app/](https://why-age-calculator.vercel.app/)

---

## Overview

Age Calculator Pro is a modern, feature-rich web application that goes far beyond simple year math. Enter your birth date (or a duration) and instantly get a rich dashboard of insights — astrological, cultural, planetary, and health-based — wrapped in a responsive glassmorphism UI with light/dark themes.

---

## Key Features

### 🎯 Dual Calculation Modes

#### 1. Calculate by Birth Date
- Select **Year** from dropdown (1900 to current year)
- Choose **Month** from dropdown (January to December)
- Pick **Day** from dropdown (1–31, auto-adjusts based on month/year)
- Intelligent date validation to prevent future dates
- Leap-year aware day selector

#### 2. Calculate by Duration
- Enter custom durations using multiple inputs:
  - **Years** input field
  - **Months** input field
  - **Weeks** input field
  - **Days** input field
- Supports any combination of inputs
- Back-calculates your birth date from the entered duration

#### 🔄 Auto-Reset Inputs
- Input fields clear automatically after a result is generated for a clean next-calculation experience.

### 🎂 Precise Age Breakdown
- Exact **Years · Months · Days** calculation
- Handles **leap years** and varying month lengths (28/30/31) precisely
- Displays the **exact day of the week** you were born (e.g., "You were born on a Tuesday")
- **Leap Year Baby** badge if applicable

### 📊 Life Progress Visualization
- **Circular SVG progress ring** + linear progress bar
- Shows percentage of an 80-year life expectancy lived
- Displays remaining years ahead in real time

### ⏳ Live Next-Birthday Countdown
- Real-time **Days · Hours · Minutes · Seconds** ticker until your next birthday
- Updates every second

### 🔮 Astrological & Cultural Insights
- **Western Zodiac Sign** with emoji (Aries → Pisces)
- **Chinese Zodiac Animal** based on birth year
- **Birthstone** for your birth month

### 📈 Total Stats Dashboard
A responsive grid showing your age in:
- **Years · Months · Weeks · Days · Hours · Minutes · Seconds**

### ❤️ Health-Based Fun Facts
Estimated totals since birth:
- **Heartbeats** (~70 bpm average)
- **Breaths taken** (~16 per minute)
- **Hours slept** (~8 hours per day)

### 🪐 Age Across the Solar System
See how old you'd be on **Mercury, Venus, Mars, Jupiter, Saturn, Uranus, Neptune**, and Pluto — based on each planet's orbital period.

### 🎨 Design & User Experience
- **Glassmorphism aesthetic** with animated gradient backgrounds
- **Dark / Light mode toggle** (auto-detects system preference)
- **Fully responsive** — mobile, tablet, desktop
- Smooth hover effects, fade-up animations, and gradient text accents
- HSL-based semantic design tokens (no hardcoded colors)
- Adaptive grid layout (2 → 3 → 7 columns across breakpoints)

### 🛡️ Validation & Error Handling
- Validates future dates, empty inputs, and mismatched day/month combinations
- Dynamically caps day selector based on selected month + leap year status
- User-friendly error messages

---

## Core Functions

Located in `src/lib/age.ts`:

| Function | Purpose |
|---|---|
| `calculateAge(birth)` | Returns precise `{ years, months, days, totalDays }` breakdown. |
| `zodiacSign(month, day)` | Western zodiac sign + emoji. |
| `chineseZodiac(year)` | Chinese zodiac animal + emoji. |
| `birthstone(month)` | Birthstone for given month. |
| `dayOfWeek(date)` | Day name the user was born. |
| `isLeapYear(year)` | Leap year detector. |
| `daysInMonth(year, month)` | Accurate day count for any month. |
| `nextBirthday(birth, now)` | Date of upcoming birthday. |
| `countdown(target, now)` | Live D/H/M/S countdown object. |
| `planets` | Orbital-period dataset for cross-planet age conversion. |

---

## 🛠️ Tech Stack

- **React 18** + **TypeScript**
- **Vite** for lightning-fast builds
- **Tailwind CSS** with an HSL-based semantic design token system
- **shadcn/ui** primitives (Button, Input, Select)
- **lucide-react** icons
- **SVG** for the circular life-progress indicator

---

## 📂 Project Structure

```
src/
├── lib/age.ts          # All date math, zodiac, countdown & planetary logic
├── pages/Index.tsx     # Main UI: input modes, result dashboard, countdown
├── index.css           # Glassmorphism tokens, gradients, animations
└── components/ui/      # shadcn primitives
```

---

## 🎯 Highlights for Portfolio

- Built a **modular pure-function calculation engine** (fully unit-testable, no UI coupling).
- Designed a **token-driven design system** (HSL variables, gradient utilities, glass surfaces) that cleanly supports light/dark themes.
- Implemented a **real-time countdown** using `setInterval` + React state without performance issues.
- Rendered a **custom SVG circular progress ring** with animated stroke-dashoffset.
- Delivered a **fully responsive** layout using Tailwind's grid system (2 → 3 → 7 columns across breakpoints).
- Integrated **astrological, cultural, health, and planetary** data layers into a single cohesive dashboard.

---

## Use Cases

1. **Personal**: Calculate your exact age with rich insights
2. **Education**: Teaching date/time calculations, astronomy, and zodiac systems
3. **Event Planning**: Real-time countdown to next birthday
4. **Portfolio Demo**: Showcase React + design-system skills

---

## Browser Support

- Chrome, Firefox, Safari, Edge, Opera (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

---

## Copyright

© 2025 Age Calculator Pro. All Rights Reserved.

---

**Developed with precision and care to provide the best age calculation experience on the web.**
