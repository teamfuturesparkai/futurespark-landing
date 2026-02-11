# FutureSpark AI — Landing Page Build Specification
## For Claude Code — Build this EXACTLY as specified

---

## PROJECT OVERVIEW

Build a single-page, fully responsive landing page for **FutureSpark AI** — an education company that teaches kids and families to BUILD with AI, not just learn about it. Founded by Jessica, a former K-12 teacher and mom.

- **Domain:** futuresparkai.org
- **Stack:** Single HTML file with embedded CSS and inline JavaScript. No frameworks, no build tools. Just one clean `index.html` file.
- **Fonts:** Google Fonts — Poppins (headings) + Inter (body)
- **Icons:** Use inline SVGs or simple unicode/emoji icons. No external icon libraries needed.
- **Mobile-first:** Must look great on phones. Parents browse on mobile.

---

## COLOR PALETTE — "Warm Earth + Spark"

Use CSS custom properties for all colors:

```css
:root {
  --deep-navy: #1A1A2E;
  --forest-green: #2D6A4F;
  --warm-coral: #E07A5F;
  --warm-gold: #D4A537;
  --teal: #3D8487;
  --warm-cream: #FAF3E8;
  --soft-white: #FFFFFF;
  --light-sage: #E8F0E8;
  --body-text: #333333;
  --light-gray: #F5F5F5;
}
```

- **Page background:** `--warm-cream`
- **Text:** `--deep-navy` for headings, `--body-text` for paragraphs
- **Primary buttons/CTAs:** `--forest-green` background with white text, hover: darken 10%
- **Accent highlights:** `--warm-coral`
- **Secondary accents:** `--teal`, `--warm-gold`
- **Card backgrounds:** `--soft-white`
- **Alternating sections:** Alternate between `--warm-cream` and `--soft-white` backgrounds

---

## TYPOGRAPHY

```css
h1, h2, h3, h4 { font-family: 'Poppins', sans-serif; }
body, p, li, a { font-family: 'Inter', sans-serif; }

/* Sizes */
h1 { font-size: clamp(2.2rem, 5vw, 3.5rem); font-weight: 700; }
h2 { font-size: clamp(1.6rem, 3.5vw, 2.2rem); font-weight: 600; }
h3 { font-size: clamp(1.2rem, 2.5vw, 1.5rem); font-weight: 600; }
body { font-size: 1.05rem; line-height: 1.7; }
```

---

## PAGE SECTIONS (Build in this exact order)

---

### SECTION 1: Navigation Bar

- **Left:** Brand name "FutureSpark AI" styled as a text logo. Use Poppins bold. Add a small sparkle/star character (use ✦ or ✧) in `--warm-gold` color before or after the name.
- **Right:** Nav links — "About" | "Programs" | "FAQ" | "Contact" — plus a CTA button "Get Free Guide" in `--forest-green`
- **Behavior:** Sticky on scroll. Starts with transparent background, fills with `--soft-white` + subtle shadow on scroll. Smooth transition.
- **Mobile:** Hamburger menu icon. Tapping opens a clean slide-down or overlay menu with all links.

---

### SECTION 2: Hero Section

**Background:** `--warm-cream` with subtle decorative elements (optional: small sparkle dots or a soft gradient)

**Headline:**
```
A Teacher-Built Program Where Kids Don't Just Learn About AI — They Build With It
```
- Style: `--deep-navy`, Poppins, bold
- The words "Build With It" should be in `--warm-coral` for emphasis

**Subheadline:**
```
Hands-on AI courses for kids grades K–12 — designed by a former classroom teacher and mom who believes every family deserves to understand the technology shaping their future.
```
- Style: `--body-text`, Inter, regular, max-width ~700px, centered

**Primary CTA Button:**
```
Download Your Free AI Starter Guide →
```
- Style: Large, `--forest-green` background, white text, rounded corners (8px), padding 16px 32px, subtle hover animation (lift + shadow)

**Secondary CTA (text link below button):**
```
Join the waitlist for upcoming workshops
```
- Style: `--teal` color, underline on hover, smaller text

**Layout:** Centered text, generous whitespace. Optional: subtle background illustration or sparkle decorations that feel warm, not techy.

---

### SECTION 3: "Why This Matters Now" (The Problem)

**Background:** `--soft-white`

**Section Headline:**
```
AI Is Already Here. Is Your Family Ready?
```
- Style: `--deep-navy`, centered

**Three cards in a row (stack on mobile):**

**Card 1 — "The Reality"**
```
AI is transforming every industry, and your kids will work alongside it — whether they're ready or not. Schools are scrambling to figure out policies, but most aren't teaching kids to actually use AI.
```
- Icon suggestion: a simple globe or lightning bolt icon in `--warm-coral`

**Card 2 — "The Gap"**
```
There's endless information about AI online, but almost nothing designed to help families learn together. Parents feel overwhelmed. Kids are curious but unsupervised. The gap is growing every day.
```
- Icon suggestion: a puzzle piece or gap icon in `--teal`

**Card 3 — "The Opportunity"**
```
Kids who learn to build with AI now won't just be prepared for the future — they'll be creating it. FutureSpark AI bridges the gap with hands-on, age-appropriate programs led by a real teacher who gets it.
```
- Icon suggestion: a rocket or sparkle icon in `--warm-gold`

**Card styling:** `--soft-white` or `--light-sage` background, subtle border or shadow, rounded corners, padding, icon at top.

---

### SECTION 4: Programs — Three Learning Tracks

**Background:** `--warm-cream`

**Section Headline:**
```
Three Tracks. Every Age. Real Skills.
```

**Three program cards (equal width, stack on mobile):**

**Track 1 — AI Explorers**
- Badge/label: "Ages 5–10 · Grades K–5"
- Tagline: "Discovery & Wonder"
- Description: "Young learners explore what AI is through play, stories, and hands-on activities. They learn to ask great questions and think critically about the technology around them."
- Topics: "What is AI? · Fun AI experiments · Creative projects with kid-friendly tools · Thinking like an inventor"
- Card accent color: `--warm-gold`

**Track 2 — AI Creators**
- Badge/label: "Ages 10–14 · Grades 6–8"
- Tagline: "Hands-On Building"
- Description: "Middle schoolers go beyond understanding into creating. They use real AI tools to build projects, solve problems, and express themselves — while learning responsible use."
- Topics: "Build real projects · Prompt engineering · Ethics and digital citizenship · Team challenges and hackathons"
- Card accent color: `--warm-coral`

**Track 3 — AI Futures**
- Badge/label: "Ages 14–18 · Grades 9–12"
- Tagline: "Ethics, Careers & Advanced Projects"
- Description: "High schoolers dive deep into how AI is reshaping industries, careers, and society. They build portfolio-worthy projects and develop the critical thinking skills employers want."
- Topics: "Advanced AI projects · Career exploration · Bias, fairness, and societal impact · Portfolio building"
- Card accent color: `--teal`

**CTA below cards:**
```
Not sure which track? Download our free guide to find the right fit for your family.
```
(Links to the same email capture / guide download)

**Card styling:** White background, top border or left border in the track's accent color, rounded corners, generous padding, subtle shadow on hover.

---

### SECTION 5: Our Approach — The Four Pillars

**Background:** `--soft-white`

**Section Headline:**
```
Every Program. Four Pillars. One Mission.
```

**Four pillars displayed as icon + title + description (2x2 grid on desktop, stack on mobile):**

**Pillar 1 — AI Literacy**
- Icon: 💡 or a lightbulb SVG in `--warm-gold`
- Description: "Understanding what AI is, how it works, and what it can (and can't) do."

**Pillar 2 — Hands-On Building**
- Icon: 🛠️ or a tools SVG in `--warm-coral`
- Description: "Creating real things with real AI tools — not just watching videos."

**Pillar 3 — Ethics & Critical Thinking**
- Icon: 🛡️ or a shield SVG in `--teal`
- Description: "Responsible use, recognizing bias, protecting privacy, thinking deeply."

**Pillar 4 — Future Readiness**
- Icon: 🚀 or a rocket SVG in `--forest-green`
- Description: "Career awareness, adaptability, and the confidence to thrive in an AI-shaped world."

**Styling:** Clean, minimal. Each pillar is a centered card with icon on top, bold title, short description. Subtle background or no background — clean and confident.

---

### SECTION 6: Meet the Founder

**Background:** `--warm-cream`

**Section Headline:**
```
Hi, I'm Jessica — Teacher, Mom, and Your Family's AI Guide
```

**Layout:** Two columns on desktop (photo left, text right). Single column stacked on mobile.

**Photo area:** A placeholder circle or rounded rectangle with text "Photo Coming Soon" and a subtle background color. Style: 280px x 280px, rounded, `--light-sage` background.

**Bio text (THIS IS THE EXACT COPY TO USE):**

```
I've spent my career in classrooms — from teaching high school math as an English major (talk about learning on the fly!) to coaching students through learning gaps, teaching life skills to third and fourth graders, and spending two wonderful years as a kindergarten teacher.

I've worked with every age group from ages 5 to 18, and I've seen firsthand how kids learn best: by doing.

When I moved into school administration and then into the world of AI technology, something clicked. I saw how powerful these tools are — and how few resources exist to help families navigate them together.

As a mom, I felt the same overwhelm every parent feels: AI is everywhere, it's moving fast, and nobody is giving us a roadmap.

So I built one.

FutureSpark AI isn't just another tech company teaching kids to code. It's a teacher-built, family-centered program where kids learn to create with AI — ethically, confidently, and with the guidance of someone who has spent years learning how children actually learn.

I'm still learning too. Every day. And I believe that's exactly the point. The families who start learning now — together — are the ones who will thrive.
```

**Important:** The line "So I built one." should be visually distinct — larger font, `--warm-coral` color, italic or bold italic. It's the emotional punch of the story.

---

### SECTION 7: Social Proof / Stats

**Background:** `--light-sage`

**Section Headline:**
```
What Families Are Saying
```

**Content:** Since this is pre-launch, show 3 cards with a note:
```
Our first cohort launches soon — check back for stories from real families!
```

**Alternatively, use 3 stat/fact cards:**
- Card 1: "K–12" / "Grade levels covered across three learning tracks"
- Card 2: "4 Pillars" / "Every program built on AI Literacy, Building, Ethics, and Future Readiness"
- Card 3: "100%" / "Hands-on — every student builds real projects, not just takes notes"

**Styling:** Cards with large stat number in `--warm-coral` or `--forest-green`, description text below. Clean and impactful.

---

### SECTION 8: FAQ Section

**Background:** `--soft-white`

**Section Headline:**
```
Questions? We've Got Answers.
```

**Accordion-style FAQ (click question to expand/collapse answer). JavaScript required.**

**Q1: Does my child need to know how to code?**
A: Not at all! Our programs are designed for complete beginners. We meet kids where they are and build from there. The goal is creative exploration with AI, not coding boot camp.

**Q2: Is this safe for kids? What about AI ethics?**
A: Safety and ethics are baked into everything we do — it's one of our four core pillars. We teach kids to think critically about AI, understand bias, protect their privacy, and use these tools responsibly.

**Q3: What age is this appropriate for?**
A: We have three tracks designed for different developmental stages: AI Explorers (ages 5–10), AI Creators (ages 10–14), and AI Futures (ages 14–18). There's a right fit for every kid.

**Q4: What makes this different from other AI programs?**
A: Most programs teach kids ABOUT AI as a concept. We teach kids to BUILD with AI as a creative tool. Plus, our founder is a former K-12 teacher — not a tech company. That means everything is designed around how kids actually learn.

**Q5: Can parents participate too?**
A: Absolutely! We believe AI literacy is a family journey. We offer parent workshops and our programs are designed so families can explore and create together.

**Q6: What does "hands-on" actually mean?**
A: It means your child will use real AI tools to create real projects — things like building a story with AI illustrations, creating a chatbot, or designing an app concept. They walk away with something they made, not just notes from a lecture.

**Q7: How much does it cost?**
A: We offer free introductory resources (like our AI Starter Guide) and free workshops to help families get started. Paid courses and Hack Week events are coming soon — join the waitlist to get early access and founding family pricing.

**FAQ styling:** Clean accordion. Question text in `--deep-navy`, bold. Plus/minus or chevron icon to indicate expand/collapse. Answer text in `--body-text`. Subtle divider between items. Smooth expand animation.

---

### SECTION 9: Final CTA + Footer

**CTA Block Background:** `--forest-green` (full-width dark section for contrast and urgency)

**CTA Headline (white text):**
```
Your Family's AI Journey Starts Here
```

**CTA Subtext (white/light text):**
```
Download our free AI Starter Guide for Families — and be the first to know when workshops and courses launch.
```

**Email form:** Inline form with email input field + "Get My Free Guide" button. Button color: `--warm-coral` with white text. Input has white background, rounded corners. The form should have `action="#"` placeholder (will connect to Kit/ConvertKit later).

**Footer (below CTA, darker background or same `--deep-navy`):**

- Left: "© 2026 FutureSpark AI. All rights reserved."
- Center or right: Social icons linking to:
  - YouTube: https://youtube.com/@futuresparkai
  - TikTok: https://tiktok.com/@futuresparkai
  - LinkedIn: (placeholder #)
- Email: futuresparkai@gmail.com
- Links: Privacy Policy | Terms of Service (both link to # as placeholders)

---

## GLOBAL DESIGN REQUIREMENTS

1. **Smooth scroll:** All nav links scroll smoothly to their sections
2. **Scroll animations:** Subtle fade-in-up animations as sections enter the viewport (use IntersectionObserver, no libraries)
3. **Responsive breakpoints:** Mobile (<768px), Tablet (768-1024px), Desktop (>1024px)
4. **Max content width:** 1200px centered, with padding on sides
5. **Section padding:** Generous vertical padding (80-100px top/bottom on desktop, 50-60px on mobile)
6. **Button hover effects:** Slight lift (transform: translateY(-2px)) + shadow increase
7. **Accessibility:** Proper heading hierarchy (single H1), alt text on images, focus states on interactive elements, sufficient color contrast
8. **SEO meta tags in head:**
   - Title: "FutureSpark AI — Kids Learn to Build with AI | Free Resources for Families"
   - Meta description: "Teacher-built AI programs for kids K-12. Hands-on courses, family workshops, and free resources. Start your family's AI journey today."
   - Open Graph tags for social sharing (og:title, og:description, og:image placeholder, og:url)
   - Twitter Card tags
9. **Favicon:** Use a sparkle emoji ✦ as favicon (or create a simple SVG favicon)
10. **Performance:** Minimal CSS, no external libraries, optimized for fast loading

---

## IMPORTANT NOTES

- Build everything in a SINGLE `index.html` file with embedded `<style>` and `<script>` tags
- Do NOT use any frameworks (no React, no Tailwind, no Bootstrap)
- Do NOT use any external JavaScript libraries
- The email form should collect submissions but just show a "Thank you!" message for now (we'll connect Kit/ConvertKit later)
- Use semantic HTML5 elements (header, nav, main, section, footer)
- Make the design feel WARM, APPROACHABLE, and TRUSTWORTHY — not cold, techy, or corporate
- The overall vibe should make a parent think "This feels safe and credible" and make a kid think "This looks fun"
