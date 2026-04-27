---
name: Adam Szilagyi Video Production Portfolio
description: A static dark portfolio system extracted from styles.css for showcasing video production work.
colors:
  page-ink: "#0f0f0f"
  header-ink: "#1a1a1a"
  rule-ink: "#222222"
  button-graphite: "#444444"
  button-hover-graphite: "#666666"
  button-hover-deep: "#333333"
  skill-fill: "#555555"
  text-white: "#ffffff"
  text-body: "#cfcfcf"
  text-soft: "#cccccc"
  text-muted: "#aaaaaa"
  tag-text: "#dddddd"
  nav-wash: "#ffffff0f"
  nav-wash-hover: "#ffffff26"
  border-faint: "#ffffff14"
  border-soft: "#ffffff1a"
  border-focus: "#ffffff4d"
  field-wash: "#ffffff0d"
  footer-wash: "#141414cc"
  tag-wash: "#55555599"
  tag-wash-hover: "#555555e6"
typography:
  display:
    fontFamily: "Arial, sans-serif"
    fontSize: "32px"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: "normal"
  headline:
    fontFamily: "Arial, sans-serif"
    fontSize: "28px"
    fontWeight: 700
    lineHeight: 1.25
    letterSpacing: "normal"
  title:
    fontFamily: "Arial, sans-serif"
    fontSize: "22px"
    fontWeight: 700
    lineHeight: 1.25
    letterSpacing: "normal"
  body:
    fontFamily: "Arial, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: "normal"
  label:
    fontFamily: "Arial, sans-serif"
    fontSize: "12px"
    fontWeight: 500
    lineHeight: 1.2
    letterSpacing: "normal"
rounded:
  xs: "5px"
  md: "8px"
  lg: "10px"
  xl: "12px"
  pill: "16px"
  round: "50%"
spacing:
  tag-y: "4px"
  tag-x: "10px"
  form-gap: "12px"
  nav-y: "10px"
  nav-x: "14px"
  button-y: "10px"
  button-x: "16px"
  mobile-gutter: "20px"
  page-gutter: "40px"
  section-y: "60px"
  portfolio-y: "80px"
components:
  button-primary:
    backgroundColor: "{colors.button-graphite}"
    textColor: "{colors.text-white}"
    rounded: "{rounded.md}"
    padding: "10px 16px"
  button-primary-hover:
    backgroundColor: "{colors.button-hover-graphite}"
    textColor: "{colors.text-white}"
    rounded: "{rounded.md}"
    padding: "10px 16px"
  nav-link:
    backgroundColor: "{colors.nav-wash}"
    textColor: "{colors.text-white}"
    rounded: "{rounded.md}"
    padding: "10px 14px"
  tag:
    backgroundColor: "{colors.tag-wash}"
    textColor: "{colors.tag-text}"
    rounded: "{rounded.pill}"
    padding: "4px 10px"
  input:
    backgroundColor: "{colors.field-wash}"
    textColor: "{colors.text-white}"
    rounded: "{rounded.md}"
    padding: "12px"
---

# Design System: Adam Szilagyi Video Production Portfolio

## 1. Overview

**Creative North Star: "The Quiet Screening Room"**

This design system is extracted from `styles.css`. The site uses a restrained dark environment, simple Arial typography, direct sectioning, and media-first presentation so Adam's video thumbnails, titles, descriptions, tags, CV, and contact form stay easy to scan.

The physical scene: a reviewer opens the portfolio on a laptop or phone, likely between other applications, and needs to sample a young video creator's range without visual noise. The dark theme works because it behaves like a viewing room around the work, not because the category demands a dark portfolio.

The current CSS has no custom properties or external framework. Its system lives in repeated values: dark neutral surfaces, soft gray text, 8px controls, rounded media, image shadows, compact tags, scroll fade-ins, and one mobile breakpoint at 768px.

**Key Characteristics:**
- Static HTML and CSS, no component framework.
- Restrained dark palette with thumbnail imagery carrying most of the color.
- Direct, compact navigation with sticky access to portfolio categories and CV.
- Media rows and video rows as the primary content structures.
- Lightweight hover and scroll motion around a simple layout.

## 2. Colors

The palette is a graphite dark system. It relies on near-black backgrounds, white and gray text, translucent white borders, and muted graphite controls.

### Primary
- **Button Graphite** (#444444): The leading color in the button gradient and the main action tone.
- **Button Hover Graphite** (#666666): The brighter hover endpoint for buttons.
- **Skill Fill Graphite** (#555555): Skill bars and tag washes use this middle gray to show capability without becoming colorful.

### Neutral
- **Page Ink** (#0f0f0f): Body background.
- **Header Ink** (#1a1a1a): Sticky header background.
- **Rule Ink** (#222222): Section dividers, skill bar tracks, and button gradient depth.
- **Button Hover Deep** (#333333): Secondary endpoint in the hover gradient.
- **Text White** (#ffffff): Current CSS text color for body, title, links, buttons, fields, and hover states.
- **Text Body** (#cfcfcf): About and portfolio-row paragraph text.
- **Text Soft** (#cccccc): Social links, skill labels, and video descriptions.
- **Text Muted** (#aaaaaa): Footer and category page descriptions.
- **Tag Text** (#dddddd): Tag labels.
- **Footer Wash** (#141414cc): Footer background, equivalent to `rgba(20, 20, 20, 0.8)`.

### Transparency Tokens
- **Nav Wash** (#ffffff0f): Navigation link background, equivalent to `rgba(255, 255, 255, 0.06)`.
- **Nav Wash Hover** (#ffffff26): Navigation link hover background, equivalent to `rgba(255, 255, 255, 0.15)`.
- **Border Faint** (#ffffff14): Navigation and footer borders, equivalent to `rgba(255, 255, 255, 0.08)`.
- **Border Soft** (#ffffff1a): Inputs and tags, equivalent to `rgba(255, 255, 255, 0.1)`.
- **Border Focus** (#ffffff4d): Input focus and tag hover borders, equivalent to `rgba(255, 255, 255, 0.3)`.
- **Field Wash** (#ffffff0d): Input and textarea background, equivalent to `rgba(255, 255, 255, 0.05)`.
- **Tag Wash** (#55555599): Tag background, equivalent to `rgba(85, 85, 85, 0.6)`.
- **Tag Wash Hover** (#555555e6): Tag hover background, equivalent to `rgba(85, 85, 85, 0.9)`.

### Named Rules

**The Thumbnail Color Rule.** The UI stays mostly neutral because the project thumbnails supply the color. Add color only when it makes category, state, or authorship clearer.

**The Future Tint Rule.** The current CSS uses raw white values. If the CSS is revised later, prefer a slightly warm near-white instead of raw white.

## 3. Typography

**Display Font:** Arial, sans-serif
**Body Font:** Arial, sans-serif
**Label/Mono Font:** Arial, sans-serif

**Character:** The type is plain, system-like, and fast to read. It should remain direct, but hierarchy needs to stay crisp because the portfolio depends on quick scanning.

### Hierarchy
- **Display** (700, 32px, 1.2): `.page-title` on category pages.
- **Headline** (700, 28px, 1.25): `.about h2` and major section headings on desktop.
- **Title** (700, 22px, 1.25): `.desc h3` category row headings.
- **Brand Title** (700, 20px desktop, 18px mobile): `.title` in the sticky header.
- **Body** (400, 16px, 1.6): About text, row descriptions, video text, and form content.
- **Video Title** (700, 16px desktop, 14px mobile): `.video-title`, with fixed minimum height for stable rows.
- **Label** (500, 12px desktop, 11px mobile): `.tag` metadata chips.
- **Footer Utility** (400, 12px): Footer text and links.

### Named Rules

**The Scan First Rule.** Keep body copy readable at 16px on desktop and avoid line lengths beyond 75ch. If a row feels dense, shorten the copy before shrinking the text.

## 4. Elevation

The system uses a hybrid of tonal layering and media shadows. Page sections stay flat, while portraits, certificates, category previews, video thumbnails, nav hovers, and button hovers receive depth.

### Shadow Vocabulary
- **Nav Hover Shadow** (`0 6px 20px rgba(0, 0, 0, 0.4)`): Hover state for sticky header links.
- **Portrait Shadow** (`0 10px 30px rgba(0, 0, 0, 0.5)`): `.about img`.
- **Certificate Drop Shadow** (`drop-shadow(0 10px 15px rgba(0, 0, 0, 0.4))`): `.cert`.
- **Portfolio Preview Shadow** (`0 10px 30px rgba(0, 0, 0, 0.6)`): `.row img`.
- **Button Hover Shadow** (`0 8px 25px rgba(0, 0, 0, 0.4)`): `button:hover`.
- **Video Thumbnail Shadow** (`0 6px 20px rgba(0, 0, 0, 0.4)`): `.video-card img`.

### Named Rules

**The Media Owns Depth Rule.** Shadows should mostly belong to images and active controls. Avoid adding floating cards around text blocks.

## 5. Components

### Buttons
- **Shape:** 8px radius.
- **Primary:** `linear-gradient(135deg, #444, #222)`, white text, no border, 10px 16px padding, pointer cursor.
- **Hover / Focus:** Hover translates up by 2px, changes to `linear-gradient(135deg, #666, #333)`, and adds `0 8px 25px rgba(0, 0, 0, 0.4)`.
- **Mobile:** 8px 12px padding, 14px text.

### Chips
- **Style:** Inline-block pill tags with 16px radius, 4px 10px padding, 12px 500-weight text, graphite translucent background, and a soft white border.
- **State:** Hover increases background opacity and border contrast.
- **Mobile:** 3px 8px padding, 11px text.

### Cards / Containers
- **Corner Style:** Thumbnails use 10px to 12px radius. Headshot and certificate assets are circular.
- **Background:** Main sections sit directly on #0f0f0f with top borders.
- **Shadow Strategy:** Images and hoverable media receive shadows. Text containers remain flat.
- **Border:** Section rhythm uses 1px top borders in #222 or translucent white.
- **Internal Padding:** Major sections use 40px to 80px vertical padding on desktop and 20px to 40px on mobile.

### Inputs / Fields
- **Style:** 12px padding, 8px radius, 1px translucent white border, translucent white background, white text, Arial font.
- **Focus:** Border shifts to `rgba(255, 255, 255, 0.3)`.
- **Error / Disabled:** Not defined in the current CSS.

### Navigation

The sticky header uses flex layout, 20px 40px padding, #1a1a1a background, and a z-index of 1000. The title is bold 20px text with a slight scale and opacity hover. Navigation links are compact 8px-radius ghost buttons with translucent backgrounds, soft borders, and a 2px hover lift. On mobile the header stacks into a centered column with 15px 20px padding and smaller links.

### Portfolio Rows

`.row` pairs a 340px by 200px preview image with a descriptive block. Desktop rows use 80px 60px padding, a max width of 1100px, and a large 200px gap. Images scale to 1.03 on hover. On mobile, rows stack vertically, center their content, reduce padding to 40px 20px, and constrain images to 300px.

### Video Rows

`.video-row` uses a 280px video card beside flexible text content. Thumbnails are 280px by 160px with 10px radius. `.video-card:hover img` scales the thumbnail to 1.08. On mobile, cards expand to full width with a 300px max, and video text drops to 14px.

### Skills

Skill rows are simple progress bars. The track is #222 with a 5px radius and 10px height; the fill is #555. The section uses 40px 180px desktop padding and 30px 20px mobile padding.

### Motion

Fade-in sections start at opacity 0 and translate down 20px, then transition to visible over 0.8s. Hover motion is short, between 0.2s and 0.3s, and uses transform, opacity, background, shadow, or color.

## 6. Do's and Don'ts

### Do:
- **Do** preserve the dark viewing-room surface: #0f0f0f body, #1a1a1a header, and #222 dividers.
- **Do** keep portfolio thumbnails, video titles, and project descriptions visually stronger than decorative interface elements.
- **Do** use 8px radii for controls, 10px to 12px radii for media, and circular treatment only for portraits or certification marks.
- **Do** keep navigation compact, sticky, and obvious across all pages.
- **Do** add visible keyboard focus and reduced-motion support when updating the CSS.
- **Do** treat the 768px breakpoint as the current mobile system boundary.

### Don't:
- **Don't** make the site feel like a generic dark portfolio template.
- **Don't** add neon creator aesthetics, heavy glassmorphism, purple-blue gradients, or overproduced agency effects.
- **Don't** use side-stripe borders, gradient text, or repeated identical icon-card grids.
- **Don't** wrap every section in a card. The sections currently work as open bands with media as the framed objects.
- **Don't** animate layout properties or make hover movement larger than the current 2px lift and subtle image scale.
- **Don't** let effects compete with the actual videos.
