# 9-Phase Content Brief Workflow

A structured workflow for generating SEO content briefs through nine sequential phases with validation checkpoints. Each phase produces specific outputs that feed into the next; advancement requires passing validation criteria.

The workflow's core innovation is **dynamic keyword density calculation** — keyword counts are derived mathematically from competitor analysis rather than chosen arbitrarily. Briefs are calibrated to outrank competitors based on their actual keyword density patterns.

---

## What this workflow produces

A complete content brief containing:

- Project specifications and success metrics
- User intent analysis using the RAID 4W framework (WHO, WHAT, WHERE, WHY)
- Mathematically-derived keyword strategy (density calculated from competitor analysis)
- Strategic sub-query coverage plan (6-10 sub-queries mapped to content sections)
- Complete content architecture (H1/H2/H3 structure with word count allocation)
- Internal linking plan (5-10 links with specific anchor text and placement)
- External citation framework (3-5 for non-YMYL, 8-10 peer-reviewed + expert quotes for YMYL)
- E-E-A-T compliance framework (when YMYL applies)
- Copywriter tone directive with do/don't examples and sample voice
- Comprehensive FAQ section
- Final validation checklist

The brief renders as inline markdown by default, with optional Excel and Word export.

---

## When to use this workflow

This workflow is calibrated for **substantive briefs where competitive ranking matters**:

- Long-form pillar content (4,000-8,000 words)
- Mid-form articles (2,000-4,000 words)
- Short-form posts where SEO discipline still matters (1,500-2,000 words)

Do NOT use this workflow for:
- Posts under 1,500 words (overhead exceeds value)
- News-cycle content where speed beats depth
- Internal documentation or knowledge-base articles
- Drafts where SEO is not a primary consideration

Time investment: ~3-4 hours per brief when executed thoroughly.

---

## How to invoke

The skill auto-fires on phrases like:

- "Generate a content brief for [keyword]"
- "Create a content brief on [topic]"
- "Build an SEO brief for [URL or topic]"
- "Run the 9-phase workflow on [keyword]"
- "Develop a content brief for [topic]"

The skill does NOT auto-fire on requests for:
- Quick blog outlines (use a lighter approach)
- Article drafts directly (this skill produces briefs, not finished articles)
- Generic "write me content" prompts (too vague)

---

## The 9 phases

| # | Phase | Time | Output |
|---|-------|------|--------|
| 1 | Foundation Analysis | ~30 min | Project specs, keyword research, SERP competitors |
| 2 | User Intent (RAID Model) | ~45 min | WHO/WHAT/WHERE/WHY analysis, intent distribution, pain points |
| 3 | Dynamic Semantic Analysis | ~60 min | Mathematical keyword count from competitor density |
| 4 | Query Fan-Out | ~45 min | 6-10 sub-queries mapped to content sections |
| 5 | Content Architecture | ~45 min | Complete H1/H2/H3 structure with word count allocation |
| 6 | Internal Linking | ~30 min | 5-10 internal links with anchor text and placement |
| 7 | External Citations | ~30-60 min | Authority sources (more for YMYL) |
| 8 | E-E-A-T Compliance | ~30 min | Activated for YMYL or on request |
| 9 | Final Brief Generation | ~45 min | Integrated brief with copywriter directive |

Each phase has explicit validation criteria. The workflow does not advance to the next phase until current criteria are met.

---

## The dynamic density formula

The core innovation. Keyword counts are derived from competitive reality, not arbitrary rules.

```
1. Sample 10 ranking competitors for the primary keyword
2. Measure each competitor's keyword density
3. Calculate competitor average density
4. Set target density = competitor average × 1.15 to 1.25 (15-25% above)
5. Total mentions = target word count × target density
6. Unique keywords = total mentions ÷ average frequency per keyword (typically 2-4)
```

Worked example:
- Competitor sample average density: 10.92%
- Target density: 12.7% (≈16% above average)
- Target word count: 6,500 words
- Total mentions: 6,500 × 0.127 = 826 mentions
- Unique keywords: 826 ÷ 2.6 = ~318 unique terms

This produces keyword strategy grounded in competitive context — not "use the keyword 5-10 times" or "target 2% density."

Detailed math with worked examples in `references/dynamic-density-formula.md`.

---

## YMYL handling

YMYL ("Your Money or Your Life") content faces stricter quality requirements from Google. The workflow handles YMYL conditionally:

**When YMYL applies (health, finance, legal, safety, civic):**
- Phase 7 escalates to 8-10 peer-reviewed citations + 3-5 expert quotes with verified credentials
- Phase 8 (E-E-A-T compliance) activates automatically
- Output format includes 2 additional sections (E-E-A-T Compliance Framework, YMYL Content Standards)
- All citations must be verifiable and accessible

**When YMYL does not apply:**
- Phase 7 uses 3-5 authority links (proportionate to non-stakes content)
- Phase 8 is skipped (unless user explicitly requests E-E-A-T compliance)
- Standard 12-section output format

The workflow asks the user once for YMYL determination if it cannot infer from inputs. When ambiguous, defaults to YMYL (stricter is safer).

---

## Repository structure

```
9-phase-content-brief-workflow/
├── SKILL.md                              # Operating instructions
├── README.md                             # This file
├── LICENSE                               # MIT
└── references/
    ├── phase-templates.md                # Detailed phase-by-phase specs
    ├── dynamic-density-formula.md        # Keyword math with worked examples
    ├── raid-model.md                     # WHO/WHAT/WHERE/WHY framework
    ├── validation-checkpoints.md         # Phase validation criteria
    └── output-format.md                  # Final brief structure (12 or 14 sections)
```

Reference files are loaded on demand by the skill.

---

## Why this workflow exists

Most content brief templates fall into two categories:

**Category 1 — Generic templates.** "Title, intro, 3 H2s, conclusion." Useful for getting started, useless for ranking on competitive queries.

**Category 2 — Tool-specific outputs.** Briefs generated by SEO tools that produce thorough but generic recommendations. Often mathematically arbitrary (why 7 sub-headings? why 2,000 words? why 5 keywords?).

This workflow occupies a different space:

- **Mathematically grounded.** Every quantitative target derives from analysis, not convention.
- **Validation-disciplined.** Each phase has explicit gates. No advancement until criteria met.
- **User-grounded.** RAID model produces deep intent analysis instead of surface classification.
- **Conditionally calibrated.** YMYL discipline activates only when content warrants it.

The result is briefs that copywriters can implement with confidence and that consistently produce ranking content when the underlying writing matches the brief's quality.

---

## Installation

To use this skill in Claude.ai:

1. Download or clone this repo
2. Upload contents to your Claude.ai skills directory
3. Verify the skill appears in your available skills
4. Trigger with a phrase like "Generate a content brief for [keyword]"

For Claude Code or API usage, configure per your platform's skill loading mechanism.

---

## Contributing

If you've found edge cases the workflow mishandles, or have refinements to suggest, open an issue. Pull requests welcome for:

- Vertical-specific calibrations (e.g., e-commerce content brief variations)
- Additional validation criteria
- Alternate density calculation methods for specific content types
- Output format polish

---

## License

MIT. Use it, adapt it, cite it. Attribution appreciated.

---

## About

Built and refined through years of producing SEO content briefs in competitive verticals. The workflow's discipline — mathematical density calculation, RAID intent analysis, validation checkpoints — emerged from observing what separated briefs that produced ranking content from briefs that produced mediocre output.

**Ivan Nonveiller** — enterprise SEO and content marketing strategist. Based in Montréal.

- LinkedIn: [ivannonveiller](https://www.linkedin.com/in/ivannonveiller/)

---

> All views shared here are my own personal work. This repository does not represent the views, strategies, or official work product of any current employer or client.
