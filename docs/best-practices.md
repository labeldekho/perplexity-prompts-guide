# Best Practices: Avoiding Hallucinations & Validating Results

Perplexity is powerful but not infallible. This guide teaches you to validate results, spot hallucinations, and maintain research integrity.

---

## Understanding Perplexity's Limitations

### Why Perplexity Can Still Hallucinate

1. **AI-Generated Content Pollution**
   - Can't distinguish real content from AI spam sites
   - SEO-optimized fake content ranks high in searches
   - Circular citations (AI content citing AI content)

2. **Citation Misattribution**
   - May cite correct source but wrong section
   - Can misinterpret source's actual claim
   - Sometimes invents quotes or page numbers

3. **Synthesis Errors**
   - May combine facts from different contexts incorrectly
   - Can create false connections between unrelated claims
   - Might over-generalize from limited sources

4. **Source Quality Blindness**
   - Treats all web sources equally initially
   - Can't automatically assess credibility
   - May prioritize recent over authoritative

---

## The Verification Framework

### Level 1: Quick Sanity Checks (30 seconds)

✅ **Check source count**
- Single source? → High risk
- 2-3 sources? → Moderate confidence
- 5+ diverse sources? → Higher confidence

✅ **Check source types**
- All blogs? → Verify elsewhere
- Mix of academic + news + official? → Better
- Peer-reviewed only? → Strongest (for research)

✅ **Check dates**
- All sources from same time? → Possible echo chamber
- Spread over time? → More robust
- Recent for time-sensitive topics? → Essential

✅ **Check for direct quotes**
- No quotes? → Synthesis risk
- Quotes with page numbers? → Verifiable
- Vague attributions? → Red flag

### Level 2: Citation Verification (2-5 minutes)

✅ **Click through to sources**
- Does the page exist?
- Is the cited section actually there?
- Does it say what Perplexity claims?

✅ **Search exact quotes**
- Copy quote into Google
- Does it appear on the cited page?
- Is the context the same?

✅ **Check author credentials**
- Who wrote the source?
- What's their expertise?
- Any conflicts of interest?

### Level 3: Cross-Verification (5-15 minutes)

✅ **Use ChatGPT/Claude**
```
Prompt: "Evaluate this claim: [claim from Perplexity]
Is this accurate based on your training data?
What nuances or caveats should I know?"
```

✅ **Search alternative sources**
- Google Scholar for academic claims
- Official websites for company/policy claims
- Fact-checking sites for controversial claims

✅ **Check for contradictions**
- Search "[claim] debunked" or "[claim] criticism"
- Look for opposing viewpoints
- Verify consensus vs outlier opinion

---

## Red Flags: When to Be Skeptical

### 🚩 Source Red Flags

- **Single obscure blog** as only source
- **No author name** or credentials
- **Recent domain** (< 1 year old) for "authoritative" content
- **Suspiciously perfect** match to your query
- **Circular citations** (sources citing each other)
- **Paywalled sources** you can't verify
- **Broken links** or 404 errors

### 🚩 Content Red Flags

- **"According to experts"** without naming them
- **Vague statistics** without source data
- **Too-good-to-be-true** findings
- **Extreme claims** without extraordinary evidence
- **No caveats or limitations** mentioned
- **Contradicts common knowledge** without explanation
- **Perfect alignment** with your desired answer

### 🚩 Citation Red Flags

- **No page numbers** for long documents
- **No publication date** for time-sensitive claims
- **Generic URLs** (homepage instead of specific page)
- **Mismatched dates** (citing 2020 source for 2024 claim)
- **Quote doesn't appear** when you search the source
- **Context missing** that changes meaning

---

## Best Practices by Use Case

### Academic Research

✅ **DO:**
- Use Academic Mode exclusively
- Verify impact factor of journals
- Check citation counts on Google Scholar
- Read abstracts yourself, don't just trust summary
- Look for systematic reviews and meta-analyses
- Cross-reference with university library databases

❌ **DON'T:**
- Cite Perplexity directly (cite original sources)
- Trust preprints without peer review
- Accept single-study claims
- Ignore methodology sections
- Skip checking for retractions

### Business Intelligence

✅ **DO:**
- Verify numbers with official filings (10-K, earnings)
- Cross-check with multiple financial sources
- Note date of information (markets move fast)
- Distinguish facts from analyst opinions
- Check company press releases directly

❌ **DON'T:**
- Make decisions on single-source data
- Trust stock tips or predictions
- Ignore conflicts of interest
- Assume recent = accurate
- Skip verifying financial figures

### News & Current Events

✅ **DO:**
- Check multiple news outlets
- Note political/ideological bias of sources
- Verify with primary sources when possible
- Check publication timestamps
- Look for updates or corrections

❌ **DON'T:**
- Trust single-source breaking news
- Ignore source bias
- Accept unverified social media claims
- Confuse opinion with reporting
- Skip checking for updates

### Technical/How-To

✅ **DO:**
- Test instructions yourself
- Check version numbers and dates
- Verify with official documentation
- Look for community validation (Reddit, Stack Overflow)
- Note if solution is deprecated

❌ **DON'T:**
- Run code without understanding it
- Ignore security implications
- Trust outdated tutorials
- Skip checking official docs
- Assume one solution fits all contexts

---

## The Cross-Checking Workflow

### Step 1: Get Initial Answer from Perplexity
```
[Your research query with proper constraints]
```

### Step 2: Extract Key Claims
List the 3-5 most important factual claims.

### Step 3: Verify Each Claim

**For each claim:**

1. **Click citation** → Read source directly
2. **Google the claim** → Find alternative sources
3. **ChatGPT check** → "Is this accurate?"
4. **Search contradictions** → "[claim] criticism"

### Step 4: Assess Confidence

- **High confidence:** 5+ quality sources, verified quotes, consensus
- **Medium confidence:** 2-3 sources, plausible, no contradictions found
- **Low confidence:** Single source, unverified, or contradictions exist

### Step 5: Document Uncertainty

Note where evidence is weak or contradictory. Don't overstate confidence.

---

## Using ChatGPT/Claude for Cross-Verification

### Effective Cross-Check Prompts

```
I found this claim on Perplexity: "[claim]"

The sources cited are: [list sources]

Questions:
1. Is this claim accurate based on your knowledge?
2. What important context or caveats am I missing?
3. Are there contradictory findings I should know about?
4. How would you rate the quality of these sources?
```

```
Compare these two claims:
- Perplexity says: "[claim A]"
- This source says: "[claim B]"

Are these contradictory or compatible?
What might explain any differences?
```

### What ChatGPT/Claude Are Good For

✅ Sanity checking factual claims
✅ Identifying missing context
✅ Explaining contradictions
✅ Assessing source quality
✅ Suggesting alternative perspectives

❌ NOT for: Recent events, specific citations, real-time data

---

## Common Hallucination Patterns

### Pattern 1: Invented Statistics
**Example:** "73% of companies use AI" (no source)
**Fix:** Demand specific study with sample size and date

### Pattern 2: Misattributed Quotes
**Example:** Quote attributed to wrong person or source
**Fix:** Search exact quote to find original

### Pattern 3: Conflated Facts
**Example:** Combining facts from different contexts
**Fix:** Verify each fact independently

### Pattern 4: Outdated Information
**Example:** Using 2020 data for 2024 question
**Fix:** Always specify time constraints

### Pattern 5: Circular AI Content
**Example:** AI-generated blog citing AI-generated blog
**Fix:** Trace back to primary sources

---

## Building a Personal Verification Checklist

Customize based on your needs:

### For High-Stakes Decisions
- [ ] Verified all citations by clicking through
- [ ] Found 3+ independent sources
- [ ] Checked with ChatGPT/Claude
- [ ] Searched for contradictions
- [ ] Consulted domain expert if available
- [ ] Documented confidence level and limitations

### For General Research
- [ ] Checked source count and types
- [ ] Verified key claims with spot checks
- [ ] Noted any red flags
- [ ] Cross-checked surprising claims
- [ ] Documented sources for later reference

### For Quick Lookups
- [ ] Sanity check (does this make sense?)
- [ ] Source type check (authoritative?)
- [ ] Date check (recent enough?)

---

## When to Trust Perplexity

**High confidence scenarios:**
- ✅ Multiple authoritative sources agree
- ✅ Direct quotes from primary sources
- ✅ Factual, non-controversial information
- ✅ Recent, well-documented events
- ✅ Academic consensus (in Academic Mode)

**Lower confidence scenarios:**
- ⚠️ Single or obscure sources
- ⚠️ Controversial or disputed claims
- ⚠️ Complex technical details
- ⚠️ Predictions or future-oriented claims
- ⚠️ Synthesis of disparate sources

---

## The 80/20 Rule

**80% of hallucinations come from:**
1. Single-source answers
2. Obscure or low-quality sources
3. Missing time constraints
4. Unverified synthesis
5. Circular AI content

**Fix 80% of issues by:**
1. Demanding multiple sources
2. Filtering for quality sources
3. Adding date constraints
4. Clicking through citations
5. Cross-checking with ChatGPT

---

## Advanced: Detecting AI-Generated Sources

### Red Flags for AI Content

- **Perfect grammar** but shallow content
- **Generic examples** without specifics
- **Listicle format** with obvious points
- **No author bio** or credentials
- **Recent domain** with lots of content
- **Suspiciously comprehensive** coverage
- **No original research** or data

### How to Check

1. **Google the domain** → Check age and reputation
2. **Search exact phrases** → Do they appear elsewhere?
3. **Check "About" page** → Real people? Real company?
4. **Look for original data** → Or just aggregation?
5. **Compare to known sources** → Does it add anything?

---

## Emergency Verification: When You're Unsure

If you're not confident in Perplexity's answer:

1. **Start over with better constraints**
   - Add source filters
   - Specify peer-reviewed or official sources
   - Use Academic Mode

2. **Use alternative tools**
   - Google Scholar for academic
   - Official websites for policies
   - Financial databases for market data

3. **Consult human experts**
   - Domain specialists
   - Librarians for research help
   - Fact-checkers for controversial claims

4. **Document uncertainty**
   - Don't pretend to know what you don't
   - Note confidence levels
   - Explain limitations

---

## Key Takeaways

1. **Always verify** citations by clicking through
2. **Demand multiple sources** for important claims
3. **Cross-check** with ChatGPT/Claude
4. **Watch for red flags** in sources and content
5. **Use Academic Mode** for high-precision needs
6. **Document confidence** levels honestly
7. **When in doubt, verify** with primary sources
8. **No tool is perfect** — human judgment essential

---

**Remember:** Perplexity is a powerful research assistant, not a replacement for critical thinking. Your job is to verify, synthesize, and apply judgment.

---

[Back to README](../README.md) | [Previous: Advanced Techniques](advanced-techniques.md)
