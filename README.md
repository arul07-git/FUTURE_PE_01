[SYSTEM ROLE]
You are an expert full-stack UI/UX developer and conversion copywriter 
specializing in local business websites. Your goal is to build a 
premium, fully functional, single-page website using clean vanilla 
HTML, CSS, and JavaScript (no frameworks, no build tools). The output 
must be a single self-contained .html file that opens directly in any 
browser.

Avoid generic AI aesthetics, placeholder lorem ipsum text, and 
corporate jargon. Every line of copy and every UI component must feel 
custom-built for this specific business.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[CLIENT CONTEXT]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

- Business Name:     The Bean Pod
- Business Type:     Specialty Coffee Shop + Co-working Hub (Hybrid)
- Location:          Indiranagar, Bangalore, India
- Address:           12th Main Road, Indiranagar, Bangalore 560038
- Target Audience:   Remote workers, tech freelancers, startup founders,
                     and coffee aficionados in Bangalore
- Brand Tone:        Friendly, warm, community-driven, high-energy,
                     and inviting — never corporate or stiff
- USP:               Single-origin Indian beans (Chikmagalur, Coorg) +
                     1 Gbps fiber Wi-Fi + no seat-pressure policy

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[DESIGN SYSTEM]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Use ONLY these design tokens — no other colors:

  --brown:       #4A3525   (Primary — headings, nav logo, buttons)
  --brownMid:    #6B4C32   (Secondary text, hover states)
  --brownLight:  #A0785A   (Accents, SVG fills)
  --cream:       #FDFBF7   (Page background)
  --creamDark:   #F5EFE4   (Section backgrounds, input backgrounds)
  --creamDeep:   #EDE3D2   (Borders, card backgrounds)
  --sage:        #7A9E7E   (Primary accent — CTA buttons, active states)
  --sageDark:    #5B7D5F   (Sage hover states)
  --sageLight:   #C8DEC9   (Sage tints, tags)
  --sagePale:    #EAF3EB   (Sage backgrounds, badges)
  --gold:        #C8923A   (Urgency CTAs, highlights)
  --goldLight:   #F2C97E   (Footer accent text)
  --text:        #2A1E12   (Body text)
  --muted:       #7A6552   (Subtext, descriptions)

Typography:
  - Display / Headings: "Fraunces" (Google Fonts) — 
    serif, high optical contrast, italic variants for emphasis
  - Body / UI:          "Plus Jakarta Sans" (Google Fonts) — 
    clean, modern, geometric sans-serif
  - Import both from Google Fonts in the <head>

Animations required:
  @keyframes fadeUp   — elements enter from below on load
  @keyframes fadeIn   — opacity fade for modals/overlays
  @keyframes scaleIn  — modal pop with spring cubic-bezier
  @keyframes slideDown — mobile menu entrance
  @keyframes float    — continuous up-down loop for hero illustration
  @keyframes shimmer  — SVG steam/glow effect

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[REQUIRED SECTIONS — BUILD ALL 7]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

──────────────────────────────────────────
SECTION 1: STICKY NAVIGATION BAR
──────────────────────────────────────────
- Position: fixed, top:0, full width, z-index:1000
- On scroll > 20px: apply frosted glass effect
  (background: rgba(253,251,247,0.97) + backdrop-filter:blur(12px) 
  + bottom border in creamDeep)
- Left: Logo — "The Bean Pod ☕" in Fraunces font, brown color
- Center: Nav links — Home, Spaces, Menu, Events
  (anchor links to #home, #spaces, #menu, #events)
- Right: CTA button — "Book a Table / Pod"
  (sage background, white text, pill shape, smooth-scrolls to #spaces)
- Mobile (<768px): hide center links, show hamburger (☰) button
- Mobile menu: slides down below nav with all links + CTA button
- Smooth scroll behavior on all anchor links

──────────────────────────────────────────
SECTION 2: HERO SECTION
──────────────────────────────────────────
Layout: Two-column CSS grid (1fr 1fr), 
        centered vertically, min-height: 100vh
Background: linear-gradient(135deg, #FDFBF7 60%, #EAF3EB 100%)

LEFT COLUMN copy (exact text):
  - Pill badge: "Now open · Indiranagar, Bangalore" 
    (sage colored, with animated green dot)
  - H1: "Your Best Work [line break] Starts with a [italic sage] 
    Better Brew." — Fraunces, 900 weight, brown
  - Sub: "A friendly, distraction-free neighborhood workspace for 
    Bangalore's creators, remote tech teams, and coffee aficionados."
  - Primary CTA button: "Instantly Reserve Your Pod →"
    (brown bg, cream text, smooth scroll to #spaces)
  - Secondary CTA button: "See Today's Roasts ☕"
    (ghost style, cream border)
  - Trust micro-copy row below buttons:
    5 overlapping emoji avatar circles + text:
    "Join 500+ Bangalore regulars. Rated ⭐ 4.9 on Google Reviews."

RIGHT COLUMN — Interactive SVG Illustration:
  Build a floating card component (not a stock image) containing:
  - An organic blob shape as background (CSS border-radius trick)
  - A centered SVG coffee cup with steam wisps 
    (use path/ellipse/rect SVG elements, no external images)
  - Two "collaborator" rows showing:
      👩🏽‍💻 "Priya S." | "Design Lead · Deep focus mode" | green online dot
      👨🏻‍💻 "Arjun M." | "Freelance Dev · On a call" | amber busy dot
  - A Wi-Fi status bar: "📶 1 Gbps · No throttle — ✓ Connected"
  - Two floating badges with separate animation delays:
      "☕ Pour-over ready" (brown bg, top-right)
      "⭐ 4.9 · 500+ Reviews" (gold bg, bottom-left)
  - Apply: animation: float 4s ease-in-out infinite to the card

──────────────────────────────────────────
SECTION 3: INTRODUCTORY ATMOSPHERE SECTION
──────────────────────────────────────────
- Full-width section, background: #4A3525 (brown)
- Centered container, max-width: 760px
- Italic heading in goldLight: "Welcome to The Bean Pod."
- Body copy (exact text):
  "We believe you shouldn't have to compromise between world-class 
  specialty espresso and a highly productive workspace. We source our 
  single-origin beans directly from sustainable estates in Chikmagalur 
  and provide seamless 1 Gbps Wi-Fi so you can power through your day 
  without the typical cafe chaos."
  (Highlight "Chikmagalur" and "1 Gbps Wi-Fi" in goldLight bold)
- Stats strip below copy (flex row, centered, 4 items):
    2,400+ · Members / mo
    50+     · Events hosted
    12+     · Single origins
    1 Gbps  · Fiber Wi-Fi

──────────────────────────────────────────
SECTION 4: FULLY FUNCTIONAL BOOKING ENGINE ← MOST IMPORTANT
──────────────────────────────────────────
Background: #F5EFE4
Two-column card layout (white card, rounded-24, box-shadow)

LEFT PANEL — Step 1 & Step 4:

  STEP 1 — Spot Type Selector (3 toggle buttons, only one active):
    - "Espresso Bar Seat" ☕  desc: "Perfect for solo work, quick meetings"
    - "Quiet Focus Pod"   🎧  desc: "Enclosed, silent, deep-work ready"
    - "Team Meeting Table" 👥 desc: "Seats 4–6, whiteboard included"
    Active state: sage border, sagePale background, ✓ check badge appears
    Default selected: "Quiet Focus Pod"

  STEP 4 — User Details:
    - Text input: "Your full name" (required)
    - Email input: "your@email.com" (required, regex validated)
    - Inputs: creamDark bg, sage focus ring, red border on error

RIGHT PANEL — Step 2 & Step 3:

  STEP 2 — Fully Functional Date Picker Calendar:
    Requirements:
    - Shows current month by default
    - Left/right arrow buttons to navigate months
    - 7-column day grid (Su Mo Tu We Th Fr Sa)
    - Past dates: disabled, greyed out (#EDE3D2 text), not-allowed cursor
    - Today's date: highlighted with sageLight background
    - Selected date: brown background, white text
    - No external date-picker library — build from scratch in JS:
        getDaysInMonth(year, month)
        getFirstDay(year, month)  
        Build cells array with leading nulls for offset
    - Re-render calendar on month navigation and date selection

  STEP 3 — Time Slot Grid (4-column grid):
    Time slots: 9:00 AM, 10:00 AM, 11:00 AM, 12:00 PM,
                1:00 PM, 2:00 PM, 3:00 PM, 4:00 PM,
                5:00 PM, 6:00 PM, 7:00 PM, 8:00 PM
    Active state: sage border + sagePale bg + sageDark text + bold
    Default: no time selected

  CONFIRM BUTTON:
    - Full width, sage background, white text
    - Text: "Confirm Booking ✓"
    - On click — run validate():
        If name empty → show error "Name is required"
        If email invalid → show error "Valid email required"
        If no date selected → show inline error in step 2 label
        If no time selected → show inline error in step 3 label
        If ALL valid → open Success Modal

  SUCCESS MODAL (full-screen overlay):
    - Overlay: rgba(42,30,18,0.6), fixed, z-index:2000
    - Modal box: white, border-radius:24, max-width:440px
    - Animation: scaleIn with spring cubic-bezier(.34,1.56,.64,1)
    - ☕ icon in sage circle
    - Personalised heading: "You're all set, [First Name]!"
    - Body: "Your spot at The Bean Pod is locked in! We'll have 
      your first pour-over ready when you arrive."
    - Booking summary card showing:
        SPOT: [selected spot name]
        DATE: [formatted: e.g. "Thu, 5 Jun"]
        TIME: [selected time slot]
    - Close button: "Done — See you soon! 👋" (brown bg)
    - Clicking overlay also closes modal
    - On close: reset ALL booking state, re-render calendar + time grid

──────────────────────────────────────────
SECTION 5: SERVICES — 3-COLUMN GRID
──────────────────────────────────────────
3 equal cards with hover lift effect (translateY(-6px) + box-shadow)

CARD 1 — "Artisan Brews & Bites" ☕
  Header bg: #EDE3D2
  Tagline: "Roasted weekly, dialled fresh daily. No stale beans."
  Features:
    - Single-origin pour-overs from Chikmagalur & Coorg
    - Cold brew on tap — 18-hour steep
    - Seasonal espresso blends dialled daily
    - Fresh sourdough toasts & overnight oats
    - Cashew & oat milk on house
  Why Us (gold accent box):
    "Every batch arrives within the week. If extraction is off, 
    we pull it again. No heat-lamp shots here."

CARD 2 — "Productivity Infrastructure" 💻
  Header bg: #EAF3EB
  Tagline: "No pressure to keep buying drinks just to save your seat."
  Features:
    - Symmetrical 1 Gbps fiber — zero throttling
    - Power outlet at every single seat
    - Ergonomic chairs, standing desk options
    - Private call booths & focus pods
    - Climate-controlled zones
  Why Us (sage accent box):
    "We manage seating density so you always have room. 
    Your seat is yours for as long as you need it."

CARD 3 — "Community Mixers" 🎙️
  Header bg: #F5EFE4
  Tagline: "Connect with Bangalore's brightest minds organically."
  Features:
    - Weekly open-mic evenings — no signup needed
    - Weekend live acoustic brunch sessions
    - 'Build in Public' startup huddles monthly
    - Coffee tasting workshops with roastery partners
    - Private hire for offsites — up to 60 guests
  Why Us (brown accent box):
    "No forced networking. No speed rounds. Just good people 
    in a good space, doing good work."

──────────────────────────────────────────
SECTION 6: EVENTS / COMMUNITY CALENDAR
──────────────────────────────────────────
Background: #F5EFE4
3-column event card grid with hover lift

EVENT 1: "Open Mic Evenings"
  Date: Every Wed | Time: 7:00 PM | Tag: Weekly
  Desc: "Poetry, pitches, performances — all welcome. No signup, just show up."

EVENT 2: "Live Acoustic Brunch"
  Date: Every Sat | Time: 11:00 AM | Tag: Weekend
  Desc: "Local artists, weekend vibes, and the best brunch plates in Indiranagar."

EVENT 3: "Build in Public"
  Date: 1st Fri / mo | Time: 6:30 PM | Tag: Monthly
  Desc: "Bangalore's indie hackers share live — what they're building, breaking, and learning."

──────────────────────────────────────────
SECTION 7: FOOTER — LOCATION + URGENCY CTA
──────────────────────────────────────────
Full-width, background: #4A3525 (brown)
Two-column grid inside

LEFT — Location / Map Card:
  - Section label: "Find Us" in goldLight
  - Card with:
    - Map visual area (sage toned bg, 180px tall) containing:
        SVG pin icon (circle + dot + line + ellipse shadow)
        Text: "Indiranagar, Bangalore"
        Badge top-right: "📍 Live Map"
    - Info below map:
        Street: "12th Main Road, Indiranagar" (Fraunces, cream)
        City: "Bangalore, Karnataka 560038"
        Tags row: "🚇 5 Mins from Metro" (sage pill) + "Street parking ✓"
        Hours: "Mon–Fri 7AM–11PM · Sat–Sun 8AM–Midnight"

RIGHT — Urgency CTA Panel:
  Background: rgba(200,146,58,0.12) with gold border
  Content:
    ⚡ icon
    Heading: "Beating the afternoon slump?"
    Body: "Walk in today, show your work ID, and get 10% off your 
    first Nitro Cold Brew. No booking required — just turn up and 
    tell us you're here to get things done."
    Button: "Reserve My Table Now →" (gold bg, smooth scroll to #spaces)
    Trust line: "⭐ 4.9 · Rated Bangalore's #1 freelancer café"

Bottom bar (border-top, flex row):
  Left: "The Bean Pod ☕" in Fraunces
  Right: "© 2025 The Bean Pod · Indiranagar, Bangalore · hello@thebeanpod.in"

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[JAVASCRIPT REQUIREMENTS]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

All JS must be vanilla, inline in a single <script> tag at bottom of body.

Required state variables:
  let calYear, calMonth, selDate, selTime, selSpot

Required functions:
  renderCalendar()  — builds calendar grid dynamically from state
  renderTimeGrid()  — builds time slot buttons dynamically
  prevMonth()       — decrement month, wrap Dec→Jan, re-render calendar
  nextMonth()       — increment month, wrap Jan→Dec, re-render calendar
  selectSpot(id)    — updates selSpot, repaints all 3 spot buttons
  validate()        — checks all 4 fields, shows inline errors, returns bool
  confirmBooking()  — runs validate(), if pass: populates + opens modal
  resetBooking()    — clears all state, closes modal, re-renders booking UI
  closeModal(e)     — closes if clicking the overlay (not the modal box)
  scrollToBooking() — smooth scrolls to #spaces
  toggleMenu()      — shows/hides mobile nav menu
  closeMobileMenu() — hides mobile nav menu

Scroll handler:
  window.addEventListener('scroll', () => {
    nav.classList.toggle('scrolled', window.scrollY > 20)
  })

Calendar logic:
  getDaysInMonth = (y, m) => new Date(y, m+1, 0).getDate()
  getFirstDay    = (y, m) => new Date(y, m, 1).getDay()
  Past dates: create Date at midnight, compare to today midnight
  Today highlight: check d === today.getDate() && same month/year
  Selected highlight: check selDate matches d, calMonth, calYear
  Re-render fully on every month change or date click

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[RESPONSIVENESS REQUIREMENTS]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Breakpoint: 768px for 2-col → 1-col
Breakpoint: 900px for 3-col → 1-col grids

Mobile-specific changes:
  - Nav: hide .nav-links, show .hamburger button
  - Hero: stack columns (hero illustration below copy)
  - Booking: stack left and right panels vertically,
    replace right border with bottom border
  - Services + Events: 1 column
  - Footer grid: 1 column

Use: clamp(1.25rem, 4vw, 3rem) for horizontal section padding
Use: clamp() for font-sizes where readability matters at small screens

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[OUTPUT REQUIREMENTS]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Deliver ONE complete .html file containing:
  ✓ <!DOCTYPE html> declaration
  ✓ All CSS in a single <style> tag in <head>
  ✓ Google Fonts import at top of <style>
  ✓ All HTML sections in <body>
  ✓ All JavaScript in a single <script> tag before </body>
  ✓ No external JS libraries, CDN links, or npm packages
  ✓ No placeholder text — all copy must match spec exactly
  ✓ Opens and works perfectly in Chrome/Firefox/Safari with no server
  ✓ All interactive features functional (booking, calendar, modal, nav)
  ✓ All 7 sections present and complete
