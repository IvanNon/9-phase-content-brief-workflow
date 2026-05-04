# Validation Checkpoints

Phase-by-phase validation criteria and what to do when checkpoints fail. The discipline of validation is what separates briefs that produce ranking content from briefs that produce mediocre output.

---

## Why validation matters

Each phase produces outputs that feed the next phase. If Phase 2's RAID analysis is weak, Phase 5's content architecture will be weak. If Phase 3's keyword math is wrong, Phase 9's final brief will have wrong keyword targets.

Validation checkpoints catch these problems before they propagate. They are quality gates that prevent advancement until the current phase has produced complete, defensible outputs.

The temptation under time pressure is to skip validation. Don't. A weak phase's outputs corrupt every downstream phase. Loop back, fix the gap, re-validate.

---

## Phase 1 validation

**Phase 1 is complete only when ALL of these are met:**

- [ ] Primary keyword identified
- [ ] At least 3 secondary keywords identified (5+ preferred)
- [ ] Top 10 SERP URLs documented (or 5+ if SERP access is limited)
- [ ] Target word count set with rationale
- [ ] Publishing surface and conversion goal specified
- [ ] Success metrics articulated

**Common failure modes:**

| Failure | Cause | Fix |
|---------|-------|-----|
| Only 1-2 secondary keywords identified | Keyword research data was thin | Run additional keyword discovery via web search; pull from "People Also Ask" and related searches |
| SERP URLs blocked or inaccessible | Bot detection, paywalls, JS rendering | Sample fewer competitors but get real ones; note the limitation in output |
| Target word count is "let's say 2000" without rationale | Defaulted instead of analyzed | Look at competitor word counts. If they average 3,500, target should account for that |
| Conversion goal is generic ("traffic") | Conversion path wasn't clarified | Press the user for the specific action: signup, demo, purchase, app install, etc. |

---

## Phase 2 validation

**Phase 2 is complete only when:**

- [ ] RAID 4W applied with substantive answers in all four dimensions
- [ ] Intent distribution percentages defined and sum to 100%
- [ ] User journey mapped across at least 3 stages
- [ ] At least 3 specific pain points identified
- [ ] Pain points are concrete, not generic

**The "specificity test":** Each RAID dimension and each pain point should fail this test as written:

> *"This same description could apply to most queries in this vertical."*

If yes, the answer is too generic. Force specificity.

**Common failure modes:**

| Failure | Cause | Fix |
|---------|-------|-----|
| RAID answers feel right but are generic | Skipped the SERP/forum read | Spend 15 minutes reading top-ranking articles and 1-2 forum threads; rewrite RAID with specific user voice |
| Intent distribution doesn't sum to 100% | Math error | Check the math, redistribute |
| Only 1-2 pain points identified | User hasn't been imagined deeply | Look at SERP gaps. Look at forum complaints. Pain points are everywhere if you look |
| Pain points are generic ("information overload") | Avoided specifics | "Users can't find a single source comparing X across Y dimensions" is concrete. Force concrete framings |

---

## Phase 3 validation

**Phase 3 is complete only when:**

- [ ] At least 5 competitors sampled (10 preferred)
- [ ] Competitor average density calculated and shown
- [ ] Target density set 15-25% above competitor average
- [ ] Total mention count calculated mathematically (not arbitrary)
- [ ] Unique keyword count derived from total mentions ÷ frequency
- [ ] Keyword clusters defined with section allocation plan
- [ ] Average mentions per keyword maintained at 2-4 for natural integration

**Common failure modes:**

| Failure | Cause | Fix |
|---------|-------|-----|
| Couldn't fetch enough competitors | JS-rendered content, paywalls | Use rendered HTML if available; sample 5+ if 10 isn't possible; note reduced confidence |
| One outlier competitor skews the average | Auto-generated content or different content type in sample | Recalculate with and without outlier; use judgment on which to use |
| Target density chosen outside 15-25% range | Picked a "round number" instead of calculation | Recalculate. The discipline is the formula |
| Unique keyword count feels too high (300+) | Average frequency set too low (1-2) | Reset frequency to 2.5-3 for long-form, 2-2.5 for mid-form |
| Unique keyword count feels too low (under 30) | Average frequency set too high (5+) | Reset frequency to 3-4. High frequencies risk keyword stuffing |

---

## Phase 4 validation

**Phase 4 is complete only when:**

- [ ] 6-10 sub-queries identified (8 is the sweet spot)
- [ ] Each sub-query has search volume data OR explicit acknowledgment that volume data wasn't available
- [ ] Each sub-query mapped to a target content section
- [ ] Integration approach defined for each
- [ ] At least 2-3 sub-queries address gaps that competitors don't cover well

**Common failure modes:**

| Failure | Cause | Fix |
|---------|-------|-----|
| Only 3-4 sub-queries identified | Didn't look beyond PAA | Sources beyond PAA: related searches, autocomplete, competitor subheadings, forum questions, AI Overview citations |
| Sub-queries have no volume data | Tools weren't queried | Even rough volume estimates are better than nothing; note "volume estimated from related queries" |
| Sub-queries duplicate primary keyword content | Selected too close to primary | Pick sub-queries that EXPAND coverage, not duplicate it |
| All sub-queries are well-covered by competitors | Selected obvious topics | Hunt for gaps. Where are competitors weak? Where do they all say the same thing? Where does the user need depth that nobody provides? |

---

## Phase 5 validation

**Phase 5 is complete only when:**

- [ ] H1 drafted with primary keyword integration
- [ ] All H2 sections outlined with subtopic coverage
- [ ] H3/H4 added where depth requires
- [ ] Word count allocated per section, summing to target ±10%
- [ ] Each section has primary keyword and cluster mapping
- [ ] All Phase 4 sub-queries placed in specific sections
- [ ] Visual element plan specifies 1 element per ~500-800 words minimum
- [ ] Architecture supports natural reading flow

**Common failure modes:**

| Failure | Cause | Fix |
|---------|-------|-----|
| Word count allocation doesn't sum to target | Distribution drift | Recalculate. Adjust H2 allocations to match target |
| Some H2s have unclear subtopics ("Tips", "Conclusion") | Filler sections | Replace with specific topical H2s. "Tips" is not a topic; "Common mistakes to avoid" is |
| Sub-queries from Phase 4 not all placed | Forgot to map them | Map each sub-query to its section. If a sub-query has no logical home, the architecture might need an H2 added |
| Visual plan is "add some images" | Vague | Specify per section what visual element will appear: hero image, comparison table, callout box, infographic, etc. |
| Architecture doesn't flow logically | Sections in arbitrary order | Reorder. The reader should be able to skim H2s and feel a progression — what they need to know first, then next, then next |

---

## Phase 6 validation

**Phase 6 is complete only when:**

- [ ] 5-10 internal links identified (8 is typical)
- [ ] Each link has destination URL
- [ ] Each anchor text is specific and natural
- [ ] Each link has section-level placement specified
- [ ] Mix of link types (topical, user-journey, conversion)
- [ ] No two links use identical anchor text

**Common failure modes:**

| Failure | Cause | Fix |
|---------|-------|-----|
| Anchor text is generic ("learn more") | Defaulted | Anchor text should describe destination specifically. "Learn more about HSA contribution limits" not "learn more" |
| Links are all topical, no conversion | Forgot conversion path | Add at least 1-2 links to conversion-relevant pages (signup, demo, primary product) |
| Links are all conversion, feels promotional | Over-corrected | Mix should be balanced: 4-5 topical, 2-3 user journey, 1-2 conversion |
| Multiple links use identical anchor text | Lazy | Vary anchor text across the article. Search engines and users notice repetition |
| Links cluster in one section | All placed in conclusion | Distribute across the article. Internal links in body content perform better than only at end |

---

## Phase 7 validation

**Phase 7 validation depends on YMYL status.**

### Non-YMYL validation

- [ ] 3-5 authority links identified
- [ ] Each citation verified accessible
- [ ] Each citation supports a specific claim
- [ ] Citations mapped to content sections

### YMYL validation

- [ ] 8-10 peer-reviewed citations identified and verified
- [ ] All citations have working URLs and DOI numbers (where applicable)
- [ ] 3-5 expert quotes with full credentials
- [ ] All experts have verified institutional affiliations
- [ ] 3-5 authority website references
- [ ] Each citation mapped to a specific claim in a specific section
- [ ] All links tested for accessibility

**Common failure modes:**

| Failure | Cause | Fix |
|---------|-------|-----|
| Couldn't find peer-reviewed citations on the topic | Wrong databases | Try PubMed (medical), Google Scholar (general), JSTOR (humanities/social), Semantic Scholar (CS/AI) |
| Citations support general topic but not specific claims | Cherry-picked | For each claim that needs support, find a citation that specifically supports THAT claim, not the general topic |
| Expert quotes from unverified sources | Used quotes from non-authoritative aggregators | Verify quotes from primary sources: published papers, recorded interviews, institutional statements |
| Citations behind paywall blocking content verification | Couldn't read the actual research | Either find an open-access version, or note "paywall-restricted" in the citation and verify abstract supports the claim |

---

## Phase 8 validation (when activated)

**Phase 8 is complete only when:**

- [ ] Experience signals defined with specific section placement
- [ ] Expertise signals defined with specific markers
- [ ] Authoritativeness signals defined with specific institutional references
- [ ] Trustworthiness signals defined with specific transparency markers
- [ ] For YMYL: appropriate disclaimer language drafted
- [ ] For YMYL health: safety-first language requirements specified

**Common failure modes:**

| Failure | Cause | Fix |
|---------|-------|-----|
| Experience signals are abstract | Hard to demonstrate experience | Use concrete examples: "section X includes user case study," "section Y includes original photograph of [thing]" |
| Expertise signals duplicate authoritativeness | Conflated the two | Expertise = author's depth of knowledge. Authoritativeness = institutional weight (citations, affiliations) |
| Trustworthiness markers are missing safety language for YMYL health | Skipped because uncomfortable | Health YMYL requires explicit safety language. Don't skip |
| Disclaimer is generic boilerplate | Used template | Tailor to specific content. "Not medical advice, consult professional" works for general health; legal/financial need vertical-specific phrasing |

---

## Phase 9 validation

**Phase 9 is complete only when:**

- [ ] All 12 standard sections completed (or 14 with YMYL)
- [ ] Phase 1-8 outputs all integrated
- [ ] Copywriter directive specifies tone, voice, examples
- [ ] Final validation checklist included
- [ ] Brief is ready to hand to a copywriter or AI writer for implementation

**Common failure modes:**

| Failure | Cause | Fix |
|---------|-------|-----|
| Some phase outputs not integrated | Lost track during integration | Cross-check: every Phase 1-8 output should appear somewhere in the final brief |
| Copywriter directive is generic ("write engagingly") | Skipped the specifics | Tone, voice attributes, do/don't examples, reading level target, sentence length norms — be specific |
| Brief is missing FAQ section | Forgot Phase 4 sub-queries can populate FAQ | Use unanswered sub-queries from Phase 4 as FAQ questions |
| Validation checklist not included | Treated as optional | Include it. The copywriter and editor will use it as a self-check |

---

## What to do when a phase repeatedly fails validation

If you keep looping back on the same phase without progress:

**1. Identify the specific failed criterion.** Not "the phase is incomplete," but "criterion X failed because Y."

**2. Determine if it's a data problem or a discipline problem.**
- Data problem: missing inputs that aren't recoverable. Example: SERP is paywalled, can't sample. Solution: proceed with reduced data and note the limitation.
- Discipline problem: enough data exists, you're just rushing. Solution: slow down and do the work.

**3. If it's a data problem, document and proceed.** Don't skip validation entirely; document what couldn't be validated and why. This honesty is part of the workflow's value.

**4. If it's a discipline problem, take a break.** Brief generation requires sustained attention. If you've been working on this brief for hours without progress, step away for 30 minutes and return fresh.

**5. If a phase keeps failing across multiple attempts on different briefs, the workflow itself may need calibration for your context.** Maybe Phase 4's "8 sub-queries" target is wrong for your vertical. Maybe Phase 7's citation requirements are unrealistic for your topic. Adjust the workflow to your reality, but document the deviation.

---

## What "good enough" means

The validation criteria are not aspirational. They're the floor. A brief that meets all criteria isn't excellent — it's *acceptable*. Excellence comes from RAID specificity, citation quality, architecture coherence, and copywriter directive depth.

Don't confuse "passed validation" with "this is a great brief." It means "this brief is ready to advance to the next phase or to the copywriter." Quality is a separate dimension from completeness.
