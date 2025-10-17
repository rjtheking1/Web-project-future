# Cybersecurity Services Company - Design Guidelines

## Design Approach
**Reference-Based Approach** inspired by industry leaders like CrowdStrike, Palo Alto Networks, and Cloudflare. The design emphasizes trust, security expertise, and modern professionalism while adapting the existing portfolio UI assets for a cybersecurity context.

**Core Principles:**
- Professional authority and technical credibility
- Clear visual hierarchy for complex security information
- Dark theme aesthetic conveying security and sophistication
- Strategic use of accent colors for calls-to-action

## Color Palette

### Dark Mode (Primary)
- **Background Primary**: 217 19% 12% (Deep navy-charcoal)
- **Background Secondary**: 217 19% 18% (Slightly lighter navy)
- **Background Elevated**: 217 19% 22% (Card/section backgrounds)

### Accent Colors
- **Primary Accent**: 210 100% 60% (Bright cyber blue - CTAs, links, highlights)
- **Secondary Accent**: 280 85% 55% (Electric purple - secondary actions, hover states)
- **Success/Secure**: 140 70% 50% (Secure green - trust indicators)
- **Warning/Threat**: 0 85% 60% (Alert red - vulnerability mentions)

### Text Colors
- **Heading Text**: 0 0% 98% (Near white)
- **Body Text**: 217 15% 75% (Light gray-blue)
- **Muted Text**: 217 10% 55% (Dimmed gray)

## Typography

**Font Families:**
- **Headings**: 'Inter' or 'Outfit' (700, 600 weights) - Modern, authoritative
- **Body**: 'Inter' or 'DM Sans' (400, 500 weights) - Clean, readable
- **Monospace**: 'JetBrains Mono' for code snippets or technical data

**Scale:**
- Hero Headline: text-5xl md:text-7xl font-bold
- Section Titles: text-3xl md:text-4xl font-semibold
- Service Cards: text-xl md:text-2xl font-semibold
- Body: text-base md:text-lg
- Small/Meta: text-sm

## Layout System

**Spacing Primitives:** Use Tailwind units of 4, 6, 8, 12, 16, 20, 24, 32 for consistent rhythm
- Section padding: py-16 md:py-24 lg:py-32
- Container max-width: max-w-7xl
- Card spacing: gap-6 md:gap-8
- Element margins: mb-4, mb-6, mb-8

**Grid Patterns:**
- Services: 3-column grid (grid-cols-1 md:grid-cols-2 lg:grid-cols-3)
- Case Studies: 2-column grid (grid-cols-1 lg:grid-cols-2)
- Team Profiles: 3-4 column grid (grid-cols-1 sm:grid-cols-2 lg:grid-cols-4)
- Pricing: 3-tier layout (grid-cols-1 md:grid-cols-3)

## Component Library

### Navigation
- Fixed top navbar with dark background (bg-[217 19% 12%]/95 backdrop-blur-md)
- Logo on left, navigation links center/right
- Demo CTA button with primary accent color
- Mobile: Hamburger menu with slide-in panel

### Hero Section
- Full viewport height (min-h-screen) with gradient overlay
- Large hero image showing security operations center, digital security visualization, or abstract tech patterns
- Centered headline with animated text or gradient text effect
- Subheadline describing core value proposition
- Dual CTA buttons: "Request Demo" (primary) + "View Services" (outline with blur background)
- Floating security stats/metrics cards (optional): "500+ Clients Protected", "99.9% Threat Detection"

### Service Cards
- Dark card background (bg-[217 19% 18%]) with border (border-[217 19% 28%])
- Icon at top (shield, lock, radar symbols from font-awesome or heroicons)
- Service title in bright heading color
- 2-3 line description
- Hover: Lift effect (hover:-translate-y-1) with glow border in primary accent

### Pricing Section
- 3 pricing tiers in card layout
- Highlighted "Most Popular" tier with accent border and subtle glow
- Feature lists with checkmarks
- Prominent "Get Started" buttons
- Monthly/Annual toggle switch

### Team Profiles
- Circular or rounded profile images
- Name and role below image
- Security certifications badges (CISSP, CEH, etc.)
- Linked specializations or expertise tags
- Hover: Overlay with bio preview or LinkedIn link

### Case Studies
- Large card format with thumbnail image
- Client industry tag
- Problem statement headline
- Key results metrics (% improvement, threats blocked, etc.)
- "Read Case Study" link
- Before/after security posture visualization

### Information Pages (Vulnerabilities/Attacks)
- Sidebar navigation for topics
- Clean content layout with max-w-3xl
- Code blocks for technical examples (bg-[217 19% 10%] with monospace font)
- Warning callouts for critical vulnerabilities (border-l-4 border-red accent)
- Inline diagrams or attack flow visualizations

### Demo Booking Form
- Clean 2-column layout (form left, info/contact right)
- Input fields with dark backgrounds and light borders
- Dropdown for service interest
- Date/time selector for demo scheduling
- Large submit button with primary accent
- Success confirmation message with animation

### Footer
- Multi-column layout: Services | Company | Resources | Contact
- Newsletter signup form
- Social media links
- Trust badges (security certifications, compliance logos)
- Copyright and legal links

## Animations
Use sparingly for professional feel:
- Fade-in on scroll for section reveals (opacity-0 to opacity-100)
- Subtle hover lifts on cards (-translate-y-1)
- Number counting animations for statistics
- Smooth page transitions
- Loading states for demo form submission

## Images

### Hero Section
**Large hero image required**: Full-width, high-quality image showing:
- Security operations center with monitors displaying threat data
- Abstract digital security visualization (network nodes, encryption patterns)
- Dark aesthetic with blue accent lighting
- Overlay: Dark gradient (from transparent to bg-primary) for text readability

### Service Section Icons
Use icon library (Heroicons or Font Awesome) for:
- Shield, lock, radar, fingerprint, network symbols
- Consistent sizing (w-12 h-12 md:w-16 h-16)

### Team Profiles
Professional headshots with consistent aspect ratio (square or 3:4)
Dark or neutral backgrounds preferred

### Case Studies
Client environment screenshots (anonymized), security dashboard visualizations, or industry-specific imagery

### Information Pages
Diagrams showing attack vectors, vulnerability exploits, security architecture
Use dark theme with accent colors for clarity

## Accessibility
- WCAG AA contrast ratios (light text on dark backgrounds)
- Focus states with accent color outlines
- Keyboard navigation throughout
- Alt text for all security diagrams and images
- Semantic HTML structure for screen readers