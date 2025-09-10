# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2025-09-10

### Added

#### Core Infrastructure
- **Project Architecture**: Implemented complete Slidev-based presentation framework with Vue 3 component system
- **Package Configuration**: Set up npm package "@pinkainc/pitch-deck-generator" with comprehensive scripts for development, building, and exporting
- **Dependencies**: Integrated Slidev CLI, Chart.js v4.4.0, D3.js v7.8.0, and Vue 3.3.0 for rich data visualization capabilities
- **Development Environment**: Configured hot-reload development server with multi-deck support

#### Design System
- **Theme Implementation**: Created shadcn-inspired minimal design system with CSS custom properties
- **Typography**: Established consistent type scale with Inter font family
- **Color Palette**: Implemented black/white/gray color scheme for professional appearance
- **Layout Components**: Built responsive grid systems (two-cols, three-cols, team-grid)
- **UI Components**: Designed metric cards, progress bars, CTA buttons, and logo walls

#### Vue Components
- **Chart.vue**: Developed unified charting component supporting:
  - Line charts for growth metrics
  - Bar charts for comparisons
  - TAM/SAM/SOM circles using D3.js
  - Responsive and animated visualizations
- **MetricCard.vue**: Created reusable metric display component with:
  - Format support for currency, percentage, and numbers
  - Change indicators for growth metrics
  - Consistent styling across all decks

#### Content & Data
- **Company Data Model**: Established comprehensive YAML structure for startup information including:
  - Company details and branding
  - Problem/solution framework
  - Market analysis and sizing
  - Business model and unit economics
  - Team and advisory information
  - Financial projections and funding details
  - Competition analysis and go-to-market strategy
- **Example Implementation**: Created complete TaskFlow example startup with realistic data
- **Bilingual Support**: Implemented Croatian/English language support for regional markets

#### Presentation Variants
- **Master Deck (20 slides)**: Comprehensive pitch deck including:
  - Executive summary with key metrics
  - Deep problem analysis with quantified impact
  - Product architecture and technical details
  - Complete financial projections
  - Risk analysis and mitigation strategies
  - Exit strategy and comparable analysis
- **Regional VC Deck (15 slides)**: CEE/SEE focused presentation featuring:
  - Bilingual headers (Croatian/English)
  - Regional market context and statistics
  - Capital efficiency emphasis
  - Conservative growth projections
  - Local partnership strategies
- **YC Deck (10 slides)**: Ultra-concise Silicon Valley format with:
  - "X for Y" positioning
  - Week-over-week growth focus
  - Bottom-up TAM calculation
  - Founder-market fit emphasis
  - Clear milestones and use of funds

#### Documentation
- **README.md**: Comprehensive project documentation with quick start guide, feature overview, and usage instructions
- **CONTRIBUTING.md**: Contribution guidelines following open source best practices
- **CHANGELOG.md**: Detailed change tracking following Keep a Changelog format
- **CLAUDE.md**: AI assistant integration guide with workflow instructions and architectural overview

#### Configuration
- **.gitignore**: Comprehensive ignore patterns for Node.js, IDE files, and build artifacts
- **Project Structure**: Organized directory layout separating concerns:
  - `/slides` for presentations
  - `/theme` for styling
  - `/data` for content
  - `/components` for Vue components
  - `/.claude` for AI workflows

### Technical Details
- **Framework**: Slidev v52.1.0 for markdown-based presentations
- **Build System**: Vite-powered build with HMR support
- **Export Formats**: PDF generation via Playwright
- **Browser Support**: Modern browsers with ES6+ support
- **Performance**: Optimized for fast loading and smooth transitions

### Testing
- Verified all three deck variants load without errors
- Confirmed development server starts successfully on multiple ports
- Validated export scripts for PDF generation
- Tested component rendering and data binding

### Known Issues
- CSS engine warning for custom theme (non-blocking, falls back to UnoCSS)

### Migration Notes
This is the initial release establishing the foundation for the open-source pitch deck generator.

## [Unreleased]
- Mobile app showcase components
- Additional chart types (pie, donut, scatter)
- More language translations
- Template marketplace integration
- AI-powered content suggestions
- Real-time collaboration features

---

*This project follows the immutable PROJECT_BLUEPRINT.md specification for consistent development.*