# SEO Machine - Claude Code Project Guide

## Project Overview
SEO Machine is a Claude Code workspace for creating long-form, SEO-optimized blog content. It provides custom commands, specialized agents, and data integrations.

**Owner:** ciaranq/seomachine
**Upstream:** TheCraigHewitt/seomachine (fetch-only, no push)

## Quick Start Commands
- `/research [topic]` - Research keywords and competitors
- `/write [topic]` - Create SEO-optimized article (2000-3000+ words)
- `/rewrite [topic]` - Update existing content
- `/analyze-existing [URL]` - Analyze existing post
- `/optimize [file]` - Final SEO optimization pass
- `/performance-review` - Data-driven content prioritization

## Project Structure
```
seomachine/
├── .claude/commands/     # Custom workflow commands
├── .claude/agents/       # Specialized analysis agents
├── context/              # Brand voice, style guide, SEO guidelines
├── data_sources/         # Analytics integrations (GA4, GSC, DataForSEO)
│   └── modules/          # Python analysis modules (tested & working)
├── topics/               # Raw topic ideas
├── research/             # Research briefs and analysis
├── drafts/               # Work in progress articles
├── published/            # Final versions
└── rewrites/             # Updated existing content
```

## Key Context Files (Customize These)
- `context/brand-voice.md` - Your brand voice and messaging
- `context/style-guide.md` - Writing style conventions
- `context/seo-guidelines.md` - SEO requirements
- `context/target-keywords.md` - Keyword research and clusters
- `context/internal-links-map.md` - Pages for internal linking
- `context/features.md` - Product/service features

## Agents Available
- **Content Analyzer** - Comprehensive data-driven analysis
- **SEO Optimizer** - On-page SEO recommendations
- **Meta Creator** - Meta title/description generation
- **Internal Linker** - Strategic internal linking
- **Keyword Mapper** - Keyword placement analysis
- **Editor** - Human-sounding content transformation
- **Performance** - Analytics-driven prioritization

## Python Analysis Modules
All modules tested and working (Python 3.9+):

| Module | Purpose |
|--------|---------|
| `readability_scorer.py` | Flesch scores, grade levels, passive voice |
| `keyword_analyzer.py` | Density, stuffing detection, LSI keywords |
| `seo_quality_rater.py` | 0-100 SEO scoring with category breakdown |
| `search_intent_analyzer.py` | Classifies informational/commercial/transactional/navigational |
| `content_length_comparator.py` | SERP competitor word count analysis |
| `content_scrubber.py` | AI watermark removal |

Install dependencies: `pip3 install -r data_sources/requirements.txt`

## Development Notes
- Python 3.9+ required
- API credentials go in `.env` (never commit this)
- See `examples/castos/` for reference implementation

## Git Workflow
- **origin** (ciaranq/seomachine): Full push/pull access
- **upstream** (TheCraigHewitt/seomachine): Fetch-only, push disabled
- Pull upstream updates: `git fetch upstream && git merge upstream/main`

## Deployment
- Target: Vercel
- Config: `vercel.json`
- Environment variables configured for GA4, GSC, DataForSEO

## Content Quality Standards
- Minimum 2,000 words (2,500-3,000+ preferred)
- Primary keyword density 1-2%
- 3-5 internal links, 2-3 external authority links
- Meta title 50-60 chars, description 150-160 chars
- 8th-10th grade reading level
