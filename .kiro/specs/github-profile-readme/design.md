# GitHub Profile README Design

## Content Architecture

The README uses a content-first portfolio structure:

1. Identity and positioning
2. Short professional summary
3. Grouped technology stack
4. Ranked featured projects
5. Selected professional impact and achievement
6. Current learning focus
7. GitHub activity and contact

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
- Use shields only for compact status and technology labels.
- Keep paragraphs short and project descriptions evidence-led.
- Provide descriptive alternative text for dynamic activity images.
- Avoid fixed backgrounds and text colors so GitHub light and dark themes both work.

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
