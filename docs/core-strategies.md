# Core Prompting Strategies for Perplexity

These 8 strategies form the foundation of effective Perplexity prompting. Each is explained with examples, rationale, and common pitfalls.

---

## Strategy 1: Add Context (A Little Goes a Long Way)

### The Principle
Simple additional words drastically improve precision. Perplexity uses context to refine search queries and filter results.

### Examples

#### ❌ Too Vague
```
climate models
```
**Result:** Generic overview of climate modeling

#### ✅ With Context
```
climate prediction models for urban planning
```
**Result:** Specific models used by city planners, with practical applications

#### ✅ Even Better
```
climate prediction models for urban planning in coastal cities
```
**Result:** Highly targeted to sea-level rise and flood modeling

### Why It Works
- Narrows search space to relevant sources
- Helps Perplexity understand your intent
- Filters out tangential information

### Common Pitfalls
- ❌ Adding too much context (becomes over-constrained)
- ❌ Using jargon without explanation
- ❌ Mixing multiple unrelated contexts

### Pro Tip
Add just enough context to disambiguate. If "climate models" could mean weather, economics, or environmental—specify which.

---

## Strategy 2: Avoid Few-Shot Prompting

### The Principle
Unlike ChatGPT, Perplexity **over-weights examples** you provide. If you say "like the Louvre," it will only fetch Louvre-like content, missing other relevant results.

### Examples

#### ❌ With Few-Shot Example
```
Find art museums like the Louvre with extensive Renaissance collections
```
**Result:** Only returns museums similar to the Louvre (large, European, classical)

#### ✅ Without Example
```
Find art museums with extensive Renaissance collections
```
**Result:** Broader range including Uffizi, Prado, Metropolitan, etc.

### Why It's Different from ChatGPT
- **ChatGPT:** Uses examples to understand output format/style
- **Perplexity:** Uses examples as search filters, narrowing results

### When Examples Are OK
- Specifying **types** not instances: "peer-reviewed journals" ✅
- Negative constraints: "not opinion pieces" ✅
- Format requirements: "like a table" ✅

### Common Pitfalls
- ❌ "Companies like Tesla" → misses non-EV companies
- ❌ "Studies similar to [specific paper]" → ignores contradictory research
- ❌ "Blogs like [example]" → limits to that blog's style/topic

---

## Strategy 3: Use Search-Control Parameters

### The Principle
State constraints explicitly in plain language to control what Perplexity searches.

### Time Filters

#### Examples
```
after October 2024
before 2023
between January 2023 and June 2024
in the last 30 days
published in 2024
```

#### Why It Matters
- **Recency:** Tech/news topics change rapidly
- **Historical:** Research specific time periods
- **Comparison:** "Before vs after" analyses

### Source Filters

#### Examples
```
from Reuters, NYT, and Wired only
using peer-reviewed sources
from official company announcements
exclude blog posts and opinion pieces
from journals with impact factor > 5
```

#### Why It Matters
- **Quality control:** Filter out low-quality sources
- **Bias awareness:** Specify diverse perspectives
- **Verification:** Stick to authoritative sources

### Depth Controls

#### Examples
```
comprehensive analysis
brief overview
detailed technical breakdown
surface-level summary
```

### Combined Example
```
Tesla's battery technology developments 
after Q3 2024
from industry publications and peer-reviewed journals only
with detailed technical specifications
```

### Common Pitfalls
- ❌ Forgetting time constraints on rapidly evolving topics
- ❌ Not specifying source quality for critical research
- ❌ Over-constraining (no results found)

---

## Strategy 4: Ask for Multiple Perspectives

### The Principle
Force triangulation instead of accepting a single synthesized answer. This reveals conflicts, biases, and gaps.

### Examples

#### ❌ Single Perspective
```
What are the benefits of remote work?
```
**Result:** Generic list of benefits, no nuance

#### ✅ Multiple Perspectives
```
Compare at least 3 peer-reviewed studies on remote work productivity 
and highlight conflicts in their conclusions
```
**Result:** Reveals methodological differences, contradictory findings, and research gaps

#### ✅ Stakeholder Perspectives
```
How do employees, managers, and executives view return-to-office mandates? 
Cite specific surveys or studies for each group.
```
**Result:** Shows divergent interests and perspectives

### Variations

**Temporal comparison:**
```
Compare expert predictions about AI from 2020 vs actual developments in 2024
```

**Geographic comparison:**
```
How do US, EU, and China approach AI regulation? Highlight key differences.
```

**Methodological comparison:**
```
Compare quantitative vs qualitative research on [topic]. What does each reveal?
```

### Why It Works
- Prevents confirmation bias
- Reveals uncertainty and debate
- Provides fuller picture of complex topics

### Common Pitfalls
- ❌ Not specifying how many perspectives (Perplexity may only show 1-2)
- ❌ Asking for "balanced view" (too vague)
- ❌ Not asking to highlight conflicts

---

## Strategy 5: Progressive Deepening

### The Principle
Start broad to map the landscape, then refine iteratively. This mirrors natural research flow and builds context.

### The Three-Round Pattern

#### Round 1: Map the Landscape
```
Overview of quantum computing applications in drug discovery
```
**Goal:** Understand the field, key players, main approaches

#### Round 2: Drill Down
```
Focus on the protein folding applications you mentioned. 
Which companies are leading this space?
```
**Goal:** Narrow to specific sub-topic, identify leaders

#### Round 3: Get Specific
```
Compare D-Wave and IBM's approaches to protein folding. 
What are the key technical differences?
```
**Goal:** Deep dive into specific comparison

### Why It Works
- Each round builds on previous context
- Allows you to discover what's interesting mid-search
- More natural than trying to specify everything upfront

### Advanced Pattern: The Funnel

```
Round 1: "AI in healthcare" (broad)
Round 2: "Focus on diagnostic imaging" (narrower)
Round 3: "Radiology AI for lung cancer detection" (specific)
Round 4: "FDA-approved radiology AI tools for lung cancer" (precise)
```

### Common Pitfalls
- ❌ Jumping to Round 3 without context
- ❌ Not building on previous responses
- ❌ Asking the same question repeatedly (refine instead)

---

## Strategy 6: Specify Output Constraints

### The Principle
Demand evidence, citations, and specific formats to reduce hallucinations and improve verifiability.

### Evidence Requirements

#### Examples
```
Provide evidence for each claim
Cite paragraph or page numbers
Link to original sources
Include direct quotes
Show methodology for each study cited
```

#### Why It Matters
- Forces Perplexity to ground claims in sources
- Makes verification easier
- Reduces unsupported synthesis

### Format Constraints

#### Examples
```
Present as a comparison table
List pros and cons separately
Organize chronologically
Group by category
Provide bullet-point summary
```

### Verification Constraints

#### Examples
```
For each claim, cite at least 2 independent sources
Highlight where sources disagree
Note confidence level for each finding
Indicate which claims lack strong evidence
```

### Combined Example
```
Benefits of intermittent fasting according to peer-reviewed studies.
For each benefit:
- Cite specific study with publication date
- Include sample size and methodology
- Note any contradictory findings
- Provide direct quotes from conclusions
```

### Common Pitfalls
- ❌ Not asking for page numbers (hard to verify)
- ❌ Accepting "according to experts" without names
- ❌ Not demanding multiple sources for important claims

---

## Strategy 7: Use Focus Modes Strategically

### The Principle
Switch modes mid-conversation to redirect Perplexity's search behavior without clearing context.

### Available Modes

| Mode | Search Targets | Best For |
|------|---------------|----------|
| **All** | General web | Broad queries, mixed sources |
| **Academic** | Scholarly databases, journals | Research papers, citations |
| **Writing** | Editorial, creative content | Style research, examples |
| **Video** | YouTube, video platforms | Tutorials, demonstrations |
| **Social** | Reddit, X, LinkedIn | Community opinions, trends |
| **Finance** | Market data, SEC filings | Company research, financials |

### Strategic Switching

#### Example Workflow
```
[Academic Mode]
"Latest research on CRISPR gene editing safety"

[Switch to Social Mode]
"What are researchers saying about CRISPR safety on Twitter/X?"

[Switch to Finance Mode]
"Which CRISPR companies are publicly traded and how are they valued?"
```

### When to Switch

- **Academic → Social:** From formal research to community discussion
- **All → Finance:** From general info to market data
- **Social → Academic:** From sentiment to evidence
- **All → Video:** From text to visual demonstrations

### Common Pitfalls
- ❌ Staying in wrong mode (Academic for news, All for papers)
- ❌ Not knowing modes exist
- ❌ Clearing conversation instead of switching modes

---

## Strategy 8: Use Spaces/Labs for Recurring Workflows

### The Principle
Create reusable workspaces with standing instructions for tasks you do repeatedly.

### Spaces: Custom Workflows

#### Example: Competitive Intelligence Space
```
Standing instructions:
- Always search company websites, press releases, and industry publications
- Focus on last 6 months unless specified
- Compare to top 3 competitors
- Highlight pricing, features, and market positioning
- Cite all claims with links
```

**Usage:** Just ask "Analyze [company]" and it follows the workflow

#### Example: Academic Research Space
```
Standing instructions:
- Use Academic mode by default
- Only cite peer-reviewed sources
- Include impact factor and citation count
- Note methodology and sample size
- Highlight contradictory findings
```

### Labs: Automated Reports

#### Example: Weekly AI News Digest
```
Configuration:
- Search AI news from last 7 days
- Focus on: OpenAI, Anthropic, Google, Meta
- Format as: Company → Development → Source
- Exclude: Opinion pieces, speculation
- Include: Product launches, research papers, funding
```

**Result:** Consistent, formatted report every week

### When to Use

- **Spaces:** Flexible workflows you adjust per query
- **Labs:** Fixed reports you run repeatedly

### Common Pitfalls
- ❌ Not using them at all (manual repetition)
- ❌ Making instructions too rigid (no flexibility)
- ❌ Not updating as needs evolve

---

## Combining Strategies

The real power comes from combining multiple strategies:

### Example: Comprehensive Research Query
```
[Strategy 1: Context]
Tesla's battery technology developments

[Strategy 3: Search controls]
after Q3 2024, from industry publications and peer-reviewed journals

[Strategy 4: Multiple perspectives]
Compare Tesla's claims with independent analyses

[Strategy 6: Output constraints]
For each claim, cite specific sources with publication dates and highlight contradictions
```

### Example: Progressive Deep Dive
```
Round 1 [Strategies 1, 3]:
Overview of AI regulation in the EU after 2023

Round 2 [Strategies 4, 6]:
Compare the EU AI Act with US and China approaches. 
Cite specific policy documents for each.

Round 3 [Strategy 7: Switch to Social]:
How are tech companies responding to the EU AI Act on LinkedIn and Twitter?
```

---

## Quick Reference

| Strategy | Key Action | Example Phrase |
|----------|-----------|----------------|
| 1. Context | Add specificity | "for urban planning" |
| 2. No Few-Shot | Avoid examples | ❌ "like Tesla" |
| 3. Search Controls | Filter explicitly | "after 2024, from NYT" |
| 4. Multiple Perspectives | Force comparison | "compare 3 studies" |
| 5. Progressive Deepening | Iterate | Round 1 → 2 → 3 |
| 6. Output Constraints | Demand evidence | "cite page numbers" |
| 7. Focus Modes | Switch context | Academic → Social |
| 8. Spaces/Labs | Reuse workflows | Create standing instructions |

---

**Next:** Explore [Advanced Techniques](advanced-techniques.md) for power users →

[Back to README](../README.md) | [Previous: Introduction](introduction.md)
