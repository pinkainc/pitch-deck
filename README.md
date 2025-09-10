# 🚀 Pitch Deck Generator

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Slidev](https://img.shields.io/badge/Slidev-3.0-blue)](https://sli.dev)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

Open-source pitch deck generator for startups. Create professional pitch decks with 3 variants: Master (20 slides), Regional VC (15 slides), and YC-style (10 slides).

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