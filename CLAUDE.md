# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Open-source pitch deck generator based on PROJECT_BLUEPRINT.md. This project creates professional pitch decks with 3 variants (Master 20 slides, Regional VC 15 slides, YC 10 slides) using Slidev, Vue components, Chart.js and D3.js visualizations.

## Immutable Foundation
This project is built according to PROJECT_BLUEPRINT.md which should never be modified.
All development must align with this blueprint.

## Deck Variants

The project provides three deck variants:
- **Master Deck** (20 slides) - Comprehensive version for due diligence
- **Regional VC Deck** (15 slides) - Optimized for European investors with capital efficiency focus
- **YC Deck** (10 slides) - Ultra-concise Silicon Valley style with growth metrics focus

## Development Commands

### Initial Setup
```bash
# Install dependencies
npm install

# Start development server
npm run dev
```

### Building and Exporting Presentations
```bash
# Export all deck variants to PDF
npm run export:all

# Export specific variants
npm run export:master    # Export 20-slide master deck
npm run export:regional  # Export 15-slide regional VC deck
npm run export:yc        # Export 10-slide YC deck

# Build for production
npm run build

# Preview built version
npm run preview
```

### Testing and Validation
```bash
# Validate data structure
npm run validate

# Run tests (when implemented)
npm run test
```

## Project Architecture

### Key Technologies
- **Slidev** - Presentation framework for developer-friendly slide creation
- **Vue 3** - Component framework for interactive elements
- **Chart.js & D3.js** - Data visualization libraries
- **Shadcn-inspired styling** - Minimal black/white/gray theme

### Directory Structure
```
pitch-deck/
├── .claude/              # AI assistant workflows and prompts
│   ├── checklists/      # Detailed requirements for each deck variant
│   └── prompts/         # Interview prompts for data collection
├── data/
│   ├── company.yaml     # Startup data (single source of truth)
│   └── translations.yaml # Multi-language support (HR/EN)
├── slides/
│   ├── deck-master.md   # 20-slide comprehensive deck
│   ├── deck-regional.md # 15-slide regional VC deck
│   ├── deck-yc.md      # 10-slide YC-style deck
│   └── components/      # Reusable Vue components
├── theme/
│   └── shadcn-style.css # Minimal design system
└── public/
    └── assets/          # Images, logos, and static files
```

### Data Flow
1. All startup information is stored in `data/company.yaml`
2. Slide decks (`.md` files) read from this YAML data
3. Vue components render charts and visualizations
4. Slidev compiles everything into presentations

## Implementation Workflow

### Phase 1: Project Initialization
Set up the folder structure, install dependencies, and configure package.json with all necessary scripts.

### Phase 2: Data Collection
Use the interview prompts in `.claude/prompts/` to gather startup information and populate `data/company.yaml`.

### Phase 3: Generate Master Deck
Create the comprehensive 20-slide presentation following `.claude/checklists/master-deck-checklist.md`.

### Phase 4: Create Regional VC Version
Adapt the master deck to 15 slides following `.claude/checklists/regional-vc-checklist.md`, emphasizing capital efficiency and conservative projections.

### Phase 5: Create YC Version
Distill to 10 ultra-concise slides following `.claude/checklists/yc-checklist.md`, focusing on growth metrics and $1B+ potential.

### Phase 6: Language Support
Implement bilingual support (Croatian/English) using translations.yaml for regional market needs.

## Key Components

### Chart.vue
Handles both Chart.js (line/bar charts) and D3.js (TAM/SAM/SOM circles) visualizations.

### MetricCard.vue
Displays key metrics with formatting options (currency, percentage, number) and growth indicators.

### MarketSize.vue
Visualizes market opportunity with TAM/SAM/SOM breakdown.

## Design Guidelines

- **Minimal aesthetic** - Black, white, and gray color scheme
- **Professional typography** - Inter font family
- **Clear hierarchy** - Consistent spacing and sizing
- **Data-focused** - Emphasis on metrics and visualizations
- **No unnecessary decorations** - Content over style

## Important Considerations

1. **Public Repository** - Everything is transparent and MIT licensed
2. **Example Data** - Use realistic but generic data that others can learn from
3. **Reusability** - Design components and structures to be easily customizable
4. **Documentation** - Maintain comprehensive docs for community use
5. **Accessibility** - Ensure presentations work across devices and export properly to PDF

## Common Tasks

### Adding a New Slide
1. Edit the appropriate deck file in `slides/`
2. Use Slidev markdown syntax
3. Import Vue components as needed
4. Test in development mode before exporting

### Updating Company Data
1. Edit `data/company.yaml`
2. All decks automatically reflect changes
3. Validate data structure with `npm run validate`

### Creating Custom Components
1. Add new Vue component to `slides/components/`
2. Follow existing component patterns
3. Import in slide markdown files as needed

### Exporting for Investors
1. Ensure all data is up-to-date in `data/company.yaml`
2. Run `npm run export:all` to generate all PDF versions
3. PDFs are created in the project root directory

## Tips for Success

- Start with complete data collection before generating slides
- Use real metrics even if small - authenticity matters
- Follow the checklists strictly - they're based on successful fundraising patterns
- Test PDF exports early to ensure formatting is preserved
- Keep the design minimal to maintain professional appearance