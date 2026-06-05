# 📋 NotionClub — Event Landing Page

A fully responsive, interactive event announcement and countdown webpage for the **Notion Club Workshop 2026**, built with pure HTML, CSS, and JavaScript — no frameworks, no dependencies.

---

## 🚀 Live Preview

Open `index.html` directly in any modern browser. No build step or server required.

---

## 📁 Project Structure

```
notion-club/
├── index.html        # Main webpage (all-in-one: HTML + CSS + JS)
├── README.md         # Project documentation
└── images/           # (Optional) Add speaker photos here
    ├── sarah.jpg
    ├── marcus.jpg
    └── aisha.jpg
```

> All CSS and JavaScript are embedded inside `index.html` for simplicity and portability.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🎯 Hero Section | Bold event title, tagline, banner poster, and CTA buttons |
| ⏱️ Live Countdown Timer | Real-time countdown to event date (Feb 15, 2026) |
| 📅 Event Details | Date, platform, capacity, and requirements — color-coded cards |
| 🎤 Speakers Section | Speaker cards with photo, name, role, and bio |
| ❓ FAQ Accordion | Expandable/collapsible questions with smooth animation |
| 📣 Marquee CTA Footer | Scrolling "SEE YOU THERE" banner with registration button |
| 📱 Fully Responsive | Mobile-friendly layout with hamburger navigation |
| 🎨 Scroll Reveal Animations | Elements animate in as you scroll down the page |

---

## 🛠️ Tech Stack

- **HTML5** — Semantic structure
- **CSS3** — Custom properties, Grid, Flexbox, keyframe animations
- **Vanilla JavaScript** — Countdown timer, FAQ accordion, scroll reveal, nav toggle
- **Google Fonts** — `Bebas Neue` (display), `DM Sans` (body), `Space Mono` (labels)

No npm, no bundler, no build process needed.

---

## 📐 Sections Breakdown

### 1. Navigation Bar
- Fixed top bar with logo, nav links, and Register button
- Hamburger menu on mobile
- Shadow appears on scroll

### 2. Hero Section
- Large typographic heading with pink accent
- Event banner with gradient background
- Two CTA buttons: **Register Now** and **Learn More**

### 3. Countdown Timer
- Counts down to `February 15, 2026 — 10:00 AM EST`
- Four colored boxes: Days (yellow), Hours (green), Minutes (pink), Seconds (blue)
- Updates every second via `setInterval`

### 4. Event Details
- 2×2 grid of info cards
- Date & Time, Platform, Capacity, Requirements
- Brutalist card style with thick borders and offset shadows

### 5. Speakers Section
- Three speaker cards with photo area, name, role, and bio
- Placeholder initials shown by default — replace with real photos

### 6. FAQ Section
- Five collapsible questions
- Only one open at a time (accordion behavior)
- Plus icon rotates to × when open

### 7. CTA Footer
- Black background with marquee scrolling text in green, yellow, and pink
- "SECURE YOUR SPOT" button
- Copyright footer

---

## 🖼️ Adding Speaker Photos

To replace the placeholder initials with real photos, locate each speaker card in `index.html` and swap the inner content:

**Before (placeholder):**
```html
<div class="speaker-photo s1">
  <span class="initials">SC</span>
</div>
```

**After (with photo):**
```html
<div class="speaker-photo s1">
  <img src="images/sarah.jpg" alt="Sarah Chen"
       style="width:100%;height:100%;object-fit:cover;display:block;">
</div>
```

Repeat for `s2` (Marcus) and `s3` (Aisha). Also remove the gradient background CSS for `.speaker-photo.s1`, `.s2`, `.s3` since they'll be replaced by actual images.

---

## ⏰ Changing the Event Date

Find this line in the `<script>` section near the bottom of `index.html`:

```javascript
const eventDate = new Date('2026-02-15T10:00:00-05:00');
```

Replace with your actual event date and time in ISO 8601 format:

```javascript
// Format: 'YYYY-MM-DDTHH:MM:SS±HH:MM'
// Example for March 10, 2026 at 9:00 AM IST (UTC+5:30):
const eventDate = new Date('2026-03-10T09:00:00+05:30');
```

---

## 🎨 Customising Colors

All colors are defined as CSS variables at the top of the `<style>` block:

```css
:root {
  --black:  #0a0a0a;
  --white:  #f5f2ee;
  --pink:   #ff3864;   /* Primary accent — buttons, roles, highlights */
  --yellow: #f5d000;   /* Days box, secondary buttons */
  --green:  #2ecc71;   /* Hours box */
  --blue:   #3b82f6;   /* Seconds box */
}
```

Change any value here and it propagates across the entire page instantly.

---

## ✏️ Updating Content

| What to change | Where to find it in `index.html` |
|---|---|
| Event title & tagline | Inside `<section id="hero">` |
| Event date/time/platform | Inside `<section id="details">` |
| Speaker names, roles, bios | Inside `<section id="speakers">` |
| FAQ questions & answers | Inside `<section id="faq">` |
| Registration link | All `href="#register"` or `href="#"` on CTA buttons |
| Footer copyright text | Bottom of `<section id="register">` |

---

## 📱 Responsive Breakpoints

| Breakpoint | Layout Changes |
|---|---|
| `> 768px` | Full desktop layout, 3-column speakers grid, 2-column details grid |
| `≤ 768px` | Hamburger nav, single-column details and speakers |
| `≤ 500px` | Smaller countdown boxes, tighter spacing |

---

## 🌐 Browser Support

Tested and works in all modern browsers:

- ✅ Chrome / Edge (Chromium)
- ✅ Firefox
- ✅ Safari
- ✅ Mobile Chrome & Safari

---

## 📄 License

This project was created for the **Notion Club Workshop 2026** event page. Free to use and modify for personal and educational purposes.

---

> Built with passion for productivity 🖤
