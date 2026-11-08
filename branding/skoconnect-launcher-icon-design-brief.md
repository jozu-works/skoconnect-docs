# SkoConnect — App Launcher Icon Design Brief

## Project Overview

**App Name:** SkoConnect  
**Platform:** Android (primary), iOS (future)  
**Category:** EdTech / School Communication  
**Target Users:** Parents, teachers, school administrators  
**Region:** Caribbean / Jamaica launch, global potential  

SkoConnect is a school communication platform that connects schools, teachers, and parents in one place — notices, events, forms, routines, emergency alerts, and messaging. The icon needs to immediately communicate **school + connection + trust** at a glance on a crowded home screen.

---

## Brand Identity

### Brand Colors (from app theme)

| Token | Hex | Usage |
|-------|-----|-------|
| Teal 500 (Primary) | `#14B8A6` | Main brand color |
| Teal 600 | `#0D9488` | Primary buttons, headers |
| Teal 700 | `#0F766E` | Darker accent |
| Teal 900 | `#044E48` | Deep tone |
| Amber 500 (Accent) | `#F59E0B` | Highlights, notifications |
| Amber 700 | `#D97706` | Darker amber |
| Surface 50 | `#FAFAF8` | Light backgrounds |
| Ink 800 | `#1C1917` | Primary text |

### Brand Personality
- Warm, approachable, trustworthy
- Education-focused but not childish
- Modern SaaS — clean, not cluttered
- Community/connection-driven

### Key Brand Themes
- **Connection** — linking schools, parents, teachers
- **Communication** — the core function (notices, chat, alerts)
- **Trust** — schools trust SkoConnect with sensitive data
- **Education** — school-centric, not generic chat

---

## Design Requirements

### What We Need
1. **Adaptive Icon Foreground** — The main icon artwork (1024×1024px)
2. **Adaptive Icon Background** — Solid color or simple gradient (1024×1024px)
3. **Legacy Icon** — Combined foreground+background for older Android (all mipmap sizes)

### Technical Specs

#### Android Adaptive Icon (API 26+)
- **Foreground layer:** 1024×1024px, content must fit within **safe zone** (center 66% = 680×680px). Outer 34% is masked by launcher shapes (circle, squircle, rounded square).
- **Background layer:** 1024×1024px, fills entire canvas (solid color or simple gradient).
- **Format:** PNG with transparency (foreground) / PNG (background)

#### Legacy Android (API 21-25)
- Combined icon at standard mipmap sizes: mdpi (48px), hdpi (72px), xhdpi (96px), xxhdpi (144px), xxxhdpi (192px)

#### iOS (Future Consideration)
- Design should work in iOS rounded square shape
- Avoid relying on specific Android mask shapes

### File Deliverables
- `icon_foreground.png` (1024×1024, transparent background)
- `icon_background.png` (1024×1024, solid/gradient)
- `icon_legacy.png` (1024×1024, combined for older devices)
- Source file (Figma, Illustrator, or PSD)

---

## Design Direction

### Must-Have
- **Bold background** — NOT white. The current white background makes the icon invisible on light home screens. Use teal brand color or a teal gradient.
- **Reads at 48dp** — The icon must be instantly recognizable at launcher size (roughly 1.5cm on screen). No tiny details, no text (except possibly a single letter).
- **Strong silhouette** — The icon shape should be distinct even as a monotone outline.

### Design Concept Options (pick one or propose)

**A. Symbol + Brand Color Background**
A single clean symbol (e.g., speech bubble + graduation cap, connected nodes, open book with chat) centered on a teal gradient background. Think: WhatsApp (phone + green), Telegram (paper plane + blue).

**B. Lettermark**
A stylized "S" or "SC" lettermark on a bold background. Clean, modern, scalable. Think: Slack, Spotify, Pinterest.

**C. Abstract Mark**
An abstract shape that evokes connection/communication — overlapping shapes, linking forms, radiating lines. On teal background. Think: Discord, Zoom.

### What to Avoid
- Detailed illustrations that don't read at small sizes
- Text-heavy designs ("SkoConnect" won't be readable at icon size)
- White or light backgrounds (current problem)
- Generic school icons (apple, chalkboard) — too cliché
- More than 2-3 colors
- Drop shadows or 3D effects (flat/modern preferred)

---

## Competitor Reference

Apps whose icon treatment works well in the EdTech/communication space:

| App | Why It Works |
|-----|-------------|
| **WhatsApp** | Bold green background, simple phone symbol, instant recognition |
| **Telegram** | Blue background, simple paper plane, reads at any size |
| **ClassDojo** | Friendly monster character on green, distinctive |
| **Remind** | Blue speech bubble, clean, communication = obvious |
| **Slack** | Multi-color pinwheel, distinctive silhouette |

---

## Current State (What We're Replacing)

The current launcher icon is the SkoConnect logo pasted onto a white background via `flutter_launcher_icons`. The logo imagery sits small and centered with massive white margins, making it look like a blurry crop-out on the home screen.

---

## Acceptance Criteria

- [ ] Icon reads clearly at 48dp (smallest launcher size)
- [ ] Works inside Android adaptive icon masks (circle, squircle, rounded square)
- [ ] Uses SkoConnect brand colors (teal primary, amber accent optional)
- [ ] No white or near-white background
- [ ] Delivered as layered foreground + background for adaptive icon
- [ ] Source file included for future edits
- [ ] Distinctive enough to stand out on a crowded home screen
- [ ] Professional quality — on par with top App Store / Play Store apps

---

## Timeline

- **ASAP** — this is a pre-launch polish item
- Preferred delivery: final assets + source file within 1 week of engagement

---

## Contact

Brief prepared by Atlas (AI Operations) on behalf of Dre Newsome, Founder, SkoConnect Ltd.

*Document generated: May 14, 2026*
