# Phase Templates

Detailed specification for each of the 9 phases. Each phase has: purpose, key tasks, validation criteria, and output format. The workflow runs phases sequentially; advancement requires passing validation.

---

## Phase 1 — Foundation Analysis & Project Setup

**Purpose:** Establish the project foundation. Parse keyword and competitive data. Define what the brief is targeting and what success looks like.

**Time investment:** ~30 minutes

### Tasks

1. **Parse keyword research inputs.** If the user provided keyword research data (CSV from SEMrush, Ahrefs, etc.), parse for:
   - Primary keyword (the main target)
   - Secondary keywords (related terms with significant search volume)
   - Long-tail variations
   - Search volumes per keyword
   - Keyword difficulty scores (if available)

   If no keyword research was provided, run light discovery via web search to identify the primary keyword's variations and related terms.

2. **Identify SERP competitors.** If the user provided competitor URLs, use them. Otherwise, search the primary keyword and capture the top 10 organic results (excluding ads, AI Overviews, featured snippets in some interpretations).

3. **Define client/publisher specifications.**
   - Publishing surface (blog, hub page, knowledge base)
   - Brand voice considerations (formal, conversational, technical)
   - Internal link targets available (other pages on the site)
   - Conversion goals (newsletter signup, product page visit, demo request, app download, etc.)

4. **Set target word count.** Use the content-type table from SKILL.md §5 if not specified by the user.

5. **Define success metrics.** What does this brief need to deliver?
   - Ranking goals (target position for primary keyword)
   - Traffic goals (if specifiable)
   - Engagement goals (time on page, scroll depth)
   - Conversion goals (specific actions)

### Validation criteria

Phase 1 is complete only when ALL of these are met:

- [ ] Primary keyword identified
- [ ] At least 3 secondary keywords identified (5+ preferred)
- [ ] Top 10 SERP URLs documented (if SERP analysis is possible) or 5+ if SERP access is limited
- [ ] Target word count set with rationale
- [ ] Publishing surface and conversion goal specified
- [ ] Success metrics articulated

If any criterion fails, loop back. Do not advance to Phase 2 with incomplete foundation.

### Output format

```markdown
## Phase 1 Output: Foundation Analysis

**Primary keyword:** [keyword] (search volume: [N], difficulty: [N])

**Secondary keywords:**
1. [keyword] (volume: [N])
2. [keyword] (volume: [N])
[...]

**SERP competitors (top 10):**
1. [URL]
2. [URL]
[...]

**Target word count:** [N] words ([content type])

**Publishing surface:** [blog / hub / knowledge base]

**Conversion goal:** [specific action]

**Success metrics:**
- Ranking: [target position]
- Traffic: [target if applicable]
- Engagement: [target if applicable]
- Conversion: [target rate or volume]
```

---

## Phase 2 — User Intent Analysis & Journey Mapping (RAID Model)

**Purpose:** Apply the RAID 4W framework (WHO, WHAT, WHERE, WHY) to deeply understand search intent and user psychology.

**Time investment:** ~45 minutes

### Tasks

Apply the RAID model in detail. See `references/raid-model.md` for the framework specification.

1. **WHO** — Who is searching this keyword?
   - Demographics (age range, professional context if relevant, life stage)
   - Knowledge level (beginner, intermediate, expert)
   - Emotional state (curious, frustrated, urgent, exploratory)
   - Decision-making stage (just learning, comparing options, ready to act)

2. **WHAT** — What are they actually trying to accomplish?
   - Surface-level question (what they typed)
   - Underlying need (what they actually want to know or do)
   - Implicit assumptions they're making
   - What success looks like for them after engaging with content

3. **WHERE** — Where are they in their journey?
   - Top of funnel (problem recognition)
   - Middle of funnel (solution exploration)
   - Bottom of funnel (decision/action)
   - Post-purchase or post-action (validation, troubleshooting)

4. **WHY** — Why this query, why now?
   - Triggering event (life change, news event, recommendation, problem appearance)
   - Motivation (curiosity, urgency, obligation, opportunity)
   - Stakes (low, medium, high)

5. **Determine intent distribution.** Based on RAID analysis, what percentage of searchers fall into each intent type?
   - Informational (want to learn)
   - Commercial (researching purchase)
   - Transactional (ready to buy/act)
   - Navigational (looking for specific source)

   Distribution must sum to 100%.

6. **Map user journey stages.** For the primary intent group, what does the journey look like? What questions arise at each stage?

7. **Identify pain points.** What frustrations does the searcher have? What gaps exist in current SERP results?

### Validation criteria

- [ ] RAID 4W applied with substantive answers in all four dimensions
- [ ] Intent distribution percentages defined and sum to 100%
- [ ] User journey mapped across at least 3 stages
- [ ] At least 3 specific pain points identified
- [ ] Pain points are concrete, not generic ("information overload" is too vague; "users can't find a single source comparing X across Y dimensions" is concrete)

### Output format

```markdown
## Phase 2 Output: User Intent Analysis (RAID Model)

### WHO
- Demographics: [description]
- Knowledge level: [description]
- Emotional state: [description]
- Decision stage: [description]

### WHAT
- Surface query: "[primary keyword]"
- Underlying need: [description]
- Implicit assumptions: [list]
- Success state: [what user wants after content engagement]

### WHERE (Journey stage)
- Primary stage: [TOFU / MOFU / BOFU]
- Secondary stages also served: [list]

### WHY
- Triggering event: [description]
- Motivation: [description]
- Stakes: [low / medium / high]

### Intent distribution
- Informational: [N]%
- Commercial: [N]%
- Transactional: [N]%
- Navigational: [N]%
*(must sum to 100%)*

### User journey stages
1. [Stage]: [questions arising]
2. [Stage]: [questions arising]
3. [Stage]: [questions arising]

### Pain points (gaps in current SERP)
1. [specific pain point]
2. [specific pain point]
3. [specific pain point]
```

---

## Phase 3 — Dynamic Semantic Analysis & Keyword Strategy

**Purpose:** Calculate keyword count and density mathematically based on competitor analysis. This is the workflow's core innovation.

**Time investment:** ~60 minutes

### Tasks

1. **Sample competitor keyword density.** For each of the top 10 SERP competitors (or as many as accessible):
   - Fetch the page content
   - Identify how many times the primary keyword + close variants appear
   - Divide by word count
   - Record density percentage

   If JavaScript-rendered content blocks fetching, sample fewer competitors (5+) and note the limitation in the output.

2. **Calculate competitor average density.** Sum all sampled densities, divide by sample size.

3. **Set target density.** Target = competitor average × 1.15 to 1.25 (15-25% above average).
   - Lower end (15% above) for verticals where density is already high
   - Higher end (25% above) for verticals where competitors are under-optimized

4. **Calculate total keyword mentions.** Total mentions = target word count × target density.

5. **Determine unique keyword count.** Unique keywords = total mentions ÷ average mention frequency per keyword (typically 2-4 mentions per keyword for natural integration).

6. **Build keyword cluster strategy.** Group keywords into clusters around themes. For each cluster:
   - Theme/topic
   - Keywords in cluster
   - Approximate mention allocation per keyword
   - Section(s) where the cluster will live

7. **Plan section-by-section keyword distribution.** Allocate keyword mentions across the content architecture (which is built in Phase 5 — for now, plan the distribution at a category level: introduction, main sections, conclusion).

The full math with worked examples lives in `references/dynamic-density-formula.md`.

### Validation criteria

- [ ] At least 5 competitors sampled (10 preferred)
- [ ] Competitor average density calculated and shown
- [ ] Target density set 15-25% above competitor average
- [ ] Total mention count calculated mathematically (not arbitrary)
- [ ] Unique keyword count derived from total mentions ÷ frequency
- [ ] Keyword clusters defined with section allocation plan
- [ ] Average mentions per keyword maintained at 2-4 for natural integration

### Output format

```markdown
## Phase 3 Output: Dynamic Semantic Analysis

### Competitor density analysis
| Competitor | Word count | Keyword count | Density |
|------------|------------|---------------|---------|
| [URL 1] | [N] | [N] | [N]% |
| [URL 2] | [N] | [N] | [N]% |
[...]

**Competitor average density:** [N]%

### Target density calculation
- Competitor average: [N]%
- Target adjustment: [+15-25%]
- **Target density: [N]%**

### Mention math
- Target word count: [N] words
- Target density: [N]%
- **Total mentions: [N] occurrences**
- Average frequency per keyword: [2-4]
- **Unique keywords needed: ~[N] terms**

### Keyword clusters
**Cluster 1 — [Theme]**
- Primary terms: [list]
- Mentions allocated: [N]
- Target sections: [list]

**Cluster 2 — [Theme]**
[...]

### Section-level distribution plan
- Introduction: ~[N] mentions
- Main sections: ~[N] mentions distributed
- Conclusion: ~[N] mentions
- Average per H2: ~[N] mentions
```

---

## Phase 4 — Query Fan-Out Content Enhancement

**Purpose:** Identify 6-10 strategic sub-queries that expand the content's topical coverage and improve its ability to rank for related searches.

**Time investment:** ~45 minutes

### Tasks

1. **Identify candidate sub-queries.** Sources:
   - "People Also Ask" boxes from the SERP
   - "Related searches" at the bottom of SERPs
   - AI Overview citations (if visible)
   - Competitor article subheadings (what questions are they answering?)
   - Forum/Reddit/Quora questions on the topic
   - Search autocomplete suggestions

2. **Evaluate each sub-query.** For each candidate:
   - Search volume (if data available)
   - Topical relevance to primary keyword
   - Whether it serves the same intent group as the primary
   - Whether competitors are addressing it well or leaving a gap

3. **Select 6-10 strategic sub-queries.** Prioritize:
   - High volume + topical relevance
   - Gaps where competitors are weak
   - Diversity of intent (some informational, some commercial if applicable)

4. **Map each sub-query to a content section.** Each sub-query should be addressable within a specific H2 or H3 of the content architecture (which is built in Phase 5). For now, identify the section-level home for each sub-query.

5. **Define integration approach for each sub-query.** Will it be:
   - A dedicated subsection (its own H3)?
   - Woven into existing prose?
   - Addressed in the FAQ section?
   - Surfaced as a callout/highlight box?

### Validation criteria

- [ ] 6-10 sub-queries identified (8 is the sweet spot)
- [ ] Each sub-query has search volume data OR explicit acknowledgment that volume data wasn't available
- [ ] Each sub-query mapped to a target content section
- [ ] Integration approach defined for each
- [ ] At least 2-3 sub-queries address gaps that competitors don't cover well (creates competitive advantage)

### Output format

```markdown
## Phase 4 Output: Query Fan-Out Strategy

### Strategic sub-queries

**1. [Sub-query]**
- Search volume: [N or "unavailable"]
- Source: [PAA / related searches / competitor analysis / forum]
- Target section: [section name from architecture]
- Integration: [dedicated subsection / woven prose / FAQ / callout]
- Competitive note: [are competitors addressing this well? gap identified?]

**2. [Sub-query]**
[...]

### Coverage matrix
| Sub-query | Section | Format | Competitive gap |
|-----------|---------|--------|-----------------|
| [query 1] | [section] | [format] | [yes/no/partial] |
| [query 2] | [section] | [format] | [yes/no/partial] |
[...]
```

---

## Phase 5 — Content Architecture Development

**Purpose:** Design the complete content structure (H1/H2/H3/H4) with word count allocation per section.

**Time investment:** ~45 minutes

### Tasks

1. **Draft the H1.** The H1 is the page's primary title. It should:
   - Include or closely paraphrase the primary keyword
   - Be compelling (not just keyword-stuffed)
   - Set clear expectations for what the content delivers
   - Be 50-65 characters when possible (matches typical SERP title length)

2. **Outline H2 sections.** Each H2 represents a major section. Aim for:
   - Long-form pillar (4,000-8,000 words): 8-15 H2 sections
   - Mid-form article (2,000-4,000 words): 5-8 H2 sections
   - Short-form post (1,500-2,000 words): 4-6 H2 sections

   Each H2 should:
   - Cover a distinct subtopic
   - Address either a sub-query (Phase 4) or a major user-journey question (Phase 2)
   - Include relevant keyword cluster (Phase 3)

3. **Add H3/H4 subsections.** Within each H2, add:
   - H3 subsections for distinct concepts within the H2 topic
   - H4 sub-subsections only when content depth requires (typically only in long-form pillars)

4. **Allocate word count.** Distribute the target word count across sections:
   - Introduction: 5-10% of target
   - Each major H2: roughly equal share of remaining (with some H2s longer if they cover sub-queries deeply)
   - Conclusion / CTA section: 5-10% of target
   - FAQ section (if included): 10-15% of target

   Sum of sections should equal target word count ±10%.

5. **Map keywords and sub-queries to sections.** For each section, specify:
   - Primary keyword presence (yes/no, if yes mention count)
   - Keyword cluster from Phase 3 covered in this section
   - Sub-query from Phase 4 addressed (if any)
   - Internal link target (filled in Phase 6)
   - External citation type (filled in Phase 7)

6. **Plan visual elements.** For each section, identify what visual elements will support the content:
   - Hero image (top of article)
   - Inline images (1 per H2 typical for long-form)
   - Tables (for comparisons, data)
   - Callout boxes (for key takeaways)
   - Diagrams or infographics
   - Video embeds
   - Pull quotes (especially for expert quotes from Phase 7)

   Aim for 1 visual element per 500-800 words on average.

### Validation criteria

- [ ] H1 drafted with primary keyword integration
- [ ] All H2 sections outlined with subtopic coverage
- [ ] H3/H4 added where depth requires
- [ ] Word count allocated per section, summing to target ±10%
- [ ] Each section has primary keyword and cluster mapping
- [ ] All Phase 4 sub-queries placed in specific sections
- [ ] Visual element plan specifies 1 element per ~500-800 words minimum
- [ ] Architecture supports natural reading flow (sections build on each other logically)

### Output format

```markdown
## Phase 5 Output: Content Architecture

### H1
[Primary title — character count]

### Section structure

**Introduction** (~[N] words)
- Sets up the topic
- Acknowledges user's pain point (from Phase 2)
- Previews what the content will deliver
- Visual: hero image
- Keywords: [primary cluster mentions]

**[H2 Section 1 title]** (~[N] words)
- Sub-topic: [description]
- Sub-query addressed: [from Phase 4]
- Keyword cluster: [from Phase 3]
- Subsections:
  - H3: [title]
  - H3: [title]
- Visual: [type]
- Internal link: [placeholder for Phase 6]
- Citation: [placeholder for Phase 7]

**[H2 Section 2 title]** (~[N] words)
[...]

**Conclusion / CTA** (~[N] words)
- Recap key insights
- Bridge to action
- Conversion CTA
- Visual: [if applicable]

**FAQ** (~[N] words, if included)
- 5-8 FAQ questions addressing additional sub-queries
- Each Q&A: 80-120 words

### Total word count check
Sum of allocated words: [N]
Target: [N]
Variance: [+/- N%]

### Visual element plan
[N] total visual elements across [N] words = 1 per [N] words
- [List of all visuals with section assignment]
```

---

## Phase 6 — Strategic Internal Linking Architecture

**Purpose:** Identify 5-10 internal links with exact anchor text, target URLs, and placement recommendations.

**Time investment:** ~30 minutes

### Tasks

1. **Inventory available internal link targets.** From the user's input or by browsing the site:
   - Related blog posts on similar topics
   - Pillar pages or hub pages
   - Product/service pages
   - About/credibility pages
   - Conversion pages (signup, demo, contact)

2. **Match link targets to content sections.** For each target, identify which section of the content it best supports:
   - Topical authority links: support the topic being discussed
   - User journey links: move the reader forward in their decision process
   - Conversion links: surface the conversion path at the right moment

3. **Draft anchor text.** Each anchor text should:
   - Be specific to the destination (not "click here" or "learn more")
   - Use natural language, not keyword stuffing
   - Match user intent at that point in the article
   - Vary across the article (don't use the same anchor text for different links)

4. **Specify placement.** For each link:
   - Which section
   - Approximate position in section (early, mid, end)
   - Sentence context

### Validation criteria

- [ ] 5-10 internal links identified (8 is typical sweet spot)
- [ ] Each link has destination URL
- [ ] Each anchor text is specific and natural
- [ ] Each link has section-level placement specified
- [ ] Mix of link types (topical, user-journey, conversion)
- [ ] No two links use identical anchor text

### Output format

```markdown
## Phase 6 Output: Internal Linking Strategy

### Strategic internal links

**1. [Anchor text]**
- Target URL: [URL]
- Section: [section name]
- Placement: [position in section]
- Purpose: [topical authority / user journey / conversion]
- Strategic rationale: [why this link helps]

**2. [Anchor text]**
[...]

### Link distribution
- Topical authority links: [N]
- User journey links: [N]
- Conversion links: [N]
- Total: [N]

### Anchor text variation check
[List confirming no duplicates]
```

---

## Phase 7 — External Linking & Citation Authority

**Purpose:** Identify external citations and authority sources to build credibility.

**Time investment:** ~30-60 minutes (longer for YMYL)

### Tasks

1. **Determine YMYL status.** See SKILL.md §6 for criteria. This affects citation requirements:

   **Non-YMYL content:** 3-5 authority links sufficient. Citations from credible publications, original research, recognized institutions.

   **YMYL content:** 8-10 verified peer-reviewed citations REQUIRED + 3-5 expert quotes with credentials + 3-5 authority website references.

2. **Research and verify citations.** For each potential citation:
   - Confirm the source is accessible (no paywall blocking the relevant content; if paywalled, note this)
   - Verify the citation supports the claim being made (don't cherry-pick)
   - Capture: full source title, author(s), publication, date, URL, DOI (for academic), excerpt of supporting passage

3. **Source expert quotes (YMYL only).** Identify experts whose perspectives can be cited:
   - Verify their institutional affiliation
   - Verify their credentials in the relevant field
   - Use quotes from their published work, interviews, or verified statements
   - Capture: name, title, institution, credentials, source URL, quote text

4. **Identify authority websites.** For non-YMYL: 3-5 trusted sites in the vertical. For YMYL: 3-5 institutional sources (medical organizations, government health sites, university research centers).

5. **Map citations to content sections.** Each citation should support a specific claim in a specific section.

### Validation criteria (non-YMYL)

- [ ] 3-5 authority links identified
- [ ] Each citation verified accessible
- [ ] Each citation supports a specific claim
- [ ] Citations mapped to content sections

### Validation criteria (YMYL)

- [ ] 8-10 peer-reviewed citations identified and verified
- [ ] All citations have working URLs and DOI numbers (where applicable)
- [ ] 3-5 expert quotes with full credentials
- [ ] All experts have verified institutional affiliations
- [ ] 3-5 authority website references
- [ ] Each citation mapped to a specific claim in a specific section
- [ ] All links tested for accessibility

### Output format (YMYL)

```markdown
## Phase 7 Output: External Citations (YMYL)

### Peer-reviewed citations
**1. [Citation title]**
- Authors: [list]
- Publication: [journal]
- Year: [year]
- DOI: [DOI]
- URL: [URL]
- Verified accessible: [yes/no]
- Supports claim: "[specific claim from content]"
- Section: [section name]

[... 7-9 more citations ...]

### Expert quotes
**1. [Expert name]**
- Title: [title]
- Institution: [institution]
- Credentials: [credentials]
- Source: [URL or publication]
- Verified: [yes/no]
- Quote: "[exact quote]"
- Section: [section name]

[... 2-4 more experts ...]

### Authority website references
1. [Organization name] — [URL] — [why authoritative]
2. [...]
```

### Output format (non-YMYL)

```markdown
## Phase 7 Output: External Citations

### Authority links
**1. [Source title]**
- Publication: [name]
- URL: [URL]
- Verified accessible: [yes/no]
- Supports claim: "[specific claim]"
- Section: [section name]

[... 2-4 more sources ...]
```

---

## Phase 8 — E-E-A-T and YMYL Compliance Framework (Conditional)

**Purpose:** Apply Google's E-E-A-T (Experience, Expertise, Authoritativeness, Trustworthiness) framework, with stricter requirements for YMYL content.

**Time investment:** ~30 minutes (when activated)

### Activation conditions

This phase is **OPT-IN**. It activates only when:
- The content is YMYL (Phase 7 already determined this)
- The user explicitly requests E-E-A-T compliance
- The content vertical demands credibility signals

If none of those trigger, skip this phase and advance to Phase 9.

### Tasks (when activated)

1. **Experience signals.** What practical, first-hand experience signals can the content surface?
   - Author has used the product/service being discussed
   - Author has lived through the situation being described
   - Original photography, screenshots, demonstrations
   - "I tried X for 30 days and here's what happened" framing where genuine

   Specify: which sections include experience signals and what form they take.

2. **Expertise signals.** What credentials and depth-of-knowledge markers will appear?
   - Author bio with credentials in the relevant field
   - Citations to academic/peer-reviewed sources (already covered in Phase 7)
   - Technical depth that demonstrates expertise
   - Use of specialist terminology with appropriate accessibility

3. **Authoritativeness signals.** What institutional credibility markers will appear?
   - Author affiliations with recognized institutions
   - Citations to authority sources (already covered in Phase 7)
   - Awards, certifications, industry recognition
   - Quotes from recognized experts (Phase 7)

4. **Trustworthiness signals.** What transparency and safety markers will appear?
   - Clear authorship attribution
   - Transparent sourcing for all factual claims
   - "Last reviewed" or "Last updated" date prominent
   - Disclaimer language for YMYL content (medical disclaimer, financial disclaimer, legal disclaimer as appropriate)
   - Safety-first approach: warnings before suggestions in safety-relevant areas

### Validation criteria

- [ ] Experience signals defined with specific section placement
- [ ] Expertise signals defined with specific markers
- [ ] Authoritativeness signals defined with specific institutional references
- [ ] Trustworthiness signals defined with specific transparency markers
- [ ] For YMYL: appropriate disclaimer language drafted
- [ ] For YMYL health: safety-first language requirements specified

### Output format

```markdown
## Phase 8 Output: E-E-A-T Compliance Framework

### Experience
- Signal 1: [description, section placement]
- Signal 2: [description, section placement]
[...]

### Expertise
- Signal 1: [credential or knowledge marker]
- Signal 2: [...]

### Authoritativeness
- Marker 1: [institutional reference]
- Marker 2: [...]

### Trustworthiness
- Marker 1: [transparency element]
- Marker 2: [...]

### YMYL-specific (if applicable)
- Disclaimer language: "[draft language]"
- Safety-first requirements: [specifications]
- "Last reviewed" date placement: [where]
```

---

## Phase 9 — Final Brief Generation & Quality Assurance

**Purpose:** Integrate all phase outputs into a final comprehensive brief.

**Time investment:** ~45 minutes

### Tasks

1. **Apply the standard output format.** See `references/output-format.md` for the section-by-section template.

2. **Integrate all phase outputs.** Each section of the final brief draws from one or more phases:
   - Section 1 (Project Specifications) ← Phase 1
   - Section 2 (Technical Requirements) ← Phase 1, Phase 5
   - Section 3 (SEO Strategy & Keywords) ← Phase 1, Phase 3
   - Section 4 (Query Fan-Out) ← Phase 4
   - Section 5 (Content Architecture) ← Phase 5
   - Section 6 (Semantic Keyword Integration) ← Phase 3, Phase 5
   - Section 7 (Internal Links) ← Phase 6
   - Section 8 (External Citations) ← Phase 7
   - Section 9 (Expert Quotes — YMYL) ← Phase 7
   - Section 10 (Brand/Product Integration) ← Phase 1
   - Section 11 (Copywriter Tone Directive) ← Phase 2 (RAID), brand voice
   - Section 12 (E-E-A-T Compliance — YMYL) ← Phase 8
   - Section 13 (YMYL Standards — YMYL) ← Phase 7, Phase 8
   - Section 14 (FAQ Section) ← Phase 4 sub-queries
   - Section 15 (Final Validation Checklist) ← All phases

3. **Write the copywriter tone directive.** Based on Phase 2 (user) and brand voice context:
   - Tone (formal, conversational, empathetic, technical, accessible)
   - Voice attributes (warm, expert, encouraging, neutral)
   - Examples of "do" and "don't" language
   - Reading level target (Flesch-Kincaid grade level)
   - Sentence/paragraph length norms

4. **Conduct final validation.** Run through the validation checklist (`references/validation-checkpoints.md`) one more time. Ensure every phase's outputs are integrated and every requirement is met.

### Validation criteria

- [ ] All 12 standard sections completed (or 14 with YMYL)
- [ ] Phase 1-8 outputs all integrated
- [ ] Copywriter directive specifies tone, voice, examples
- [ ] Final validation checklist included
- [ ] Brief is ready to hand to a copywriter or AI writer for implementation

### Output

The complete brief in the standard format. See `references/output-format.md` for the full section-by-section template.

The brief is delivered as inline markdown by default. If the user requests Excel or Word, generate the corresponding format using the same content structure.
