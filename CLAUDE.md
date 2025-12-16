# SEO Machine - Claude Code Project Guide

## Project Overview
SEO Machine is a Claude Code workspace for creating long-form, SEO-optimized blog content. It provides custom commands, specialized agents, and data integrations.

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

## Development Notes
- Python dependencies in `data_sources/requirements.txt`
- API credentials go in `.env` (never commit this)
- See `examples/castos/` for reference implementation

## Deployment
- Target: Vercel
- Branch: main (your customized version)
- Upstream: TheCraigHewitt/seomachine (fetch only)

## Content Quality Standards
- Minimum 2,000 words (2,500-3,000+ preferred)
- Primary keyword density 1-2%
- 3-5 internal links, 2-3 external authority links
- Meta title 50-60 chars, description 150-160 chars
- 8th-10th grade reading level
