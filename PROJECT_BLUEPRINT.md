# 🚀 Open-Source Pitch Deck Generator - Claude Code Initialization
## Complete Transparent Starter Kit for VC Pitch Decks

---

## INITIALIZATION PROMPT FOR CLAUDE CODE

```
Initialize an open-source pitch deck generator starter kit for the PUBLIC GitHub repository at https://github.com/pinkainc/pitch-deck. 
This is a fully transparent template project under MIT license, designed to help startups create professional pitch decks.
Create a complete working example with realistic but generic data that others can fork and customize for their own startups.
Set up Slidev with support for Master (20 slides), Regional VC (15 slides), and YC (10 slides) pitch decks with Croatian and English support.
```

---

## PROJECT PHILOSOPHY

This is an **open-source starter kit** for creating professional pitch decks. Everything is transparent and public:
- Complete working example with realistic demo data
- Full source code and templates
- Ready to fork and customize
- MIT licensed for maximum reusability
- No hidden or private components

---

## PROJECT STRUCTURE

```
pitch-deck/
├── .github/
│   ├── workflows/
│   │   └── ci.yml              # GitHub Actions for testing
│   └── ISSUE_TEMPLATE/
│       ├── bug_report.md
│       └── feature_request.md
├── .claude/
│   ├── workflow.md             # AI-assisted workflow
│   ├── checklists/
│   │   ├── master-deck-checklist.md
│   │   ├── regional-vc-checklist.md
│   │   └── yc-checklist.md
│   └── prompts/
│       ├── 01-interview.md
│       ├── 02-structure.md
│       └── 03-generate.md
├── data/
│   ├── company.yaml           # Example startup data
│   └── translations.yaml      # HR/EN translations
├── slides/
│   ├── deck-master.md         # Master deck (20 slides)
│   ├── deck-regional.md       # Regional VC deck (15 slides)
│   ├── deck-yc.md            # YC deck (10 slides)
│   └── components/
│       ├── Chart.vue
│       ├── MetricCard.vue
│       └── MarketSize.vue
├── theme/
│   └── shadcn-style.css      # Minimal B&W theme
├── public/
│   └── assets/
│       └── logo-example.svg
├── docs/
│   ├── CUSTOMIZATION.md      # How to customize
│   ├── EXAMPLES.md           # Success stories
│   └── FAQ.md                # Common questions
├── .gitignore                # Standard ignores
├── .env.example              # Environment template
├── package.json
├── README.md                 # Comprehensive docs
├── LICENSE                   # MIT License
└── CONTRIBUTING.md          # How to contribute
```

---

## PACKAGE.JSON

```json
{
  "name": "@pinkainc/pitch-deck-generator",
  "version": "1.0.0",
  "description": "Open-source pitch deck generator for startups",
  "keywords": ["pitch-deck", "startup", "vc", "slidev", "presentation"],
  "homepage": "https://github.com/pinkainc/pitch-deck",
  "bugs": "https://github.com/pinkainc/pitch-deck/issues",
  "license": "MIT",
  "author": "Pinka Inc.",
  "repository": {
    "type": "git",
    "url": "https://github.com/pinkainc/pitch-deck.git"
  },
  "scripts": {
    "dev": "slidev",
    "build": "slidev build",
    "export": "slidev export",
    "export:all": "npm run export:master && npm run export:regional && npm run export:yc",
    "export:master": "slidev export slides/deck-master.md",
    "export:regional": "slidev export slides/deck-regional.md", 
    "export:yc": "slidev export slides/deck-yc.md",
    "preview": "slidev preview",
    "validate": "node scripts/validate.js",
    "test": "echo 'No tests yet'"
  },
  "dependencies": {
    "@slidev/cli": "latest",
    "chart.js": "^4.4.0",
    "d3": "^7.8.0",
    "vue": "^3.3.0"
  },
  "devDependencies": {
    "playwright-chromium": "latest"
  }
}
```

---

## MASTER DECK CHECKLIST

```markdown
# Master Pitch Deck Checklist - Complete Version (20 Slides)
## Pre-seed/Seed Stage - Comprehensive Documentation

### 📋 Pre-Work Requirements
- [ ] Company Basics
  - [ ] Registered company name
  - [ ] Logo in high resolution (PNG/SVG)
  - [ ] Brand colors defined
  - [ ] Consistent font selection
  - [ ] Professional email domain setup
- [ ] Pre-seed Specific Focus (70% team, 30% idea)
  - [ ] Team credibility emphasized
  - [ ] Problem-solution fit validated
  - [ ] Early customer feedback collected
  - [ ] MVP or prototype ready
  - [ ] Domain expertise demonstrated

### Slide 1: Title Slide
- [ ] Company Logo (high quality)
- [ ] Company Name (clearly visible)
- [ ] Tagline (7-10 words max describing what you do)
- [ ] Contact Information
  - [ ] Email address
  - [ ] Phone number
  - [ ] Website URL
  - [ ] LinkedIn profile
- [ ] Date/Version of presentation
- [ ] Confidentiality notice (if needed)

### Slide 2: Executive Summary
- [ ] Mission Statement (1 sentence)
- [ ] Vision Statement (where you're going)
- [ ] Key Metrics (3-4 bullet points)
  - [ ] Current users/customers
  - [ ] Revenue (if any)
  - [ ] Growth rate
  - [ ] Key achievement
- [ ] Funding Ask (amount and use)
- [ ] Investment Highlights (why invest now)

### Slide 3: The Problem
- [ ] Problem Statement (clear, concise)
- [ ] Pain Points (3-5 specific examples)
  - [ ] Quantify the pain (time/money lost)
  - [ ] Real customer quotes/feedback
- [ ] Current Solutions
  - [ ] Why they fail
  - [ ] What's missing
- [ ] Market Evidence
  - [ ] Statistics supporting problem existence
  - [ ] Research/survey data
- [ ] Target Audience who has this problem

### Slide 4: The Solution
- [ ] Product Description (one paragraph)
- [ ] Core Features (3-4 maximum)
  - [ ] Feature 1 + benefit
  - [ ] Feature 2 + benefit
  - [ ] Feature 3 + benefit
- [ ] Value Proposition (clear statement)
- [ ] Product Screenshots/Demo
  - [ ] UI/UX mockups
  - [ ] Actual product (if available)
- [ ] Technology Stack (brief mention)
- [ ] IP/Patents (if applicable)

### Slide 5: Product Deep Dive
- [ ] Product Architecture
- [ ] User Journey/Flow
- [ ] Technical Differentiators
- [ ] Development Status
  - [ ] What's built
  - [ ] What's in development
  - [ ] Future roadmap
- [ ] Platform/Device Coverage

### Slide 6: Market Opportunity
- [ ] TAM (Total Addressable Market)
  - [ ] Global number
  - [ ] Calculation methodology
- [ ] SAM (Serviceable Available Market)
  - [ ] Realistic reach in 5 years
- [ ] SOM (Serviceable Obtainable Market)
  - [ ] Year 1-3 projections
- [ ] Market Growth Rate (CAGR)
- [ ] Market Drivers
  - [ ] Why is market growing?
  - [ ] Trends supporting growth
- [ ] Geographic Focus
  - [ ] Initial markets
  - [ ] Expansion plans

### Slide 7: Target Customer
- [ ] Customer Personas (2-3 detailed)
  - [ ] Demographics
  - [ ] Psychographics
  - [ ] Buying behavior
- [ ] Customer Segments
  - [ ] Primary segment
  - [ ] Secondary segments
- [ ] Use Cases (specific scenarios)
- [ ] Customer Journey Map
- [ ] Decision Makers vs Users

### Slide 8: Business Model
- [ ] Revenue Streams
  - [ ] Primary revenue model
  - [ ] Secondary revenue opportunities
- [ ] Pricing Strategy
  - [ ] Price points
  - [ ] Pricing model (subscription/one-time/usage)
  - [ ] Pricing justification
- [ ] Unit Economics
  - [ ] CAC (Customer Acquisition Cost)
  - [ ] LTV (Lifetime Value)
  - [ ] LTV/CAC ratio
  - [ ] Gross margins
  - [ ] Churn rate
- [ ] Sales Cycle length
- [ ] Payment Terms

### Slide 9: Go-to-Market Strategy
- [ ] Customer Acquisition Strategy
  - [ ] Channels (ranked by priority)
  - [ ] Channel costs
  - [ ] Channel scalability
- [ ] Marketing Plan
  - [ ] Content marketing
  - [ ] Paid acquisition
  - [ ] Organic/SEO
  - [ ] Social media
- [ ] Sales Strategy
  - [ ] Direct sales
  - [ ] Self-serve
  - [ ] Channel partners
- [ ] Launch Plan
  - [ ] Beta launch details
  - [ ] Full launch timeline
- [ ] Partnership Strategy

### Slide 10: Competitive Analysis
- [ ] Competitive Matrix (visual)
  - [ ] 5-8 competitors
  - [ ] Key differentiators
  - [ ] Feature comparison
- [ ] Positioning Map (2x2 matrix)
- [ ] Competitive Advantages
  - [ ] Sustainable moats
  - [ ] Unfair advantages
- [ ] Why You Win
  - [ ] Speed to market
  - [ ] Technical superiority
  - [ ] Cost advantage
  - [ ] Network effects

### Slide 11: Traction & Validation
- [ ] Key Metrics Dashboard
  - [ ] Users/Customers (total, active)
  - [ ] Revenue (MRR/ARR if applicable)
  - [ ] Growth rate (MoM, YoY)
  - [ ] Engagement metrics
  - [ ] Retention/Churn
- [ ] Customer Evidence
  - [ ] Testimonials
  - [ ] Case studies
  - [ ] NPS score
  - [ ] Logo wall (if B2B)
- [ ] Milestones Achieved
  - [ ] Product milestones
  - [ ] Business milestones
  - [ ] Team milestones
- [ ] Media/PR Coverage
- [ ] Awards/Recognition

### Slide 12: Financial Projections
- [ ] Revenue Projections (3-5 years)
  - [ ] Monthly/Annual breakdown
  - [ ] Revenue by segment/product
  - [ ] Key assumptions
- [ ] Cost Structure
  - [ ] COGS
  - [ ] Operating expenses
  - [ ] Capital requirements
- [ ] Path to Profitability
  - [ ] Break-even timeline
  - [ ] Cash flow projections
- [ ] Key Financial Metrics
  - [ ] Burn rate
  - [ ] Runway
  - [ ] Gross margin evolution

### Slide 13: Team
- [ ] Founders (detailed profiles)
  - [ ] Photos
  - [ ] Relevant experience
  - [ ] Domain expertise
  - [ ] Previous exits (if any)
  - [ ] Education
  - [ ] Key achievements
- [ ] Key Team Members
  - [ ] CTO/CPO/CMO profiles
  - [ ] Relevant expertise
- [ ] Advisory Board
  - [ ] Names and credentials
  - [ ] Value they bring
- [ ] Board of Directors (if exists)
- [ ] Team Gaps to Fill
  - [ ] Key hires planned
  - [ ] Timeline for hiring

### Slide 14: Funding History & Use of Funds
- [ ] Previous Funding (if any)
  - [ ] Amount raised
  - [ ] Investors
  - [ ] Valuation (if disclosable)
  - [ ] Use of previous funds
- [ ] Current Round Details
  - [ ] Amount raising
  - [ ] Pre-money valuation
  - [ ] Round structure
  - [ ] Lead investor (if any)
- [ ] Use of Funds (detailed breakdown)
  - [ ] Product development (%)
  - [ ] Sales & Marketing (%)
  - [ ] Team/Hiring (%)
  - [ ] Operations (%)
  - [ ] Other (%)
- [ ] Milestones to be Achieved
  - [ ] With this funding
  - [ ] Timeline for each

### Slide 15: Technology & IP
- [ ] Tech Stack Details
- [ ] Architecture Diagrams
- [ ] Scalability Plan
- [ ] Security/Compliance
- [ ] Patents Filed/Granted
- [ ] Trade Secrets
- [ ] Technical Roadmap

### Slide 16: Risk Analysis & Mitigation
- [ ] Market Risks
  - [ ] Mitigation strategies
- [ ] Technical Risks
  - [ ] Mitigation strategies
- [ ] Regulatory Risks
  - [ ] Mitigation strategies
- [ ] Competitive Risks
  - [ ] Mitigation strategies
- [ ] Execution Risks
  - [ ] Mitigation strategies

### Slide 17: Strategic Roadmap
- [ ] 12-Month Roadmap
  - [ ] Product milestones
  - [ ] Business milestones
  - [ ] Team milestones
- [ ] 3-Year Vision
  - [ ] Product evolution
  - [ ] Market expansion
  - [ ] Revenue targets
- [ ] 5-Year Vision
  - [ ] Market position
  - [ ] Exit opportunities

### Slide 18: Partnerships & Ecosystem
- [ ] Current Partners
  - [ ] Strategic partners
  - [ ] Technology partners
  - [ ] Distribution partners
- [ ] Pipeline Partners
- [ ] Ecosystem Position
- [ ] Integration Strategy

### Slide 19: Exit Strategy
- [ ] Potential Acquirers
  - [ ] Strategic buyers
  - [ ] Financial buyers
- [ ] IPO Possibility
- [ ] Comparable Exits
  - [ ] Similar companies
  - [ ] Exit multiples
- [ ] Timeline Expectations

### Slide 20: Call to Action & Contact
- [ ] Clear Ask (repeated)
  - [ ] Investment amount
  - [ ] Terms
  - [ ] Timeline
- [ ] Next Steps
  - [ ] Due diligence process
  - [ ] Timeline for decision
- [ ] Contact Information (repeated)
  - [ ] All founder contacts
  - [ ] Preferred contact method
- [ ] Thank You Message
- [ ] Q&A Invitation
```

---

## REGIONAL VC CHECKLIST

```markdown
# Regional VC Pitch Deck Checklist (15 Slides)
## For SiliconGardens, AYMO Ventures, and Regional Investors
## Pre-seed/Seed Stage - CEE/SEE Region Focus

### 🎯 Regional VC Specific Requirements
- [ ] Language Versions
  - [ ] Croatian/Local version
  - [ ] English version
  - [ ] Terminology consistency
- [ ] Regional Context
  - [ ] Local market data
  - [ ] Regional success stories referenced
  - [ ] Cultural adaptations

### Slide 1: Title & Introduction
- [ ] Company Logo
- [ ] Company Name (with d.o.o./LLC designation)
- [ ] Tagline (in local language + English)
- [ ] Location (City, Country - emphasize if in hub)
- [ ] Contact Details
  - [ ] Email
  - [ ] Phone (with country code)
  - [ ] Website
  - [ ] LinkedIn
- [ ] Date of Presentation

### Slide 2: Problem Definition
- [ ] Regional Problem Context
  - [ ] How problem manifests locally
  - [ ] Statistics from regional markets
  - [ ] Local pain points (specific examples)
- [ ] Quantified Impact
  - [ ] Number of affected businesses/people in region
  - [ ] Economic impact in EUR/local currency
- [ ] Current Local Solutions
  - [ ] Why they don't work here
  - [ ] Infrastructure limitations
  - [ ] Cultural/regulatory barriers
- [ ] Customer Quotes (from regional customers)

### Slide 3: Solution
- [ ] Product Overview (simple, clear)
- [ ] Key Features (maximum 4)
  - [ ] Localized features
  - [ ] Language support
  - [ ] Regional compliance
- [ ] Product Screenshots
  - [ ] In local language
  - [ ] Local use cases
- [ ] Unique Value Proposition
  - [ ] For regional market
  - [ ] Competitive advantages locally
- [ ] Development Status
  - [ ] MVP/Beta/Live
  - [ ] Tech stack (briefly)

### Slide 4: Market Opportunity
- [ ] Regional Market Size
  - [ ] Croatia/Primary market (EUR)
  - [ ] CEE/SEE expansion markets (EUR)
  - [ ] Western Europe potential
- [ ] Bottom-up Calculation
  - [ ] Number of potential customers
  - [ ] Average revenue per customer
  - [ ] Realistic market share
- [ ] Market Growth
  - [ ] Regional digitalization trends
  - [ ] EU funding opportunities
  - [ ] Post-COVID acceleration
- [ ] Market Timing
  - [ ] Why now in this region

### Slide 5: Business Model
- [ ] Revenue Model
  - [ ] Pricing in EUR
  - [ ] Pricing adapted to regional purchasing power
  - [ ] Payment methods (local preferences)
- [ ] Unit Economics
  - [ ] CAC in regional context
  - [ ] LTV with regional retention rates
  - [ ] Gross margins
  - [ ] Path to profitability (important!)
- [ ] Scalability
  - [ ] From Croatia to region
  - [ ] Minimal localization costs

### Slide 6: Traction & Validation
- [ ] Current Metrics
  - [ ] Users/Customers (by country)
  - [ ] Revenue (MRR in EUR)
  - [ ] Growth rate (monthly)
  - [ ] Key regional clients/logos
- [ ] Proof Points
  - [ ] LOIs from regional companies
  - [ ] Pilot projects
  - [ ] Government contracts/interest
  - [ ] EU grants received/applied
- [ ] Customer Testimonials
  - [ ] Regional customer success stories
  - [ ] NPS from local market
- [ ] Media Coverage
  - [ ] Local press mentions
  - [ ] Industry recognition

### Slide 7: Go-to-Market Strategy
- [ ] Regional Launch Strategy
  - [ ] Croatia first approach
  - [ ] City-by-city rollout
  - [ ] Key partnerships needed
- [ ] Customer Acquisition
  - [ ] Direct sales (enterprise)
  - [ ] Digital marketing (costs in region)
  - [ ] Local events/conferences
  - [ ] Government/EU tenders
- [ ] Regional Expansion Plan
  - [ ] Slovenia, Serbia, Bosnia (timeline)
  - [ ] Poland, Czech, Hungary (next phase)
  - [ ] Localization requirements
- [ ] Strategic Partnerships
  - [ ] Local system integrators
  - [ ] Regional telcos
  - [ ] Government agencies

### Slide 8: Competition
- [ ] Regional Competitors
  - [ ] Local players analysis
  - [ ] International players in region
  - [ ] Feature/price comparison
- [ ] Competitive Advantages
  - [ ] Local presence/support
  - [ ] Language/cultural fit
  - [ ] Regional compliance
  - [ ] Price advantage
- [ ] Barriers to Entry
  - [ ] First mover in region
  - [ ] Local relationships
  - [ ] Regional expertise
- [ ] Positioning (visual matrix)

### Slide 9: Team
- [ ] Founders
  - [ ] Photos and names
  - [ ] Regional expertise/connections
  - [ ] Previous experience (emphasize regional successes)
  - [ ] Language skills
  - [ ] Domain expertise
- [ ] Key Team Members
  - [ ] Technical lead
  - [ ] Sales/BD lead
  - [ ] Local market experts
- [ ] Advisors
  - [ ] Regional business leaders
  - [ ] Industry experts
  - [ ] Previous entrepreneurs (exits)
- [ ] Why This Team
  - [ ] Unique regional advantages
  - [ ] Network in region

### Slide 10: Financial Projections
- [ ] 3-Year Forecast (conservative)
  - [ ] Revenue by year (EUR)
  - [ ] Revenue by country/region
  - [ ] Cost structure
  - [ ] EBITDA timeline
- [ ] Key Assumptions
  - [ ] Customer acquisition rate
  - [ ] Pricing evolution
  - [ ] Market penetration %
- [ ] Capital Efficiency
  - [ ] Lower costs vs Western Europe
  - [ ] Remote team advantages
  - [ ] Government incentives

### Slide 11: Funding Ask
- [ ] Investment Amount
  - [ ] EUR amount (e.g., 300-500K)
  - [ ] Equity offered (15-20% typical)
  - [ ] Valuation (if disclosing)
- [ ] Use of Funds (18-month runway)
  - [ ] Product development (30-40%)
  - [ ] Sales & Marketing (30-40%)
  - [ ] Team expansion (20-30%)
  - [ ] Operations (10%)
- [ ] Co-investors
  - [ ] Other regional VCs interested
  - [ ] Government grants secured/pending
  - [ ] Angel investors committed

### Slide 12: Milestones & Roadmap
- [ ] Next 12 Months (with this funding)
  - [ ] Product milestones
  - [ ] Revenue targets (monthly)
  - [ ] Customer acquisition targets
  - [ ] Team growth (key hires)
  - [ ] Geographic expansion
- [ ] Success Metrics
  - [ ] KPIs to track
  - [ ] Reporting frequency
- [ ] Next Funding Round
  - [ ] Series A timeline
  - [ ] Milestones needed

### Slide 13: Regional Expansion Vision
- [ ] Phase 1 (Year 1)
  - [ ] Dominate local market
  - [ ] Proof of concept
- [ ] Phase 2 (Year 2-3)
  - [ ] Regional expansion (CEE/SEE)
  - [ ] Strategic partnerships
- [ ] Phase 3 (Year 3-5)
  - [ ] Western Europe entry
  - [ ] Potential exit opportunities
- [ ] Why Start Here
  - [ ] Test market advantages
  - [ ] Lower competition
  - [ ] EU expansion benefits

### Slide 14: Investment Highlights
- [ ] Why Invest Now
  - [ ] Market timing
  - [ ] Team readiness
  - [ ] Traction proof
  - [ ] Regional opportunity
- [ ] Return Potential
  - [ ] Exit comparables in region
  - [ ] Strategic buyer interest
  - [ ] Revenue multiples
- [ ] Risk Mitigation
  - [ ] Conservative projections
  - [ ] Multiple revenue streams
  - [ ] Regional diversification

### Slide 15: Contact & Next Steps
- [ ] Thank You Message (in local language)
- [ ] Contact Information
  - [ ] All founder contacts
  - [ ] Website/Demo access
- [ ] Next Steps
  - [ ] Follow-up timeline
  - [ ] Due diligence readiness
  - [ ] Additional materials available
- [ ] Q&A

### 📊 Regional VC Hot Buttons
- [ ] B2B SaaS model ✓
- [ ] Regional scaling potential ✓
- [ ] Capital efficient growth ✓
- [ ] Strong local team ✓
- [ ] Government/EU support ✓
- [ ] Clear monetization ✓
- [ ] Exit opportunities identified ✓
- [ ] Tech-enabled traditional business ✓
- [ ] Domain expertise in team ✓
- [ ] Previous startup experience in region ✓
```

---

## YC CHECKLIST

```markdown
# Y Combinator / Global VC Pitch Deck Checklist (10 Slides)
## Ultra-Concise, Growth-Focused Format

### ⚡ YC Core Principles Check
- [ ] Can become $1B+ company?
- [ ] Growing 10-20% week-over-week?
- [ ] Founders working full-time?
- [ ] Technical co-founder on team?
- [ ] Talking to users daily?
- [ ] Launching in weeks, not months?

### Slide 1: Title + One-Liner
- [ ] Company Name (memorable, .com available)
- [ ] One-Line Description (X for Y format)
  - [ ] "We're building the [Known Thing] for [Market]"
  - [ ] 7 words maximum
  - [ ] Instantly understandable
- [ ] Contact (email only)
- [ ] Demo Link (if live product)

### Slide 2: Problem
- [ ] One Specific Problem (not multiple)
- [ ] Why It's PAINFUL
  - [ ] Quantify pain ($$ or time)
  - [ ] Frequency (how often)
  - [ ] Growing urgency
- [ ] Who Has This Problem
  - [ ] Specific user persona
  - [ ] How many globally
- [ ] Current Solutions Suck Because...
  - [ ] Too expensive
  - [ ] Too slow
  - [ ] Too complex
  - [ ] Doesn't exist
- [ ] Your Unique Insight
  - [ ] What do you know others don't?

### Slide 3: Solution
- [ ] What You Built (one sentence)
- [ ] Live Demo/Screenshots
  - [ ] Show, don't tell
  - [ ] Real product, not mockups
  - [ ] Core flow only (30 seconds)
- [ ] How It Works (3 steps max)
  - [ ] Step 1: User does X
  - [ ] Step 2: Product does Y
  - [ ] Step 3: Problem solved
- [ ] Why 10x Better
  - [ ] 10x faster
  - [ ] 10x cheaper
  - [ ] 10x easier
  - [ ] First time possible
- [ ] Technical Moat (if any)
  - [ ] Proprietary tech
  - [ ] Network effects
  - [ ] Data advantage

### Slide 4: Traction 📈
- [ ] The Graph (up and to the right!)
  - [ ] Weekly growth rate (%)
  - [ ] Revenue OR users (pick one)
  - [ ] Last 8-12 weeks
  - [ ] Clear labels/numbers
- [ ] Key Metrics (choose relevant)
  - [ ] MRR/ARR + growth %
  - [ ] Active users + growth %
  - [ ] GMV + growth %
  - [ ] Transactions + growth %
- [ ] Customer Love
  - [ ] NPS score (if 50+)
  - [ ] Organic growth %
  - [ ] Retention/Churn
  - [ ] One killer testimonial
- [ ] Notable Customers (logos if B2B)

### Slide 5: Market
- [ ] TAM Calculation (bottom-up ONLY)
  - [ ] # of potential users globally
  - [ ] × $ per user per year
  - [ ] = $XXB market
- [ ] Why NOW (most important!)
  - [ ] New technology enabler
  - [ ] Regulation change
  - [ ] Behavior shift (COVID, etc.)
  - [ ] Platform shift
  - [ ] Cost reduction
- [ ] Market Growing Because...
  - [ ] Specific trend + data
  - [ ] Annual growth rate %
- [ ] Expansion Potential
  - [ ] Start with X, expand to Y
  - [ ] Land and expand strategy

### Slide 6: Product & Tech
- [ ] Current Product Status
  - [ ] Live (how long)
  - [ ] Beta (# of users)
  - [ ] Building (launch date)
- [ ] Core Tech Stack (one line)
- [ ] Unique Technical Insights
  - [ ] Why you can build this
  - [ ] Technical breakthrough
  - [ ] Speed advantage
- [ ] Product Roadmap (next 3 months)
  - [ ] Feature 1 (date)
  - [ ] Feature 2 (date)
  - [ ] Feature 3 (date)
- [ ] Platform Strategy
  - [ ] Mobile/Web/API
  - [ ] Global from day 1

### Slide 7: Business Model
- [ ] How You Make Money (one sentence)
- [ ] Pricing
  - [ ] Current pricing
  - [ ] Price vs competitors
  - [ ] Pricing power
- [ ] Unit Economics (must have)
  - [ ] CAC: $X
  - [ ] LTV: $Y (X×10 minimum)
  - [ ] Gross Margin: Z%
  - [ ] Payback Period: months
- [ ] Growth Loops
  - [ ] Viral coefficient
  - [ ] Network effects
  - [ ] Organic vs paid split
- [ ] Scale Economics
  - [ ] Margins improve with scale

### Slide 8: Team
- [ ] Founders Only (2-3 max)
  - [ ] Name + Role
  - [ ] Superpower (one line)
  - [ ] Relevant background
  - [ ] Years working together
- [ ] Why YOU Will Win
  - [ ] Domain expertise proof
  - [ ] Technical excellence proof
  - [ ] Execution speed proof
  - [ ] Previous startup experience
  - [ ] Dropped out of [Stanford/MIT] (if true)
- [ ] Team Velocity
  - [ ] Shipped X features in Y weeks
  - [ ] Commits/deployments per week
- [ ] Obsession Indicator
  - [ ] Working on this for X years
  - [ ] Personal pain point
  - [ ] Won't stop until...

### Slide 9: Financials & Ask
- [ ] Current Runway (months left)
- [ ] Burn Rate (monthly)
- [ ] Revenue Growth
  - [ ] Last month: $X
  - [ ] This month: $Y
  - [ ] Next month projection: $Z
- [ ] The Ask
  - [ ] Raising: $X (typically $500K-$2M)
  - [ ] Valuation: SAFE/Standard terms
  - [ ] Use: 18 months runway
- [ ] Use of Funds (simple)
  - [ ] Engineers: X%
  - [ ] Growth: Y%
  - [ ] Infrastructure: Z%
- [ ] Milestones With This Money
  - [ ] Users: X → Y
  - [ ] Revenue: X → Y
  - [ ] Product: launch Z

### Slide 10: Vision
- [ ] The Ask (repeated, clear)
- [ ] 12-Month Goals
  - [ ] User/revenue target
  - [ ] Product milestone
  - [ ] Team size
- [ ] Why This Becomes Huge
  - [ ] Network effects kick in at X
  - [ ] Winner-take-all dynamics
  - [ ] Platform expansion
  - [ ] Global by default
- [ ] Contact (email, calendly link)

### ⚡ YC-Specific Language That Works
- [ ] "We talk to users every day"
- [ ] "We ship code every day"
- [ ] "Growing X% week-over-week"
- [ ] "Users love us because..."
- [ ] "We're the experts in X because..."
- [ ] "We can build this 10x faster because..."
- [ ] "This is a winner-take-all market"
- [ ] "We're default alive"
- [ ] "Move fast and break things"
- [ ] "Strong opinions, loosely held"
- [ ] "Default alive, not default dead"

### ❌ YC Red Flags to Avoid
- [ ] No "we're the Uber for X" (unless very clear)
- [ ] No TAM slides with concentric circles
- [ ] No 5-year financial projections
- [ ] No "if we get 1% of market"
- [ ] No advisor slides
- [ ] No press quotes
- [ ] No "patent pending"
- [ ] No complex diagrams
- [ ] No walls of text
- [ ] No "seeking strategic partners"
```

---

## WORKFLOW PHASES

### PHASE 1: PROJECT INITIALIZATION
```bash
# Create folder structure
mkdir -p pitch-deck/{.github/{workflows,ISSUE_TEMPLATE},.claude/{checklists,prompts},data,slides/components,theme,public/assets,docs}

# Initialize package.json
cd pitch-deck && npm init -y
npm install -D @slidev/cli
npm install chart.js d3 vue

# Add scripts to package.json
npm pkg set scripts.dev="slidev"
npm pkg set scripts.build="slidev build"
npm pkg set scripts.export="slidev export"
npm pkg set scripts.export:all="npm run export:master && npm run export:regional && npm run export:yc"
```

### PHASE 2: DATA COLLECTION PROMPT
```
I need to collect startup information for our EXAMPLE pitch deck template.
This will be a realistic but generic example that others can learn from and customize.
Ask me questions in Croatian and save to data/company.yaml:

1. TVRTKA: Naziv, slogan, lokacija, website?
2. PROBLEM: Koji problem rješavate? Koliko ljudi? Koliko košta? Zašto postojeća rješenja ne rade?
3. RJEŠENJE: Što ste izgradili? 3 ključne funkcionalnosti? Zašto 10x bolje? Status (MVP/Beta/Live)?
4. TRŽIŠTE: Veličina HR (EUR)? Regionalno (EUR)? Godišnji rast?
5. MODEL: Kako zarađujete? Cijena? Trenutni MRR? Broj korisnika?
6. TIM: Osnivači (ime, pozicija, background)? Ključni članovi?
7. TRACTION: Korisnici? Mjesečni rast? Ključni klijenti? Postignuća?
8. FINANCIJE: Koliko tražite (EUR)? Za što? Runway?

Format as YAML in data/company.yaml as a working example for the template.
```

### PHASE 3: GENERATE MASTER DECK
```
Using data/company.yaml, generate complete Slidev presentation following master-deck-checklist.md:
- 20 slides total
- Croatian language initially
- Shadcn minimal style (black/white/gray)
- Add working chart components
- Save to slides/deck-master.md
This should be a fully functional example that demonstrates all features.
```

### PHASE 4: CREATE REGIONAL VC VERSION
```
Create regional VC version from master deck:
- Follow regional-vc-checklist.md
- 15 slides max
- Conservative projections
- EUR amounts
- Capital efficiency focus
- Path to profitability emphasis
- Save to slides/deck-regional.md
This demonstrates how to adapt for regional investors.
```

### PHASE 5: CREATE YC VERSION
```
Create YC version (English):
- Follow yc-checklist.md
- 10 slides only
- Ultra-concise
- Focus on growth metrics
- $1B+ TAM
- Week-over-week growth
- Save to slides/deck-yc.md
This shows how to create a Silicon Valley style deck.
```

### PHASE 6: ENGLISH CONVERSION
```
Convert Croatian examples to English:
- Update data/company.yaml with English translations
- Create English versions where needed
- Professional business English
- Keep both language versions as examples
```

### PHASE 7: DOCUMENTATION
```
Create comprehensive documentation:
- docs/CUSTOMIZATION.md - How to adapt for your startup
- docs/EXAMPLES.md - Success stories and tips
- docs/FAQ.md - Common questions
- Update README.md with clear instructions
```

---

## SHADCN-STYLE THEME

```css
/* theme/shadcn-style.css */
:root {
  --primary: #000000;
  --secondary: #ffffff;
  --muted: #f4f4f5;
  --border: #e4e4e7;
  --text: #18181b;
  --text-muted: #71717a;
  --accent: #000000;
  --font-sans: 'Inter', system-ui, -apple-system, sans-serif;
  --radius: 0.375rem;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.slidev-layout {
  background: var(--secondary);
  color: var(--text);
  font-family: var(--font-sans);
  padding: 80px;
}

h1 {
  font-size: 48px;
  font-weight: 700;
  letter-spacing: -0.02em;
  margin-bottom: 24px;
  line-height: 1.1;
}

h2 {
  font-size: 32px;
  font-weight: 600;
  letter-spacing: -0.01em;
  margin-bottom: 16px;
  color: var(--text-muted);
}

h3 {
  font-size: 24px;
  font-weight: 500;
  margin-bottom: 12px;
}

p, li {
  font-size: 18px;
  line-height: 1.6;
  color: var(--text);
}

.metric-card {
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 24px;
  background: var(--secondary);
  margin-bottom: 16px;
}

.metric-value {
  font-size: 36px;
  font-weight: 700;
  letter-spacing: -0.02em;
  margin-bottom: 4px;
}

.metric-label {
  font-size: 14px;
  color: var(--text-muted);
  text-transform: uppercase;
  letter-spacing: 0.05em;
}

.metric-change {
  font-size: 14px;
  color: #10b981;
  font-weight: 500;
}

.chart-container {
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 24px;
  background: var(--secondary);
  margin: 24px 0;
}

.two-cols {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 40px;
  align-items: start;
}

.three-cols {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}

.team-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 24px;
  margin-top: 32px;
}

.team-member {
  text-align: center;
}

.team-photo {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  margin: 0 auto 12px;
  border: 2px solid var(--border);
}

.cta-button {
  background: var(--primary);
  color: var(--secondary);
  padding: 12px 24px;
  border-radius: var(--radius);
  font-weight: 600;
  font-size: 16px;
  border: none;
  cursor: pointer;
  display: inline-block;
  margin-top: 24px;
}

.highlight {
  background: var(--muted);
  padding: 2px 6px;
  border-radius: 4px;
  font-weight: 600;
}

blockquote {
  border-left: 3px solid var(--border);
  padding-left: 24px;
  margin: 24px 0;
  font-style: italic;
  color: var(--text-muted);
}

table {
  width: 100%;
  border-collapse: collapse;
  margin: 24px 0;
}

th {
  text-align: left;
  padding: 12px;
  border-bottom: 2px solid var(--border);
  font-weight: 600;
}

td {
  padding: 12px;
  border-bottom: 1px solid var(--border);
}

.logo-wall {
  display: flex;
  flex-wrap: wrap;
  gap: 24px;
  align-items: center;
  justify-content: center;
  margin: 32px 0;
}

.logo-wall img {
  height: 40px;
  opacity: 0.7;
  filter: grayscale(100%);
}

code {
  background: var(--muted);
  padding: 2px 6px;
  border-radius: 4px;
  font-family: 'JetBrains Mono', monospace;
  font-size: 14px;
}

.progress-bar {
  width: 100%;
  height: 8px;
  background: var(--border);
  border-radius: 4px;
  overflow: hidden;
}

.progress-fill {
  height: 100%;
  background: var(--primary);
  transition: width 0.3s ease;
}
```

---

## VUE COMPONENTS

### Chart.vue
```vue
<template>
  <div class="chart-container">
    <canvas v-if="type === 'line' || type === 'bar'" ref="chartCanvas"></canvas>
    <div v-else ref="d3Container"></div>
  </div>
</template>

<script setup>
import { onMounted, ref } from 'vue'
import { Chart } from 'chart.js/auto'
import * as d3 from 'd3'

const props = defineProps({
  data: Object,
  type: {
    type: String,
    default: 'line'
  },
  title: String
})

const chartCanvas = ref(null)
const d3Container = ref(null)

onMounted(() => {
  if (props.type === 'line' || props.type === 'bar') {
    // Chart.js for simple charts
    new Chart(chartCanvas.value, {
      type: props.type,
      data: {
        labels: props.data.labels,
        datasets: [{
          label: props.title,
          data: props.data.values,
          borderColor: '#000',
          backgroundColor: props.type === 'bar' ? '#000' : 'transparent',
          tension: 0.4
        }]
      },
      options: {
        responsive: true,
        plugins: {
          legend: { display: false },
          title: {
            display: !!props.title,
            text: props.title
          }
        },
        scales: {
          y: {
            beginAtZero: true,
            grid: {
              color: '#e4e4e7'
            }
          },
          x: {
            grid: {
              display: false
            }
          }
        }
      }
    })
  } else if (props.type === 'tam') {
    // D3.js for TAM/SAM/SOM circles
    const width = 400
    const height = 400
    
    const svg = d3.select(d3Container.value)
      .append('svg')
      .attr('width', width)
      .attr('height', height)
    
    const circles = [
      { radius: 180, label: 'TAM', value: props.data.tam },
      { radius: 120, label: 'SAM', value: props.data.sam },
      { radius: 60, label: 'SOM', value: props.data.som }
    ]
    
    const g = svg.append('g')
      .attr('transform', `translate(${width/2}, ${height/2})`)
    
    circles.forEach((circle, i) => {
      g.append('circle')
        .attr('r', circle.radius)
        .attr('fill', 'none')
        .attr('stroke', '#000')
        .attr('stroke-width', 2)
        .attr('opacity', 0.3 + i * 0.2)
      
      g.append('text')
        .attr('y', -circle.radius + 20)
        .attr('text-anchor', 'middle')
        .style('font-weight', 'bold')
        .text(`${circle.label}: ${circle.value}`)
    })
  }
})
</script>
```

### MetricCard.vue
```vue
<template>
  <div class="metric-card">
    <div class="metric-value">{{ formattedValue }}</div>
    <div class="metric-label">{{ label }}</div>
    <div v-if="change" class="metric-change">
      {{ change > 0 ? '+' : '' }}{{ change }}%
    </div>
  </div>
</template>

<script setup>
import { computed } from 'vue'

const props = defineProps({
  value: [Number, String],
  label: String,
  change: Number,
  format: {
    type: String,
    default: 'number'
  }
})

const formattedValue = computed(() => {
  if (props.format === 'currency') {
    return `€${props.value.toLocaleString()}`
  } else if (props.format === 'percentage') {
    return `${props.value}%`
  } else {
    return props.value.toLocaleString()
  }
})
</script>
```

---

## EXAMPLE DATA STRUCTURE

```yaml
# data/company.yaml
# This is a complete working example for a fictional startup
# Fork this repo and replace with your own data

company:
  name: "TaskFlow"
  tagline:
    hr: "Automatizacija zadataka za male timove"
    en: "Task automation for small teams"
  location: "Zagreb, Croatia"
  website: "www.taskflow.example"
  email: "pitch@taskflow.example"
  phone: "+385 91 000 0000"
  founded: "2023"
  industry: "B2B SaaS"

problem:
  statement:
    hr: "Mali timovi gube 15 sati tjedno na repetitivne zadatke"
    en: "Small teams waste 15 hours weekly on repetitive tasks"
  affected_people: 500000
  cost_per_person: 300
  frequency: "weekly"
  current_solutions:
    - name: "Manual tracking"
      why_fails: "Time consuming, error prone"
    - name: "Enterprise tools"
      why_fails: "Too complex, too expensive"
    - name: "Spreadsheets"
      why_fails: "Not scalable, no automation"

solution:
  description:
    hr: "No-code platforma za automatizaciju radnih procesa"
    en: "No-code platform for workflow automation"
  features:
    - name:
        hr: "Visual Builder"
        en: "Visual Builder"
      benefit:
        hr: "Kreirajte workflow u minutama"
        en: "Create workflows in minutes"
    - name:
        hr: "100+ integracija"
        en: "100+ integrations"
      benefit:
        hr: "Spojite sve vaše alate"
        en: "Connect all your tools"
    - name:
        hr: "AI asistent"
        en: "AI assistant"
      benefit:
        hr: "Automatske preporuke optimizacije"
        en: "Automatic optimization suggestions"
  status: "Beta"
  tech_stack: "Vue.js, Node.js, PostgreSQL, Docker"
  demo_url: "demo.taskflow.example"

market:
  tam: 5000000000  # €5B
  sam: 500000000   # €500M
  som: 50000000    # €50M
  growth_rate: 28
  timing_why:
    hr: "Remote rad povećao potrebu za automatizacijom"
    en: "Remote work increased automation needs"
  segments:
    - "Digital agencies"
    - "Startups (10-50 employees)"
    - "Consultancies"

business_model:
  revenue_model: "SaaS Subscription"
  pricing_tiers:
    - name: "Starter"
      price: 29
      users: 5
    - name: "Team"
      price: 99
      users: 20
    - name: "Business"
      price: 299
      users: "unlimited"
  unit_economics:
    cac: 150
    ltv: 1800
    ltv_cac_ratio: 12
    gross_margin: 82
    payback_months: 3
    churn_monthly: 2.5

traction:
  metrics:
    users: 2500
    paying_customers: 125
    mrr: 8750
    arr: 105000
    growth_rate_monthly: 22
    nps: 68
  milestones:
    - "Launched private beta (Month 1)"
    - "First paying customer (Month 2)"
    - "€5k MRR (Month 4)"
    - "100 customers (Month 6)"
  customers:
    - "TechStartup Ltd"
    - "Digital Agency X"
    - "Consulting Group Y"
  testimonials:
    - customer: "Ana Novak, CEO"
      company: "TechStartup Ltd"
      quote:
        hr: "TaskFlow nam je uštedio 20 sati tjedno!"
        en: "TaskFlow saved us 20 hours per week!"

team:
  founders:
    - name: "Marko Horvat"
      role: "CEO"
      background: "Ex-Infobip, 10y product management"
      linkedin: "linkedin.com/in/example"
      education: "FER Zagreb"
    - name: "Ana Kovač"
      role: "CTO"
      background: "Ex-Rimac, Full-stack engineer"
      linkedin: "linkedin.com/in/example"
      education: "PMF Zagreb"
  employees: 5
  advisors:
    - name: "Ivan Mrvoš"
      credential: "Founder of Include (exited), Angel investor"
    - name: "Petra Novak"
      credential: "VP Sales at Productive"

financial:
  runway_months: 8
  burn_rate_monthly: 25000
  revenue_last_month: 7200
  revenue_this_month: 8750
  revenue_projection_next: 10700
  
  projections_3y:
    year1: 210000
    year2: 850000
    year3: 2400000
  
  previous_funding:
    - round: "Pre-seed"
      amount: 150000
      investors: ["CRANE", "Angel investors"]
      date: "2023-06"

funding:
  round: "Seed"
  amount_seeking: 500000
  valuation: 2500000
  equity_offered: 20
  use_of_funds:
    product_development: 35
    sales_marketing: 40
    team_expansion: 20
    operations: 5
  milestones_with_funding:
    - "Scale to 1000 customers"
    - "€100k MRR"
    - "Launch in 3 new markets"
    - "Mobile app release"
  next_round:
    timing: "18 months"
    target: "Series A - €2-3M"

competition:
  competitors:
    - name: "Zapier"
      strengths: "Market leader, many integrations"
      weaknesses: "Expensive, complex for simple tasks"
      pricing: "$20-100/month"
    - name: "Make (Integromat)"
      strengths: "Powerful, visual"
      weaknesses: "Steep learning curve"
      pricing: "$9-30/month"
    - name: "n8n"
      strengths: "Open source option"
      weaknesses: "Requires technical knowledge"
      pricing: "Free self-hosted"
  competitive_advantages:
    - "Designed for non-technical users"
    - "AI-powered optimization"
    - "Local presence and support"
    - "50% cheaper than alternatives"
    - "5-minute setup vs 2-hour average"

go_to_market:
  channels:
    - channel: "Content Marketing"
      cac: 100
      share: 40
    - channel: "Product-led growth"
      cac: 50
      share: 30
    - channel: "Direct Sales"
      cac: 500
      share: 20
    - channel: "Partnerships"
      cac: 200
      share: 10
  partnerships:
    - "Local SaaS companies"
    - "Digital agencies"
    - "Business consultants"
  expansion_plan:
    phase1: "Croatia & Slovenia (Year 1)"
    phase2: "CEE Region (Year 2)"
    phase3: "Western Europe (Year 3)"
```

---

## SAMPLE SLIDEV DECK

```markdown
---
theme: none
css: ./theme/shadcn-style.css
title: TaskFlow - Pitch Deck
info: |
  ## TaskFlow Pitch Deck
  Task automation for small teams
---

# TaskFlow

## Task automation for small teams

<div class="absolute bottom-10 left-10">
Zagreb, Croatia | www.taskflow.example
</div>

---

# Problem

## Small teams waste 15 hours weekly on repetitive tasks

<div class="two-cols">
<div>

### The Pain

- **15 hours/week** lost per team
- **€300/month** productivity loss
- **67%** of tasks are repetitive
- **3x** more errors in manual work

### Current Solutions Fail

- **Manual tracking**: Time consuming
- **Enterprise tools**: Too complex
- **Spreadsheets**: Not scalable

</div>
<div>

<Chart :data="{
  labels: ['Data Entry', 'Reporting', 'Task Assignment', 'Follow-ups'],
  values: [35, 25, 20, 20]
}" type="bar" title="Time Wasted (%)" />

</div>
</div>

---

# Solution

## No-code platform for workflow automation

<div class="three-cols">
<div class="metric-card">
<h3>🎨 Visual Builder</h3>
Create workflows in minutes, not hours
</div>

<div class="metric-card">
<h3>🔗 100+ Integrations</h3>
Connect all your existing tools
</div>

<div class="metric-card">
<h3>🤖 AI Assistant</h3>
Automatic optimization suggestions
</div>
</div>

### How It Works

1. **Connect** your tools (Slack, Gmail, etc.)
2. **Build** workflows with drag-and-drop
3. **Automate** and save 15+ hours weekly

<div class="mt-8">
[Live Demo Screenshot]
</div>

---

# Market Opportunity

## €5B market growing 28% annually

<div class="two-cols">
<div>

### Market Size

- **TAM:** €5B (Global SMB automation)
- **SAM:** €500M (European SMBs)
- **SOM:** €50M (Achievable in 3 years)

### Why Now?

- Remote work revolution
- No-code movement mainstream
- SMBs digitalization accelerated
- AI makes automation smarter

</div>
<div>

<Chart :data="{
  tam: '€5B',
  sam: '€500M',
  som: '€50M'
}" type="tam" />

</div>
</div>

---

# Traction

## Growing 22% month-over-month

<div class="two-cols">
<div>

<MetricCard :value="2500" label="Active Users" :change="22" />
<MetricCard :value="8750" label="MRR" format="currency" :change="22" />
<MetricCard :value="68" label="NPS Score" />

### Milestones

- ✅ Launched beta (Month 1)
- ✅ First customer (Month 2)  
- ✅ €5k MRR (Month 4)
- ✅ 100 customers (Month 6)

</div>
<div>

<Chart :data="{
  labels: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun'],
  values: [1000, 1800, 3200, 5000, 7200, 8750]
}" type="line" title="Monthly Revenue (€)" />

> "TaskFlow saved us 20 hours per week!"
> — Ana Novak, CEO at TechStartup Ltd

</div>
</div>

---

# Business Model

## SaaS with strong unit economics

<div class="two-cols">
<div>

### Pricing Tiers

| Plan | Price | Users |
|------|-------|-------|
| Starter | €29/mo | 5 |
| Team | €99/mo | 20 |
| Business | €299/mo | Unlimited |

### Revenue Streams

- Monthly subscriptions (90%)
- Annual plans (10% discount)
- Enterprise custom pricing

</div>
<div>

### Unit Economics

<MetricCard :value="150" label="CAC" format="currency" />
<MetricCard :value="1800" label="LTV" format="currency" />
<MetricCard :value="12" label="LTV/CAC Ratio" />

- **82%** Gross Margin
- **3 months** Payback Period
- **2.5%** Monthly Churn

</div>
</div>

---

# Team

## Experienced founders with domain expertise

<div class="team-grid">
<div class="team-member">
<div class="team-photo">[Photo]</div>
<h3>Marko Horvat</h3>
<p><strong>CEO</strong></p>
<p class="text-sm text-muted">Ex-Infobip, 10y product management</p>
<p class="text-sm text-muted">FER Zagreb</p>
</div>

<div class="team-member">
<div class="team-photo">[Photo]</div>
<h3>Ana Kovač</h3>
<p><strong>CTO</strong></p>
<p class="text-sm text-muted">Ex-Rimac, Full-stack engineer</p>
<p class="text-sm text-muted">PMF Zagreb</p>
</div>
</div>

### Advisors

- **Ivan Mrvoš** - Founder of Include (exited), Angel investor
- **Petra Novak** - VP Sales at Productive

---

# Competition

## Better, faster, cheaper

<div class="two-cols">
<div>

### Competitive Matrix

| Feature | TaskFlow | Zapier | Make |
|---------|----------|--------|------|
| No-code | ✅ | ✅ | ⚠️ |
| AI-powered | ✅ | ❌ | ❌ |
| Price | €29 | €75 | €30 |
| Setup time | 5min | 2hr | 1hr |
| Local support | ✅ | ❌ | ❌ |

</div>
<div>

### Our Advantages

1. **50% cheaper** than Zapier
2. **10x faster** setup
3. **AI optimization** unique feature
4. **Local presence** in CEE
5. **Non-technical** user focus

</div>
</div>

---

# Financial Projections

## Path to €2.4M ARR in 3 years

<div class="two-cols">
<div>

### Revenue Projections

- **Year 1:** €210k
- **Year 2:** €850k
- **Year 3:** €2.4M

### Key Assumptions

- 22% monthly growth (Year 1)
- 15% monthly growth (Year 2)
- 10% monthly growth (Year 3)
- 2.5% monthly churn
- €99 average revenue per user

</div>
<div>

<Chart :data="{
  labels: ['Y1', 'Y2', 'Y3'],
  values: [210000, 850000, 2400000]
}" type="bar" title="Revenue Projection (€)" />

### Path to Profitability

- **Month 18:** Cash flow positive
- **Month 24:** EBITDA positive

</div>
</div>

---

# The Ask

## Raising €500k to accelerate growth

<div class="two-cols">
<div>

### Investment Terms

- **Amount:** €500,000
- **Valuation:** €2.5M pre-money
- **Equity:** 20%
- **Type:** Equity round
- **Lead:** Looking for lead investor

### Use of Funds

- **Product (35%):** AI features, mobile app
- **Sales & Marketing (40%):** Scale GTM
- **Team (20%):** 3 key hires
- **Operations (5%):** Infrastructure

</div>
<div>

### Milestones with Funding

- 📈 Scale to **1,000 customers**
- 💰 Reach **€100k MRR**
- 🌍 Launch in **3 new markets**
- 📱 Release **mobile app**
- 🤝 **10 enterprise** clients

### Returns Potential

- Next round: Series A in 18 months
- Exit opportunity: €20-50M (5-7 years)
- Strategic buyers: Atlassian, Monday

</div>
</div>

---

# Contact

## Let's build the future of work together!

<div class="text-center mt-20">

### 📧 pitch@taskflow.example
### 📱 +385 91 000 0000
### 🌐 www.taskflow.example
### 📅 calendly.com/taskflow-pitch

<button class="cta-button">Schedule a Call</button>

</div>

<div class="absolute bottom-10 left-10">
Thank you! | Q&A
</div>
```

---

## .GITIGNORE FILE

```gitignore
# Dependencies
node_modules/
dist/
.slidev/
package-lock.json
yarn.lock

# Build outputs
.output/
.nuxt/
build/

# IDE files
.vscode/
.idea/
*.swp
*.swo
*~

# OS files
.DS_Store
.DS_Store?
._*
.Spotlight-V100
.Trashes
ehthumbs.db
Thumbs.db

# Logs
logs/
*.log
npm-debug.log*
yarn-debug.log*
yarn-error.log*
lerna-debug.log*

# Environment variables
.env
.env.local
.env.*.local

# Temporary files
*.tmp
*.temp
.temp/
.tmp/

# Test coverage
coverage/
.nyc_output/

# Optional: PDF exports (if you don't want to version them)
# exports/*.pdf

# Optional: If someone adds private data by mistake
*-private.*
*-confidential.*
*.backup
```

---

## README.md

```markdown
# 🚀 Pitch Deck Generator

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Slidev](https://img.shields.io/badge/Slidev-3.0-blue)](https://sli.dev)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

Open-source pitch deck generator for startups. Create professional pitch decks with 3 variants: Master (20 slides), Regional VC (15 slides), and YC-style (10 slides).

**Live Example:** [View Demo Deck](https://taskflow-pitch.example.com)

## 🎯 Why This Project?

Creating a compelling pitch deck is crucial for startup success, but it's time-consuming and expensive. This open-source template provides:

- **Professional structure** based on successful fundraising decks
- **Three variants** optimized for different investors
- **Working example** with realistic data
- **AI-ready workflow** for Claude Code assistance
- **Beautiful design** with shadcn-inspired minimalism

## ✨ Features

### 📊 Three Deck Variants

1. **Master Deck (20 slides)**
   - Comprehensive presentation for due diligence
   - All details investors might ask for
   - Perfect for later-stage discussions

2. **Regional VC Deck (15 slides)**
   - Optimized for European investors
   - Focus on capital efficiency
   - Conservative projections
   - Path to profitability emphasis

3. **YC Deck (10 slides)**
   - Ultra-concise format
   - Growth metrics focus
   - $1B+ potential narrative
   - Silicon Valley style

### 🎨 Design & Tech

- **Shadcn-inspired theme** - Clean, minimal, professional
- **Chart.js & D3.js** - Beautiful data visualizations
- **Slidev powered** - Developer-friendly presentations
- **Multi-language** - Croatian & English examples
- **PDF export** - Investor-ready outputs
- **Responsive** - Works on all devices

## 🚀 Quick Start

### Prerequisites

- Node.js 16+ installed
- Git for version control
- Basic terminal knowledge

### Installation

```bash
# Clone the repository
git clone https://github.com/pinkainc/pitch-deck.git
cd pitch-deck

# Install dependencies
npm install

# Start development server
npm run dev

# Open http://localhost:3030
```

### Creating Your Deck

1. **Edit the data file**
   ```bash
   # Edit with your startup data
   nano data/company.yaml
   ```

2. **Preview your deck**
   ```bash
   npm run dev
   ```

3. **Export to PDF**
   ```bash
   npm run export:all
   ```

## 📁 Project Structure

```
pitch-deck/
├── .claude/               # AI assistant workflows
│   ├── checklists/       # Deck requirements
│   └── prompts/          # Claude Code prompts
├── data/
│   └── company.yaml      # Your startup data
├── slides/
│   ├── deck-master.md    # 20-slide version
│   ├── deck-regional.md  # 15-slide version
│   └── deck-yc.md        # 10-slide version
├── theme/                # Design system
└── components/           # Vue components
```

## 🤖 AI-Assisted Workflow

This project is optimized for Claude Code AI assistant:

```bash
# Start Claude Code in the project directory
# Then say: "Let's create a pitch deck"

# Claude will guide you through:
1. Data collection interview
2. Deck generation
3. Variant creation
4. Export to PDF
```

## 📚 Documentation

- [Customization Guide](docs/CUSTOMIZATION.md) - Adapt for your startup
- [Examples](docs/EXAMPLES.md) - Success stories and tips
- [FAQ](docs/FAQ.md) - Common questions
- [Contributing](CONTRIBUTING.md) - How to contribute

## 🎯 Deck Checklists

Each deck variant follows a detailed checklist:

### Master Deck Checklist
- ✅ 20 comprehensive slides
- ✅ Complete financial projections
- ✅ Detailed competition analysis
- ✅ Full team backgrounds
- ✅ Risk analysis & mitigation

### Regional VC Checklist
- ✅ Capital efficiency focus
- ✅ Path to profitability
- ✅ Local market validation
- ✅ Conservative projections
- ✅ EU expansion strategy

### YC Checklist
- ✅ 10 slides maximum
- ✅ Problem-Solution-Traction focus
- ✅ Week-over-week growth
- ✅ $1B+ TAM
- ✅ Why now urgency

## 💡 Tips for Success

1. **Start with data** - Fill out company.yaml completely
2. **Use real metrics** - Even if small, real > projected
3. **Tell a story** - Each slide should flow to the next
4. **Practice presenting** - Use Slidev's presenter mode
5. **Get feedback** - Share with advisors before investors

## 🤝 Contributing

We welcome contributions! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

### Ways to Contribute

- 🐛 Report bugs
- 💡 Suggest features
- 📝 Improve documentation
- 🎨 Enhance design
- 🌍 Add translations
- ⭐ Star the repo

## 📄 License

MIT License - see [LICENSE](LICENSE) file. Use freely for your startup!

## 🙏 Acknowledgments

- [Slidev](https://sli.dev) - Presentation framework
- [shadcn/ui](https://ui.shadcn.com) - Design inspiration
- [YC Library](https://www.ycombinator.com/library) - Pitch deck wisdom
- All contributors and stargazers

## 📧 Support

- **Issues:** [GitHub Issues](https://github.com/pinkainc/pitch-deck/issues)
- **Discussions:** [GitHub Discussions](https://github.com/pinkainc/pitch-deck/discussions)
- **Email:** opensource@pinkainc.com

## 🚀 Success Stories

> "Used this template to raise €500k. The structure is perfect!" - Startup Founder

> "Finally, a pitch deck template that actually works." - Angel Investor

> "The YC variant helped us get into the batch!" - YC Founder

---

**Made with ❤️ by the startup community, for the startup community**

If this helped you raise funding, please:
1. ⭐ Star the repo
2. 📣 Share your success story
3. 🤝 Contribute improvements

Happy fundraising! 🦄
```

---

## CONTRIBUTING.md

```markdown
# Contributing to Pitch Deck Generator

First off, thank you for considering contributing! 🙏

## How Can You Contribute?

### 🐛 Reporting Bugs
- Use GitHub Issues
- Provide clear description
- Include steps to reproduce
- Share your environment details

### 💡 Suggesting Features
- Check existing issues first
- Explain the use case
- Provide examples if possible

### 📝 Improving Documentation
- Fix typos and grammar
- Add examples
- Improve clarity
- Translate to other languages

### 🎨 Enhancing Design
- Improve CSS styles
- Add new layouts
- Create better visualizations
- Optimize for mobile

### 💻 Code Contributions
1. Fork the repository
2. Create feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open Pull Request

## Guidelines

### Code Style
- Use 2 spaces for indentation
- Follow Vue.js best practices
- Comment complex logic
- Keep functions small

### Commit Messages
- Use present tense ("Add feature" not "Added feature")
- Be descriptive but concise
- Reference issues when applicable

### Pull Requests
- Update README if needed
- Add tests if applicable
- Ensure all checks pass
- Request review from maintainers

## Development Setup

```bash
# Fork and clone
git clone https://github.com/YOUR-USERNAME/pitch-deck.git

# Install dependencies
npm install

# Create branch
git checkout -b your-feature

# Make changes and test
npm run dev

# Submit PR when ready
```

## Questions?

Feel free to open an issue or reach out to opensource@pinkainc.com

Thank you for making this project better! 🚀
```

---

## LICENSE (MIT)

```
MIT License

Copyright (c) 2024 Pinka Inc. and Contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## INITIALIZATION SCRIPT

```bash
#!/bin/bash
# init-pitch-deck.sh - Initialize open-source pitch deck generator

echo "🚀 Initializing Open-Source Pitch Deck Generator"
echo "📍 Repository: https://github.com/pinkainc/pitch-deck"
echo "📄 License: MIT - Free to use and modify!"
echo ""

# Create directory structure
echo "📁 Creating project structure..."
mkdir -p pitch-deck/{.github/{workflows,ISSUE_TEMPLATE},.claude/{checklists,prompts},data,slides/components,theme,public/assets,docs}

cd pitch-deck

# Initialize npm
echo "📦 Initializing package.json..."
npm init -y

# Install dependencies
echo "📚 Installing dependencies..."
npm install -D @slidev/cli playwright-chromium
npm install chart.js d3 vue

# Add npm scripts
echo "⚙️ Configuring npm scripts..."
npm pkg set scripts.dev="slidev"
npm pkg set scripts.build="slidev build"
npm pkg set scripts.export="slidev export"
npm pkg set scripts.export:all="npm run export:master && npm run export:regional && npm run export:yc"
npm pkg set scripts.export:master="slidev export slides/deck-master.md"
npm pkg set scripts.export:regional="slidev export slides/deck-regional.md"
npm pkg set scripts.export:yc="slidev export slides/deck-yc.md"
npm pkg set scripts.preview="slidev preview"

# Create .gitignore
echo "🔒 Creating .gitignore..."
cat > .gitignore << 'EOF'
# Dependencies
node_modules/
dist/
.slidev/
package-lock.json
yarn.lock

# Build outputs
.output/
.nuxt/
build/

# IDE files
.vscode/
.idea/
*.swp
*.swo
*~

# OS files
.DS_Store
Thumbs.db

# Logs
*.log

# Environment
.env
.env.local

# Temporary
*.tmp
.temp/
EOF

echo ""
echo "✅ Project initialized successfully!"
echo ""
echo "📖 Next steps:"
echo "  1. cd pitch-deck"
echo "  2. Edit data/company.yaml with your startup data"
echo "  3. npm run dev (start development server)"
echo "  4. npm run export:all (generate PDFs)"
echo ""
echo "🤖 Or use with Claude Code:"
echo "  Just say: 'Let's create a pitch deck'"
echo ""
echo "⭐ Don't forget to star the repo!"
echo "   https://github.com/pinkainc/pitch-deck"
```

---

## END OF DOCUMENT

This complete initialization document creates a fully transparent, open-source pitch deck generator that serves as both a working template and a learning resource for the startup community. Everything is public, documented, and ready to fork!