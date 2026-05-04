# Dynamic Density Formula

The mathematical method for deriving keyword count and density from competitor analysis. This is the workflow's core innovation — keyword targets are calculated from competitive reality, not chosen arbitrarily.

---

## Why dynamic calculation matters

Most SEO content advice picks keyword counts arbitrarily: "use the keyword 5-10 times" or "target 2% density." These rules are detached from the actual competitive context.

The dynamic formula instead asks: **what density are competitors actually using to rank for this query?** Then sets a target slightly above that average, so the content has measurable competitive advantage.

This produces three benefits:

1. **Calibrated to the vertical.** A density that wins in one vertical (where competitors heavily optimize) might be insufficient in another (where competitors under-optimize). The formula adapts.

2. **Defensible to the editorial team.** "We targeted 12.7% density because competitors averaged 10.92% and we wanted 16% above" is a defensible decision. "We picked 5 mentions" is not.

3. **Consistent across briefs.** Every brief uses the same method. Output quality is consistent across content writers and projects.

---

## The formula

```
1. Sample N competitor URLs (top 10 ranking for the primary keyword preferred)
2. For each competitor:
   - Fetch the page content
   - Count primary keyword + close variant occurrences
   - Divide by word count → density percentage
3. Calculate competitor average density = sum of all densities ÷ sample size
4. Set target density = competitor average × 1.15 to 1.25
5. Total keyword mentions = target word count × target density
6. Unique keyword count = total mentions ÷ average frequency per keyword (typically 2-4)
```

Each step matters. Skipping or shortcutting compromises the discipline.

---

## Step-by-step explanation

### Step 1 — Sample competitors

**Sample size:** 10 is ideal. 5 is the floor. Below 5, the average becomes too noisy to be reliable.

**Which competitors:** The top 10 organic ranking URLs for the primary keyword. Exclude:
- Ads (sponsored results)
- Aggregators that don't add their own content (some Pinterest/comparison sites)
- Competitor URLs that are very different content types (e.g., a YouTube video ranking when you're producing an article)

**When sampling fails:** If competitors are JS-heavy (content not in raw HTML), paywalled, or bot-blocked, sampling is harder. You can:
- Use rendered HTML via headless browser tools if available
- Manually copy content from public-facing rendered pages
- Sample fewer competitors (5-7) and note the reduced confidence in Phase 3 output

### Step 2 — Measure each competitor's density

**Count the primary keyword.** Search the content for occurrences of the primary keyword. Include:
- Exact matches
- Close variants (singular/plural, capitalization, minor word order changes)

Exclude:
- Distant variants (different intent, different topic)
- Mentions in navigation, footer, sidebar, or unrelated UI elements
- Mentions in author bio or unrelated promotional content

**Count the word count.** The primary content body — title through conclusion. Exclude:
- Navigation and footer
- Author bio (unless integral to content)
- Comment sections
- Related posts widgets

**Calculate density:**
```
density = (keyword count ÷ word count) × 100
```

Express as a percentage. So 30 occurrences in 3,000 words = 1.0% density.

### Step 3 — Calculate competitor average

Sum all measured densities, divide by sample size.

```
average density = (D1 + D2 + ... + DN) ÷ N
```

Note: this is a simple arithmetic mean. If one or two competitors have wildly outlier densities (e.g., one has 25% while others cluster around 8-12%), consider:
- Whether the outlier is a different content type (FAQ page, comparison chart) and should be excluded
- Whether the outlier represents a strategy choice (heavily optimized) vs. an anomaly (auto-generated content)
- If unsure, calculate both with and without the outlier and use judgment

### Step 4 — Set target density

```
target density = competitor average × adjustment factor (1.15 to 1.25)
```

The adjustment factor (15-25% above average) creates measurable competitive advantage without going so high that content becomes keyword-stuffed.

**Choosing within the 15-25% range:**

| Use lower end (1.15) when | Use higher end (1.25) when |
|----------------------------|------------------------------|
| Competitor average is already high (>10%) | Competitor average is moderate (4-8%) |
| Vertical is mature, well-optimized | Vertical is under-optimized |
| Content is short-form (lower densities are natural) | Content is long-form pillar (higher densities sustainable) |
| YMYL where over-optimization risks E-E-A-T | Non-YMYL commercial content |

### Step 5 — Calculate total mentions

```
total mentions = target word count × target density
```

This is the total number of keyword occurrences (including all variants and the primary keyword) that the content should include across its full length.

### Step 6 — Calculate unique keyword count

```
unique keywords = total mentions ÷ average frequency per keyword
```

The denominator (average frequency per keyword) typically lands at 2-4. This reflects natural usage:
- The primary keyword might appear 8-15 times across a long piece
- Secondary keywords appear 2-5 times each
- Tertiary supporting terms appear 1-2 times each

Average across all of them: 2-4 mentions per unique keyword.

**Choosing within the 2-4 range:**
- 2 (low end): more unique terms, broader semantic coverage, useful for topical authority plays
- 4 (high end): fewer unique terms, more concentrated reinforcement of primary themes
- 2.5-3 is the typical sweet spot

---

## Worked example 1 — Long-form pillar (6,000 words)

**Scenario:** A B2B SaaS blog targeting "best CRM for small business." Content is a comprehensive comparison/guide.

**Sample:** Top 10 ranking competitors fetched and measured.

```
Competitor densities:
1. 11.4%
2. 9.8%
3. 12.1%
4. 10.5%
5. 13.2%
6. 9.6%
7. 11.8%
8. 10.3%
9. 12.7%
10. 8.9%

Sum: 110.3
Average: 110.3 ÷ 10 = 11.03%
```

**Target density:** 11.03% × 1.20 = **13.24%** (using 1.20 as middle of 1.15-1.25 range, adjusted for moderate competitive density)

**Total mentions:** 6,000 × 0.1324 = **794 mentions**

**Unique keywords:** 794 ÷ 3 = **~265 unique terms** (using 3 as average frequency for long-form pillar)

**Distribution across architecture:**
- 12 H2 sections × ~60 mentions per section
- Plus 50 in introduction, 50 in conclusion, 100 in FAQ
- Total: 720 + 200 = 920 (close to target, allows for natural variation)

---

## Worked example 2 — Mid-form article (2,800 words)

**Scenario:** A consumer lifestyle blog targeting "morning routine for productivity." Content is a tactical guide.

**Sample:** 8 ranking competitors successfully fetched (2 had paywalls).

```
Competitor densities:
1. 6.2%
2. 5.8%
3. 7.4%
4. 6.9%
5. 5.4%
6. 8.1%
7. 6.5%
8. 7.0%

Sum: 53.3
Average: 53.3 ÷ 8 = 6.66%
```

**Target density:** 6.66% × 1.22 = **8.13%** (using 1.22, slightly higher in 1.15-1.25 range because vertical is moderately optimized)

**Total mentions:** 2,800 × 0.0813 = **228 mentions**

**Unique keywords:** 228 ÷ 2.5 = **~91 unique terms** (using 2.5 because mid-form has less room for term diversity)

**Distribution across architecture:**
- 6 H2 sections × ~30 mentions per section = 180
- Plus 25 in introduction, 25 in conclusion = 230 total

---

## Worked example 3 — Short-form post (1,800 words)

**Scenario:** A SaaS product blog targeting "how to set up two-factor authentication." Content is a how-to guide.

**Sample:** Top 5 competitors fetched (highly technical content; some on documentation sites, sample varied).

```
Competitor densities:
1. 4.2%
2. 5.1%
3. 3.8%
4. 4.7%
5. 4.5%

Sum: 22.3
Average: 22.3 ÷ 5 = 4.46%
```

**Target density:** 4.46% × 1.18 = **5.26%** (using 1.18 — lower end because technical how-to content is naturally concise)

**Total mentions:** 1,800 × 0.0526 = **95 mentions**

**Unique keywords:** 95 ÷ 2 = **~48 unique terms** (using 2 — short-form needs term variety)

**Distribution across architecture:**
- 4 H2 sections × ~18 mentions per section = 72
- Plus 12 in introduction, 12 in conclusion = 96 total

---

## What "natural distribution" means

The formula gives a target. But mentions must distribute naturally across the content, not pile up in one section.

**Natural distribution indicators:**
- No section has dramatically more keyword density than the average
- Primary keyword appears in: H1, first paragraph, at least one H2, conclusion, meta description
- Secondary keywords appear in their thematically appropriate sections
- Tertiary terms appear once or twice where contextually relevant
- Reading the content aloud doesn't reveal repetitive language

**Unnatural distribution warning signs:**
- A section with density 3x the average (looks keyword-stuffed)
- The same keyword appearing in 4+ consecutive sentences
- Awkward grammatical contortions to fit a keyword
- Keywords appearing in lists or headers that don't naturally serve the content

If the math produces a number that creates unnatural distribution at the section level, the content architecture (Phase 5) needs adjustment, not the keyword target.

---

## Common pitfalls

### Pitfall 1: Treating the target as a hard floor

The target is what the content *aims for*, not a minimum that must be exceeded. If natural writing lands at 11% when the target was 13%, that's usually fine — overshooting risks keyword stuffing.

### Pitfall 2: Counting only exact matches

Search engines understand semantic variants. "Best CRM" and "top CRM software" are close enough that both count as the keyword for density purposes. Be liberal on close variants; strict on distant variants.

### Pitfall 3: Sampling competitors that aren't real competitors

If the top 10 SERP for your query includes 3 government sites, 4 forum threads, and 3 commercial articles, sampling all 10 is misleading. The forum threads and government sites use language differently. Sample the 3 commercial articles or articles from competitors who match your content type.

### Pitfall 4: Skipping the math under time pressure

The formula takes 30-60 minutes done properly. The temptation under time pressure is to skip the sampling step and just pick a number. This defeats the entire point of the workflow. Either commit to the discipline or use a different (lighter) workflow.

### Pitfall 5: Confusing density with keyword stuffing

Density of 12% sounds high in the abstract, but it includes all variants of the primary keyword across thousands of words. In a 6,000-word piece at 12% density (720 mentions across 318 unique terms), each term averages 2-3 mentions. That's not stuffing — that's normal long-form content.

Stuffing is concentration in a small space, not aggregate count across long content.

---

## When NOT to use the dynamic formula

The formula is calibrated for substantive briefs targeting competitive queries. Use lighter approaches when:

- The query has fewer than 3 commercial competitors (no meaningful average)
- The content is so short (under 800 words) that density math becomes noisy
- The content is news or time-sensitive (competitive density isn't the right framing)
- The content is internal documentation or knowledge-base material (ranking isn't a goal)

In those cases, default to common-sense keyword usage: primary keyword in H1, opening paragraph, 1-2 subheadings, and naturally throughout. Skip the formula.
