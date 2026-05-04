---
name: 9-phase-content-brief-workflow
description: "Use this skill to generate a comprehensive SEO content brief through a structured 9-phase workflow. Trigger on phrases like: generate a content brief, create a content brief, build an SEO brief, run the 9-phase workflow, content brief workflow, develop a content brief, write me a content brief, dynamic content brief. Also trigger when a user provides keyword research, SERP data, or topic specifications and asks for a structured brief output. The workflow walks through Foundation Analysis, User Intent (RAID model), Dynamic Semantic Analysis, Query Fan-Out, Content Architecture, Internal Linking, External Citations, optional E-E-A-T/YMYL Compliance, and Final Brief Generation. Produces a complete brief with copywriter directives. Do NOT use this skill for quick blog post outlines or short content drafts — it is calibrated for substantive briefs (1,500+ words) where competitive ranking matters."
---

# 9-Phase Content Brief Workflow

A structured workflow for generating SEO content briefs through nine sequential phases with validation checkpoints. Each phase produces specific outputs that feed into the next; advancement requires passing validation criteria.

The workflow's core innovation is **dynamic keyword density calculation** — keyword counts are derived mathematically from competitive analysis rather than chosen arbitrarily. Briefs produced through this workflow are calibrated to outrank competitors based on their actual keyword density patterns, not on intuition.

**Output:** A complete content brief with keyword strategy, content architecture, internal linking plan, citation framework, copywriter directive, and validation checklist.

**Time investment:** ~3-4 hours per brief when executed thoroughly.

---

## 1. When to use this workflow

This workflow is calibrated for **substantive briefs where competitive ranking matters**. Use it when:

- Target word count is 1,500+ words (typical: 2,500-8,000 words)
- The content is competing for ranked positions on commercially valuable queries
- Topical authority and citation discipline matter to the content's success
- The piece is a pillar article, a hub piece, or a strategic blog post (not a quick news update or short-form social content)

Do NOT use this workflow for:
- Short-form posts (under 1,500 words) — overhead exceeds value
- News-cycle content where speed beats depth
- Internal documentation, knowledge base articles, or product copy
- Drafts where SEO is not a primary consideration

---

## 2. Required inputs

| Input | Required | Notes |
|-------|----------|-------|
| **Primary keyword** | Yes | The query the brief targets |
| **Topic / content angle** | Yes | What the content is about |
| **Target word count** | Optional | Defaults from `references/output-format.md` content-type table |
| **SERP / competitor URLs** | Optional but recommended | Top 10 ranking URLs; if not provided, the workflow will identify them via search |
| **Keyword research data** | Optional | Search volumes, related keywords, sub-queries from any tool (SEMrush, Ahrefs, Google Keyword Planner, etc.) |
| **Brand / publisher context** | Optional | Internal linking targets, product integration points |
| **Content vertical** | Optional | Used to determine YMYL applicability (see §6) |

Minimum viable input: a primary keyword and a topic angle. Everything else is enriched during the workflow.

---

## 3. The 9 phases

Each phase has a specific purpose, set of tasks, validation criteria, and output. The workflow does not advance to the next phase until current phase validation passes.

Detailed phase specifications live in `references/phase-templates.md`.

### Phase 1 — Foundation Analysis & Project Setup

**Purpose:** Establish project foundation. Parse keyword/SERP data. Identify competitors.

**Key outputs:** Primary keyword + 5-10 secondary keywords identified, top 10 SERP URLs documented, target word count set per content-type table, success criteria defined.

**Time:** ~30 minutes.

### Phase 2 — User Intent Analysis & Journey Mapping (RAID Model)

**Purpose:** Apply the RAID 4W framework (WHO, WHAT, WHERE, WHY) to understand search intent and user psychology.

**Key outputs:** RAID 4W analysis complete, intent distribution percentages (informational/commercial/transactional/navigational summing to 100%), user journey stages mapped, pain points identified.

**Time:** ~45 minutes.

Detailed RAID model spec in `references/raid-model.md`.

### Phase 3 — Dynamic Semantic Analysis & Keyword Strategy

**Purpose:** Calculate keyword count and density mathematically based on competitor analysis. This is the core innovation of the workflow.

**Key outputs:** Competitor average density measured (sample of top 10), target density calculated (15-25% above competitor average), total keyword mentions = target word count × target density, unique keyword count = total mentions ÷ average mention frequency, section-by-section keyword distribution.

**Time:** ~60 minutes.

The math, with worked examples, lives in `references/dynamic-density-formula.md`.

### Phase 4 — Query Fan-Out Content Enhancement

**Purpose:** Identify 6-10 strategic sub-queries that expand topical coverage, mapping each to specific content sections.

**Key outputs:** Sub-queries identified with search volume data (where available), each sub-query mapped to a content section with integration approach, competitive coverage gaps identified.

**Time:** ~45 minutes.

### Phase 5 — Content Architecture Development

**Purpose:** Design complete content structure (H1/H2/H3/H4) with word count allocation per section.

**Key outputs:** Complete heading hierarchy, word count per section summing to target, keyword distribution per section, sub-query integration mapped to sections, visual element plan (images, tables, callouts, embedded media).

**Time:** ~45 minutes.

### Phase 6 — Strategic Internal Linking Architecture

**Purpose:** Identify 5-10 internal links with exact anchor text, target URLs, and placement recommendations.

**Key outputs:** Internal link list with anchor text and target URLs, strategic purpose per link (topical authority, user journey, conversion path), placement recommendations (which section, what context).

**Time:** ~30 minutes.

### Phase 7 — External Linking & Citation Authority

**Purpose:** Identify external citations and authority sources to build credibility.

**Key outputs:** 
- For non-YMYL content: 3-5 authority links sufficient
- For YMYL content (see §6): 8-10 verified peer-reviewed citations + 3-5 expert quotes with credentials + 3-5 authority websites

**Time:** ~30-60 minutes (longer for YMYL).

**Critical requirement:** All citations must be verifiable and accessible. If a citation cannot be verified, exclude it.

### Phase 8 — E-E-A-T and YMYL Compliance (Optional, conditional)

**Purpose:** Apply Google's E-E-A-T (Experience, Expertise, Authoritativeness, Trustworthiness) framework, with stricter YMYL requirements when applicable.

**This phase is OPT-IN.** It activates when:
- The content is YMYL (see §6 for criteria)
- The user explicitly requests E-E-A-T compliance
- The content vertical demands credibility signals (health, finance, legal, safety)

If none of those trigger, Phase 8 is skipped and the workflow advances to Phase 9.

**Key outputs (when activated):** Experience signals defined, Expertise sources identified, Authoritativeness markers planned, Trustworthiness/safety language requirements specified.

**Time:** ~30 minutes (when activated).

### Phase 9 — Final Brief Generation & Quality Assurance

**Purpose:** Integrate all phase outputs into a final comprehensive brief.

**Key outputs:** Complete brief in standardized format (see `references/output-format.md`), copywriter directive with tone guidelines, final validation checklist, ready-to-implement deliverable.

**Time:** ~45 minutes.

The final brief structure has 12-14 sections depending on whether YMYL was activated.

---

## 4. Validation discipline

Each phase has explicit validation criteria. The workflow does not advance to the next phase until current criteria are met.

When validation fails:
1. Identify which criterion failed and why
2. Loop back within the current phase to address the gap
3. Re-validate
4. Only advance once all criteria pass

This discipline is what separates briefs that produce ranking content from briefs that produce mediocre output. Do not skip validation under time pressure.

Detailed validation criteria per phase live in `references/validation-checkpoints.md`.

---

## 5. Content-type word count table

The workflow calibrates differently based on content type. Use this table to set the target word count if not specified by the user:

| Content type | Word count range | Default | Use case |
|--------------|------------------|---------|----------|
| **Long-form pillar** | 4,000-8,000 | 6,000 | Comprehensive topic coverage, hub piece for clusters |
| **Mid-form article** | 2,000-4,000 | 2,800 | Standard blog post on a defined query |
| **Short-form post** | 1,500-2,000 | 1,800 | Tactical post on a narrow query |

If the user requests a target outside these ranges (under 1,500 or over 8,000), proceed but note the range divergence in the brief.

These ranges are starting points. Adjust based on:
- Competitor average word count (if competitors average 2,000 words, a long-form pillar might land at 3,500 instead of 6,000)
- Query intent (informational queries often need more depth than transactional)
- Vertical norms (B2B SaaS articles average longer than consumer lifestyle)

---

## 6. YMYL determination

YMYL ("Your Money or Your Life") is Google's category for content that can affect user wellbeing, finances, or safety. YMYL content faces stricter quality requirements.

The workflow asks the user (or determines from inputs) whether the content is YMYL:

**The content is YMYL if it covers:**
- Health, medical, or wellness topics where bad advice could cause harm
- Financial topics (investing, taxes, loans, insurance) where bad advice has financial consequences
- Legal topics where bad advice has legal consequences
- Safety topics (parenting, food safety, product safety)
- Civic information (voting, public services) requiring accuracy
- News on topics with significant public consequence

**The content is NOT YMYL if it covers:**
- Entertainment, hobbies, lifestyle topics with low stakes
- Product recommendations where the worst case is "user buys a different product than ideal"
- General educational content not in a YMYL vertical
- Marketing, business, or technology topics without high-stakes implications

When YMYL applies:
- Phase 7 escalates to 8-10 verified peer-reviewed citations + expert quotes with full credentials
- Phase 8 (E-E-A-T compliance) activates automatically
- The output format includes a YMYL Health Content Standards section
- Verification discipline tightens — every citation must be confirmed accessible

When YMYL does not apply, the workflow runs in standard mode with proportionate citation requirements.

---

## 7. Output format

The final brief produced by Phase 9 follows a standardized format with these sections:

**Standard format (non-YMYL):** 12 sections covering project specifications, technical requirements, SEO strategy, query fan-out, content architecture, semantic keyword integration, internal links, external citations, copywriter tone directive, FAQ section, validation checklist, and quality criteria.

**YMYL format:** Same 12 sections plus 2 additional sections — E-E-A-T Compliance Framework and YMYL Health Content Standards.

Detailed format specification with section-by-section templates lives in `references/output-format.md`.

The brief is delivered as inline markdown by default. If the user requests Excel or Word export, generate the corresponding format using the same content structure.

---

## 8. The dynamic density formula — quick reference

The workflow's core innovation. Detailed math and worked examples in `references/dynamic-density-formula.md`. Quick reference here:

```
1. Sample 10 ranking competitors for the primary keyword
2. Measure each competitor's keyword density (occurrences ÷ word count)
3. Calculate competitor average density
4. Set target density = competitor average × 1.15-1.25 (15-25% above)
5. Total mentions = target word count × target density
6. Unique keywords = total mentions ÷ average frequency per keyword (typically 2-4)
7. Distribute unique keywords across content sections per Phase 5 architecture
```

Worked example:
- Competitor sample average density: 10.92%
- Target density: 12.7% (≈16% above average)
- Target word count: 6,500 words
- Total mentions: 6,500 × 0.127 = 826 mentions
- Average frequency per keyword: 2.6
- Unique keywords needed: 826 ÷ 2.6 = ~318 unique terms

This produces keyword strategy grounded in competitive reality, not arbitrary targets.

---

## 9. Failure modes and how to handle them

| Situation | Handling |
|-----------|----------|
| User provides only a topic with no keyword research | Run light keyword discovery via web search; flag in the brief that deeper research would strengthen Phase 3 |
| Cannot access competitor URLs (paywalled, JS-heavy, blocked) | Note the limitation, sample fewer competitors but flag in Phase 3 output that density calculation has reduced confidence |
| User's word count target conflicts with content type norms | Proceed with user's target. Note divergence in the brief |
| YMYL determination is ambiguous (could go either way) | Ask the user once. Default to YMYL if no answer (stricter is safer) |
| Citation verification fails for some sources | Exclude unverified citations from the brief; aim to meet the citation count requirements with verified sources only |
| User asks the workflow to skip phases | Politely explain that phases are sequential. Each phase's output feeds the next. Skipping breaks the math |
| User asks for a "quick" version | The workflow is calibrated for substantive briefs. For quick briefs, recommend a different approach (light SEO outline, not this workflow) |

---

## 10. Reference files

These files contain the detailed specifications. Read them when running the workflow.

- `references/phase-templates.md` — Detailed phase-by-phase task lists, validation criteria, output specifications
- `references/dynamic-density-formula.md` — Keyword math with worked examples across content types
- `references/raid-model.md` — The 4W (WHO, WHAT, WHERE, WHY) user intent framework with application examples
- `references/validation-checkpoints.md` — Phase-by-phase validation criteria and what to do when checkpoints fail
- `references/output-format.md` — Final brief structure with section-by-section templates (12 sections standard, 14 with YMYL)

These are loaded on demand. Don't memorize them — reference them when running the workflow.

---

## 11. What this workflow is NOT

To prevent scope creep:

- **NOT a quick blog outline tool.** It's calibrated for substantive briefs.
- **NOT an automated content generator.** It produces briefs that copywriters or AI writers then implement.
- **NOT a replacement for editorial judgment.** Briefs are starting points; humans (or AI editors) refine the actual writing.
- **NOT a one-size-fits-all template.** The dynamic density calculation adapts the brief to the specific competitive context.
- **NOT a substitute for keyword research tools.** It uses keyword research data; it doesn't generate keyword research from scratch.

If the user asks for any of the above, redirect honestly. The workflow stays in its lane.
