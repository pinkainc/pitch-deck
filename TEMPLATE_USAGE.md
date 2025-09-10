# 🎯 Using This Template for Your Startup

This branch (`template-stable`) serves as a clean starting point for creating your own pitch deck.

## 🚀 Quick Start for New Projects

### Option 1: Use the Template Branch
```bash
# Clone the template branch
git clone --branch template-stable https://github.com/pinkainc/pitch-deck.git my-startup-deck
cd my-startup-deck

# Remove existing git history and start fresh
rm -rf .git
git init
git add .
git commit -m "Initial commit from pitch-deck template v1.0.0"

# Set your own remote
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
git push -u origin main
```

### Option 2: Use the Stable Tag
```bash
# Clone from the v1.0.0 tag
git clone --branch v1.0.0 https://github.com/pinkainc/pitch-deck.git my-startup-deck
cd my-startup-deck

# Remove template git history
rm -rf .git
git init
```

## 📝 Customization Steps

### 1. Update Company Data
Edit `data/company.yaml` with your startup information:
```yaml
company:
  name: "Your Startup Name"
  tagline:
    en: "Your tagline in English"
  # ... update all fields
```

### 2. Replace Example Content
- Update all TaskFlow references with your company name
- Replace example metrics with your actual data
- Update team information
- Add your company logo to `public/assets/`

### 3. Customize Styling (Optional)
- Modify `theme/shadcn-style.css` for brand colors
- Update fonts if needed
- Adjust layouts in slide markdown files

### 4. Choose Your Deck Variant
Focus on the variant that matches your needs:
- `slides/deck-master.md` - For comprehensive due diligence
- `slides/deck-regional.md` - For European/regional investors
- `slides/deck-yc.md` - For Silicon Valley VCs

### 5. Preview and Export
```bash
# Install dependencies
npm install

# Preview your deck
npm run dev

# Export to PDF
npm run export:all
```

## 🔄 Staying Updated

To get updates from the template while preserving your changes:

```bash
# Add template as upstream remote
git remote add template https://github.com/pinkainc/pitch-deck.git

# Fetch template updates
git fetch template

# Merge template improvements (carefully review changes)
git merge template/template-stable --allow-unrelated-histories
```

## 🏷️ Version Strategy

- **v1.0.0** - Initial stable release with TaskFlow example
- **template-stable** - Always points to latest stable template
- **main** - Pinka's specific implementation (not for template use)

## 📚 Resources

- [Full Documentation](README.md)
- [Contributing Guidelines](CONTRIBUTING.md)
- [Changelog](CHANGELOG.md)
- [AI Assistant Guide](CLAUDE.md)

## 🤝 Contributing Back

If you improve the template structure (not your specific content):
1. Fork the original repo
2. Make improvements on `template-stable` branch
3. Submit PR with template enhancements

## 📄 License

This template is MIT licensed. You're free to:
- Use commercially
- Modify freely
- Distribute
- Use privately

Just include the original MIT license in your project.

---

**Remember:** This template branch will always contain generic example data (TaskFlow).
Your specific company data should only exist in your own fork/repository.