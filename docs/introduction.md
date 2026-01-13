# Introduction to Perplexity AI

Understanding how Perplexity works is essential to using it effectively. This guide explains the fundamental architecture and why it requires different prompting strategies than ChatGPT or Claude.

---

## What is Perplexity AI?

Perplexity is an **AI-native search engine** built on **Retrieval-Augmented Generation (RAG)** architecture. Unlike traditional chatbots, it doesn't just rely on pre-trained knowledge—it actively searches the internet, retrieves relevant sources, and synthesizes information with citations.

**Think of it as:** Google's search capability + ChatGPT's synthesis ability + automatic citations

---

## How RAG Architecture Works

### Traditional LLMs (ChatGPT, Claude)
```
User Query → Model Weights → Generated Answer
```
- **Knowledge source:** Pre-trained parameters (frozen at training cutoff)
- **Strengths:** Reasoning, creativity, code generation
- **Weaknesses:** Outdated info, no citations, hallucinations

### Perplexity's RAG Approach
```
User Query → Internet Search → Retrieve Sources → Synthesize with LLM → Cited Answer
```
- **Knowledge source:** Real-time internet + model reasoning
- **Strengths:** Current info, citations, fact-finding
- **Weaknesses:** Limited reasoning depth, search quality dependent

---

## Key Architectural Differences

| Aspect | Perplexity (RAG) | ChatGPT (Parametric) |
|--------|------------------|----------------------|
| **Knowledge** | External (internet) | Internal (weights) |
| **Recency** | Always current | Fixed cutoff date |
| **Citations** | Automatic | None |
| **Search** | Multi-source retrieval | Pattern matching |
| **Accuracy** | Source-dependent | Training-dependent |
| **Best use** | Factual research | Creative reasoning |

---

## Research Mode: Deep RAG

Perplexity's **Research Mode** takes RAG further:

1. **Multiple search passes** - Performs 5-10 searches instead of 1-2
2. **Hundreds of sources** - Reads 100+ pages vs. ~10 in normal mode
3. **Iterative synthesis** - Multiple RAG cycles to refine understanding
4. **Deeper analysis** - Identifies patterns, conflicts, and gaps

**When to use Research Mode:**
- Complex topics requiring comprehensive coverage
- Literature reviews or market research
- When you need to find contradictions or gaps
- Multi-faceted questions with no simple answer

**Cost:** Uses more credits, takes longer (~30-60 seconds)

---

## Why Prompting Strategies Differ

Because Perplexity **searches first, synthesizes second**, your prompts need to be:

### ✅ Search-Optimized
- Specific keywords and context
- Time and source constraints
- Clear scope and boundaries

### ❌ NOT Instruction-Heavy
- Long system prompts don't help
- Few-shot examples over-constrain search
- Complex reasoning instructions are ignored

**Example:**

**Bad (ChatGPT-style):**
```
You are an expert researcher. I want you to analyze climate models 
like you would for a scientific journal. Use a formal tone and 
provide detailed explanations with examples similar to IPCC reports.
```

**Good (Perplexity-optimized):**
```
Climate prediction models for urban planning after 2023, 
focusing on peer-reviewed sources from Nature Climate Change or Science
```

---

## The Search-Synthesis Pipeline

Understanding the internal flow helps you craft better prompts:

### Step 1: Query Understanding
Perplexity extracts:
- **Core topic** (what to search for)
- **Constraints** (time, source, type)
- **Intent** (comparison, verification, discovery)

### Step 2: Search Execution
- Generates search queries (often multiple)
- Retrieves top results from web/databases
- Filters by constraints (date, source, etc.)

### Step 3: Source Reading
- Extracts relevant passages
- Identifies key claims and evidence
- Notes contradictions or gaps

### Step 4: Synthesis
- LLM combines information from sources
- Generates coherent answer
- Adds citations for each claim

### Step 5: Presentation
- Formats with markdown
- Links to original sources
- Provides follow-up suggestions

**Your prompt influences Steps 1-2 most directly**, which is why search-optimization matters more than synthesis instructions.

---

## Focus Modes: Specialized Search Behavior

Perplexity offers different "lenses" that change search behavior:

| Mode | Search Targets | Best For |
|------|---------------|----------|
| **All** | General web | Broad queries |
| **Academic** | Scholarly databases | Research papers |
| **Writing** | Editorial content | Creative research |
| **Video** | YouTube, video platforms | Tutorials, demos |
| **Social** | Reddit, X, LinkedIn | Community sentiment |
| **Finance** | Market data, filings | Company research |

**Pro tip:** You can switch modes mid-conversation to pivot search direction without losing context.

---

## Spaces & Labs: Persistent Workflows

### Spaces
- **What:** Workspaces with standing instructions
- **Use for:** Recurring research workflows
- **Example:** "Competitive intelligence space" that always searches specific sources

### Labs
- **What:** Automated report generation
- **Use for:** Structured, repeatable analysis
- **Example:** "Weekly AI news digest" that formats results consistently

Both allow you to **encode your prompting strategy once** and reuse it.

---

## Limitations to Understand

Perplexity is powerful but not perfect:

### 1. Search Quality Dependency
- Can only synthesize what it finds
- Obscure topics may have poor sources
- AI-generated spam sites can pollute results

### 2. Limited Reasoning Depth
- Not designed for complex multi-step reasoning
- Better at "what" than "why" or "how"
- Struggles with hypotheticals

### 3. Citation Accuracy
- Sometimes misattributes quotes
- May cite irrelevant sections of pages
- Can't distinguish high/low quality sources automatically

### 4. No Memory of External Context
- Can't access your files or previous conversations (unless in same thread)
- No awareness of your specific situation
- Requires explicit context in each query

**Mitigation:** Use Perplexity for research, then use ChatGPT/Claude for reasoning and analysis.

---

## The Complementary Workflow

**Best practice:** Use Perplexity and ChatGPT together

```
1. Research in Perplexity
   ↓
2. Verify citations manually
   ↓
3. Cross-check claims in ChatGPT
   ↓
4. Synthesize insights in ChatGPT
   ↓
5. Use Perplexity to fill gaps
```

**Example:**
- **Perplexity:** "Find recent studies on remote work productivity"
- **Verify:** Click citations, check if quotes are accurate
- **ChatGPT:** "Analyze these 5 studies and identify methodological differences"
- **Perplexity:** "Find critiques of [specific methodology] in remote work research"

This workflow combines **Perplexity's factual retrieval** with **ChatGPT's reasoning ability**.

---

## Key Takeaways

1. **Perplexity is a search engine**, not a reasoning engine
2. **RAG architecture** means it searches first, synthesizes second
3. **Prompts should be search-optimized**, not instruction-heavy
4. **Research Mode** provides deeper, multi-pass analysis
5. **Focus Modes** change search behavior for specialized needs
6. **Always verify** citations and cross-check with other tools
7. **Use complementarily** with ChatGPT/Claude for best results

---

**Next:** Learn the [8 Core Strategies](core-strategies.md) for effective prompting →

[Back to README](../README.md)
