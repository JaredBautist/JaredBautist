# GitHub Profile README Design

## Content Architecture

The README uses a content-first portfolio structure:

1. Identity and positioning
2. Professional details table
3. Short professional summary
4. Grouped technology stack
5. Ranked featured projects
6. Selected professional impact and achievement
7. Current learning focus
8. GitHub activity and contact

The ordering lets a recruiter understand the profile quickly, then inspect concrete
evidence without reading a long autobiography.

## Data Sources

| Content | Source |
| --- | --- |
| Name, location, role, achievement, experience | User-provided profile draft |
| Repository links, stars, languages, activity | GitHub repository metadata |
| Project capabilities and stacks | Each repository's README and manifest descriptions |

## Presentation Decisions

- Use native Markdown and small amounts of GitHub-supported HTML for alignment.
- Use one repository-owned SVG hero with a deep navy palette, high-contrast text,
  and restrained motion.
- Use shields only for compact status and technology labels.
- Group technology icons into frontend, backend, data/cloud, and engineering
  categories to mirror the supplied reference without copying it.
- Keep paragraphs short and project descriptions evidence-led.
- Provide descriptive alternative text for dynamic activity images.
- Avoid fixed backgrounds and text colors so GitHub light and dark themes both work.
- Respect `prefers-reduced-motion` inside the SVG and keep professional information
  available as real README text rather than embedding it only in an image.
- Present AI development tools in one centered, borderless icon row. Place each
  official logo on a standardized dark rounded tile at the same displayed size and
  spacing used by the other technology icon rows. Keep every tile linked and provide
  a descriptive alternative text instead of a visible product label.

## ADR-001: Featured Project Ranking

### Context

Most repositories have no stars, so ranking only by popularity would not distinguish
portfolio quality.

### Options Considered

1. Stars only: objective, but ignores business impact and engineering breadth.
2. Recent activity only: favors maintenance recency over project quality.
3. Weighted portfolio relevance: combines public interest, recency, technical depth,
   and professional impact.

### Decision

Use weighted portfolio relevance. AXOLOT ranks first due to public adoption signals
and active development; Coworking ranks second for full-stack breadth; MIPRES ranks
third for domain and operational impact.

### Consequences

The order is meaningful to recruiters but is an editorial ranking, not a generated
GitHub popularity leaderboard.

## ADR-002: Contact Information

### Contact Context

The draft contains LinkedIn and email labels without destinations.

### Contact Decision

Publish the verified GitHub link only. Add LinkedIn or email later when Jared provides
the exact public destinations.

### Contact Consequences

There are no dead links or accidental disclosures, but the initial profile has one
contact channel.

## ADR-003: Animated Header Asset

### Animation Context

The supplied reference uses a dark, visual hero, and Jared requested animation. GitHub
READMEs cannot run arbitrary JavaScript, so the motion must be image-based.

### Animation Options Considered

1. Animated GIF: broadly compatible, but heavy, rasterized, and inaccessible to
   reduced-motion preferences.
2. Third-party typing SVG: quick to embed, but adds a runtime dependency and produces
   a familiar template look.
3. Repository-owned SVG: lightweight, scalable, customizable, and able to include a
   reduced-motion media query.

### Animation Decision

Use one repository-owned SVG banner. Animate only the initial title treatment, accent
line, and ambient wave geometry; keep the motion subtle and non-essential.

### Animation Consequences

The profile gains a distinctive visual identity without relying on a third-party
animation service. The same banner remains readable if SVG animation is unavailable
or reduced motion is enabled.

## ADR-004: AI Tool Brand Assets

### Brand Asset Context

Claude Code, Codex, Antigravity, and Kiro do not all exist in the same public icon
library, and substituting generic AI symbols would make the tools harder to recognize.

### Brand Asset Decision

Use the official Claude mark and the product icons distributed with the locally
installed official Codex, Antigravity, and Kiro applications. Preserve their original
colors and aspect ratios, store optimized copies in the profile repository, and place
presentation copies on a shared dark rounded-tile canvas.

### Brand Asset Consequences

The four tools have accurate, stable visual identities without runtime dependence on
an icon CDN. The shared canvas makes icons from different vendors feel consistent
with the technology stack while leaving the source brand assets unchanged.
